# <h1><span style="text-decoration: underline;"><strong>Cryptographic Key Management</strong></span></h1>
<p><strong><u>What are the common cryptographic keys in use?</u></strong></p>
<ul>
	<li>Asymmetric keys for PKI</li>
	<li>Asymmetric keys for SSL tunnel creation</li>
	<li>Symmetric keys used for encryption of data</li>
</ul>
<p><strong><u>How does the Web Server / Load Balancer create the SSL session key for encrypting each session with the Client browser?</u></strong></p>
<p>The secret session key for an SSL session is derived from a pre-master secret created by the client browser using its OS’s inherent random number generator.  The browser encrypts the pre-master secret with the server’s public key and sent to the server.  The server uses the pre-master secret to derive the secret key for further onward encryption of the data transferred in the SSL session.  The secret key is stored in cache only and is purged after the session expires.</p>
<p><strong><u>How does proprietary Database, Fileserver, Data Backup Solution Server encrypt data?</u></strong></p>
<p>Case-in-Point: Oracle Transparent Database Encryption (TDE).</p>
<ul>
	<li>Uses built-in Key Management solution.</li>
</ul>
<p>Case-in-Point: EMC Data Domain which can be used as a Data Backup and Recovery Solution.  It provides the below options for Data-At-Rest encryption:</p>
<ul>
	<li>Static Key managed internally.</li>
	<li>Internal Key Management for periodic Key Rotation.</li>
	<li>External Key Management is allowed through RSA Data Protection Manager (DPM) server.</li>
</ul>
<p>Case-in-Point: EMC VNX series of Storage Devices which could be used as a File Server.</p>
<ul>
	<li>Includes a Keystore, which is an embedded and independently encrypted container which holds all the Data-at-Rest Encryption keys on the data arrays.  The data array has an internal key manager called VNX Key Manager.  External key managers are not supported.</li>
</ul>
<p><strong><u>Key Management Solution (KMS)</u></strong></p>
<p>A key management solution (KMS) is an integrated approach for generating, distributing and managing cryptographic keys for devices and applications. Compared to the term key management, a KMS is tailored to specific use-cases such as secure software update or machine-to-machine communication. In an holistic approach, it covers all aspects of security - from the secure generation of keys over the secure exchange of keys up to secure key handling and storage on the client. Thus, a KMS includes the backend functionality for key generation, distribution, and replacement as well as the client functionality for injecting keys, storing and managing keys on devices. With the Internet of Things, KMS becomes a crucial part for the security of connected devices.</p>
<p>There are many proprietary KMS.  Example: RSA Data Protection Manager, Amazon Web Service KMS, HP Enterprise Security Key Manager, Oracle Key Manager, Safenet Enterprise Key Management.</p>
<p><strong><u>Use of Hardware Security Module (HSM) for the protection of Cryptographic Keys</u></strong></p>
<p>A hardware security module (HSM) is a physical computing device that safeguards and manages digital keys for strong authentication and provides cryptoprocessing. These modules traditionally come in the form of a plug-in card or an external device that attaches directly to a computer or network server.  HSMs may possess controls that provide tamper evidence such as logging and alerting and tamper resistance such as deleting keys upon tamper detection. Each module contains one or more secure cryptoprocessor chips to prevent tampering and bus probing.  Many HSM systems have means to securely backup the keys they handle either in a wrapped form via the computer's operating system or externally using a smartcard or some other security token.  Because HSMs are often part of a mission-critical infrastructure such as a public key infrastructure or online banking application, HSMs can typically be clustered for high availability. Some HSMs feature dual power supplies and field replaceable components such as cooling fans to conform to the high-availability requirements of data center environments and to enable business continuity.</p>
<p>A hardware security module can be employed in any application that uses digital keys. Typically the keys must be of high-value - meaning there would be a significant, negative impact to the owner of the key if it were compromised.  The functions of an HSM are:</p>
<ul>
	<li>onboard secure cryptographic key generation</li>
	<li>onboard secure cryptographic key storage and management</li>
	<li>use of cryptographic and sensitive data material</li>
	<li>offloading application servers for complete asymmetric and symmetric cryptography</li>
</ul>
<p>HSM are also deployed to manage Transparent Data Encryption keys for databases.  HSMs provide both logical and physical protection of these materials, including cryptographic keys, from non-authorized use and potential adversaries.  The cryptographic material handled by most HSMs are asymmetric key pairs (and certificates) used in public-key cryptography.  Some HSMs can also handle symmetric keys and other arbitrary data.</p>
<p><strong><u>Use of HSM for End-to-End Encryption of User Password</u></strong></p>
<p>HSM mainly provides end-to-end encryption of the User Password - [i] Browser to HSM Flow; and [ii] HSM to Application Database Flow.  This is  through secure generation of Asymmetric key pairs on demand (for end-to-end encryption of User Password from Browser to HSM) and secure management of a Symmetric key for storage of User Password in an encrypted format in an external Database (for end-to-end encryption of User Password from HSM to Application Database).  The User Password remains in an unencrypted form only at the User’s Browser.  The User Password remains in a cleartext-hashed format at both the User’s Browser and the HSM, but nowhere else.</p>
<p><strong><u>General HSM Security Features</u></strong></p>
<ul>
	<li>Provide strong physical and logical protection of cryptographic keys – Asymmetric key pairs and Symmetric keys.</li>
	<li>Asymmetric key pairs are created to handle User Authentication.  Public key created will be passed to the application server who passes it to the application client.  The application client encrypts the user password hash with the public key.  The user password hash will be retrieved by the HSM by decrypting using the private key.  The user password hash will then be encrypted with a secret key and passed to the application server for storage in its LDAP or Database.  Both the values – user password hash encrypted with public key and user password hash encrypted with secret key – will be passed back to the UAS for matching and authentication of a User.</li>
	<li>Only allow connectivity from pre-defined servers using IP restriction.</li>
	<li>Configuration of HSM only allowed by physically visiting the HSM at the Datacenter with the physical Keys and User ID/Password credentials.</li>
	<li>Installation and configuration of HSM driver is needed at the connecting server before connection establishment.</li>
	<li>Support for High-Availability clustering supported by configuration in the HSM driver.</li>
