# Website thiệp mời lễ tốt nghiệp OU

## Tính năng
- Trang mở thiệp riêng trước khi vào nội dung, cảm giác gần với thiệp mời online.
- Tông xanh dương/trắng, phong cách Đại học Mở TP.HCM và ngành Công nghệ thông tin.
- Tên khách mời thay đổi theo tham số `?guest=...`.
- Khu vực thông tin sự kiện, liên kết bản đồ tùy chọn, nút xác nhận tham dự và sao chép link.
- Responsive cho điện thoại và máy tính. Ảnh trang trí được để dành cho bước thiết kế sau.

## Cập nhật thông tin
Mở `index.html`, tìm `const INVITATION = {` ở gần cuối file và nhập:
- `date`: thời gian chính thức
- `dateNote`: ghi chú
- `venue`: tên địa điểm
- `address`: địa chỉ
- `mapUrl`: link Google Maps (nếu có)
- `contactEmail`: email nhận xác nhận tham dự (nếu để trống, nút xác nhận chỉ sao chép nội dung, không tự gửi thông báo)

Không điền ngày giờ/địa điểm phỏng đoán; cập nhật khi có thông báo chính thức.

## Đưa lên GitHub Pages
1. Tạo repository mới, ví dụ `thiep-tot-nghiep-ou`, hoặc dùng repository riêng mà bạn muốn.
2. Upload `index.html` vào thư mục gốc và Commit changes.
3. Vào **Settings → Pages**.
4. Trong **Build and deployment**, chọn **Deploy from a branch**.
5. Chọn branch `main`, folder `/(root)`, bấm **Save**.
6. Đợi GitHub xuất bản website. Link thường có dạng `https://TEN-GITHUB.github.io/thiep-tot-nghiep-ou/`.

## Link tên khách mời
Sau khi thay bằng link GitHub Pages thật:
- `...?guest=Ch%C3%BA%20Thi%E1%BB%87m%20Nghi`
- `...?guest=Nguy%E1%BB%85n%20V%C4%83n%20A`

Website hiện không lưu dữ liệu khách truy cập và chưa có hệ thống RSVP trực tuyến phía máy chủ. Nếu `contactEmail` được điền, nút RSVP chỉ mở ứng dụng email của khách bằng liên kết `mailto:`; nó không tự gửi email ở nền. Nếu để trống, website chỉ sao chép nội dung xác nhận.


## Thêm ảnh và nhạc nền
- Tạo thư mục `assets` cùng cấp với `index.html`.
- Thêm ảnh của bạn vào thư mục này (ví dụ `anh-tot-nghiep.jpg`). Các ô ảnh hiện tại là vị trí mẫu; có thể thay bằng ảnh thật khi sẵn sàng.
- Thêm file nhạc MP3 mà bạn có quyền sử dụng và đặt tên chính xác là `nhac-nen.mp3` trong thư mục `assets`.
- Website thử tự phát nhạc khi vừa tải trang và thử lại khi khách bấm **Mở thư mời**. Trình duyệt có thể chặn tự phát âm thanh; khi đó khách cần bấm **Bật nhạc nền**. Cần có file `assets/nhac-nen.mp3` thì nhạc mới phát được.
- Không đưa ảnh riêng tư hoặc nhạc có bản quyền khi chưa có quyền sử dụng.
