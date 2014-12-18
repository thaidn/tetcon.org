---
layout: talk
header-img: "img/index-bg.jpg"
title: Building a “perfect” X86 diassembly framework
speakers:
  - Nguyen Anh Quynh
description:
  - "Disassembly framework is the core component in all security tools about binary analysis, malware analysis, reversing, debugging and exploit development. In any case, it is fundamental to have correct disassembly decoded from the machinecode, or the quality of the tools built on top it will be badly affected."

  - "However, building a “perfect” disassembly framework for Intel's X86 architecture is extremely challenging due to the special characteristics of X86 ISA. This talk is about some interesting tricky X86 code that are incorrectly handled by all public frameworks and reversing tools. Several “0-day“ X86 code that has never been documented in public will be released at the same time."

  - "One of the most biggest issues that we face during the development of X86 engine for Capstone framework (www.capstone-engine.org) is to discover undocumented X86 instructions. Towards the solution for this this problem, we will present some methodologies & tools that can help to automatically find undocumented code & verify their semantics. Some tools - with full source code - will also be public after this talk."
language: Vietnamese
start_time: "11:00"
---
