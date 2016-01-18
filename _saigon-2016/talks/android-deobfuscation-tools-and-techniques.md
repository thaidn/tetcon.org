---
layout: talk
header-img: "img/index-bg.jpg"
title: "Android Deobfuscation Tools and Techniques"
speakers:
  - display_name: Caleb Fenton
    link_name: Caleb Fenton
description:
  - "State of android deobfuscation is weak. Commercial obfuscators are getting more common, and reversers need to understand how to deobfuscate them. This talk provides an overview of different obfuscation types. After that, it describes two code deobfuscation approaches: pattern recognition and virtual execution."
  - "Pattern recognition focuses mainly on identifying obfuscation patterns, crafting into regular expressions, and then repeatedly applying pattern-based transformations on the code. Insight into code behavior is improved by limited execution of certain methods and storing the result."
  - "Virtual execution involves simulating the applications code to determine semantics. A context sensitive graph is generated representing every possible execution path and all possible register + class states for each execution of each instruction. This is then analyzed and modified to make the code easier to understand but behaves identically."

language: English
start_time: "09:00"
presentation_urls:
  - https://drive.google.com/open?id=0B_L6MdkbAn4MTGRFRFYzT1UxS28
github_urls:
  - https://github.com/CalebFenton/dex-oracle
  - https://github.com/CalebFenton/simplify
---
