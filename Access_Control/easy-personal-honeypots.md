# Easy Personal Honeypots
<p><span style="text-decoration: underline;">Honeypots</span></p>
<p>Honeypots are tools which helps in informing the owner of an asset if his private / confidential property is being snooped / intruded upon by an attacker.  Honeypots are aimed at luring the perpetrator who got unauthorized access to the property - Email, Online Storage, Personal Laptop, Server, Network, etc - to interact with the honeypot, thereby triggering an alert to the owner.</p>
<p>Traditionally, the setup of honeypots have been limited to devices in the network that were setup purely as honeypots and were expensive.  But with the advent of Honeytokens, they offer a much easier and cheaper way of detecting intrusion to your private / confidential property.</p>
<p><u>Honeytokens</u></p>
<p>Honeytokens are honeypots that are not computer systems.  Honeytokens can exist in almost any form, from a dead, fake account to a database entry that would only be selected by malicious queries, making the concept ideally suited to ensuring data integrity—any use of them is inherently suspicious if not necessarily malicious.</p>
<p>Honeytokens can be embedded in folders, files, URL links, Database Tables, Email, DNS, etc.  Any interaction with these items would trigger an alert to the administrator.</p>
<p><u>Canarytokens</u></p>
<p>Canarytokens, provided by <u>Canarytokens.org</u> are honeytokens intended for easy use by the masses.  The site lets users easily create honeytokens intended for a particular property and trigger an alert to the users' custom provided email address.</p>
<p>Any interaction with the token would trigger a connection to the Canarytokens domain, from where an alert would be then triggered to the users' custom set email address informing  users of the breach.</p>
<p>Recommended places to put Canarytokens are:</p>
<ul>
	<li>Dropbox</li>
	<li>Google Drive</li>
	<li>Gmail</li>
	<li>Confidential directory and files in your personal computer</li>
	<li>Server directory and files</li>
	<li>Your customer mailing list</li>
</ul>
<p>Canarytokens may fail if the perpetrator manages to block traffic to Canarytokens domain.  To overcome this, the user can make use of <a href="https://github.com/thinkst/canarytokens-docker">Dockerized  Canarytokens</a> and install them in a the user's custom internet facing domain.</p>
<p>&nbsp;</p>
<p><u>References</u>:</p>
<p><a href="https://en.wikipedia.org/wiki/Honeytoken">https://en.wikipedia.org/wiki/Honeytoken</a></p>
<p><a href="http://canarytokens.org/generate" target="_blank" rel="noopener">http://canarytokens.org/generate </a></p>
<p><a href="http://blog.thinkst.com/p/canarytokensorg-quick-free-detection.html" target="_blank" rel="noopener">http://blog.thinkst.com/p/canarytokensorg-quick-free-detection.html</a></p>
<p><a href="https://github.com/thinkst/canarytokens-docker" target="_blank" rel="noopener">https://github.com/thinkst/canarytokens-docker</a></p>
<p><a href="https://canary.tools/" target="_blank" rel="noopener">https://canary.tools/</a></p>
