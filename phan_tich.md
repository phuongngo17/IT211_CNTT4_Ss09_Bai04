# Phân tích sự khác biệt về mục đích cấu hình giữa môi trường Dev và Prod.

## Môi trường Dev
- Mục tiêu:
  Hỗ trợ lập trình viên debug nhanh trong quá trình phát triển.

- Đặc điểm cấu hình:
    + In log trực tiếp ra Console để dễ quan sát realtime.
    + Sử dụng mức DEBUG để hiển thị nhiều thông tin chi tiết.
    + Không cần lưu file log lâu dài.

- Lợi ích:
    + Dễ tìm lỗi khi code.
    + Tăng tốc độ phát triển và kiểm thử.

------------------------------------------------------------

## Môi trường Production (Prod)
- Mục tiêu:
  Đảm bảo hệ thống ổn định, lưu vết lỗi đầy đủ và tiết kiệm tài nguyên server.

- Đặc điểm cấu hình:
    + Ghi log ra file app.log.
    + Chỉ ghi từ mức INFO trở lên để tránh log rác.
    + Tự động rotate log khi file vượt 10MB.
    + Nén và lưu tối đa 30 ngày để tránh đầy ổ cứng.

- Lợi ích:
    + Hỗ trợ truy vết lỗi Production.
    + Giảm nguy cơ đầy disk server.
    + Dễ tích hợp hệ thống monitoring/log aggregation.