# TẠO VPS VỚI MẠNG RIÊNG (PRIVATE NETWORK)

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

- Quý khách chọn từ danh sách hệ điều hành có sẵn. Chúng tôi sẽ liên tục cập nhật các hệ điều hành phổ biến và mới nhất có thể ở danh sách này.

<div align="center">
  <img src="https://github.com/volevu17/VM-private/blob/main/003.png?raw=true" alt="Demo Image" width="800"/>
</div>

### Bước 4: Chọn Cấu Hình Máy Ảo 

- Mặc đinh hệ thống sẽ tự động mặc định thông số tối đa của gói toàn bộ tài nguyên của quý khách, quý khách có thể tùy chỉnh để phân chia số lượng máy chủ của mình mong muốn nếu cần tạo nhiều máy ảo hơn:

<div align="center">
  <img src="https://github.com/volevu17/VM-private/blob/main/004.png?raw=true" alt="Demo Image" width="800"/>
</div>

### Bước 5: Cấu Hình Mạng

- Tại mục **Interface net0** chọn chế độ Bridge tương ứng:
  - **Pri1501 (Private):** để sử dụng mạng nội bộ, để cấp Ip private cho VPS.
  - **Vmbr1 (Public):** để sử dụng mạng công cộng, để cấp Ip public cho VPS.
 
- Ở hướng dẫn này, chọn **Pri1501 (Private)** để sử dụng mạng riêng nội bộ.

<div align="center">
  <img src="https://github.com/volevu17/VM-private/blob/main/005.png?raw=true" alt="Demo Image" width="800"/>
</div>

### Bước 6: Khởi Tạo Máy Ảo

- Sau khi bấm nút **Tạo máy ảo mới** thì máy chủ của quý khách đang khởi tạo, quý khách vui lòng chờ đến khi máy chủ khởi tạo hoàn tất. Thời gian khởi tạo đối với máy ảo chạy hệ điều hành Windows Server (10 phút) sẽ lâu hơn Linux (3 phút).

- Quá trình khởi tạo tất, trang web sẽ tự động chuyển sang trang mới với tất cả thông tin máy chủ quý khách.

<div align="center">
  <img src="https://github.com/volevu17/VM-private/blob/main/006.png?raw=true" alt="Demo Image" width="800"/>
</div>

- Đến đây máy chủ ảo của quý khách đã tạo xong, quý khách có thể truy cập vào **Console** để sử dụng.

----
# THÊM NIC PRIVATE VÀO VPS ĐANG HOẠT ĐỘNG

Kính chào quý khách,

Dưới đây là hướng dẫn cách thêm hoặc xoá NIC mạng nội bộ (Private NIC) cho VPS đang sử dụng. Quý khách vui lòng thực hiện theo các bước sau:

### Bước 1: Chọn Máy Ảo Cần Nâng Cấp

- Chọn máy ảo cần nâng cấp và tắt máy (shutdown) để đảm bảo an toàn. Quý khách có thể shutdown trực tiếp từ bên trong máy chủ hoặc bấm nút **Tắt nguồn**.

<div align="center">
  <img src="https://github.com/volevu17/VM-private/blob/main/007.png?raw=true" alt="Demo Image" width="800"/>
</div>

### Bước 2: Tiến Hành Nâng Cấp Và Thêm Card Mạng

- Đảm bảo máy chủ ở trạng thái OFF, sau đó bấm vào nút **Nâng cấp**

<div align="center">
  <img src="https://github.com/volevu17/VM-private/blob/main/008.png?raw=true" alt="Demo Image" width="800"/>
</div>

- Chuyển đến tab Mạng > chọn Interfaces > nhấn **Thêm card mạng mới**.
  
<div align="center">
  <img src="https://github.com/volevu17/VM-private/blob/main/009.png?raw=true" alt="Demo Image" width="800"/>
</div>

- Trang web sẽ tự động chuyển sang phần cấu hình **Thêm card mạng** cho VPS.

- Tại mục **Bridge** quý khách có thể lựa chọn.
  - **Pri1501 (Private):** để sử dụng mạng nội bộ, để cấp Ip private cho VPS.
  - **Vmbr1 (Public):** để sử dụng mạng công cộng, để cấp Ip public cho VPS.
- Tại hướng dẫn này, để sử dụng mạng nội bộ chọn **Pri1501 (Private):**

- Tiếp theo quý khách chọn **Assign new IP:** để hệ thống tự động cấp một địa chỉ IP mới cho card mạng vừa thêm. 

<div align="center">
  <img src="https://github.com/volevu17/VM-private/blob/main/010.png?raw=true" alt="Demo Image" width="800"/>
</div>

- Click **Thêm card mạng mới** để hoàn tất. Hệ thống sẽ xử lý và cập nhật cấu hình.

- Sau đó, khởi động lại VPS để bắt đầu sử dụng với NIC mới.

<div align="center">
  <img src="https://github.com/volevu17/VM-private/blob/main/011.png?raw=true" alt="Demo Image" width="800"/>
</div>

### Bước 3: Kiểm Tra Bên Trong OS 

- Sau khi VPS khởi động lại, quý khách có thể kiểm tra bên trong OS:

  - Với Linux thì dùng lệnh: 

   ```bash
    ip a
   ```

- Với Windows thì dùng lệnh này ở CMD:

```bash
    ipconfig /all
   ```
<div align="center">
  <img src="https://github.com/volevu17/VM-private/blob/main/012.png?raw=true" alt="Demo Image" width="800"/>
</div>

### Bước 4: Xóa Gateway khỏi NIC Private

 #### 1. Xóa Gateway khỏi NIC Private ở Linux
- Khi có 2 card mạng đều thuộc mạng nội bộ (Private), quý khách nên gỡ một gateway để tránh xung đột định tuyến.

- Mở file cấu hình trong OS

```bash
sudo nano /etc/netplan/50-cloud-init.yaml
```

- Tiếp theo gỡ Gateway của card mạng vừa thêm

<div align="center">
  <img src="https://github.com/volevu17/VM-private/blob/main/013.png?raw=true" alt="Demo Image" width="800"/>
</div>

- Lưu và áp dụng cấu hình bằng lệnh:

```bash
sudo netplan apply
```

#### 2. Xóa Gateway khỏi NIC Private ở Windows

- Chạy **Run** và nhập dòng lệnh **ncpa.cpl** để vào được *Network Connections*
  
- Chọn **Ethernet 2:** Là NIC private vừa được thêm vào

<div align="center">
  <img src="https://github.com/volevu17/VM-private/blob/main/014.png?raw=true" alt="Demo Image" width="800"/>
</div>

- Click chuột chọn **Properties** > Internet Protocol Version 4 (TCP/IPv4)
- Xóa giá trị tại trường **Default Gateway** > Nhấn **OK** để lưu

<div align="center">
  <img src="https://github.com/volevu17/VM-private/blob/main/015.png?raw=true" alt="Demo Image" width="800"/>
</div>

Trên đây là toàn bộ hướng dẫn tạo VPS sử dụng mạng nội bộ (private network) và cách thêm NIC private vào máy chủ đang hoạt động. Hy vọng bài viết sẽ giúp quý khách dễ dàng quản lý và mở rộng hệ thống mạng của mình. Kính chúc quý khách sử dụng dịch vụ Cloud VPS tại VNDATA hiệu quả và ổn định.




