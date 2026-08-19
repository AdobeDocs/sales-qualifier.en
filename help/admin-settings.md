---
title: Admin settings
description: Learn how to manage CRM fields, activity synchronization, email opt-out, and other Sales Qualifier administration settings.
feature: Agentic AI, Sales Insights, Account Journeys
role: Admin
TQID: 'https://experienceleague.adobe.com/vbtO6I67ZEaZz3oio9InNErvq5D0wjbRxyDZpTq8Lzo'
product_v2:
  - id: d0a3eab4-7b10-4d96-a71e-6c0f8e7b7c87
    internal-label: CX Enterprise
feature_v2:
  - id: fc7979f3-56c3-43ca-9784-f1ea3dc69c4b
    internal-label: Integrations
  - id: fdbb8fc9-ffa3-4b86-88fe-aa4c5a3e1bc6
    internal-label: Administration

internal-label: Administration
---

# Admin settings

Use **[!UICONTROL Admin Settings]** to configure CRM integrations, manage the Knowledge Center, and configure email opt-out.

Sales Qualifier connects to Salesforce or Microsoft Dynamics 365. The connection gives the Account Qualification Agent (AQA) a consistent view of leads, accounts, contacts, activities, and owners. Sales Qualifier can also write outreach activities and opt-out status back to the CRM and synchronize outreach activities to Marketo.

To configure CRM connections, field mapping, and activity synchronization, go to **[!UICONTROL Administration]** > **[!UICONTROL Admin Settings]** > **[!UICONTROL CRM connections]**. Standard users can use the configured CRM data and filters but cannot change these settings. To connect a CRM for the first time, see [Get started](getting-started.md#connect-your-crm).

>[!IMPORTANT]
>
>Accessing **[!UICONTROL Admin Settings]** requires membership in both the `Sales Qualifier` and `Sales Qualifier Admins` user groups. See [User roles and permissions](user-roles-permissions.md).

## CRM MCP and the embedded plugin

Sales Qualifier works with your CRM in these ways:

* **CRM MCP queries**—The Account Qualification Agent queries live CRM data so that answers and insights reflect the current state of your records.
* **Embedded plugin**—The CRM plugin displays [!DNL Marketo Sales Insights] (MSI) insights and agentic data in your CRM. Use the plugin to add a prospect to Sales Qualifier.
* **Activity synchronization**—When an administrator turns on **[!UICONTROL Activity sync]**, outreach activities synchronize to the CRM and Marketo.

## CRM access scope

Sales Qualifier reads users, contacts, owner mappings, leads, accounts, opportunities, and activities from the CRM. It writes only logged outreach activities and opt-out status to the CRM, and it synchronizes outreach activities to Marketo. Your CRM administrator prepares API access in Salesforce or Dynamics. A Sales Qualifier administrator then connects the CRM, maps inbound fields, and chooses whether to synchronize activities.

>[!NOTE]
>
>The credential steps in [Get started](getting-started.md#connect-your-crm) describe read access to CRM objects. If you turn on activity sync or opt-out write-back, work with your CRM administrator to grant the corresponding write access required by your CRM configuration.

## Map CRM fields (inbound mapping)

After the CRM is connected, select **[!UICONTROL Manage]** for the connection and open **[!UICONTROL Inbound mapping]**. Inbound mapping controls which CRM fields Sales Qualifier pulls into the application.

1. Select **[!UICONTROL Add section]**.
1. Enter a section name and description.
1. Select an entity type. **[!UICONTROL Prospects]** is selected by default. **[!UICONTROL Contacts]**, **[!UICONTROL Accounts]**, and **[!UICONTROL Opportunities]** are also available.
1. Select the CRM fields to import.

   Each field row displays its **[!UICONTROL Display name]**, **[!UICONTROL Field name]**, and **[!UICONTROL Data type]**.

1. Turn on **[!UICONTROL Filterable]** for each prospect, contact, or opportunity field that you want to make available as a filter on the **[!UICONTROL Prospects]** list.
1. Preview the section and select **[!UICONTROL Add]**.

Mapped fields appear in the corresponding areas of Sales Qualifier:

* Prospect fields appear on the **[!UICONTROL Person]** tab.
* Account fields appear on the **[!UICONTROL Account]** tab.
* Opportunity fields appear in the **[!UICONTROL Account Opportunity]** section. Filterable opportunity fields also appear as their own columns in **[!UICONTROL My Opportunity Contacts]**, with labels such as **[!UICONTROL Stage (Opportunity)]** to distinguish them from contact fields.

## Configure activity sync (outbound mapping)

1. From **[!UICONTROL CRM connections]**, select **[!UICONTROL Manage]** for the connected CRM.
1. Open **[!UICONTROL Outbound mapping]**.
1. Turn on **[!UICONTROL Activity sync]** to sync Sales Qualifier outreach activities to the CRM and Marketo. Email sent, opened, clicked, and replied activities include the Engagement Plan name.

When activity sync is off, Sales Qualifier continues to use inbound CRM data but does not synchronize outreach activities to the CRM or Marketo.

## Configure global email opt-out

1. In the left navigation, expand **[!UICONTROL Administration]** and select **[!UICONTROL Admin Settings]**.
1. Select **[!UICONTROL Email settings]** under **[!UICONTROL Compliance]**.
1. Turn on **[!UICONTROL Include opt-out link in every email]** to append an unsubscribe footer to outbound emails.
1. In **[!UICONTROL Opt-out message template]**, enter the footer text. Include the `{opt_out_link}` token where the unsubscribe link should appear.

The settings save automatically.

When a prospect selects the link, Sales Qualifier stops sending emails to that prospect and synchronizes the opt-out status to the connected CRM.

## Reference: sample API parameters

Your CRM team can use these examples to confirm read access returns the expected lead fields.

### Dynamics OData example

```text
$select=fullname,_ownerid_value,leadid,emailaddress1,jobtitle,statuscode,createdon,modifiedon,statecode
$filter=_ownerid_value eq '<crmUserId>' [AND additional filters]
$expand=Lead_ActivityPointers(...),parentaccountid(...)
$orderby=modifiedon desc
```

### Salesforce SOQL example

```sql
SELECT Id, Salutation, FirstName, LastName, Name, Title, Company, Email,
  LeadSource, Status, OwnerId, LastModifiedDate, LastActivityDate, CreatedDate,
  (SELECT Id, Subject, ActivityDate, Status FROM Tasks ORDER BY ActivityDate DESC LIMIT 1),
  (SELECT Id, Subject, ActivityDateTime FROM Events ORDER BY ActivityDateTime DESC LIMIT 1)
FROM Lead
WHERE OwnerId = '<crmUserId>' AND IsDeleted = false
ORDER BY LastModifiedDate DESC
```

>[!MORELIKETHIS]
>
>* [Get started](getting-started.md)
>* [User roles and permissions](user-roles-permissions.md)
>* [Prospects](prospects.md)
