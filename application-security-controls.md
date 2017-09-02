# Application Security Controls
<p>Below are the main Application Security controls that should be implemented:</p>
<p><span style="text-decoration: underline;"><b>Access Authentication</b> </span></p>
<p>Access to the Application should use Secure Authentication Methods which meets or exceeds the Company’s authentication standards.  The session should be ended and user logged-out after a stipulated period of inactivity.  A stipulated number of consecutive failed login attempts should result in lockout of the account, which should only be unlocked by an administrator.  Privileged Access to the Application should ideally be using a higher level of security than normal access (example: Multi-factor authentication, more stringent password criteria, etc).<u></u><u></u> The Business Application Owner should define the following:<u></u><u></u></p>
<ul>
	<li>Threshold of idle time before logout of user<u></u><u></u></li>
	<li>Number of consecutive failed logins before lockout<u></u><u></u></li>
	<li>Privileged Access vs Normal Access within the Application<u></u><u></u></li>
</ul>
<p><i>Main Points: (Passwords, Inactivity Account Log-Out, Failed Login Attempt Account Lockout, Privileged Access Authentication)<u></u><u></u></i></p>
<p><span style="text-decoration: underline;"><b>Access Authorization</b> </span></p>
<p>Access Matrix defining the different Roles and their Privileges within the Application should be documented.  The process through which access to the Application can be Requested/Modified/Deleted and the associated Approvals required should be defined and documented.  The process should also cater for immediate removal of Leaver/Transferee accounts.   Audit trails should be created for all access changes using the Company’s Standard Access Request Management platform.<u></u><u></u></p>
<p><i>Main Points: (Access Matrix, Access Management Process, Audit Trail Maintenance)<u></u><u></u></i></p>
<p><span style="text-decoration: underline;"><b>Access Recertification</b></span> </p>
<p>Normal and Privileged Accounts within the Application should be recertified periodically (Normal accounts – at least once a year; Privileged Accounts – at least once every quarter).    Evidence of recertification and follow-up action taken to correct the access provisioning, should be retained.  The process for carrying out recertification, responsible parties, timeframe of execution, follow-up actions, and evidence retention mechanism should be defined and documented.<u></u><u></u></p>
<p><i>Main Points: (Access Recertification Process, Evidence Retention)<u></u><u></u></i></p>
<p><span style="text-decoration: underline;"><b>Activity Logging</b> </span></p>
<p>Activity Logging should be enabled by the application.  The logs should capture the following:<u></u><u></u></p>
<ul>
	<li>Timestamp of occurrence of the activity<u></u><u></u></li>
	<li>User ID carrying out the activity<u></u><u></u></li>
	<li>Normal activity/transaction details (example: financial transactions, user login/logoff, configuration changes to the application, application exceptions, etc)<u></u><u></u></li>
	<li>Sensitive activity/transaction details (example: financial transactions beyond a threshold, adding/modifying/deleting customer/user accounts, sensitive configuration changes to the application, user account lockout, critical application exceptions, etc)<u></u><u></u></li>
</ul>
<p>Logs should not capture passwords, sensitive Personally Identifiable Information (PII) or Payment Card Information.<u></u><u></u> The Business Application Owner should define the activity/transactions to be captured by the Application.<u></u><u></u></p>
<p><span style="text-decoration: underline;"><b>Activity Log Retention</b> </span></p>
<p>Activity Logs should be available readily for review by the responsible party.  Activity logs should be retained in backup for a defined-lifetime. (as-is the current practice within the Company).<u></u><u></u></p>
<p><strong><u>Privileged Account Identification</u></strong></p>
<p>Privileged access gives an <strong>elevated level of access</strong> in order to perform a task on operating systems, databases, network devices and applications. These include accesses that:</p>
<ul>
	<li>Have the ability to create other accounts, delete existing accounts or change the privileges of accounts; and/or</li>
	<li>Have the ability to modify system security and critical application configurations (examples: Password Requirements, Transaction limits, Portfolio limit, Watch List Monitoring Parameters, etc);  and/or</li>
	<li>Bypass system security controls (example: delete logs, turn off security services, modify data in the backend application database directly).</li>
</ul>
<p><span style="text-decoration: underline;"><b>Privileged Activity Review</b></span> </p>
<p>Sensitive activity/transactions should be reviewed periodically by a Responsible Party.  The process for carrying out review of sensitive activity/transactions, parties responsible for performing the review, timeframe for review, follow-up actions, format of storage of evidence of review and evidence retention mechanisms should be defined and documented.<u></u><u></u></p>
<p><i>Main Points: (Sensitive Activity Review Process, Evidence Retention)<u></u><u></u></i></p>
<p><span style="text-decoration: underline;"><b>Data Security</b></span></p>
<p>Data Integrity and Confidentiality should be protected in transit, storage and in disposal.  Secure electronic data transfer/access mechanisms (based on SSL/TLS) should be used.<u></u><u></u></p>
<p><span style="text-decoration: underline;"><b>Transaction Signing</b></span></p>
<p>FIs should implement two-factor authentication at login for all types of online financial systems and transaction-signing for authorizing transactions from customers.<u></u><u></u></p>
<p><span style="text-decoration: underline;"><b>Location based Access Control</b></span></p>
<p>Software-as-a-Service used by the Company over the Internet should restrict access to the Company’s staff by only allowing connection from the Company’s office locations (based on IP address).</p>
