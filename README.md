# 🌸 Hệ thống phân loại hoa bằng Edge AI (Đa nền tảng)

**Sinh viên thực hiện: Trần Quốc Đạt
**Mã sinh viên:** N23DCCI013
**Học phần:** Mạng cảm biến

Dự án này ứng dụng công nghệ Trí tuệ nhân tạo tại biên (Edge AI) với cấu trúc mạng MobileNetV2 (int8) để phân loại 4 nhãn hoa: Hồng, Hướng dương, Lan và Sen. 

Mô hình đã được lượng tử hóa và biên dịch sang định dạng **WebAssembly (.wasm)**, cho phép hệ thống chạy độc lập, tự suy luận trực tiếp ngay trên trình duyệt của Máy tính và Điện thoại di động mà không cần cài đặt môi trường C++ phức tạp.

---

## 💻 1. Hướng dẫn chạy thử nghiệm trên Máy tính (PC/Laptop)
Để mở giao diện camera nhận diện trên máy tính, vui lòng thực hiện theo các bước sau:

**Cách sử dụng Visual Studio Code (Khuyên dùng):**
1. Tải toàn bộ mã nguồn của kho lưu trữ này về máy tính và giải nén.
2. Mở phần mềm Visual Studio Code, kéo thả thư mục `browser` vào phần mềm.
3. Cài đặt tiện ích mở rộng **Live Server** (nếu chưa có).
4. Click chuột phải vào tệp `index.html` bên trong thư mục `browser` -> Chọn **Open with Live Server**.
5. Trình duyệt web sẽ tự động mở ra. Vui lòng cấp quyền truy cập Camera và đưa hình ảnh các loại hoa vào ống kính để kiểm tra độ chính xác.

*(Ghi chú: Nếu sử dụng Terminal/Command Prompt, có thể di chuyển vào thư mục `browser`, gõ lệnh `python -m http.server 8000` và truy cập địa chỉ `http://localhost:8000` trên trình duyệt).*

---

## 📱 2. Hướng dẫn chạy thử nghiệm trên Điện thoại di động (Smartphone)
Để đánh giá tốc độ nhận diện và độ trễ (latency) của thuật toán trong môi trường thực tế, hệ thống hỗ trợ quét trực tiếp thông qua camera của điện thoại di động (Safari/Chrome):

1. Đảm bảo điện thoại thông minh có kết nối Internet.
2. Mở ứng dụng Máy ảnh, quét **Mã QR kiểm thử** được đính kèm trong quyển Báo cáo (Hình 3.6) hoặc quét trực tiếp mã QR trên giao diện Deployment của Edge Impulse Studio với link:https://studio.edgeimpulse.com/studio/1021295 .
3. Bấm vào liên kết hiện ra. Trình duyệt trên điện thoại sẽ tự động tải "bộ não" AI thu nhỏ này về bộ nhớ đệm.
4. Nhấn cấp quyền sử dụng Camera. Lúc này, có thể cầm điện thoại soi trực tiếp vào các bông hoa thực tế để xem kết quả phân loại hiển thị theo thời gian thực (Real-time).