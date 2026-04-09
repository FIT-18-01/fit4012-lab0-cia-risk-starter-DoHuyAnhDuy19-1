# Lab 01 Answers
## CIA & Risk: Hệ thống lưu điểm

**Họ và tên:** Đỗ Huy Anh Duy

**MSSV:** 1871020190

**Lớp/Nhóm:** CNTT18-01

---

## 1. Assets
Liệt kê ít nhất 2 assets cần bảo vệ.

- Asset 1:Cơ sở dữ liệu người dùng (Thông tin cá nhân, mật khẩu đã mã hóa).
- Asset 2:Mã nguồn ứng dụng (Business Logic, API Keys).
- Asset 3 (nếu có):Hạ tầng máy chủ và lưu trữ (Server/Cloud Hosting).

---

## 2. Mapping CIA
Ghép từng sự cố với CIA.

- Sự cố A -> Confidentiality
- Sự cố B -> Integrity
- Sự cố C -> Availability 

---

## 3. Phân tích sự cố B
- Threat: Hacker hoặc người dùng có ý đồ xấu thực hiện chèn các đoạn mã SQL độc hại qua form đăng nhập/tìm kiếm.
- Vulnerability: Hệ thống thiếu bước kiểm tra (validation) và lọc dữ liệu đầu vào; không sử dụng Parameterized Queries.
- Mitigation: Sử dụng Prepared Statements hoặc Entity Framework (với LINQ) để truy vấn; thực hiện phân quyền chặt chẽ trên database (Least Privilege).

---

## 4. Reflection
Qua bài tập này, em nhận thấy rằng việc bảo mật không chỉ đơn thuần là cài đặt phần mềm chống virus mà là một quy trình toàn diện. Việc hiểu rõ mô hình CIA giúp em xác định được ưu tiên bảo vệ cho từng loại tài sản khác nhau. Trong quá trình phát triển các ứng dụng bằng C# hay Python, việc chú trọng vào khâu kiểm soát dữ liệu đầu vào là cực kỳ quan trọng để ngăn chặn các lỗ hổng như SQL Injection. Điều này giúp em có tư duy cẩn trọng hơn khi thiết kế kiến trúc hệ thống và xây dựng cơ sở dữ liệu sau này.


---

## 5. Bonus Flag
`FIT4012{A-?-B-?-C-?}`

Flag của em: FIT4012{A-Confidentiality-B-Integrity-C-Availability}

