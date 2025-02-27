---
pcx-content-type: concept
title: Managed Rulesets
weight: 6
---

# Managed Rulesets

The WAF Managed Rulesets are pre-configured rulesets that provide immediate protection against:

* Zero-day vulnerabilities
* Top-10 attack techniques
* Use of stolen/exposed credentials
* Extraction of sensitive data

These rulesets are regularly updated. You can adjust the behavior of managed rules, choosing from several possible actions.

Cloudflare provides the following WAF Managed Rulesets:

{{<table-wrap>}}
<table style="table-layout:fixed; width:100%;">
  <thead>
    <tr>
      <th style='width:30%; white-space:normal'><strong>Ruleset</strong></th>
      <th style='width:70%; word-wrap:break-word; white-space:normal'><strong>Description</strong></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style='width:30%; word-wrap:break-word; white-space:normal'><a href='/waf/managed-rulesets/cloudflare-managed-ruleset/'>Cloudflare Managed Ruleset</a></td>
      <td>Created by the Cloudflare security team, this ruleset provides fast and effective protection for all of your applications. The ruleset is updated frequently to cover new vulnerabilities and reduce false positives.</td>
    </tr>
    <tr>
      <td style='width:30%; word-wrap:break-word; white-space:normal'><a href='/waf/managed-rulesets/owasp-core-ruleset/'>Cloudflare OWASP Core Ruleset</a></td>
      <td>Cloudflare's implementation of the Open Web Application Security Project, or OWASP ModSecurity Core Rule Set. Cloudflare routinely monitors for updates from OWASP based on the latest version available from the official code repository.</td>
    </tr>
    <tr>
      <td style='width:30%; word-wrap:break-word; white-space:normal'><a href='/waf/managed-rulesets/exposed-credentials-check/'>Cloudflare Exposed Credentials Check</a></td>
      <td>Deploy an automated credentials check on your end-user authentication endpoints. For any credential pair, the Cloudflare WAF performs a lookup against a public database of stolen credentials.</td>
    </tr>
    <tr>
      <td style='width:30%; word-wrap:break-word; white-space:normal'>Cloudflare Free Managed Ruleset</td>
      <td>Available on all Cloudflare plans. Designed to provide mitigation against high and wide impacting vulnerabilities. The rules are safe to deploy on most applications. If you deployed the Cloudflare Managed Ruleset for your site, you do not need to deploy this Managed Ruleset.</td>
    </tr>
  </tbody>
</table>
{{</table-wrap>}}

The following rulesets run in the response phase:

{{<table-wrap>}}
<table style="table-layout:fixed; width:100%;">
  <thead>
    <tr>
      <th style='width:30%; white-space:normal'><strong>Ruleset</strong></th>
      <th style='width:70%; word-wrap:break-word; white-space:normal'><strong>Description</strong></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style='width:30%; word-wrap:break-word; white-space:normal'>Cloudflare Sensitive Data Detection (Beta)</td>
      <td>Created by Cloudflare to address common data loss threats. These rules monitor the download of specific sensitive data — for example, financial and personally identifiable information. Available in <strong>Firewall</strong> > <strong>Data</strong>.</td>
    </tr>
  </tbody>
</table>
{{</table-wrap>}}

## Phases of deployed Managed Rulesets

When you enable a Managed Ruleset in **Security** > **WAF** > **Managed rules**, you are deploying that Managed Ruleset to the zone-level `http_request_firewall_managed` phase.

Other Managed Rulesets, like DDoS Managed Rulesets, are deployed to a different phase. Refer to the specific Managed Ruleset documentation for details.

For more information on phases, refer to [Phases](/ruleset-engine/about/#phases).
