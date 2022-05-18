---
layout: default
parent: Guides
title: ActBlue Webhooks
---

# 💳 ActBlue Webhooks

This feature requires the Finance Hub.

Hubble _strongly recommends_ using ActBlue for accepting online donations. Once ActBlue has approved your committee you
can follow their guide to [request a webhook integration](https://support.actblue.com/campaign_hub/the-dashboard/setting-up-a-webhook-integration/)
between ActBlue and Hubble.

You'll need a few things from your [Admin Hub](https://app.hubble.vote/admin) to complete the setup.

1. API Username
2. API Password
3. Endpoint URL for each webhook integration

![Screenshot of ActBlue configuration in the Admin Hub](/assets/images/screenshots/actblue.png)

Optionally, you can specify `hello@hubble.vote` as the technical contact to keep us in the loop on your webhook requests.

| ActBlue Type          | Hubble Type/Endpoint | URL                                                             |
| --------------------- | -------------------: | --------------------------------------------------------------- |
| Default               |        Contributions | `https://app.hubble.vote/api/actblue/{ UNIVERSE_ID }/contributions` |
| Default Cancellations |        Cancellations | `https://app.hubble.vote/api/actblue/{ UNIVERSE_ID }/cancellations` |
| Default Refunds       |              Refunds | `https://app.hubble.vote/api/actblue/{ UNIVERSE_ID }/refunds`       |

Contact [Hubble Support](mailto:help@hubble.vote) if you have any questions.
