---
title: Prospects in Sales Qualifier
description: Learn how to build, filter, and review your prospect list in Sales Qualifier to prioritize outreach.
feature: Agentic AI, Sales Insights, Account Journeys
role: User
TQID: 'https://experienceleague.adobe.com/zf2H5rq1JlIT26LqLPMrm2Mq3tSIrLOiTEw6BXb1w2U'
product_v2:
  - id: d0a3eab4-7b10-4d96-a71e-6c0f8e7b7c87
    internal-label: CX Enterprise
feature_v2:
  - id: fc7979f3-56c3-43ca-9784-f1ea3dc69c4b
    internal-label: Integrations
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
    internal-label: Insights
---

# Prospects

Select **[!UICONTROL Prospects]** in the left navigation to view the leads and contacts that you can access. Use the list to review each prospect's status and latest activity.

![Prospects table displaying lead status and last activity for prospect management](./assets/prospects.png){width="800" zoomable="yes"}

* **[!UICONTROL Leads]**—Leads assigned to you in the connected CRM.
* **[!UICONTROL Contacts]**—Contacts assigned to you in the connected CRM.
* **[!UICONTROL People list]**—Prospects that you import or add manually.

## Build your prospect list

The prospect list combines people from more than one source:

* **CRM prospects**—Sales Qualifier automatically imports leads and contacts assigned to the connected user. See [Integrations](integrations.md).
* **Imported prospects**—Prospects imported from a CSV file.
* **Manually added prospects**—Individual prospects added in Sales Qualifier.

To add prospects that do not come from your CRM:

1. On the **[!UICONTROL Prospects]** page, select **[!UICONTROL People list]**.
1. Select **[!UICONTROL + Add people]**, then select **[!UICONTROL Import CSV]** or **[!UICONTROL Add person]**.

   * For a CSV import, upload a CSV in the `firstname,email` format.
     First name and email are required. Last name is optional. The CSV template does not include the CRM lead ID column, but you can add the column and its values to the file before import. If the import fails, review the error message for the fields or values to correct, then upload the file again.
   * To add a person manually, enter their details in the form.

1. Select **[!UICONTROL Save]**.

## Filter and find prospects

Select **[!UICONTROL Filter]** to narrow the list. You can filter by:

* Engagement Plan status
* Created by
* Job title
* Account
* Source
* Last updated

Administrators can also make mapped CRM fields available as filters. In **[!UICONTROL Admin Settings]**, turn on **[!UICONTROL Filterable]** for each field that representatives use to find prospects. See [Map CRM fields](integrations.md#map-crm-fields-inbound-mapping).

In **[!UICONTROL My Opportunity Contacts]**, you can also filter contacts by fields from their associated opportunities, such as stage, type, and close date. Opportunity fields have labels such as **[!UICONTROL Stage (Opportunity)]**, which distinguishes them from contact fields. Your administrator controls which opportunity fields are available as filters.

### Filter by Marketo engagement

Find and prioritize prospects by their live [!DNL Marketo] engagement, such as email opens and clicks, web visits, form fills, and interesting moments. Engagement appears in near real time, as it happens.

To filter prospects by Marketo engagement:

1. Select **[!UICONTROL Filter]**.
1. Add a [!DNL Marketo] engagement filter and set the activity type, campaign, or other attributes to focus on the engagement that matters.

Each prospect shows their latest [!DNL Marketo] activity along with recent history.

Marketo engagement filtering is available in all production regions. Your administrator turns it on for your org and sandbox, and a marketer completes a one-time setup in [!DNL Marketo]. See [Turn on Marketo engagement filtering](integrations.md#turn-on-marketo-engagement-filtering).

## Review prospect details

Select a prospect to open their profile. Review the signals that matter before you reach out:

* **AI person summary**—An AI-written snapshot of the lead or contact and their recent engagement. Use the summary to understand the person at a glance before reviewing individual activities. AI person summaries are available on instances running Adobe Journey Optimizer B2B Edition Prime or Ultimate.
* **Activity list**—A chronological list of activities and recent behavior.
* **Timeline view**—A visual timeline of engagement across channels.
* **Viewed content**—Web pages and assets that the prospect viewed. Select an item to open it.

>[!MORELIKETHIS]
>
>* [Accounts](accounts.md)
>* [Engagement Plans](outbound-workflows.md)
>* [AI Chat](ai-assistant.md)
