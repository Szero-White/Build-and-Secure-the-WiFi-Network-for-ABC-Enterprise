# 🚀 Build and Secure the WiFi Network for ABC Enterprise

---

## 🏢 Giới thiệu dự án

Dự án này tập trung vào việc **thiết kế, mô phỏng, triển khai và bảo mật một mạng WiFi hoàn chỉnh cho doanh nghiệp ABC**. Mục tiêu hướng tới xây dựng hệ thống mạng không dây ổn định, hiệu quả, đồng thời áp dụng các biện pháp bảo mật để bảo vệ dữ liệu và người dùng trong doanh nghiệp khỏi các nguy cơ tấn công.

---

## 📚 Các bước thực hiện chi tiết

### 1. 📑 Phân tích yêu cầu và thiết kế mạng

- **Khảo sát mặt bằng và phân tích nhu cầu sử dụng:**  
  Tiến hành khảo sát số lượng phòng ban/tầng/lầu, số lượng thiết bị, và phạm vi vùng phủ sóng cần thiết cho doanh nghiệp ABC.
- **Lập sơ đồ mạng tổng thể:**  
  Sử dụng sơ đồ trực quan để xác định vị trí router, switch, các điểm truy cập (AP), chia khu vực làm việc, guest, phòng Server,...
- **Tính toán số lượng thiết bị hợp lý:**  
  Đưa ra giải pháp chọn loại thiết bị router, switch, AP phù hợp với nhu cầu truy cập, đảm bảo hiệu suất và độ tin cậy.

---

### 2. ⚙️ Mô phỏng cấu hình trên Cisco Packet Tracer

- **Kết nối các thành phần vật lý:**  
  - Thiết lập các router, switch, AP, PC,... trên giao diện Packet Tracer.
  - Đấu nối dây mạng vật lý các thiết bị đầu cuối, các lớp mạng LAN, WAN.
- **Chia VLAN hợp lý:**  
  - VLAN cho từng phòng ban (VLAN nhân viên, VLAN khách, VLAN quản trị).
  - Gán cổng switch tương ứng với VLAN cần thiết.

---

### 3. 🔗 Cấu hình mạng không dây (WiFi)

- **Khởi tạo SSID cho từng đối tượng:**  
  - Tạo SSID riêng cho nhân viên (Staff), khách (Guest), và ban quản trị (Management).
- **Ẩn SSID nhạy cảm:**  
  - SSID dành cho quản trị ẩn khỏi danh sách phát sóng để tăng bảo mật.
- **Cấu hình chuẩn bảo mật WPA2/WPA3:**  
  - Áp dụng mã hóa WPA2 hoặc WPA3 với passphrase mạnh cho toàn bộ hệ thống WiFi.
  - Cấu hình Pre-Shared Key (PSK) đủ mạnh, có phân biệt Guest - Staff.
- **Thiết lập lọc địa chỉ MAC (MAC Filtering):**  
  - Chỉ cho phép thiết bị đã đăng ký truy cập WiFi theo từng vùng nhất định.
- **Giới hạn số lượng truy cập đồng thời:**  
  - Ngăn chặn sử dụng "lậu" b��ng thông trên mỗi SSID.

---

### 4. 🛡️ Triển khai các biện pháp bảo mật mạng

- **Cấu hình Firewall trên router:**  
  Lọc các luồng traffic nguy hiểm, chặn truy cập trái phép vào server nội bộ từ ngoài Internet.
- **Tạo Access Control List (ACL):**  
  - Ngăn truy cập giữa các phòng ban nhạy cảm.
  - Chỉ cho phép các nhóm VLAN nhất định truy cập phần tài nguyên phù hợp.
- **Bật Protected Management Frames (PMF):**  
  - Tăng cường bảo vệ các gói quản trị không dây khỏi hành động tấn công giả mạo.
- **Bật Isolation Mode với Guest WiFi:**  
  - Cách ly các thiết bị khách không được phép giao tiếp với nhau hoặc truy cập LAN chính.
