---
layout: talk
header-img: "img/index-bg.jpg"

title: "Xây dựng thư viện dịch ngược “hoàn hảo” cho kiến trúc X86"

speakers:
  - link_name: Nguyen Anh Quynh
    display_name: Nguyễn Anh Quỳnh

description:
  - "Dịch ngược mã máy (machine code) ra mã assembly là phần cốt lõi của các công cụ bảo mật trong một loạt các lĩnh vực như phân tích tự động mã máy (binary analysis), phân tích mã độc (malware), dịch ngược (reverse), gỡ rối (debug), hay viết mã khai thác lỗi (exploit development). Trên mọi trường hợp, việc dịch ngược một cách đầy đủ và chính xác là một yêu cầu căn bản có ý nghĩa quyết định cho chất lượng của những công cụ liên quan."

  - "Tuy nhiên, dịch ngược mã máy X86 là một thách thức lớn do tập lệnh của nền tảng Intel này có kiến trúc rất độc đáo. Bài trình bày này là một câu chuyện kể về một loạt các mã máy X86 dị biệt bị diễn giải sai bởi tất cả các thư viện cũng như phần lớn các công cụ dịch ngược hiện hành. Một số mã máy “0-day” chưa từng được đề cập từ trước tới nay được chúng tôi phát hiện trong quá trình phát triển bộ thư viện dịch ngược Capstone (www.capstone-engine.org) sẽ lần đầu tiên được công bố."

  - "Một trong những khó khăn lớn nhất đặt ra là việc tìm kiếm và kiểm chứng những mã máy không được hỗ trợ một cách chính thống, hoặc thậm chí được giữ “bí mật” bởi Intel. Để giải quyết vấn đề này, chúng tôi sẽ đề xuất vài phương pháp, và giới thiệu những công cụ mới đã được xây dựng và triển khai một cách có hệ thống góp phần giúp kiểm chứng ngữ nghĩa của mã máy một cách tự động. Một số công cụ, kèm theo mã nguồn mở, cũng sẽ được cung cấp sau đó."

title_en: Building a “perfect” X86 diassembly framework
description_en:
  - "Disassembly framework is the core component in all security tools about binary analysis, malware analysis, reversing, debugging and exploit development. In any case, it is fundamental to have correct disassembly decoded from the machinecode, or the quality of the tools built on top it will be badly affected."

  - "However, building a “perfect” disassembly framework for Intel's X86 architecture is extremely challenging due to the special characteristics of X86 ISA. This talk is about some interesting tricky X86 code that are incorrectly handled by all public frameworks and reversing tools. Several “0-day“ X86 code that has never been documented in public will be released at the same time."

  - "One of the most biggest issues that we face during the development of X86 engine for Capstone framework (www.capstone-engine.org) is to discover undocumented X86 instructions. Towards the solution for this this problem, we will present some methodologies & tools that can help to automatically find undocumented code & verify their semantics. Some tools - with full source code - will also be public after this talk."
language: Vietnamese
start_time: "15:45"
---
