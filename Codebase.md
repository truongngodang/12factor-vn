# I. Codebase

Một codebase được theo dõi trong kiểm soát sửa đổi, nhiều triển khai.

Một twelve app luôn được theo dõi trong một hệ thống version control system, chẳng hạn như Git, Mercurial hoặc Subversion. Một cơ sở dữ liệu lưu trữ mã nguồn và theo dõi sự thay đổi của mã nguồn được biết đến như là một kho lưu trữ code (code repository), gọi tắt là code repo hay repo.

Một codebase là bất kỳ repo đơn lẻ nào (trong hệ thống kiểm soát sửa đổi tập trung như Subversion) hoặc bất kỳ tập hợp repos nào có share commit (trong hệ thống kiểm soát sửa đổi phi tập trung như Git).

Luôn có mối tương quan một-một giữa codebase và ứng dụng:

Nếu có nhiều cơ sở mã hóa, thì nó không phải là một ứng dụng - đó là một hệ thống phân tán. Mỗi thành phần trong một hệ thống phân tán là một ứng dụng và mỗi thành phần có thể tuân thủ riêng mười hai yếu tố.
Nhiều ứng dụng chia sẻ cùng một mã là vi phạm mười hai yếu tố. Giải pháp ở đây là đóng gói mã đó thành các thư viện có thể được chia sẻ thông qua trình quản lý phụ thuộc (dependency manager).

![alt codebase](codebase-deploys.png)

Chỉ có duy nhất một codebase cho mỗi ứng dụng, nhưng sẽ có nhiều triển khai (deploys) cho ứng dụng. Một triển khai là một phiên bản có thể chạy của ứng dụng. Đây thường là một bản production và một hoặc nhiều bản dựng (staging). Ngoài ra, mọi nhà phát triển đều có một bản sao của ứng dụng chạy trong môi trường phát triển nội bộ của họ, mỗi ứng dụng cũng có thể triển khai độc lập như bản production.

Codebase giống nhau trên tất cả các triển khai, mặc dù có thể có sự khác nhau về nhãn các phiên bản (version name) trên mỗi triển khai. Ví dụ, một developer có một số commit chưa được triển khai trên bản dựng (staging); bản dựng có một số commit chưa được triển khai trên bản production. Nhưng tất cả chúng đều có chung một codebase, do đó làm cho chúng có thể được xác định như là các triển khai khác nhau của cùng một ứng dụng.
