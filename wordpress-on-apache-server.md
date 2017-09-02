# <p><strong><u>Setting Up WordPress on an Apache Server on Ubuntu</u></strong></p>
<p>Install the Ubuntu Operating System on your Computer’s Hard Disk physically or using a Virtualization Software.</p>
<p>Install the LAMP (Linux, Apache, MySQL and PHP) stack bundle by following instructions at this <a href="https://www.digitalocean.com/community/tutorials/how-to-install-linux-apache-mysql-php-lamp-stack-on-ubuntu-14-04" target="_blank" rel="noopener">link</a>.</p>
<p>Install WordPress Content Management System (CMS) in Ubuntu leveraging on the LAMP stack by following instructions at this <a href="https://www.digitalocean.com/community/tutorials/how-to-install-wordpress-on-ubuntu-14-04" target="_blank" rel="noopener">link</a>.  Before going into the “Configure Pretty Permalinks for WordPress” section in the link, the server need to be allocated a domain name or IP address which always points to the server.</p>
<p>A dynamic DNS service could be used to achieve the same.  One such provider is: <a href="https://www.noip.com" target="_blank" rel="noopener">https://www.noip.com</a> .  You can create a free account with them and add about three hosts to a subdomain of your choosing to the domains they offer.</p>
<p>Make sure that the public IP address of the computer where your apache is installed is added to the host list. </p>
<p><img class="alignnone" src="https://farm6.staticflickr.com/5695/22593407716_f423bc6bb6_o.png" alt="No-IP_HostName_to_DomainName_Config" width="832" height="593" /></p>
<p><script src="//embedr.flickr.com/assets/client-code.js" async="" charset="utf-8"></script></p>
<p>Enable IP Address Reservation at the NAT Router for the machine on which the Apache Server is installed, so that it gets a reserved internal address after any reboot.</p>
<p><img class="alignnone" src="https://farm6.staticflickr.com/5704/22593408056_eb9d41a28b_o.png" alt="NAT_Router_Address_Reservation" width="1222" height="361" /></p>
<p><script src="//embedr.flickr.com/assets/client-code.js" async="" charset="utf-8"></script></p>
<p>Configure your NAT router so that requests that are received at port 80 (HTTP) / 443 (HTTPS) / 8245 (No-IP DUC Port) are forwarded to the internal IP address of the machine where the Apache server is installed.</p>
<p><img class="alignnone" src="https://farm6.staticflickr.com/5772/22605891892_84ec3ac300_o.png" alt="NAT_Router_Port_Forwarding" width="1078" height="365" /></p>
<p><script src="//embedr.flickr.com/assets/client-code.js" async="" charset="utf-8"></script></p>
<p>Install the Linux Dynamic DNS Update Client (DUC) by following the instructions at this <a href="https://www.noip.com/support/knowledgebase/installing-the-linux-dynamic-update-client-on-ubuntu/" target="_blank" rel="noopener">link</a>.</p>
<p>To ensure that the No-IP DUC is running at startup and closing when the system is being shutdown, a script should be created and placed at /etc/init.d/</p>
<p>The contents of the script should be as shown below:</p>
<pre class="lang:sh decode:true ">        #######################################################
        #! /bin/sh

        case "$1" in
            start)
                echo "Starting noip2."
                /usr/local/bin/noip2
            ;;
            stop)
                echo -n "Shutting down noip2."
         
                for i in `/usr/local/bin/noip2 -S 2&gt;&amp;1 | grep Process | awk '{print $2}' | tr -d ','`
  		do
    			/usr/local/bin/noip2 -K $i
  		done

       		#killproc -TERM /usr/local/bin/noip2
            ;;
            *)
                echo "Usage: $0 {start|stop}"
                exit 1
        esac
        exit 0
        #######################################################
