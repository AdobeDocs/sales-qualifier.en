---
title: Create and manage outbound workflows
description: Learn how to create, review, and manage AI-generated outbound workflows in Sales Qualifier to run goal-driven outreach cadences.
feature: Agentic AI, Sales Insights, Account Journeys
role: User
TQID: 'https://experienceleague.adobe.com/n3FbuiM2zF9QSqaKx1bhBSdbsf-w7vEsEGjCQTBo3g4'
product_v2:
  - id: d0a3eab4-7b10-4d96-a71e-6c0f8e7b7c87
    internal-label: CX Enterprise
feature_v2:
  - id: fc7979f3-56c3-43ca-9784-f1ea3dc69c4b
    internal-label: Integrations
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
    internal-label: Security
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
    internal-label: Personalization
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
    internal-label: Insights
---

# Outbound workflows

>[!NOTE]
>
>Outbound workflows created by product administrators are shared with all users in your organization.

An outbound workflow is a goal-driven outreach cadence. You define the goal and targeting criteria. AI then proposes a multitouch cadence and writes personalized email content for each prospect. Before you activate the cadence, review and approve each email.

An outbound workflow connects four elements:

* **Goal**—The outcome you want from the outreach, such as booking a discovery call or increasing event registration.
* **Targeting filters**—Conditions that determine which prospects are eligible.
* **Touchpoint cadence**—The ordered sequence of email, phone call, and LinkedIn InMail steps.
* **Personalized email content**—AI-generated content based on the prospect profile, account context, engagement history, and recent news.

The goal drives everything downstream: the AI uses it to suggest targeting filters, design the cadence, draft touchpoint prompts, and shape personalization for every generated email.

## Key concepts

| Concept | Description |
| --- | --- |
| **Workflow** | A reusable outbound activity defined by a goal, targeting filters, cadence, and settings. |
| **Goal** | What the outreach should accomplish. |
| **Touchpoint** | One step in the cadence (email, phone call, or LinkedIn InMail), scheduled relative to enrollment. |
| **Touchpoint prompt** | Instructions the AI follows when generating email body and subject for a prospect: tone, length, focus, and call to action. |
| **Cadence** | The full sequence of touchpoints: how many, in what order, and on which days. |
| **Targeting filter** | A condition that limits the workflow to a subset of prospects. |
| **Draft** | A generated email that is ready for review but not yet approved. |
| **Reasoning** | The AI's explanation of how it wrote a given email, including the signals and data sources it used. |
| **Enrollment** | Approving a prospect's drafts, which activates the cadence and queues emails to send during the workflow's send window. |

The following sections explain how to create a workflow, review generated emails, approve prospects, and manage workflows.

## Create an outbound workflow

The workflow wizard has five steps: **[!UICONTROL Goal]**, **[!UICONTROL Targeting]**, **[!UICONTROL Generate touchpoints]**, **[!UICONTROL Settings]**, and **[!UICONTROL Add prospects]**. Your goal shapes the remaining steps.

1. In the left navigation, select **[!UICONTROL Outbound workflows]**.
1. On the **[!UICONTROL Browse]** tab, select **[!UICONTROL + Create workflow]** in the upper-right corner.

### Step 1: Define your goal

The goal defines the intended outcome and guides targeting, cadence, and email generation.

1. Choose **[!UICONTROL Start from scratch]** to write your own goal, or **[!UICONTROL Start from template]** to use a saved template.

1. Choose one of the **[!UICONTROL Recommended goals]** as a starting point, or enter your own goal.
1. Select **[!UICONTROL Next: Targeting]**.

State a specific outcome in the goal. For example, enter `Book a 15-minute discovery call with marketing leaders evaluating campaign automation` instead of `Promote campaign automation`.

### Step 2: Configure targeting filters

Targeting filters define which prospects are eligible. When you add prospects later, only those prospects who match these filters appear in the selection list.

1. Select the down arrow to display the **[!UICONTROL Add a filter]** list and select a filter to apply.

1. Set values for the filter.
1. Add more filters if you need to narrow the audience.

1. Select **[!UICONTROL Next: Generate touchpoints]**.

### Step 3: Generate and review touchpoints

After you configure targeting, AI analyzes the goal and targeting criteria. It then defines the cadence and writes a prompt for each touchpoint. The cadence can include email, phone call, and LinkedIn InMail steps.

To read its prompt, expand an email touchpoint. This instruction guides the AI when writing each prospect's email, including tone, length, focus, and call to action.

#### Regenerate the cadence

If the cadence is not what you want, select **[!UICONTROL Regenerate]** and enter a refinement instruction. For example:

* `Use three touchpoints across two weeks`
* `Lead with an executive briefing offer in the first email`
* `Add a nurture touch focused on a relevant case study`

AI rewrites the full cadence based on your instruction. To adjust one email touchpoint, edit its prompt instead of regenerating the cadence.

#### Use the Knowledge Center in prompts

If your organization has built a [Knowledge Center](knowledge-center.md) playbook, refer to it in the prompt. Name the document and describe the context to use. For example, enter `Use the ABC positioning guide from the Knowledge Center and focus on the security value proposition`.

When the cadence and prompts are ready, select **[!UICONTROL Next: Settings]**.

Refine the touchpoint prompts before generating prospect emails. AI uses these prompts for every selected prospect.

### Step 4: Configure workflow settings

The **[!UICONTROL Settings]** step controls how the workflow runs.

