---
title: Customer Insights - Journeys link tracking mechanics
description: Learn about link tracking mechanics in Dynamics 365 Customer Insights - Journeys.
ms.date: 07/07/2023
ms.custom: 
  - dyn365-marketing
ms.topic: article
author: alfergus
ms.author: alfergus
search.audienceType: 
  - admin
  - customizer
  - enduser
---

# Customer Insights - Journeys link tracking mechanics

When executing customer journeys, all relevant hyperlinks are replaced with trackable links. If the content of a message is HTML, we also create an invisible pixel inside the message body. The invisible pixel is necessary to determine whether a user clicked on a link or opened the message.

Replaced links have the following format:

`https://[geo-specific].dynamics.com/api/orgs/[hashed organization-identifier]/r/[link identifier]?targetUrl={targetUrl}&digest={digest}&secretVersion={secretVersion}`

Links are replaced when the following conditions are met:

- The links aren't marked as **non-trackable** inside the message editor.
- The recipient customer profile indicates that the customer has consented to tracking.

When the recipient selects a link or opens a message with a tracking pixel, two things happen:

1. The recipient is redirected to the original URL.
1. The link click interaction is recorded.

If the recipient previously opted out from tracking, the interaction is generated as anonymous. When the recipient has opted out, the interaction doesn't store a customer profile reference. Link remains trackable for 365 days - afterwards they are still clickable but new clicks won't emit link clicked event any more.

> [!NOTE]
> All links generated in the [text message channel](real-time-marketing-outbound-text-messaging.md) are shortened, regardless of whether they are replaced with tracking links. Shortened links are expired within 365 days, afterwards they are no longer clickable.

## See Also
[Manage user compliance settings in Customer Insights - Journeys](real-time-marketing-compliance-settings.md)
[Manage consent for email and text messages in Customer Insights - Journeys](real-time-marketing-email-text-consent.md)

[!INCLUDE [footer-include](./includes/footer-banner.md)]
