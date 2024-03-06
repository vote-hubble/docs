# 💳 ActBlue Webhooks

{% hint style="info" %}
This feature requires the Finance Hub.
{% endhint %}

Hubble _strongly recommends_ using ActBlue to accept online donations. Once ActBlue has approved your committee, you can follow their guide to [request a webhook integration](https://support.actblue.com/campaign\_hub/the-dashboard/setting-up-a-webhook-integration/) between ActBlue and Hubble.

You’ll need a few things from your [Admin Hub](https://app.hubble.vote/admin) to complete the setup.

1. API Username
2. API Password
3. Endpoint URL for each webhook integration

<figure><img src="https://cdn.hubble.vote/images/screenshots/admin-hub-actblue.png" alt=""><figcaption></figcaption></figure>

Optionally, specify `hello@hubble.vote` as the technical contact to keep us in the loop on your webhook requests.

<table data-full-width="true"><thead><tr><th width="227.33333333333337">ActBlue Type</th><th width="224">Hubble Type/Endpoint</th><th>URL</th></tr></thead><tbody><tr><td>Default</td><td>Contributions</td><td><code>https://api.hubble.vote/actblue/contributions</code></td></tr><tr><td>Default Cancellations</td><td>Cancellations</td><td><code>https://api.hubble.vote/actblue/cancellations</code></td></tr><tr><td>Default Refunds</td><td>Refunds</td><td><code>https://api.hubble.vote/actblue/refunds</code></td></tr></tbody></table>

Contact [Hubble Support](mailto:help@hubble.vote) if you have any questions.