</ul>
<p><strong><u>PKI environment (CA HSMs)</u></strong></p>
<p>In PKI environments, the HSMs may be used by certification authorities (CAs) and registration authorities (RAs) to generate, store, and handle key pairs. In these cases, there are some fundamental features a device must have, namely:</p>
<ul>
	<li>Logical and physical high level protection</li>
	<li>Multi-part user authorization schema</li>
	<li>Full audit and log traces</li>
	<li>Secure key backup</li>
</ul>
<p>On the other hand, device performance in a PKI environment is generally less important, in both online and offline operations, as Registration Authority procedures represent the performance bottleneck of the Infrastructure.</p>
<p><strong><u>Card payment system HSMs (bank HSMs)</u></strong></p>
<p>Limited-feature HSMs are used in card processing systems. These systems are usually less complex than CA HSMs and normally do not feature a standard API. These devices can be grouped in two main classes:</p>
<p>OEM or integrated modules  - for automated teller machines and point of sale terminals:</p>
<ul>
	<li>to encrypt the personal identification number (PIN) entered when using the card</li>
	<li>to load keys into protected memory</li>
</ul>
<p>Authorisation and personalisation modules:</p>
<ul>
	<li>check an on-line PIN by comparing with an encrypted PIN block</li>
	<li>in conjunction with an ATM controller, verify credit/debit card transactions by checking card security codes or by performing host processing component of an EMV based transaction</li>
	<li>support a crypto-API with a smart card (such as an EMV)</li>
	<li>re-encrypt a PIN block to send it to another authorisation host</li>
	<li>support a protocol of POS ATM network management</li>
	<li>support de facto standards of host-host key|data exchange API</li>
	<li>generate and print a "PIN mailer"</li>
	<li>generate data for a magnetic stripe card (PVV, CVV)</li>
	<li>generate a card keyset and support the personalisation process for smart cards</li>
</ul>
<p>The major organization that produces and maintains standards for HSMs on banking market is the Payment Card Industry Security Standards Council.</p>
<p><span style="text-decoration: underline;">References:</span></p>
<p><a href="https://en.wikipedia.org/wiki/Hardware_security_module" target="_blank" rel="noopener">https://en.wikipedia.org/wiki/Hardware_security_module</a></p>
<p><a href="http://security.stackexchange.com/questions/4755/web-application-encryption-key-management" target="_blank" rel="noopener">http://security.stackexchange.com/questions/4755/web-application-encryption-key-management</a></p>
<p><a href="http://security.stackexchange.com/questions/104520/what-benefits-do-hardware-security-modules-provide-when-keys-are-not-stored-insi" target="_blank" rel="noopener">http://security.stackexchange.com/questions/104520/what-benefits-do-hardware-security-modules-provide-when-keys-are-not-stored-insi</a></p>
<p><a href="https://www.digicert.com/ssl-cryptography.htm" target="_blank" rel="noopener">https://www.digicert.com/ssl-cryptography.htm</a></p>
<p><a href="https://en.wikipedia.org/wiki/Session_key" target="_blank" rel="noopener">https://en.wikipedia.org/wiki/Session_key</a></p>
<p><a href="http://www-01.ibm.com/support/knowledgecenter/SSCKBL_6.1.0/com.ibm.websphere.edge.doc/edge/cp/admingd118.htm" target="_blank" rel="noopener">http://www-01.ibm.com/support/knowledgecenter/SSCKBL_6.1.0/com.ibm.websphere.edge.doc/edge/cp/admingd118.htm</a></p>
<p><a href="https://msdn.microsoft.com/en-us/library/windows/desktop/aa380513(v=vs.85).aspx" target="_blank" rel="noopener">https://msdn.microsoft.com/en-us/library/windows/desktop/aa380513(v=vs.85).aspx</a></p>
<p><a href="http://security.stackexchange.com/questions/63971/how-is-the-premaster-secret-used-in-tls-generated" target="_blank" rel="noopener">http://security.stackexchange.com/questions/63971/how-is-the-premaster-secret-used-in-tls-generated</a></p>
<p><a href="https://www.emc.com/collateral/white-papers/h11561-data-domain-encryption-wp.pdf" target="_blank" rel="noopener">https://www.emc.com/collateral/white-papers/h11561-data-domain-encryption-wp.pdf</a></p>
<p><a href="https://www.emc.com/collateral/white-paper/h13296-dare-wp.pdf" target="_blank" rel="noopener">https://www.emc.com/collateral/white-paper/h13296-dare-wp.pdf</a></p>
<p><a href="http://www.emc.com/data-protection/index.htm" target="_blank" rel="noopener">http://www.emc.com/data-protection/index.htm</a></p>
<p><a href="https://www.emc.com/collateral/white-papers/h11561-data-domain-encryption-wp.pdf" target="_blank" rel="noopener">https://www.emc.com/collateral/white-papers/h11561-data-domain-encryption-wp.pdf</a></p>
<p><a href="http://www.oracle.com/technetwork/database/security/tde-faq-093689.html" target="_blank" rel="noopener">http://www.oracle.com/technetwork/database/security/tde-faq-093689.html</a></p>
<p>&nbsp;</p>
