# Network Configuration for Home Virtual Lab Setup
<p><u>Virtualization Software</u></p>
<p>Virtualization Software which can be installed on top of your existing Operating System (OS) helps to create multiple Virtual OSes on top of the Host OS.  Each instance of the Virtual OS is called a Virtual Machine (VM).  VMs and the Host OS could be connected to each other and even to the Internet through different Networking Configurations.  The most popular Virtualization Software are VMWare and VirtualBox.  </p>
<p><u>Installing an Operating System as a Virtual Machine</u></p>
<p lang="en-US">Download an ISO image of the OS to be installed or pop in the Installation CD.  Follow the instructions for the Virtualization Software to create a VM with the new OS.  Install the OS from the ISO image or installation CD.</p>
<p lang="en-US"><u>Network Configuration</u></p>
<p lang="en-US">Networking Configurations  are the most important part of correctly interconnecting different VMs with the Host OS and with other machines in the outside work (in the LAN or over the Internet).  In a VMWare Workstation context, go to Edit &gt; Virtual Network Editor.  Administrator privileges may be required to carry out the edit.</p>
<p lang="en-US">Create three different Virtual Networks - (i) Connected to the Host OS only; (ii) Connected to the LAN/Internet by using NAT (Network Address Translation) using the Host OS's IP; (iii) Connected to the LAN/Internet by a separate IP acquired through the Network Adapter of the Host OS (Bridged Network).</p>
<p><img src="https://farm6.staticflickr.com/5712/22427913805_46847b9d9f_o.png" alt="Virtual_Networks_1" width="706" height="677" /><script async src="//embedr.flickr.com/assets/client-code.js" charset="utf-8"></script></p>
<p lang="en-US">Once the Virtual Networks have been setup, new VMs could be added to the Virtual Networks according to their connectivity needs.  Right click on VM &gt; Choose "Settings" &gt; Click "Network Adapter" &gt; Choose "Custom: Specific virtual network".</p>
<p><img src="https://farm1.staticflickr.com/712/22401920746_85a290ec24_o.png" alt="VM_Network_Settings_1" width="815" height="784" /><script async src="//embedr.flickr.com/assets/client-code.js" charset="utf-8"></script></p>
<p>You can join all your VMs to your Host OS and other Computers in the Network.  This makes the setup of Virtual Lab for Home much easier!!!</p>
<p>&nbsp;</p>
<p><u>References</u></p>
<p><a href="http://lifehacker.com/5714966/five-best-virtual-machine-applications" target="_blank" rel="noopener">http://lifehacker.com/5714966/five-best-virtual-machine-applications </a></p>
<p><a href="http://www.vmware.com/products/workstation" target="_blank" rel="noopener">www.vmware.com/products/workstation</a></p>
<p><a href="http://www.virtualbox.org/wiki/Downloads" target="_blank" rel="noopener">www.virtualbox.org/wiki/Downloads</a></p>
<p><a href="http://kb.vmware.com/selfservice/microsites/search.do?language=en_US&amp;cmd=displayKC&amp;externalId=1007250" target="_blank" rel="noopener">http://kb.vmware.com/selfservice/microsites/search.do?language=en_US&amp;cmd=displayKC&amp;externalId=1007250 </a></p>
