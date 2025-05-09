# TẠO VPS VỚI NETWORK PRIVATE

Kính chào quý khách,

Sau khi quý khách đăng ký và thanh toán thành công, hệ thống sẽ tự động khởi tạo dịch vụ Cloud VPS và quý khách đã có thể tiến hành tạo máy chủ để sử dụng.

Các bước hướng dẫn bên dưới được thực hiện sau khi quý khách đã đăng nhập thành công vào trang Portal để quản lý dịch vụ (https://clients.vndata.vn/ ), sau khi đăng nhập thành công thì thực hiện theo các bước sau:

### Bước 1: Thêm Máy Chủ Mới 

* Quý khách click vào **Thêm máy chủ mới** như trên hình

<div align="center">
  <img src="https://github.com/volevu17/VM-private/blob/main/001.png?raw=true" alt="Demo Image" width="800"/>
</div>

### Bước 2: Giao Diện "Tạo Máy Chủ Mới"

* Trang web sẽ tự động chuyển sang phần điền thông tin và cấu hình máy chủ quý khách cần khởi tạo

<div align="center">
  <img src="https://github.com/volevu17/VM-private/blob/main/002.png?raw=true" alt="Demo Image" width="800"/>
</div>

- **Tên máy chủ**: Là hostname (đối với Linux), Computer name (đối với Windows).
- **Mật khẩu**: Quý khách sẽ sử dụng mật khẩu này để kết nối đến máy chủ, ssh (đối với Linux), remote desktop (đối với Windows).
- **SSH Keys (tùy chọn)**: Hoặc quý khách có thể bỏ qua bước này nếu không muốn sử dụng public ssh key: chỉ hoạt động đối với OS Linux, quý khách có thể add public ssh key của máy mình lên server thông qua quá trình khởi tạo.
  - Để add ssh key vào server, quý khách click chuột vào Quản lý SSH Keys.
  - Trang web sẽ chuyển sang phần add ssh key.
  - Quý khách chọn “ Add new ssh key “.

### Bước 3: Lựa Chọn Cài Đặt Hệ Điều Hành
- Quý khách chọn từ danh sách hệ điều hành có sẳn. Chúng tôi sẽ liên tục cập nhật các hệ điều hành phổ biến và mới nhất có thể ở danh sách này.

<div align="center">
  <img src="https://github.com/volevu17/VM-private/blob/main/003.png?raw=true" alt="Demo Image" width="800"/>
</div>

### Bước 4: Chọn Cấu Hình Máy Ảo 

- Mặc đinh hệ thống sẽ tự động mặc định thông số tối đa của gói toàn bộ tài nguyên của quý khách, quý khách có thể tùy chỉnh để phân chia số lượng máy chủ của mình mong muốn nếu cần tạo nhiều máy ảo hơn:

<div align="center">
  <img src="https://github.com/volevu17/VM-private/blob/main/004.png?raw=true" alt="Demo Image" width="800"/>
</div>
