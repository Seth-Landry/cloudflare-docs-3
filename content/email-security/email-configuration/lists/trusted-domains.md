---
title: Trusted domains
pcx-content-type: concept
weight: 2
---

# Trusted domains

When messages come to your recipients from certain domains, Area 1 triggers certain [detections](/email-security/reference/dispositions-and-attributes/) by default:

- **Proximity Domains**: Domains spelled similarly to well-known domains. Will often trigger a `Spoof` detection.
- **Recent Domains**: Domains created recently (exact definition set in [Added Detections](/email-security/email-configuration/enhanced-detections/added-detections/)). Will often trigger a `Malicious` or `Suspicious` detection.

To exempt specific domains from these detections, you can add trusted domains.

## Add a trusted domain

To add a trusted domain:

1. Log in to the [Area 1 dashboard](https://horizon.area1security.com/).
2. Go to **Settings** (the gear icon).
3. On **Email Configuration**, go to **Allow List** > **Trusted Domains**.
4. Click **+ Add Domain**.
5. The exact flow varies based on what you select for your **Pattern Type**:

    - **Domain**: Allows you to specify a particular domain and then adjust triggers for *Proximity Domain* and *Recent Domain*.
    - **Create Regex**: Allows you to create Regex rules for the domain name, top-level domain (TLDs), and subdomains and then adjust triggers for *Proximity Domain* and *Recent Domain*.

6. Click **Save**.

### CSV uploads

You can also upload a CSV file of multiple allowed patterns, so long as the file is smaller than 150 KB, starts with a header row of all required values, and contains no additional fields.

An example file would look like this:

```txt
Domain, Notes, Proximity, Recent
mydomain.com, First Person, true, true
testdomain.com, New Hire, false, true
```