---
layout: talk
header-img: "img/index-bg.jpg"
title: Rosetta Flash
start_time: "10:45"
language: English
speakers:
  - link_name: Michele Spagnuolo
    display_name: Michele Spagnuolo
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
presentation_urls:
  - https://docs.google.com/a/tetcon.org/file/d/0B__XkpZ7x-l0Q2M4X05NZ1c5SDQ/edit
---
