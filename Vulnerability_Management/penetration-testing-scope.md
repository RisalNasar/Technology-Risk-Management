# Penetration Testing Scope - Best Practices
<p><strong><u>Penetration Testing Scope – Application Server-Side</u></strong></p>
<ul>
	<li>Information Leakage - Tests should be carried out to detect network system verbosity and promiscuity.</li>
	<li>Business Logic  - Mistakes made in implementing business logic can lead to security holes.</li>
	<li>Authentication - Authentication testing should ensure that security requirements (credential expiry, revocation, reuse etc.) are implemented correctly and the protection of security functions and cryptographic keys is robust.</li>
	<li>Authorization - Tests should be conducted to verify that the security access matrix works correctly in various permutations.</li>
	<li>Input Data Validation - Proper data validation should include the following:

<ul style="list-style-type: circle;">
	<li>Every input to the applications should be validated.</li>
	<li>All forms of data (such as text boxes, select boxes and hidden fields) should be checked.</li>
	<li>The handling of null and incorrect data input should be verified.</li>
	<li>Content formatting should be checked.</li>
	<li>Maximum length for each input field should be validated.</li>
</ul>
</li>
	<li>Exception / Error Handling - Leakage of sensitive information should not be an outcome of a system failure.</li>
	<li>Session Management - To ensure secure session management, the following conditions should be specified:

<ul style="list-style-type: circle;">
	<li>Sensitive information that is passed in the cookies is encrypted.</li>
	<li>Session identifier should be random and unique.</li>
	<li>Session should expire after a pre-defined length of time.</li>
</ul>
</li>
</ul>
<ul>
	<li>Cryptography - The implementation of cryptography must be rigorously tested covering all cryptographic functions (encryption, decryption, hashing, signing) and key management procedures (generation, distribution, installation, renewal, revocation and expiry).</li>
	<li>Vulnerability Testing – Testing against common vulnerabilities such as the OWASP Top Ten.</li>
</ul>
<p><strong><u>Penetration Testing Scope – Mobile App/Client</u></strong></p>
<ul>
	<li>Environmental Analysis – Business case surrounding the application will be studied.</li>
	<li>Architectural Analysis</li>
	<li>Static Analysis</li>
	<li>Dynamic Analysis</li>
	<li>File System Analysis</li>
</ul>
<p><strong><u>Penetration Testing Scope – Network</u></strong></p>
<ul>
	<li>Information gathering</li>
	<li>Network Surveying</li>
	<li>Port Scanning</li>
	<li>System and Service Scanning</li>
	<li>Vulnerability Assessment</li>
	<li>Platform misconfiguration</li>
	<li>Patch Management</li>
	<li>Authentication Mechanisms</li>
</ul>
<p>&nbsp;</p>
