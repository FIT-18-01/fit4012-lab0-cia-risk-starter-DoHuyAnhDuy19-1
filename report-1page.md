# FIT4012 - Report 1 Page
## Lab 01 - CIA & Risk: Hệ thống lưu điểm

### 1. Mục tiêu bài lab
- Nhận diện tài sản cần bảo vệ trong một hệ thống thông tin đơn giản.
- Phân biệt Confidentiality, Integrity, Availability.
- Xác định threat, vulnerability, mitigation.
- Thực hành workflow GitHub cơ bản để nhận và nộp bài.

### 2. Cách làm
- Đọc bối cảnh và xác định các thành phần quan trọng của hệ thống.
- Phân tích từng sự cố theo bộ ba CIA.
- Chọn sự cố B để phân tích sâu hơn theo threat - vulnerability - mitigation.
- Hoàn thiện bài làm trong repo và commit/push lên GitHub.

### 3. Kết quả chính
**Assets:**
- Cơ sở dữ liệu điểm số: Đây là tài sản quan trọng nhất, chứa kết quả học tập của toàn bộ sinh viên.
- Thông tin định danh người dùng: Bao gồm tài khoản/mật khẩu của giảng viên và quản trị viên hệ thống để ngăn chặn việc truy cập trái phép.

**CIA mapping:**
- Sự cố A -> Confidentiality
- Sự cố B -> Integrity
- Sự cố C -> Availability

**Phân tích sự cố B:**
- Threat: Kẻ tấn công (hacker) hoặc sinh viên có kiến thức kỹ thuật thực hiện tấn công SQL Injection hoặc đánh cắp session của giảng viên.
- Vulnerability: Hệ thống không kiểm tra tính hợp lệ của dữ liệu đầu vào (Input Validation) hoặc không có cơ chế ghi log (Audit Log) để theo dõi các thay đổi dữ liệu.
- Mitigation: Sử dụng Parameterized Queries (truy vấn có tham số), triển khai cơ chế xác thực đa yếu tố (MFA) cho giảng viên và thiết lập hệ thống ghi lại lịch sử thay đổi điểm

### 4. Kết luận ngắn
Qua bài lab này, em đã hiểu rõ hơn cách áp dụng mô hình CIA để đánh giá mức độ nghiêm trọng của một sự cố an ninh. Phần khó nhất là phân biệt giữa Threat và Vulnerability, vì đôi khi chúng ta dễ nhầm lẫn giữa tác nhân bên ngoài và điểm yếu nội tại của hệ thống. Điều quan trọng nhất khi phân tích một sự cố là phải nhìn nhận đa chiều: không chỉ tập trung vào việc ngăn chặn kẻ tấn công mà còn phải chú trọng vào việc xây dựng các rào cản kỹ thuật để giảm thiểu lỗ hổng hệ thống.