- **Bảo vệ cổng truy cập vật lý:**  
  - Quản lý chặt chẽ vị trí đặt AP, khóa vật lý hoặc sử dụng bảo vệ phần cứng khi cần.

---

### 5. ⚡ Tối ưu hiệu suất mạng

- **Chọn kênh phát sóng hợp lý:**  
  - Tránh trùng kênh sóng giữa các AP, ngăn hiện tượng nhiễu (WiFi Channel Overlap).
- **Điều chỉnh công suất phát tín hiệu:**  
  - Phát vừa đủ vùng phủ sóng cần bảo vệ, tránh "rò rỉ" sóng ra khu vực ngoài doanh nghiệp.
- **Thử nghiệm roaming:**  
  - Di chuyển giữa các AP đảm bảo kết nối ổn định không bị rớt mạng (Wifi Seamless Roaming).

---

### 6. 🧪 Kiểm thử hệ thống và đánh giá bảo mật

- **Tấn công giả lập:**  
  - Dùng công cụ sniffing, stress test WiFi, thử brute-force passphrase.
- **Kiểm thử truy cập từ client:**  
  - Kiểm tra từng VLAN, thử đăng nhập các loại tài khoản, xem xét quyền truy cập thực tế.
- **Phân tích log và ghi nhận điểm yếu:**  
  - Review nhật ký hệ thống để phát hiện bất thường.

---

### 7. 📝 Báo cáo & trình bày

- **File .docx/.pdf:**  
  Báo cáo chi tiết từng bước, hình ảnh minh hoạ Packet Tracer, ghi chú cấu hình, kết quả kiểm thử.
- **File .pptx:**  
  Slide gọn gàng, trực quan để thuyết trình.
- **File .pkt:**  
  - Packet Tracer mô phỏng toàn bộ dự án, có thể mở kiểm tra lại, chỉnh sửa, phát triển thêm mô hình mạng.

---

## 🔗 Một số file chính

| Tên File | Chức năng |
|----------|-----------|
| [Build and Secure the WiFi Network for ABC Enterprise.docx/.pdf](./Build%20and%20Secure%20the%20WiFi%20Network%20for%20ABC%20Enterprise.pdf) | Báo cáo đầy đủ dự án |
| [Build and Secure the WiFi Network for ABC Enterprise.pptx](./Build%20and%20Secure%20the%20WiFi%20Network%20for%20ABC%20Enterprise.pptx) | Slide trình bày tóm lược, minh hoạ |
| [Build and Secure the WiFi Network for ABC Enterprise.pkt](./Build%20and%20Secure%20the%20WiFi%20Network%20for%20ABC%20Enterprise.pkt) | Mô phỏng Packet Tracer toàn bộ mạng |
| [Demo_Mesh.pkt](./Demo_Mesh.pkt) | Mô hình mở rộng mạng mesh nhiều AP |

---

## 👉 Kết quả đạt được

- ✅ Thiết kế hoàn chỉnh mạng WiFi cho doanh nghiệp, chia phân quyền rõ ràng, kiểm soát bảo mật tốt.
- ✅ Đã mô phỏng thành công các tình huống thực tế, kiểm thử các biện pháp bảo vệ mạng không dây, cải thiện hiệu suất.
- ✅ Bộ tài liệu và mô phỏng đầy đủ giúp mọi người dễ dàng học tập, áp dụng và phát triển thêm cho doanh nghiệp/quy mô lớn hơn.

---

## 📌 Tài liệu/bài học hữu ích liên quan

- Kinh nghiệm thực tế xây dựng và bảo vệ mạng doanh nghiệp từ các nguồn: Cisco, các diễn đàn an toàn thông tin, chuyên gia mạng.
- Có thể cài đặt Packet Tracer để mở và thực hành ngay trên file .pkt đã cung cấp.

---

## 🌟 Nếu repo này giúp ích cho bạn, đừng quên ⭐ Star để ủng hộ tác giả nhé!

---

**Liên hệ:**  
> Github: [Szero-White](https://github.com/Szero-White)
