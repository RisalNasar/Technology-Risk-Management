# Improve Internet Speed by creating Customized DNS List
<p><span style="text-decoration: underline;">DNS Default Settings</span></p>
<p>Most computers that are behind a NAT Router will depend on the Router to get the DNS address.  To check how DNS is configured in your computer, go to Control Panel &gt; Network and Sharing Center &gt; Change adapter settings &gt; Right click the "Network Connection" you are using currently &gt; Properties &gt; Internet Protocol Version 4/6 (Choose the version that you are using).</p>
<p><img class="alignnone" src="https://farm1.staticflickr.com/563/22078302499_83c6f301b5_o.png" alt="Internet_Protocol_Configuration" width="493" height="579" /></p>

<p>If your computer is dependent on the Router to get the DNS information, you will see settings as shown below.</p>
<p><img class="alignnone" src="https://farm6.staticflickr.com/5823/22239090336_6e50d64034_o.png" alt="Internet_Protocol_DNS_Properties_Automatic" width="478" height="562" /></p>

<p>At the NAT Router, you would be able to see the DNS configuration received from your ISP.  Depending upon your NAT router, you would see something like the below:</p>
<p><img class="alignnone" src="https://farm6.staticflickr.com/5714/22265156525_bb275f8735_o.png" alt="Router_DNS_Info" width="1005" height="715" /></p>

<p><span style="text-decoration: underline;">Problems in depending on the NAT Router for DNS Information (default ISP DNS servers)</span></p>
<p>1. Speed of Name Resolution: The default DNS servers (your ISP's DNS servers) may not be the fastest around.  If the DNS server responses slow down, your Internet Browsing experience slows down with it.  </p>
<p>2. Router Resource Limitations: There might be resource limitations in the NAT Router in handling/passing forward/resolving DNS queries, which might further affect your Internet Browser page loads.  Certain routers do not allow to configure more than two DNS servers.</p>
<p>3. Privacy Concerns: The DNS server that you are depending upon to resolve the addresses of the sites you are trying to reach may be collecting and piling up information on you (example: your IP address, the sites that you are visiting, trend over time, etc)</p>
<p><strong><span style="text-decoration: underline;">DNS Benchmarking, Optimization and creation of Customized DNS Server List</span></strong></p>
<p>Use <a href="https://www.grc.com/dns/benchmark.htm" target="_blank" rel="noopener">GRC's DNS Benchmarking tool</a> to find out the fastest DNS servers for your location and network.  The tool does not need any installation and can be directly executed.  Below are a few screenshots.</p>
<p><img class="alignnone" src="https://farm1.staticflickr.com/604/21642426144_9d9f60be12_o.png" alt="GRC_DNS_Benchmark_Test" width="614" height="1016" /></p>

<p><img class="alignnone" src="https://farm6.staticflickr.com/5678/22077410748_444a37cbaa_o.png" alt="GRC_DNS_Custom_DNS_List" width="493" height="395" /></p>

<p><img class="alignnone" src="https://farm1.staticflickr.com/775/21644112343_9b7675224c_o.png" alt="GRC_DNS_Custom_DNS_List_Creation" width="612" height="1014" /></p>

<p>Once you create a list of the fastest DNS servers customized for your situation, please vet the list and prepare a filtered list of around 10 DNS servers that are fast and that you absolutely trust.  I would recommend OpenDNS, Google DNS and your own ISP's DNS as last resort.</p>
<p>Once your filtered custom DNS list is created, the next step is to add it to your Computer's DNS settings or your Router's DNS settings.</p>
<p>You can use <a href="https://www.grc.com/dns/configuring.htm" target="_blank" rel="noopener">GRC's configuration guide</a> or <a href="https://store.opendns.com/setup/#/" target="_blank" rel="noopener">configuration guide provided by OpenDNS.</a></p>
<p>Below screenshots also shows how this could be performed on a Windows machine.  Internet Protocol Version Properties &gt; Choose "Use the following DNS server addresses" &gt; Click "Advanced".</p>
<p><img class="alignnone" src="https://farm6.staticflickr.com/5682/21642425654_9d55884aca_o.png" alt="Internet_Protocol_DNS_Properties" width="478" height="562" /></p>
<p>Choose the "DNS" tab &gt; Click "Add" and add the IP address of the DNS servers in the filtered Customized DNS list, one-by-one.</p>

<p><img class="alignnone" src="https://farm1.staticflickr.com/569/21644111823_cc45d31f41_o.png" alt="Internet_Protocol_DNS_Properties_Advanced" width="474" height="605" /></p>

<p><img class="alignnone" src="https://farm1.staticflickr.com/590/22252314192_9803f88b5c_o.png" alt="Internet_Protocol_DNS_Properties_Advanced_Add" width="474" height="603" /></p>
<p>Once you are finished, click "OK".  And you are done!!!  Check if there is a visible improvement in your Internet Page Load speed!!!</p>
<p><span style="text-decoration: underline;">DNS and Potential Issues with CDN (Content Delivery Network)</span></p>
<p>After you have changed your DNS settings, if you ever find that for contents provided through a CDN, your browser is taking more time than usual for loading, then you might want to change the order of your DNS list and place your ISP's DNS servers before other Third Party alternatives - OpenDNS and Google DNS.</p>
<p>More on this potential issue could be found at this <a href="http://www.economist.com/blogs/babbage/2011/03/internet_plumbing" target="_blank" rel="noopener">economist link</a> and this <a href="http://lifehacker.com/5788230/why-you-might-want-to-stick-with-your-isps-dns-server-after-all" target="_blank" rel="noopener">lifehacker link.</a></p>
<p>&nbsp;</p>

<p><span style="text-decoration: underline;">References</span></p>
<p><a href="http://www.labnol.org/internet/changing-dns-servers/18996/" target="_blank" rel="noopener">http://www.labnol.org/internet/changing-dns-servers/18996/ </a></p>
<p><a href="http://softwarerecs.stackexchange.com/questions/10116/set-custom-dns-servers-in-google-chrome" target="_blank" rel="noopener">http://softwarerecs.stackexchange.com/questions/10116/set-custom-dns-servers-in-google-chrome</a></p>
