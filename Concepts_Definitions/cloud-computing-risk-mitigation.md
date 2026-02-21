# Cloud Computing Risk Mitigation
<p><strong><u>NIST Definition of Cloud Computing</u></strong></p>
<p>Cloud computing is a model for enabling on-demand network access to a shared pool of configurable computing resources (e.g.: networks, servers, storage, applications, and services) that can be rapidly provisioned and released with minimal management effort or service provider interaction. </p>
<p>An in-depth Risk Assessment should be performed for Cloud Computing Outsourcing.</p>
<p><strong><u>Risk Mitigation in any Outsourcing Scenario (To satisfy MAS Requirements)</u></strong></p>
<p>The below controls, which are applicable to an Service Outsourcing scenario is also applicable to a Cloud Outsourcing scenario and would help to reduce inherent risks.</p>
<ul>
	<li>The Client Company should be able to contractually restrict the Production, DR and Non-Prod Datacenters where their data is hosted. Locations from which the data will be accessed / processed should also be contractually restricted.  The Client Company should have Sovereignty over their Data.</li>
	<li>The Client Company should have the contractual power and means to promptly remove or destroy data stored at the service provider’s systems and backups.</li>
	<li>The Client Company should have the contractual power to audit the Service Provider and any Sub-Contractors who are hosting/processing/accessing the Client Company’s data.</li>
	<li>Data Loss Prevention solutions (Encryption, Access Control, Leakage Prevention) for Data at Rest, at Motion and at End Points should be enforced.</li>
	<li>In case where the Outsourced Service is Critical/Key to the functioning of the Client Company, any System Malfunction or IT Security Incident with Material Impact on the Client Company or its Customers should be reported to the Client Company who has an obligation to report to MAS within 1 hour and followed up with Root Cause Analysis (RCA) within 14 days.</li>
</ul>
<p><span style="text-decoration: underline;"><span style="line-height: 1.5;">References</span></span></p>
<p><a href="http://csrc.nist.gov/publications/nistpubs/800-145/SP800-145.pdf" target="_blank" rel="noopener">http://csrc.nist.gov/publications/nistpubs/800-145/SP800-145.pdf </a></p>
<p><a href="http://www.mas.gov.sg/~/media/MAS/Regulations%20and%20Financial%20Stability/Regulatory%20and%20Supervisory%20Framework/Risk%20Management/TRM%20Guidelines%20%2021%20June%202013.pdf" target="_blank" rel="noopener">MAS TRM Guidelines</a> </p>
<p><strong><u>Bare-Metal Server vs Virtual Servers</u></strong></p>
<p>Bare-Metal refers to the creation of a server using a Hypervisor directly on the Hardware platform.  The server created is dedicated for one single tenant.</p>
<p>Virtual Server refers to creating a virtual server with flexible resources.  Typically one virtual server exist together with many other virtual servers built on top of a Host OS.  This scenario causes multi-tenancy issues.</p>
<p><span style="text-decoration: underline; font-size: 12pt;">References:</span></p>
<p><span style="font-size: 12pt;"><a href="http://www.internap.com/2015/02/26/bare-metal-vs-hypervisor/" target="_blank" rel="noopener">http://www.internap.com/2015/02/26/bare-metal-vs-hypervisor/</a></span></p>
<p><span style="font-size: 12pt;"><a href="http://www.thoughtsoncloud.com/2014/07/bare-metal-vs-virtual-servers-choice-right/" target="_blank" rel="noopener">http://www.thoughtsoncloud.com/2014/07/bare-metal-vs-virtual-servers-choice-right/</a></span></p>
<p><span style="font-size: 12pt;"><a href="http://www.softlayer.com/bare-metal-servers" target="_blank" rel="noopener">http://www.softlayer.com/bare-metal-servers</a></span></p>
<p><span style="font-size: 12pt;"><a href="http://www.softlayer.com/virtual-servers" target="_blank" rel="noopener">http://www.softlayer.com/virtual-servers</a></span></p>
