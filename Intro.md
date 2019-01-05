# Dẫn nhập

Trong kỷ nguyên hiện đại, phần mềm thường được phân phối dưới dạng dịch vụ: được gọi là ứng dụng web hoặc phần mềm dưới dạng dịch vụ. The Twelve Factor là một phương pháp để xây dựng các ứng dụng dưới dạng dịch vụ:

- Sử dụng các mẫu **Khai Báo (declarative)** để tự động hóa thiết lập, để giảm thiểu thời gian và chi phí cho các nhà phát triển mới tham gia dự án;
- Có một **Thoả Thuận Rõ Ràng (clean contract)** với các nền tảng hệ điều hành cơ bản, cung cấp tính di động tối đa giữa các môi trường thực thi;
- Thích hợp để **triển khai (deployment)** trên các nền tảng đám mây hiện đại, không cần phải quản trị hệ thống và máy chủ;
- **Giảm thiểu sự khác biệt** giữa phát triển (Devlopment) và sản xuất(Production), cho phép triển khai liên tục để nhanh nhẹn nhất;
- Và có thể **mở rộng quy mô** mà không có thay đổi đáng kể đối với công cụ, kiến trúc hoặc thực tiễn phát triển.

The Twelve Factor có thể được áp dụng cho các ứng dụng được viết bằng bất kỳ ngôn ngữ lập trình nào và bất kỳ dịch vụ hỗ trợ lưu trữ (cơ sở dữ liệu, hàng đợi, bộ nhớ cache, v.v.).

# Nền

Những người đóng góp cho tài liệu này đã trực tiếp tham gia vào việc phát triển và triển khai hàng trăm ứng dụng và gián tiếp chứng kiến sự phát triển, vận hành và nhân rộng hàng trăm ngàn ứng dụng thông qua công việc của chúng tôi trên nền tảng Heroku.

Tài liệu này tổng hợp tất cả kinh nghiệm và quan sát của chúng tôi về rất nhiều ứng dụng phần mềm phát triển dưới dạng dịch vụ với các diễn đạt tự nhiên nhất. Đây là một kim chỉ nang lý tưởng và thực tiễn để phát triển ứng dụng, đặc biệt chú ý đến khả năng mở rộng tính năng của ứng dụng theo thời gian, khả năng hợp tác giữa các nhà phát triển làm việc trên codebase của ứng dụng và tránh chi phí phát sinh khi phát triển phần mềm.

Cách trình bày của chúng tôi là xây dựng một sự chuẩn bị trước về một số vấn đề mang tính hệ thống mà chúng tôi đã thấy trong quá trình phát triển ứng dụng hiện đại, để cung cấp vốn từ vựng để thảo luận về các vấn đề đó và đưa ra một loạt các khái niệm, giải pháp cho các vấn đề đó với thuật ngữ đi kèm. Các trình bày này được lấy cảm hứng từ các cuốn sách của Martin Fowler, các mô hình kiến trúc và tái cấu trúc ứng dụng doanh nghiệp.

Ai nên đọc tài liệu này?

Bất kỳ nhà phát triển ứng dụng xây dựng nào chạy như một dịch vụ. Các kỹ sư Ops triển khai hoặc quản lý các ứng dụng đó.