1. Review the **[!UICONTROL Workflow name]** and change it if needed.
1. In **[!UICONTROL Max prospects per workflow]**, confirm the upper limit on how many prospects the workflow can manage at once.
1. Set the **[!UICONTROL Send window]** for the hours when outbound emails are allowed to send.
1. Turn on **[!UICONTROL Skip Weekends]** to move any touchpoint that falls on a weekend to the next business day.
1. To stop follow-up touchpoints automatically once a prospect books a meeting, turn on **[!UICONTROL Meeting Booking Pause]**.
1. Confirm that the **[!UICONTROL Timezone]** matches your audience.
1. Select **[!UICONTROL Save and add prospects]**.

The opt-out footer is configured globally by an administrator and applies to outbound emails independently of the workflow settings. See [Configure global email opt-out](integrations.md#configure-global-email-opt-out).

### Step 5: Add prospects and start email generation

Saving opens the prospect selection view with the targeting filters from step 2 applied.

1. Review the list.

   Rows typically include prospect name, account, email, job title, engagement status, and prospect status.

1. Adjust filters here if you need to expand or narrow the list.
1. Select prospects using the checkboxes.
1. Select **[!UICONTROL Next: Review touchpoints]** to start per-prospect email generation.

AI generates a personalized email for each selected prospect and email touchpoint. Phone and LinkedIn InMail touchpoints remain scheduled steps. To continue working during generation, select **[!UICONTROL Notify when ready]**.

For each prospect, the AI combines each touchpoint prompt with prospect-specific data (person, account, engagement history, recent news) to produce a subject line and body.

## Review and refine generated emails

When generation finishes, the workflow detail view prompts you to review the drafts. Sales Qualifier does not send email until you approve it.

1. In the workflow detail view, select **[!UICONTROL Review drafts]** in the banner.
1. The **[!UICONTROL Review touchpoints]** step has two tabs:
   * **[!UICONTROL Ready for Review]**—Emails that have finished generating.
   * **[!UICONTROL Generating]**—Emails that are still being written.
1. In the prospect list on the left, select a name to load that prospect's touchpoints on the right.
1. Use the chevron (**>**) on a touchpoint to expand and read the full subject line and body.

### Read the AI reasoning

For each generated email, **[!UICONTROL Reasoning]** explains how the AI crafted that message, including signals, attributes, and sources that shaped the content and call to action. Review this information and validate personalization before you approve.

### Edit emails directly

For small wording or tone changes:

1. On the expanded touchpoint, select the _Edit_ icon to open the editor.
1. Edit the subject line or body.
1. Select **[!UICONTROL Save]**.

### Refine emails with AI

For structural or emphasis changes, use **[!UICONTROL Generate with AI]**. AI rewrites the email while retaining its personalization context.

1. In the email editor, select **[!UICONTROL Generate with AI]**.

1. Enter a clear instruction, for example:
   * `Make it shorter and more direct. Keep it under 100 words.`
   * `Focus more on the prospect's role and how the solution helps them specifically.`
   * `Change the call-to-action to suggest a 15-minute introductory call instead.`
1. Review the revision and edit it if needed.
1. Select **[!UICONTROL Save]**.

>[!TIP]
>
>Direct edits suit wording and tone. Use _[!UICONTROL Generate with AI]_ to rewrite the email from scratch.

## Approve and enroll prospects

Approval activates the cadence for a prospect. Until a prospect is approved and enrolled, the system does not send emails to them.

1. In the left prospect list, select the prospects whose emails you have reviewed and are ready to send.
1. Select **[!UICONTROL Approve and enroll prospects]** in the lower-right corner.

Approved emails are sent during the workflow send window in the configured time zone. Each touchpoint is scheduled relative to the enrollment date. Unapproved prospects remain in **[!UICONTROL Ready for Review]**.

## Manage existing workflows

On the **[!UICONTROL Outbound workflows]** page, the **[!UICONTROL Browse]** tab lists every workflow. Each card shows the goal, configured touchpoints, and performance metrics. Use this view to monitor workflows, review drafts, or add prospects.

## Email outbox

The [Email Outbox](email-outbox.md) lists the automated emails sent on your behalf and any replies.

## Meeting booking

Sales Qualifier turns engaged conversations into booked meetings without leaving the outbound flow. When you connect your calendar, Sales Qualifier generates a personal booking link that prospects use to schedule time with you.

* **Booking links**—Configure your calendar connection and availability in [Profile settings](profile-settings.md). Add the booking link to your email signature so that it appears in outbound emails.
* **Cadence placement**—Sales Qualifier inserts your booking link at relevant points in a cadence. You can change its placement.
* **Booking pause**—When a prospect books a meeting, **[!UICONTROL Meeting Booking Pause]** stops further follow-ups. See [Step 4: Configure workflow settings](#step-4-configure-workflow-settings).

Track booking outcomes on the [Outbound performance](performance.md) page.

## Outbound workflow best practices

* **Invest in the goal.** Downstream targeting, cadence, and emails all trace back to the goal. Specific, outcome-focused goals outperform vague ones.
* **Finalize touchpoint prompts before per-prospect generation.** After bulk generation, changes are typically made one prospect at a time.
* **Use Reasoning as a quality check.** If the wrong signal is emphasized, or an obvious one is missing, edit the email or revisit the touchpoint prompt and regenerate the cadence.
* **Match the editing tool to the change.** Use direct edits for wording and tone. Use **[!UICONTROL Generate with AI]** for restructuring or reframing.
* **Approve only what you have reviewed.** Expand touchpoints, read the content, and refine where needed before enrollment.

>[!MORELIKETHIS]
>
>* [Tasks](tasks.md)
>* [Knowledge Center](knowledge-center.md)
>* [Outbound performance](performance.md)
