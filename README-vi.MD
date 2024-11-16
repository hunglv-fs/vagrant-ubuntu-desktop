Dưới đây là các **tập lệnh (commands)** hay sử dụng trong Vagrant, giúp bạn quản lý và thao tác với máy ảo:

### 1. **Khởi tạo và cấu hình Vagrant**
- **`vagrant init`**  
  Tạo một file `Vagrantfile` mới trong thư mục hiện tại.
  ```bash
  vagrant init
  ```

### 2. **Quản lý máy ảo**
- **`vagrant up`**  
  Khởi động máy ảo. Nếu máy ảo chưa tồn tại, Vagrant sẽ tự động tải và tạo máy ảo từ box đã cấu hình trong `Vagrantfile`.
  ```bash
  vagrant up
  ```

- **`vagrant halt`**  
  Tắt máy ảo một cách nhẹ nhàng (không tắt hoàn toàn, mà giống như tắt máy tính).
  ```bash
  vagrant halt
  ```

- **`vagrant destroy`**  
  Xóa hoàn toàn máy ảo và các tài nguyên liên quan đến nó (máy ảo không thể phục hồi).
  ```bash
  vagrant destroy
  ```

- **`vagrant reload`**  
  Tải lại máy ảo, áp dụng các thay đổi trong `Vagrantfile`.
  ```bash
  vagrant reload
  ```

- **`vagrant suspend`**  
  Tạm dừng máy ảo và lưu trạng thái hiện tại.
  ```bash
  vagrant suspend
  ```

- **`vagrant resume`**  
  Tiếp tục máy ảo sau khi đã tạm dừng.
  ```bash
  vagrant resume
  ```

- **`vagrant status`**  
  Kiểm tra trạng thái của máy ảo (đang chạy, tắt, v.v.).
  ```bash
  vagrant status
  ```

- **`vagrant provision`**  
  Chạy lại các tập lệnh provision đã được cấu hình trong `Vagrantfile`.
  ```bash
  vagrant provision
  ```

### 3. **Kết nối với máy ảo**
- **`vagrant ssh`**  
  Kết nối vào máy ảo thông qua SSH mà không cần nhập mật khẩu (Vagrant đã cấu hình SSH key).
  ```bash
  vagrant ssh
  ```

### 4. **Quản lý box (image của máy ảo)**
- **`vagrant box add`**  
  Thêm một box vào danh sách box của Vagrant.
  ```bash
  vagrant box add <box-name> <box-url>
  ```

- **`vagrant box list`**  
  Liệt kê tất cả các box đã được cài đặt trong Vagrant.
  ```bash
  vagrant box list
  ```

- **`vagrant box remove`**  
  Xóa một box khỏi danh sách các box cài đặt.
  ```bash
  vagrant box remove <box-name>
  ```

### 5. **Cập nhật và quản lý Vagrant**
- **`vagrant plugin install <plugin-name>`**  
  Cài đặt một plugin cho Vagrant.
  ```bash
  vagrant plugin install <plugin-name>
  ```

- **`vagrant plugin list`**  
  Liệt kê tất cả các plugin đã được cài đặt.
  ```bash
  vagrant plugin list
  ```

- **`vagrant plugin update`**  
  Cập nhật tất cả các plugin đã cài đặt.
  ```bash
  vagrant plugin update
  ```

- **`vagrant box outdated`**  
  Kiểm tra xem có box nào đã lỗi thời và cần cập nhật.
  ```bash
  vagrant box outdated
  ```

### 6. **Quản lý thư mục đồng bộ**
- **`vagrant rsync`**  
  Đồng bộ hóa thư mục giữa máy chủ (host) và máy ảo (guest) thông qua `rsync`.
  ```bash
  vagrant rsync
  ```

### 7. **Quản lý môi trường Vagrant**
- **`vagrant global-status`**  
  Liệt kê tất cả các máy ảo đang được quản lý bởi Vagrant trên hệ thống của bạn, kể cả những máy đã bị xóa hoặc không còn tồn tại.
  ```bash
  vagrant global-status
  ```

- **`vagrant ssh-config`**  
  Hiển thị thông tin SSH cấu hình cho việc kết nối từ máy chủ tới máy ảo.
  ```bash
  vagrant ssh-config
  ```

### 8. **Khắc phục sự cố**
- **`vagrant up --debug`**  
  Chạy `vagrant up` với chế độ debug, cung cấp thêm thông tin để giúp xác định vấn đề khi khởi động máy ảo.
  ```bash
  vagrant up --debug
  ```

- **`vagrant up --provision`**  
  Khởi động lại máy ảo và chạy các tập lệnh provision lại.
  ```bash
  vagrant up --provision
  ```

### 9. **Sử dụng Vagrant với VirtualBox**
- **`vagrant vbguest`**  
  Cài đặt và cập nhật **VirtualBox Guest Additions** cho máy ảo của bạn (cần thiết cho một số tính năng như chia sẻ thư mục và chế độ fullscreen).
  ```bash
  vagrant vbguest
  ```

### Tóm tắt:
Những lệnh trên sẽ giúp bạn thao tác hiệu quả với Vagrant, từ việc tạo và quản lý máy ảo cho đến việc sử dụng các box, plugin và công cụ khác để tối ưu hóa công việc phát triển và thử nghiệm.