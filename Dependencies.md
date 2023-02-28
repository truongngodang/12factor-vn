II. Dependencies

Khai báo tường minh và cô lập các phụ thuộc

Hầu hết các ngôn ngữ lập trình cung cấp một hệ thống đóng gói để phân phối các thư viện hỗ trợ, chẳng hạn như CPAN cho Perl hoặc Rubygems cho Ruby. Các thư viện được cài đặt thông qua một hệ thống đóng gói có thể được cài đặt trên toàn hệ thống (được gọi là “sites package”) hoặc nằm trong phạm vi thư mục chứa ứng dụng (được gọi là “vendoring” hoặc “bundling”).

Một ứng dụng tuân thủ twelve-factor không bao giờ phụ thuộc vào sự tồn tại ngầm định của các gói trên toàn hệ thống. Nó khai báo tất cả các phụ thuộc, đầy đủ và chính xác, thông qua một dependency declaration manifest. Hơn nữa, nó sử dụng một dependency isolation trong quá trình thực thi để đảm bảo rằng không có phụ thuộc ngầm nào “rò rỉ” từ hệ thống xung quanh. Đặc tả phụ thuộc đầy đủ và rõ ràng được áp dụng thống nhất cho cả sản xuất và phát triển.

Ví dụ: Bundler cho Ruby cung cấp định dạng tệp kê khai Gemfile để khai báo phần phụ thuộc và gói exec để cách ly phần phụ thuộc. Trong Python có hai công cụ riêng biệt cho các bước này – Pip được sử dụng để khai báo và Virtualenv để cách ly. Ngay cả C cũng có Autoconf để khai báo phụ thuộc và liên kết tĩnh có thể cung cấp cách ly phụ thuộc. Bất kể chuỗi công cụ nào, khai báo phụ thuộc và cách ly phải luôn được sử dụng cùng nhau – chỉ cái này hay cái kia là không đủ để đáp ứng 12 yếu tố.

Một lợi ích của việc khai báo phụ thuộc rõ ràng là nó đơn giản hóa việc thiết lập cho các nhà phát triển mới sử dụng ứng dụng. Nhà phát triển mới có thể kiểm tra cơ sở mã của ứng dụng trên máy phát triển của họ, chỉ yêu cầu thời gian chạy ngôn ngữ và trình quản lý phụ thuộc được cài đặt làm điều kiện tiên quyết. Họ sẽ có thể thiết lập mọi thứ cần thiết để chạy mã của ứng dụng bằng lệnh xây dựng xác định. Ví dụ: lệnh xây dựng cho Ruby/Bundler là cài đặt gói, trong khi đối với Clojure/Leiningen, đó là lein deps.
