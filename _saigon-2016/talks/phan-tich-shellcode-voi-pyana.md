---
layout: talk
header-img: "img/index-bg.jpg"
title: "Phân tích shellcode với PyAna"
speakers:
  - display_name: Luc Nguyen 
    link_name: Luc Nguyen 
description:
  - "Phân tích shellcode không hề dễ dàng, đặc biệt các shellcode được phát triển chạy trên hệ điều hành Windows. Quá trình phân tích tĩnh thường kém hiệu quả và dễ dàng bị vượt qua bởi shellcode, hơn thế nữa các công cụ phân tích tĩnh thường không miễn phí. Quá trình phân tích động đòi hỏi shellcode được debug trong một không gian bộ nhớ của một process khác và thực thi trong một môi trường máy ảo phù hợp."
  - "Chúng tôi đã phát triển PyAna, nhằm giải quyết các khó khăn trong việc phân tích shellcode trên Windows. PyAna sử dụng Unicorn Framework để mô phỏng CPU và mô phỏng một process trên Windows để phân tích shellcode. Bằng việc mô phỏng, PyAna cho phép tự động hóa quá trình phân tích, cung cấp khả năng phân tích mềm dẻo, linh hoạt, đặc biệt là đa nền tảng mà không cần một máy ảo phân tích."
  - "Trong tương lai, ý tưởng của PyAna có thể được ứng dụng vào các lĩnh vực khác của security như phân tích malware, fuzzing hoặc phát hiện lỗ hổng phần mềm."
language: Vietnamese 
start_time: "14:15"
presentation_urls:
  - https://drive.google.com/open?id=0B_L6MdkbAn4MWHE4UmNMcno2eU0
github_urls:
  - https://github.com/PyAna/PyAna
---
