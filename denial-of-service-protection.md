
# Denial Of Service (DoS) Attack - Protection
<p><u>Firewalls – DoS Protection Profile</u></p>
<p>Firewalls can provide a certain level of protection against Denial Of Service (DoS) Attacks, where the traffic threshold is not very high.  Certain brand of firewalls (ex: Palo Alto) provide DoS Protection Profiles to be setup which allows to control the number of sessions between interfaces, zones, addresses, and countries based on aggregate sessions or source and/or destination IP addresses.  But when the traffic size becomes huge, firewalls start to fail.</p>
<p><u>Limitations of Firewalls and Intrusion Prevention Systems (IPS)</u></p>
<p>Firewalls and IPS are stateful devices.  As stateful devices, firewalls and IPS track all connections for inspection and store them in a connection table. Every packet is matched against the connection table to verify that it was transmitted over an established, legitimate connection.</p>
<p>The typical connection table can store tens of thousands of active connections, which is sufficient for normal network activity. However, a Distributed DoS (DDoS) attack may include thousands of packets per second. As the first device in the organizational network to handle the traffic, the firewall or IPS will open a new connection in its connection table for each malicious packet, resulting in the quick exhaustion of the connection table. Once the connection table reaches its maximum capacity, it will not allow additional connections to be opened, ultimately blocking legitimate users from establishing connections.</p>
<p>Clean Pipe solutions, on the other hand, include a stateless protection mechanism that can handle millions of connection attempts without requiring connection table entries or exhausting other system resources.</p>
<p><u>Clean Pipe Solutions</u></p>
<p>Clean Pipe solution providers have large networks which work as “Scrubbing Centers” of network traffic to detect and drop bad traffic.  When a DDoS attack is detected, the traffic to the client company is routed to the Clean Pipe network for “scrubbing”.  Only legitimate traffic is allowed to reach the client company’s network.</p>
<p>Clean Pipe solution providers include Prolexic  Technologies, Verizon, Incapsula, etc.</p>
<p><u>References:</u></p>
<p><a href="https://www.paloaltonetworks.com/documentation/61/pan-os/pan-os/policy/dos-protection-profile.html">https://www.paloaltonetworks.com/documentation/61/pan-os/pan-os/policy/dos-protection-profile.html</a></p>
<p><a href="http://www.corero.com/blog/609-the-ddos-myth-about-the-firewall-and-the-ips.html">http://www.corero.com/blog/609-the-ddos-myth-about-the-firewall-and-the-ips.html</a></p>
<p><a href="http://blog.radware.com/security/2013/05/can-firewall-and-ips-block-ddos-attacks/">http://blog.radware.com/security/2013/05/can-firewall-and-ips-block-ddos-attacks/</a></p>
<p><a href="https://en.wikipedia.org/wiki/Denial-of-service_attack">https://en.wikipedia.org/wiki/Denial-of-service_attack</a></p>
<p>&nbsp;</p>
