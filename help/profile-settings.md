---
title: Configure profile settings
description: Learn how to configure your email connection, signature, and calendar availability in Sales Qualifier profile settings.
feature: Agentic AI, Sales Insights, Account Journeys
role: User
TQID: 'https://experienceleague.adobe.com/juP3sddkmc-nSTcTEKGWolbCwNWDgSA0yr6XK1X-w94'
product_v2:
  - id: d0a3eab4-7b10-4d96-a71e-6c0f8e7b7c87
    internal-label: CX Enterprise
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
    internal-label: Insights
---

# Profile settings

In the left navigation, expand **[!UICONTROL Configuration]** and select **[!UICONTROL Profile settings]**. Use these settings to manage your personal details, email, calendar, and chat availability.

## Email settings

In the **[!UICONTROL Email settings]** tab, set up your email connections.

* **[!UICONTROL Email connections]**—Select **[!UICONTROL Connect]** and follow the Microsoft sign-in process.
* **[!UICONTROL Email signature]**—Configure the signature used in generated emails. Add your [meeting booking](outbound-workflows.md#meeting-booking) link so that prospects can schedule time with you.

## Calendar configuration

On the **[!UICONTROL Calendar configuration]** tab, set your time zone and availability.

* **[!UICONTROL Calendar connection]**—Select **[!UICONTROL Connect]** and follow the Microsoft sign-in process.
* **[!UICONTROL Meeting confirmation email]**—Define the subject and body of the confirmation email that a prospect receives after booking a meeting.
* **[!UICONTROL Preferences]**—Set the default meeting length and the buffer between meetings.

If you disconnect your calendar:

* Active booking links stop working.
* The booking page shows a temporary unavailability message.
* Your settings are preserved when you reconnect.

## Calendar availability

Your calendar availability in Sales Qualifier is based on two inputs:

* Your connected work calendar, such as Outlook or Gmail
* The availability and time-slot rules in **[!UICONTROL Calendar configuration]**

Sales Qualifier reads free/busy status, not event details, from the connected calendar. It combines this status with your rules to determine the time slots that prospects can book.

You can configure:

* Working hours by day of week
* Multiple blocks per day, for example 9:00–12:00 and 1:00–5:00
* Your time zone
* Meeting duration
* Buffer before and after meetings
* Minimum notice
* Booking window

>[!MORELIKETHIS]
>
>* [Outbound workflows](outbound-workflows.md)
>* [Tasks](tasks.md)