</pre>
<p>&nbsp;</p>
<p>Please refer to instructions at this <a href="https://www.howtoforge.com/how-to-install-no-ip2-on-ubuntu-12.04-lts-in-order-to-host-servers-on-a-dynamic-ip-address" target="_blank" rel="noopener">link</a>.  It mentions further on how to test the above script, adding the correct permissions and invoking the script for multi user loads by adding the scirpt call to /etc/rc.local script file.</p>
<p>Continue with instructions at this <a href="https://www.digitalocean.com/community/tutorials/how-to-install-wordpress-on-ubuntu-14-04" target="_blank" rel="noopener">link</a> and complete instructions under the section “Configure Pretty Permalinks for WordPress”, after using the domain name acquired through No-IP as the ServerName.</p>
<p>In order to enable Wordpress updates, without setting up FTP/SSH accounts in the server, add the below statement into /var/www/html/wp-config.php</p>
<pre class="lang:sh decode:true">define('FS_METHOD','direct');</pre>
<p>You may refer to this <a href="http://www.hongkiat.com/blog/update-wordpress-without-ftp/" target="_blank" rel="noopener">link</a> for detailed screenshots and instructions.</p>
<p><strong><u>Making WordPress accessible from the Internet</u></strong></p>
<p>Most ISPs block traffic to common ports (port 22, 23, 80,, etc) of the IP address allocated to their customers as a security measure against attacks.</p>
<p>If the HTTP port (80) is blocked by your ISP, then your WordPress site would not be reachable over the Internet, but only within your LAN (Internal network).</p>
<p><img class="alignnone" src="https://farm1.staticflickr.com/687/22615600422_e42ba2b15c_o.png" alt="Internet_Access_Before_Redirection" width="892" height="469" /></p>
<p><script src="//embedr.flickr.com/assets/client-code.js" async="" charset="utf-8"></script></p>
<p>In order to make the WordPress site available over the Internet, the NAT Router, WordPress and apache web server configurations should be modified to enable web communication over a non-standard port (example: 8080 instead of 80).</p>
<p>Change the NAT Router configuration to forward web requests over port 8080 to be redirected to the internal IP address of the server installation.</p>
<p><img class="alignnone" src="https://farm6.staticflickr.com/5669/22006042404_d452371a22_o.png" alt="NAT_Router_Non-Standard_Port_Forwarding" width="1132" height="371" /></p>
<p>At the WordPress site, go to Dashboard &gt; Settings &gt; General.  Change the WordPress Address (URL) and Site Address (URL) to point to <em>your_site_address:8080.  </em></p>
<p><script src="//embedr.flickr.com/assets/client-code.js" async="" charset="utf-8"></script></p>
<p><img class="alignnone" src="https://farm1.staticflickr.com/604/22007674233_7cc24dc15a_o.png" alt="WordPress_Dashboard_URL_Configuration" width="888" height="460" /></p>
<p><script src="//embedr.flickr.com/assets/client-code.js" async="" charset="utf-8"></script></p>
<p>Save the URL configuration change in the Settings page.</p>
<p>Within the Ubuntu OS, perform the below configurations with apache:</p>
<pre class="lang:sh decode:true">sudo vim /etc/apache2/ports.conf</pre>
<p>Configurations should be modified to be as shown below:</p>
<p><img class="alignnone" src="https://farm1.staticflickr.com/650/22602813156_b0bcfa8743_o.png" alt="port_listen_conf" width="314" height="182" /></p>
<p><script src="//embedr.flickr.com/assets/client-code.js" async="" charset="utf-8"></script></p>
<pre class="lang:sh decode:true">sudo vim /etc/apache2/sites-available/000-default.conf</pre>
<p>Change configurations to be as shown below:</p>
<p><img class="alignnone" src="https://farm6.staticflickr.com/5672/22602813126_934e22fcf9_o.png" alt="virtualhost_port_conf" width="461" height="240" /></p>
<p><script src="//embedr.flickr.com/assets/client-code.js" async="" charset="utf-8"></script></p>
<p>Restart apache server.</p>
<pre class="lang:sh decode:true">sudo service apache2 restart</pre>
<p>Now you should be able to reach the WordPress site by using the URL <em>your_site_url:8080 </em>(example: <em>www.example.com:8080</em>) !!!</p>
<p><img class="alignnone" src="https://farm1.staticflickr.com/664/22007992533_21a20783d5_o.png" alt="Internet_Access_Port_Redirected" width="1033" height="396" /></p>
<p>&nbsp;</p>
<p><strong><u>Enabling SSL through a Self-Signed Certificate for the WordPress Installation</u></strong></p>
<p>Open the WordPress Dashboard -&gt; Settings -&gt; General.  Modify the WordPress Address (URL) and Site Address (URL) values to indicate <em>https://your_site_address</em></p>
<p><img class="alignnone" src="https://farm1.staticflickr.com/780/22042214924_f657a6afa5_o.png" alt="WordPress_Dashboard_URL_Configuration_HTTPS" width="846" height="343" /></p>
<p><script src="//embedr.flickr.com/assets/client-code.js" async="" charset="utf-8"></script></p>
<p>Check to ensure that .htaccess overrides are allowed for folder locations where the WordPress files are installed.  This is required to enable Permalinks to fuction.  The below code should be present in  your /etc/apache2/apache2.conf file.</p>
<pre class="lang:sh decode:true">&lt;Directory /var/www/html/&gt;
    Options FollowSymLinks
    AllowOverride All
 &lt;/Directory&gt;</pre>
<p>Finally, follow instructions at this <a href="https://www.digitalocean.com/community/tutorials/how-to-create-a-ssl-certificate-on-apache-for-ubuntu-14-04" target="_blank" rel="noopener">link</a> to generate a self-signed SSL certificate, enable SSL apache modules and set SSL apache configurations.</p>
<p>Now, your entire site should be accessible over HTTPS !!!</p>
<p><script src="//embedr.flickr.com/assets/client-code.js" async="" charset="utf-8"></script></p>
<p><u>Other References</u></p>
<p>Install Ubuntu 14.04 LTS in VMware Workstation: <a href="https://www.youtube.com/watch?v=w9gtQEPtnI8" target="_blank" rel="noopener">https://www.youtube.com/watch?v=w9gtQEPtnI8</a></p>
<p><a href="http://www.ubuntu.com/download/desktop" target="_blank" rel="noopener">http://www.ubuntu.com/download/desktop</a></p>
<p><a href="https://mobiarch.wordpress.com/2014/05/16/creating-an-init-script-in-ubuntu-14-04/" target="_blank" rel="noopener">https://mobiarch.wordpress.com/2014/05/16/creating-an-init-script-in-ubuntu-14-04/</a></p>
<p><a href="http://www.noip.com/support/knowledgebase/what-port-does-the-dynamic-update-client-use/" target="_blank" rel="noopener">http://www.noip.com/support/knowledgebase/what-port-does-the-dynamic-update-client-use/</a></p>
<p><a href="http://codex.wordpress.org/Using_Permalinks" target="_blank" rel="noopener">http://codex.wordpress.org/Using_Permalinks</a></p>
