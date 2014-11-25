---
layout:     post
title:      "tetcon.org is now HTTPS only"
date:       2014-11-24 12:00:00
author:     "Thai"
header-img: "img/index-bg.jpg"
---
<p>
I still remember the first certificate that I ordered from Verisign costed a few thousand dollars. The verification process took several weeks and a lot of paperwork. I even had to scan and send Verisign my employer's operating license. It was such a bad experience and so expensive that I thought I would never run SSL on my personal sites, until I found <a href="https://sslmate.com">SSLMate</a> a few days ago. Woah! I just need to run a command to buy a certificate that is accepted by all browsers for only 15 bucks/year - as the saying goes it's even cheaper than a bowl of pho! Of course I get what I pay for, some browsers won't even show a green bar, but security-wise tetcon.org and its users get as much protection as www.google.com. Below is the configuration I used for my nginx web server - it's rated <a href="https://www.ssllabs.com/ssltest/analyze.html?d=tetcon.org">A+</a> by the SSL Labs:

<pre>
  <code>
  server {
    listen   80;
    listen 443 ssl;
    server_name tetcon.org www.tetcon.org;
    ssl_certificate     www.tetcon.org.chained.crt;
    ssl_certificate_key www.tetcon.org.key;
    ssl_protocols TLSv1 TLSv1.1 TLSv1.2;
    ssl_prefer_server_ciphers on;
    ssl_ciphers "EECDH+ECDSA+AESGCM EECDH+aRSA+AESGCM EECDH+ECDSA+SHA384 EECDH+ECDSA+SHA256 EECDH+aRSA+SHA384 EECDH+aRSA+SHA256 EECDH+aRSA+RC4 EECDH EDH+aRSA RC4 !aNULL !eNULL !LOW !3DES !MD5 !EXP !PSK !SRP !DSS !RC4";
    if ($ssl_protocol = "") {
       rewrite ^ https://$server_name$request_uri? permanent;
    }
    add_header Strict-Transport-Security 'max-age=31536000; includeSubDomains';
    add_header Public-Key-Pins 'max-age=3600; pin-sha256="Cm7n+dyRY9t97OOp3nIdI1sBq5U1BZfO+Y5WecBFgB0="; pin-sha256="k+4a7obu5IVsq0xaxDrzBSjPO0eNapo4x0xlahj3tlY="; includeSubDomains';
    ...
  }
  </code>
</pre>
</p>

<p>
	<i>Discuss this post on <a href="http://tinsang.net/news/3269">Tin Sang</a>.</i>
</p>
