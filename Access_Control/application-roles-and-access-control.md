# Application Roles and Access Control
<p>Below are the main process controls that should be put in place surrounding Application Roles and Access Controls.</p>
<p><strong>1)      </strong><strong><u>Access Roles-Rights Matrix</u></strong></p>
<p>Business Owner should clearly define and document the access roles and rights assigned to each role within the application (example: functionality that could be invoked, pages that could be viewed, read-only vs read-write, etc).  Each role should be assigned a Role Owner, who has the ability to approve requests for adding a user to the role.  The document should be updated annually or with every major change to the application.</p>
<p><strong>2)      </strong><strong><u>Joiner, Mover and Leaver (JML) Access Management and Audit Trails</u></strong></p>
<p>A formal documented process should be created for managing access of Joiners, Movers and Leavers.  Each request for access to a role should be reviewed by the Role Owner before approval.  Access should be granted on a Least-Privilege basis and Segregation of Duties should be enforced.  A unique identifier (User ID) should be assigned to each user of the application.  Accurate logs of all requests and approvals should be created and stored in a secure manner and should be available for audit at any time.  It is advisable to use an Access Management Workflow tool to make the process easier.  SLAs and response timeline should be established for the provisioning / change / removal of access, especially defining the process and timeline for removal of access for leavers or emergency revocation.  The document should be updated annually or with every major change to the application.</p>
<p><strong>3)      </strong><strong><u>Privileged Roles Identification and Controls</u></strong></p>
<p>Privileged access gives an elevated level of access in order to perform a task on operating systems, databases, network devices and applications. These include accesses that:</p>
<ul>
	<li>Have the ability to create other accounts, delete existing accounts or change the rights of accounts; and/or</li>
	<li>Have the ability to modify system security and critical application configurations (examples: Password Requirements, Transaction limits, Portfolio limit, Watch List Monitoring Parameters, etc);  and/or</li>
	<li>Bypass system security controls (example: delete logs, turn off security services, modify data in the backend application database directly).</li>
</ul>
<p>Privileged Roles should be clearly identified.  Extra precaution should be given surrounding the approval (example: two levels of approval, approval by the Business Owner himself, etc) and actual use of Privileged Accounts (example: limited to very few number of users, used only during absolute necessity circumstances, review of activity logs for the usage of privileged accounts, etc).  Privileged Roles and the additional controls surrounding them should be clearly documented.  The document should be updated annually or with every major change to the application.</p>
<p><strong>4)      </strong><strong><u>Access-Assignment Recertification and Access-Roles-Rights Recertification</u></strong></p>
<p>User Access-Assignment recertification is to verify that access assigned is appropriate for the user’s business role.  User Access-Assignment recertification should be performed at least every six months (both for Standard Roles and Privileged Roles).  In order to support the recertification process, Access-Assignment Information / Access Control List (ACL) should be extractable directly from the application (and not from any other source – example: Access Management Workflow tool).  The application should cater for these periodic report extractions.  The latest extract of the ACL, not older than 6 weeks, should be used for recertification.  The recertification should be validated by the Role Owner / Business Owner.  Evidence that a recertification has taken place should be recorded and retained.  Any access that has not been recertified within 8 weeks of a review commencing, should be removed.</p>
<p>Access-Roles-Rights recertification is to verify that the rights allowed for a particular role is appropriate and enforces segregation of duties between the different roles.  Access-Roles-Rights recertification should be performed at least annually, by the Business Owner.  The recertification should result in updating the Access Roles-Rights Matrix document.  Evidence that a recertification has taken place should be recorded and retained. </p>
<p>A process to perform Access-Assignment Recertification and Access-Roles-Rights Recertification should be documented.  The document should be updated annually or with every major change to the application.</p>
<p><strong>5)      </strong><strong><u>Application Activity Logging, Retention and Monitoring</u></strong></p>
<p><strong><u>5.1)  Application Activity Logging</u></strong></p>
<p>Activity Logging should be enabled by the application.  The logs should capture the following:</p>
<ul>
	<li>Timestamp of occurrence of the activity</li>
	<li>User ID carrying out the activity</li>
	<li>Standard Account activity details (example: financial transactions, user login/logoff, configuration changes, etc)</li>
	<li>Privileged Account activity details (example: financial transactions beyond a threshold, adding/modifying/deleting user accounts, sensitive configuration changes, etc)</li>
	<li>Sensitive application events (example: user account lockout, application exceptions, etc)</li>
</ul>
<p>Logs should not capture passwords, sensitive Personally Identifiable Information (PII) or Payment Card Information. </p>
<p><strong><u>5.2)  Application Activity Log Retention </u></strong></p>
<p>Activity logs should be available readily for review by the Business Owner.  Activity logs should be retained in backup for a defined-lifetime (at least 7 years).</p>
<p><strong><u>5.3)  Privileged Activity Review</u></strong></p>
<p>Privileged Activity logs should be reviewed periodically by the Business Owner or delegate.  The process for carrying out the review, personnel accountable for the review, timeframe for review, follow-up actions, format of storage of evidence of review and evidence retention mechanisms should be defined by the Business Owner.</p>
<p>Application Activity Logging, Retention and Monitoring process should be documented.  The document should be updated annually or with every major change to the application.</p>
