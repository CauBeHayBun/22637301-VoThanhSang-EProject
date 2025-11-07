# 22637301_VoThanhSang_EProject
Hệ thống Thương mại Điện tử Kiến trúc Microservices
### Tóm tắt Project
Đây là một dự án hệ thống bán hàng trực tuyến được phát triển dựa trên mô hình kiến trúc Microservices tiên tiến. Mục đích chính là trình bày một cách rõ ràng và thực tiễn việc xây dựng, mở rộng và triển khai các dịch vụ độc lập một cách hiệu quả thông qua công cụ Docker.

### Thực hiện bởi: Võ Thanh Sang - MSSV: 22637301

### Kiến trúc và Thành phần Chính
Hệ thống được cấu thành từ các dịch vụ nhỏ, chuyên biệt, giao tiếp với nhau:

**API Gateway** : Đảm nhận vai trò cửa ngõ, tiếp nhận và định tuyến (forward) mọi yêu cầu (request) từ người dùng (client) đến dịch vụ nội bộ tương ứng.

**Auth Service** (Dịch vụ Xác thực): Quản lý quy trình đăng ký, đăng nhập và xác thực người dùng, sử dụng cơ chế API Key để bảo mật.

**Product Service** (Dịch vụ Sản phẩm): Chịu trách nhiệm quản lý thông tin sản phẩm, danh mục sản phẩm, và logic liên quan đến việc khởi tạo đơn hàng.

**Order Service** (Dịch vụ Đơn hàng): Tập trung xử lý và quản lý toàn bộ các giao dịch và đơn hàng của khách hàng.

MongoDB: Cơ sở dữ liệu NoSQL được sử dụng để lưu trữ dữ liệu phân tán cho từng Microservice.

RabbitMQ: Một Message Broker, đóng vai trò quan trọng trong việc hỗ trợ giao tiếp bất đồng bộ (messaging) giữa các dịch vụ, đặc biệt là trong luồng xử lý của Order Service.

### Công nghệ Triển khai
Dự án ứng dụng các công nghệ hiện đại để đảm bảo hiệu suất và khả năng mở rộng:

**Nền tảng phát triển**: Node.js kết hợp với framework Express.

**Lưu trữ**: MongoDB.

**Giao tiếp bất đồng bộ**: RabbitMQ.

**Đóng gói và Triển khai**: Docker và Docker Compose.

**Cơ chế Cổng API**: Sử dụng HTTP Proxy cho API Gateway.

**Bảo mật**: Xác thực dựa trên API Key.