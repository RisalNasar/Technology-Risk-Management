# Web Server Hardening Guide

Do not leak server version information to the outside world.  If this information is released, malicious actors could find the exact vulnerability your web server is susceptible to and attack you with much ease!

As a minimum, set in below in Apache Configuration `httpd.conf`:

```
ServerTokens Prod
ServerSignature Off
```

Further detailed instructions:

[Apache Web Server Hardening Steps](https://geekflare.com/apache-web-server-hardening-security/)

[Configure Web Servers to Hide Identity](https://www.acunetix.com/blog/articles/configure-web-server-disclose-identity/)