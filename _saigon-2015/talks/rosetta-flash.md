---
layout: talk
header-img: "img/index-bg.jpg"
title: Rosetta Flash
start_time: "13:30"
speakers:
  - Michele Spagnuolo
paper_url: https://docs.google.com/document/d/1CBfcPB4gl91MLmZAxnJcwS97yGcUwgHa5dB7yB6nrOo/edit?usp=sharing
slides_url: https://miki.it/RosettaFlash/RosettaFlash.pdf
description:
  - "In this talk we present Rosetta Flash (CVE-2014-4671, CVE-2014-5333),
  an exploitation technique that involves crafting charset-restricted
  Flash SWF files in order to abuse JSONP endpoints and allow Cross
  Site Request Forgery attacks against domains hosting JSONP endpoints,
  bypassing Same Origin Policy."

  - "With this attack it is possible to make a victim perform arbitrary
  requests to the domain with the JSONP endpoint and exfiltrate
  potentially sensitive data, not limited to JSONP responses, to an
  attacker-controlled site."

  - "High profile Google domains, YouTube, Twitter, LinkedIn, Yahoo!,
  eBay, Mail.ru, Flickr, Baidu, Instagram, Tumblr and Olark have had
  or still have vulnerable JSONP endpoints at the time of writing.
  Popular web development framework Ruby on Rails and MediaWiki also
  addressed this vulnerability."

  - "To better understand the attack scenario it is important to take
  into account the combination of three factors:"

  - "1) With Flash, a SWF file can perform cookie-carrying GET and POST requests to the domain that hosts it, with no crossdomain.xml check. This is why allowing users to upload a SWF file on a sensitive domain is dangerous: by uploading a carefully crafted SWF, an attacker can make the victim perform requests that have side effects and exfiltrate sensitive data to an external, attacker-controlled, domain."

  - "2) JSONP, by design, allows an attacker to control the first bytes of the output of an endpoint by specifying the callback parameter in the request URL. Since most JSONP callbacks restrict the allowed charset to [a-zA-Z_\\.], our tool focuses on this very restrictive charset, but it is general enough to work with different user-specified allowed charsets."

  - "3) SWF files can be embedded on an attacker-controlled domain using a Content-Type forcing <object> tag, and will be executed as Flash as long as the content looks like a valid Flash file."

  - "Rosetta Flash leverages zlib, Huffman encoding and ADLER32 checksum bruteforcing to convert any SWF file to an equivalent one composed of only alphanumeric characters, so that it can be passed as a JSONP callback and then reflected by the endpoint, effectively hosting the Flash file on the vulnerable domain. We use ad-hoc Huffman encoders in order to map non-allowed bytes to allowed ones. Naturally, since we are mapping a wider charset to a more restrictive one, this is not a real compression, but an inflation: we are, in a way, using Huffman as a Rosetta stone."

  - "In the Rosetta Flash GitHub repository (https://github.com/mikispag/rosettaflash) we provide ready-to-be-pasted full featured proofs of concept with ActionScript sources."

  - "Rosetta Flash has been nominated for a Pwnie Award and won an Internet Bug Bounty by HackerOne."
---
