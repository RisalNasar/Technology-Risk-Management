<p><span style="text-decoration: underline;"><strong>IT Security # Requirements for a new IT System</strong></span></p>
<table>
<tbody>
<tr>
<td width="623">
<p>Ownership and Criticality of the System:</p>
<p>Business Owner (Name, Department and Designation);</p>
<p>IT System Manager (Name, Department and Designation);</p>
<p>Project Manager;</p>
<p>Project Name;</p>
<p>Cost Charge Code;</p>
<p>Confidentiality, Integrity and Availability rating of the System (Define Worst Case Impact if each of the components is affected).</p>
<p>Availability rating should determine the RTO and RPO of the system.</p>
</td>
</tr>
<tr>
<td width="623">
<p>Describe the scope of change introduced by the project.</p>
<p>Describe the purpose of the system and its functions.</p>
<p>Describe the user base of the system.</p>
</td>
</tr>
<tr>
<td width="623">
<p>Provide inter-system (between different systems) connectivity diagram.</p>
<p>Provide intra-system (within the system) connectivity diagram.</p>
<p>Indicate the Datacenter (DC) where each system is hosted.</p>
</td>
</tr>
<tr>
<td width="623">
<p>Data-In-Motion Encryption – All data transfer from component to component should be using secure protocols which provides encryption of the data being transferred (SFTP, FTPS, Secure-JDBC, SSL, SSH, etc)</p>
</td>
</tr>
<tr>
<td width="623">
<p>Data-At-Rest Encryption:</p>
<p>Option 1 – Application Server level encryption of data before storing into Database (Application administrators have full access to data)</p>
<p>Option 2 – Database level encryption of data (Application administrators and DBAs have full access to data).</p>
<p>Option 3 – Disk/SAN level encryption of data (Application administrators, DBAs and OS administrators have full access to data).</p>
</td>
</tr>
<tr>
<td width="623">
<p>Password Controls:</p>
<p>Password should enforce the inclusion of Uppercase, Lowercase, Number and Symbol.  Enforce the non-usage of past 10 passwords.  Enforce password expiry for every 90 days.  Passwords must use a minimum of 15 characters.</p>
<p>[Guidance: Use Passphrases instead of a word.  Example: IHave1cat&amp;ILoveIt! ]</p>
</td>
</tr>
<tr>
<td width="623">
<p>Two-Factor Authentication should be used for access to application/systems over the Internet.  The second factor being SMS OTP or Hardware Token OTP.</p>
</td>
</tr>
<tr>
<td width="623">
<p>Transaction Signing (OTP generated from Hardware Token based on input value related to the transaction or input value sent through SMS) should be used for authorizing financial transactions and for changing of critical customer data, over the internet.</p>
</td>
</tr>
<tr>
<td width="623">
<p>Session Inactivity:</p>
<p>(i) [Optional] The session should be locked after a pre-defined period of inactivity;</p>
<p>(ii) The session should be logged-out after a pre-defined period of inactivity;</p>
</td>
</tr>
<tr>
<td width="623">
<p>Confidential data at Endpoint Devices:</p>
<p>Confidential data should not be stored into disk storage in Endpoint devices, without a strong Need-To-Have.  If there is a strong Need-To-Have, the data should be stored into Encrypted Containers and the Integrity of the Container should be verified before the data is re-used by the application.</p>
</td>
</tr>
<tr>
<td width="623">
<p>Cache at Endpoint Devices:</p>
<p>Cache used in endpoint devices should be cleared when the application logs out.</p>
</td>
</tr>
<tr>
<td width="623">
<p>Critical Processes at Trusted System:</p>
<p>Input Validation, Output Encoding, Authentication, Authorization, Session Identifier Creation, Cryptographic Functions to protect secrets from Application User and Logging Controls should be implemented at the Trusted System - at the Server side; and not at the User Endpoint.</p>
<p>Authentication should be required for accessing each page and resource at the server side, unless public usage is intended. </p>
</td>
</tr>
<tr>
<td width="623">
<p>Access Control:</p>
<p>Please provide Access Roles-Permissions Matrix (including Business and IT).  Please indicate which Roles are classified as Privileged Roles.</p>
</td>
</tr>
<tr>
<td width="623">
<p>Security Logging:</p>
<p>Process for recording, protection, retention, ~review of security logs (login/logout, change to access rights, security configurations, etc) should be established.</p>
</td>
</tr>
<tr>
<td width="623">
<p>Activity Logging:</p>
<p>Process for recording, protection, retention and ~review of activity logs should be established.</p>
</td>
</tr>
<tr>
<td width="623">
<p>Secure Coding Practices:</p>
<p>Use OWASP Secure Coding Practice Quick Reference Checklist during code development and review.</p>
</td>
</tr>
<tr>
<td width="623">
<p>Integrity of Golden Source Data:</p>
<p>Any data that is received by the application to be used as a golden source should be integrity verified by the Business Owner.</p>
</td>
</tr>
<tr>
<td width="623">
<p>Network and Application Penetration Testing:</p>
<p>Internal Network and Application Gray Box Penetration Testing should be performed for Internet Facing Systems and Critical Internal Systems before Go-Live.</p>
</td>
</tr>
<tr>
<td width="623">
<p>Platform Vulnerability Assessment:</p>
<p>Platform (OS, DB, and Device) vulnerability assessment should be performed before System Go-Live.</p>
</td>
</tr>
<tr>
<td width="623">
<p>Anti-Malware Protection:</p>
<p>Anti-Malware Solutions should be installed on all Wintel Platforms supporting the System.</p>
</td>
</tr>
<tr>
<td width="623">
<p>Support Documentations:</p>
<p>Documentations should be created to ensure that there is adequate information to support ongoing operations, problem resolution and future maintenance of the system.</p>
</td>
</tr>
</tbody>
</table>
<p>Project Level IT Security Requirements (Non-Functional Requirements) - https://github.com/GreenDiary/risk_assessment_best_practices/blob/master/IT_Security_Requirements_Project_Level_v0.01.docx</p>
