# Server Onboarding Process

<p> Below described is a process that needs to be followed in an organization, to ensure that the organization's servers are hardened and secured before being released for use by the wider IT / Business teams:
<ul>
  <li> The Requestor requests for the server.
  <li> Infra Team provisions the server, performs Hardening on the server (to be compliant with Server Baseline) and creates the default accounts necessary for Security Monitoring (Security Logging, Vulnerability Scanning, Privileged ID Management, etc).
  <li> Infra team enters the server details into the Asset Tracker.
  <li> Infra team releases the server to IT Security Team for their review.
  <li> IT Security Team reviews the Server Hardening and Account Configurations using Read-Only access.  Any Exceptions found needs to be signed off by Management and documented.
  <li> IT Security Team adds all Privileged IDs to the Privileged ID Management Tool.
  <li> IT Security Team releases server back to the Infra Team.
  <li> IT Security Team monitors for any servers that did not follow the above process, through periodic Asset Scanning on the entire Asset IP Range.  Non-Compliances should be escalated to Management.
</ul>
