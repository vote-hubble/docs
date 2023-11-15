# 📮 Mailbox Configuration

{% hint style="info" %}
This feature requires the Communication Hub.
{% endhint %}

You’ve designed eye-catching emails in Hubble, and you want to make sure that everyone in your network is seeing them. With 10 minutes of work, you can guarantee emails are delivered to inboxes, not spam folders.

#### Overview  <a href="#overview" id="overview"></a>

Hubble uses Amazon Web Services to deliver emails and must register each domain used to send emails. After you create a [Mailbox in the Admin Hub](https://app.hubble.vote/mailboxes), Hubble Support is alerted, and the process is kicked off.

#### SPF  <a href="#spf" id="spf"></a>

[Sender Policy Framework (SPF) DNS](https://www.cloudflare.com/learning/dns/dns-records/dns-spf-record/) records are a type of DNS TXT record commonly used for email authentication. SPF records include IP addresses and domains authorized to send emails from that domain.

In our case, we are authorizing all emails sent from the domain: `comms.hubble.vote`.

<table><thead><tr><th width="211">Field</th><th>Value</th></tr></thead><tbody><tr><td>Type</td><td><code>TXT</code></td></tr><tr><td>Host</td><td><code>@</code></td></tr><tr><td>Value</td><td><code>v=spf1 include:comms.hubble.vote ~all</code></td></tr><tr><td>Time to Live (TTL)</td><td>3600</td></tr></tbody></table>

#### DKIM  <a href="#dkim" id="dkim"></a>

[DomainKeys Identified Mail (DKIM) DNS](https://www.cloudflare.com/learning/dns/dns-records/dns-dkim-record/) records are specialized DNS TXT records that store the public key to verify an email’s authenticity.

When Hubble Support registers your domain with AWS, they will be given three (3) CNAME records that must be created (by you) before DKIM is enabled.
