---
layout: default
parent: Guides
description: Configuring your Domain Network Settings (DNS) for sending emails from Hubble
---

# 📮 Mailbox Configuration

You've designed eyecatching emails in Hubble and you want to make sure that everyone in your network is seeing them. With 10 minutes of work, you can guarantee emails are delivered to inboxes and not spam folders.

### Overview

Hubble uses Amazon Web Services to deliver emails and is required to register each domain that's used to send emails. After you create a [Mailbox in the Admin Hub](https://hubble.vote/mailboxes), Hubble Support is alerted and the process is kicked off.

### SPF

[Sender Policy Framework (SPF) DNS](https://www.cloudflare.com/learning/dns/dns-records/dns-spf-record/) records are a type of DNS TXT record commonly used for email authentication. SPF records include a list of IP addresses and domains authorized to send emails from that domain.

In our case, we are authorizing all emails sent from the domain `mail.hubble.vote`.

| Field              |                                  Value |
| ------------------ | -------------------------------------: |
| Type               |                                    TXT |
| Host               |                                      @ |
| Value              | `v=spf1 include:mail.hubble.vote ~all` |
| Time to Live (TTL) |                                   3600 |

### DKIM

[DomainKeys Identified Mail (DKIM) DNS](https://www.cloudflare.com/learning/dns/dns-records/dns-dkim-record/) records are specialized DNS TXT record that store the public key used to verify an email's authenticity.

When Hubble Support is registering your domain with AWS they will be given three (3) CNAME records that must be created before DKIM is enabled.
