# <p><span style="text-decoration: underline;"><strong>External Module Password Management at the Application Server</strong></span></p>
<ul>
	<li>Do not hardcode secrets (example: passwords, private keys, etc) in source code.</li>
	<li>Keep secrets in a separate centralized configuration file, that can be referenced by different application modules.  The configuration file should have much restrictive access permissions.  It should not be added to Version Control Programs.  It should not be in the downloadable path of any web application.</li>
	<li>Keep the configuration file contents encrypted using a separate application password.  The application can decrypt the file on-the-fly to retrieve the secret information and leave the file encrypted after use.</li>
	<li>If the configuration file contents cannot be encrypted, at least store them in encoded format (Base 16, Base 32, Base 64, etc), so that they cannot be easily memorized.</li>
	<li>Access to the configuration file should also be logged by the Operating System into a Central log server.</li>
</ul>
<p><u>References:</u></p>
<p><u><a href="https://security.web.cern.ch/security/recommendations/en/password_alternatives.shtml" target="_blank" rel="noopener">https://security.web.cern.ch/security/recommendations/en/password_alternatives.shtml</a></u></p>
<p><u><a href="http://security.stackexchange.com/questions/15040/standards-for-encrypting-passwords-in-configuration-files" target="_blank" rel="noopener">http://security.stackexchange.com/questions/15040/standards-for-encrypting-passwords-in-configuration-files</a></u></p>
<p><u><a href="https://ostermiller.org/calc/encode.html" target="_blank" rel="noopener">https://ostermiller.org/calc/encode.html</a></u></p>
