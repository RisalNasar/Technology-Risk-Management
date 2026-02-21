# <p><strong><span style="text-decoration: underline;">Patch SSL Vulnerabilities in Browser and Server</span></strong></p>
<p>Use <a href="https://www.ssllabs.com/index.html" target="_blank" rel="noopener">SSL Labs</a> to test your Browser and Server for SSL vulnerabilities.  The most common vulnerabilities and how to patch them are mentioned below:</p>
<p>1) Certificate uses weak hashing algorithm (example: MD5, SHA-1, etc)</p>
<p>Get new SSL certificates issued with the latest hashing algorithm (example: SHA-2, SHA-3)</p>
<p>2) SSL v2 / v3, which are vulnerable versions of SSL, are supported by the browser / server.</p>
<p>Update your browser to the latest version.</p>
<p>To mitigate server side SSL vulnerabilities, please refer to <a href="https://wiki.mozilla.org/Security/Server_Side_TLS" target="_blank" rel="noopener">https://wiki.mozilla.org/Security/Server_Side_TLS </a> to learn about the best SSL configuration for common server platforms.</p>
<p>3) Forward Secrecy is not enabled.</p>
<p>The ordering of a ciphersuite is very important in deciding which algorithms are going to be selected in priority. The recommendation in the mozilla link above prioritizes algorithms that provide perfect forward secrecy.</p>
<p>4) Weak cipher suites are enabled.</p>
<p>Refer to the recommendations in the mozilla link above for common servers.</p>
<p>4) Vulnerable to SSL Fallback attack.</p>
<p>Upgrade to the latest version of OpenSSL which supports the TLS_FALLBACK_SCSV implementation which prevents an SSL protocol downgrade attack.</p>
<p><span style="text-decoration: underline;">Note</span>: For IBM HTTP Servers, refer to this <a href="http://www-01.ibm.com/support/docview.wss?uid=swg21179559" target="_blank" rel="noopener">link </a>to learn more about how to configure SSL.  The commands are not covered in the mozilla link above.  But, the idea is to learn from the mozilla link and implement using the IBM proprietary directives mentioned in the IBM link.</p>
<p><span style="text-decoration: underline;">References</span></p>
<p><a href="http://unix.stackexchange.com/questions/162478/how-to-disable-sslv3-in-apache" target="_blank" rel="noopener">http://unix.stackexchange.com/questions/162478/how-to-disable-sslv3-in-apache</a></p>
<p><a href="http://askubuntu.com/questions/537196/how-do-i-patch-workaround-sslv3-poodle-vulnerability-cve-2014-3566" target="_blank" rel="noopener">http://askubuntu.com/questions/537196/how-do-i-patch-workaround-sslv3-poodle-vulnerability-cve-2014-3566</a></p>
<p><a href="http://stackoverflow.com/questions/26406586/how-to-enable-tls-fallback-scsv-on-apache" target="_blank" rel="noopener">http://stackoverflow.com/questions/26406586/how-to-enable-tls-fallback-scsv-on-apache</a></p>
<p><a href="https://www-01.ibm.com/support/knowledgecenter/linuxonibm/liaag/wascrypt/l0wscry00_configihssslsupport.htm" target="_blank" rel="noopener">https://www-01.ibm.com/support/knowledgecenter/linuxonibm/liaag/wascrypt/l0wscry00_configihssslsupport.htm</a></p>
<p><a href="http://www-01.ibm.com/support/knowledgecenter/SSAW57_8.5.5/com.ibm.websphere.ihs.doc/ihs/rihs_ssldirs.html" target="_blank" rel="noopener">http://www-01.ibm.com/support/knowledgecenter/SSAW57_8.5.5/com.ibm.websphere.ihs.doc/ihs/rihs_ssldirs.html</a></p>
<p><a href="https://developer.ibm.com/answers/questions/210626/does-ibm-http-server-support-apache-directive-sslh.html" target="_blank" rel="noopener">https://developer.ibm.com/answers/questions/210626/does-ibm-http-server-support-apache-directive-sslh.html</a></p>
