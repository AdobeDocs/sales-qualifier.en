---
title: User roles and permissions
description: Learn how Sales Qualifier user groups control application and administration access.
feature: Agentic AI, Sales Insights, Account Journeys
role: Admin
TQID: 'https://experienceleague.adobe.com/9X9DYGMvLGcPG--G6rHcDEk91hdT9-XYc9wbiL2Qoww'
product_v2:
  - id: d0a3eab4-7b10-4d96-a71e-6c0f8e7b7c87
    internal-label: CX Enterprise
feature_v2:
  - id: fc7979f3-56c3-43ca-9784-f1ea3dc69c4b
    internal-label: Integrations
  - id: fdbb8fc9-ffa3-4b86-88fe-aa4c5a3e1bc6
    internal-label: Administration
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
    internal-label: Insights
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
---

# User roles and permissions

Sales Qualifier uses two required user groups to separate sales tasks from organization-wide configuration.

## Required user groups

| Group | Who belongs | What it grants |
| --- | --- | --- |
| `Sales Qualifier` | Every user, including administrators | Access to the application: Prospects, Accounts, Outbound workflows, Tasks, Performance, and Profile settings. |
| `Sales Qualifier Admins` | Administrators only, in addition to the `Sales Qualifier` group | Access to **[!UICONTROL Admin Settings]**, which governs CRM connections, the Knowledge Center, and compliance settings for the whole organization. |

Standard users need only the `Sales Qualifier` group. Administrators need membership in both groups. See [Get started](getting-started.md) to create these groups.

Organizations can also create an optional `Sales Qualifier BDR managers` group. Members can access email performance reports.

## Administrator access

**[!UICONTROL Admin Settings]** appears under **[!UICONTROL Administration]** only for users who belong to both required groups. Changes to these settings apply to the entire organization.

## What admins control

| Setting | Where to configure it | Effect |
| --- | --- | --- |
| CRM connection and field mapping | [Integrations and CRM](integrations.md#map-crm-fields-inbound-mapping) | Determines which CRM fields appear for a prospect or account and which fields are available as filters. |
| Global email opt-out | [Integrations and CRM](integrations.md#configure-global-email-opt-out) | Adds an unsubscribe footer to every outbound email. |
| Knowledge Center and playbook | [Knowledge Center](knowledge-center.md) | Makes the company playbook available in outbound prompts and [AI Assistant](ai-assistant.md). |
| Activity sync | [Integrations and CRM](integrations.md#configure-activity-sync-outbound-mapping) | Determines whether Sales Qualifier outreach activities appear in the CRM. |

Standard users can use these settings but cannot change them. If an expected filter, playbook reference, or CRM field is missing, contact an administrator.

>[!MORELIKETHIS]
>
>* [Get started](getting-started.md)
>* [Integrations and CRM](integrations.md)
>* [Knowledge Center](knowledge-center.md)
