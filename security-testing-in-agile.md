# Security Testing in the Agile World

<p>Traditionally, Security is thought about only at the last mile of a project timeline.  This is usually after the full set of UAT (User Acceptance Test) is completed, after which a Penetration Test would be performed by an External Penetration Test Service Provider.  Due to pressing timelines for Product Release, typically, plugging the security holes are done in a haphazard manner.  High and Medium rated vulnerabilities would be plugged through less thought-out workaround solutions, whereas Low rated items would typically be <i>Risk Accepted</i>.

<p>The above practice exists, even when people know that the cost of change increases exponentially over time.



<p><h3>Continuous Security Testing in the Agile World</h3>

<p> In the new world where projects are more-and-more adopting the Agile approach, or a combination of Agile and Waterfall, it is imperative that Security Testing is also embedded very deeply and from the start into the Development Methodology.  A Security Tester / Expert / Consultant / SME should be part of the core development team from the start of the project.  The Security Tester should have the below responsibilities:

<ul>
	<li> Ensure that the <a href="https://www.owasp.org/index.php/Category:OWASP_Application_Security_Verification_Standard_Project" target="_blank" rel="noopener">OWASP Application Security Verification Standards (ASVS)</a> and <a href="https://www.owasp.org/index.php/OWASP_Secure_Coding_Practices_-_Quick_Reference_Guide" target="_blank" rel="noopener">Secure Coding Practices (SCP)</a> are followed in each module being developed.</li>
	<li> Carry out Secure Code Reviews (Automated and Human) and Security Testing for each module to ensure the above.</li>
	<li> Drive Vulnerability Scanning (using tools such as Nexpose, Nessus, etc) and Remediation on the Platforms (Dev, UAT, SIT and Production) being used, from the start itself.  This will make sure that the application can works well on a hardened platform.
	<li> Facilitate Penetration Testing by an External Service Provider, once the Product is ready for Major Release.
</ul>

<p><h3>Penetration Testing Criteria</h3>

<p>How do we determine, when would be the right times to conduct External Service Provider Penetration Testing in the Agile world, where changes happen with every Sprint?

<p>There is no clear answer to this question.  But certain best-put suggestions would be:
<ul>
	<li> Perform External Pen Test, atleast once a year. Regulations, such as the MAS TRMG (Technology Risk Management Guidelines), recommends this.</li>
	<li> The Security Tester, on a Subjective basis, should suggest an External Pen Test, following a change, if there were any <i>Significant-Impact-Changes</i> to the Application, especially on the below areas:</li>
	<ul>
		<li> Authentication and Password Management</li>
		<li> Authorization and Access Management </li>
		<li> Session Management</li>
		<li> Sensitive Information Management</li>
		<li> Input and Output Data Validations</li>
	</ul>
</ul>


<p><h4>References:</h4>

<p><a href="https://www.thoughtworks.com/insights/blog/application-security-agile-projects" target="_blank" rel="noopener">https://www.thoughtworks.com/insights/blog/application-security-agile-projects</a>

<p><a href="https://blog.udemy.com/agile-vs-waterfall/" target="_blank" rel="noopener">https://blog.udemy.com/agile-vs-waterfall/</a>

<p><a href="https://lists.owasp.org/pipermail/owasp-community/2014-December/000472.html" target="_blank" rel="noopener">https://lists.owasp.org/pipermail/owasp-community/2014-December/000472.html</a>

