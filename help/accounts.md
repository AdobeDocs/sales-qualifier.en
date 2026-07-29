---
title: Accounts in Sales Qualifier
description: Learn how to review account intelligence in Sales Qualifier, including AI research, recent news, opportunities, and top engaged contacts, to prioritize outreach.
feature: Agentic AI, Sales Insights, Account Journeys
role: User
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

# Accounts

The account view combines AI-generated research, recent news, open opportunities, pipeline value, and engaged contacts. Use this information to understand the account before you reach out.

## Open an account

Account information is reached through a prospect who belongs to it.

1. Select **[!UICONTROL Prospects]** in the left navigation and open a prospect. See [Prospects](prospects.md).
1. On the prospect detail page, select the **[!UICONTROL Account]** tab.

Sales Qualifier identifies the account from the prospect's CRM record. The same account view is available from every prospect who works there. If Sales Qualifier cannot match an account, the tab shows _No account found_.

>[!NOTE]
>
>The available sections and metrics depend on your CRM, your organization's configuration, and the account data. If a section described here does not appear, its data or feature is not configured.

The account view has two tabs: **[!UICONTROL Details]** and **[!UICONTROL Account Research]**.

## Review the account details

The **[!UICONTROL Details]** tab gives you a snapshot of the account and its pipeline.

### Account overview

The overview card at the top of the tab identifies the account and summarizes its value:

* The account name and region
* **Annual recurring revenue (ARR)**—The annual recurring revenue across all active subscriptions. Select **[!UICONTROL View All]** to review ARR by product in the **[!UICONTROL Annual Recurring Revenue]** dialog.
* Account statistics, including the number of open opportunities and contacts, and the pipeline value.

### Account overview summary

The **[!UICONTROL Account Overview]** panel summarizes the account based on CRM data and Account Qualification Agent research. If research is in progress, the panel shows a loading state. If research is unavailable, the panel shows a message.

### Account insights

Use the buttons below the overview to switch between account views. The available views depend on your CRM and configuration:

| View | What it shows |
| --- | --- |
| **[!UICONTROL Opportunities]** | Open opportunities linked to the account, with key fields for each. Select **[!UICONTROL View all]** to see the full list in a table. |
| **[!UICONTROL Top Members]** | The account's top engaged contacts, ranked by engagement. Each contact shows their job title, email, a relative engagement score, and a relative urgency indicator. |
| **[!UICONTROL Intent data]** | Buying intent signals for the account, such as the products and topics the account is researching. |
| **[!UICONTROL Account Team Members]** | People assigned to the account, with their email, job title, territory, and product group. |
| **[!UICONTROL CRM fields]** | Account fields imported from your CRM, as configured in inbound mapping. See [Integrations and CRM](integrations.md#map-crm-fields-inbound-mapping). |

From the **[!UICONTROL Top Members]** view, take either of these actions for a contact:

* **[!UICONTROL Add to Outbound Workflow]**—Enroll the contact in an [outbound workflow](outbound-workflows.md).
* **[!UICONTROL Add to Marketo campaign]**—Trigger a [!DNL Marketo] campaign for the contact.

## Research the account

The **[!UICONTROL Account Research]** tab contains three areas:

* **[!UICONTROL Research categories]**—Research topics. Select a category to view its research in the center pane.
* **Research content**—AI-generated research cards grouped by category. A card can include the source domain and the dates when the signal was first and last detected.
* **[!UICONTROL Recent news]**—Current news about the account, including dates, tags, and source links.

If research or news cannot load, each area offers a **[!UICONTROL Reload]** action to try again.

## Use account intelligence in outreach

Account intelligence is most valuable when it shapes what you send:

* Reference a recent news item or research signal to open with relevance instead of a generic pitch.
* Check open opportunities and pipeline value to decide whether to prioritize the account.
* Use **[!UICONTROL Top Members]** to identify who to contact, then enroll them in an outbound workflow.
* Ask the [AI Assistant](ai-assistant.md) to build positioning for the account before a call.

>[!MORELIKETHIS]
>
>* [Prospects](prospects.md)
>* [Outbound workflows](outbound-workflows.md)
>* [AI Assistant](ai-assistant.md)
