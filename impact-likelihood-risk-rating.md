# <h1><strong>Impact, Likelihood and Risk Rating</strong></h1>
<p>&nbsp;</p>
<p>The first step is to identify a security risk that needs to be rated. The risk assessor needs to gather information about the threat agent involved, the attack that will be used, the vulnerability involved, and the impact of a successful exploit on the business. There may be multiple possible groups of attackers, or even multiple possible business impacts. In general, it's best to err on the side of caution by using the worst-case option, as that will result in the highest overall risk.</p>
<h2><strong>Likelihood RATING</strong></h2>
<p>&nbsp;</p>
<p>There are a number of factors that can help determine the likelihood. The first set of factors are related to the threat agent involved. The goal is to estimate the likelihood of a successful attack from a group of possible attackers. Note that there may be multiple threat agents that can exploit a particular vulnerability, so it's usually best to use the worst-case scenario. For example, an insider may be a much more likely attacker than an anonymous outsider, but it depends on a number of factors.</p>
<p><br />
 Note that each factor has a set of options, and each option has a likelihood rating from 0 to 9 associated with it. These numbers will be used later to estimate the overall likelihood.</p>
<p>The first set of factors are related to the threat agent involved. The goal here is to estimate the likelihood of a successful attack by this group of threat agents. Use the worst-case threat agent.</p>
<h3>Threat Agent Factors</h3>
<p>&nbsp;</p>
<p><strong>Skill Level</strong></p>
<p>How technically skilled is this group of threat agents? Security penetration skills (9), network and programming skills (6), advanced computer user (5), some technical skills (3), no technical skills (1)</p>
<p><strong>Motive</strong></p>
<p>How motivated is this group of threat agents to find and exploit this vulnerability? Low or no reward (1), possible reward (4), high reward (9)</p>
<p><strong>Opportunity</strong></p>
<p>What resources and opportunities are required for this group of threat agents to find and exploit this vulnerability? Full access or expensive resources required (0), special access or resources required (4), some access or resources required (7), no access or resources required (9)</p>
<p><strong>Size</strong></p>
<p>How large is this group of threat agents? Developers (2), system administrators (2), intranet users (4), partners (5), authenticated users (6), anonymous Internet users (9)</p>
<h3>Vulnerability Factors</h3>
<p>&nbsp;</p>
<p>The next set of factors are related to the vulnerability involved. The goal here is to estimate the likelihood of the particular vulnerability involved being discovered and exploited. Assume the threat agent selected above.</p>
<p><strong>Ease of Discovery</strong></p>
<p>How easy is it for this group of threat agents to discover this vulnerability? Practically impossible (1), difficult (3), easy (7), automated tools available (9)</p>
<p><strong>Ease of Exploit</strong></p>
<p>How easy is it for this group of threat agents to actually exploit this vulnerability? Theoretical (1), difficult (3), easy (5), automated tools available (9)</p>
<p><strong>Awareness</strong></p>
<p>How well known is this vulnerability to this group of threat agents? Unknown (1), hidden (4), obvious (6), public knowledge (9)</p>
<p><strong>Intrusion Detection</strong></p>
<p>How likely is an exploit to be detected? Active detection in application (1), logged and reviewed (3), logged without review (8), not logged (9)</p>
<p>The overall Likelihood rating could be determined by taking the average of all factors.  Based on the average score, you can map it to a single likelihood rating by using the below table:</p>
<p><img class="alignnone" src="https://farm2.staticflickr.com/1577/24879957666_3e3921a331_o.png" alt="Likelihood_Rating" width="480" height="154" /></p>
<p><script src="//embedr.flickr.com/assets/client-code.js" async="" charset="utf-8"></script></p>
<h2>IMPACT RATING</h2>
<p>&nbsp;</p>
<p>The business impact requires a deep understanding of what is important to the company running the application. The business risk is what justifies investment in fixing security problems.</p>
<p><strong>Financial Damage</strong></p>
<p>How much financial damage will result from an exploit? Less than the cost to fix the vulnerability (1), minor effect on annual profit (3), significant effect on annual profit (7), bankruptcy (9)</p>
<p><strong>Reputation Damage</strong></p>
<p>Would an exploit result in reputation damage that would harm the business? Minimal damage (1), Loss of major accounts (4), loss of goodwill (5), brand damage (9)</p>
<p><strong>Non-Compliance</strong></p>
<p>How much exposure does non-compliance introduce? Minor violation (2), clear violation (5), high profile violation (7)</p>
<p><strong>Privacy Violation</strong></p>
<p>How much personally identifiable information could be disclosed? One individual (3), hundreds of people (5), thousands of people (7), millions of people (9)</p>
<p>The overall Business Impact rating could be determined by taking the average of all factors.  Based on the average score, you can map it to a single impact rating by using the below table:</p>
<p><img class="alignnone" src="https://farm2.staticflickr.com/1666/24880034996_1968e01d8e_o.png" alt="Business_Impact_Rating" width="348" height="157" /></p>
<h2>Risk Rating Presentation</h2>
<p>&nbsp;</p>
<p>The old adage mentions that Risk = Impact * Likelihood.  Even though this is true, a mathematical multiplication of compartmentalized Impact and Likelihood ratings often gives a Risk Rating which does not reveal the actual gravity behind the risk.</p>
<p>The best way to present the gravity of a risk seems to be to explain the Business Impact of the risk along the lines of below four factors, as this is what a Business Owner can directly relate to:</p>
<ul>
	<li><strong>Financial Damage</strong></li>
	<li><strong>Reputation Damage</strong></li>
	<li><strong>Non-Compliance</strong></li>
	<li><strong>Privacy Violation</strong></li>
</ul>
<p>The likelihood of the risk taking place is best explained through the five levels and their real life examples:</p>
<ul>
	<li><strong>Certain</strong> - Toe Injury</li>
	<li><strong>Likely</strong> - Fall</li>
	<li><strong>Possible</strong> - Major Car Accident</li>
	<li><strong>Unlikely</strong> - Aircraft Crash</li>
	<li><strong>Rare</strong> - Major Tsunami</li>
</ul>
<p>An excel guide to help arrive at the likelihood rating and optionally, the impact rating is available at: <a href="https://github.com/GreenDiary/risk_assessment_best_practices/blob/master/OWASP_Risk_Rating_Methedology_v0.02.xlsx" target="_blank" rel="noopener">https://github.com/GreenDiary/risk_assessment_best_practices/blob/master/OWASP_Risk_Rating_Methedology_v0.02.xlsx </a></p>
<p><span style="text-decoration: underline;">References:</span></p>
<dl>
<dd>
<p><a href="https://www.owasp.org/index.php/OWASP_Risk_Rating_Methodology" target="_blank" rel="noopener">https://www.owasp.org/index.php/OWASP_Risk_Rating_Methodology </a></p>
<p><a href="https://en.wikipedia.org/wiki/Risk_Matrix" target="_blank" rel="noopener">https://en.wikipedia.org/wiki/Risk_Matrix</a></p>
</dd>
</dl>
