# ĐẶC TẢ SƠ ĐỒ HOẠT ĐỘNG PHÂN LÀN (SIMPLIFIED ACTIVITY SWIMLANE)
## Tính năng: Gói học thử 7 ngày (Trial 50% 3 bài đầu & Xác thực thẻ thanh toán)
**Dự án:** Nền tảng học trực tuyến ANSERA  
**Phiên bản:** 2.0.0 (Tối giản 2 làn tương tác người dùng - hệ thống)  
**Tệp nguồn PlantUML:** [ACTIVITY_SWIMLANE.puml](./ACTIVITY_SWIMLANE.puml)  
**Tài liệu tham chiếu:** [User Story Specification.md](./User%20Story%20Specification.md) | [USER_FLOW.md](./USER_FLOW.md)

---

## 1. Nguyên tắc thiết kế sơ đồ (Design Principles)
1. **Gộp tác nhân:** Toàn bộ thành phần kỹ thuật ngầm (Frontend, Backend, Database, Cổng thanh toán, Cron Scheduler) được gom chung thành một làn duy nhất: **`Hệ thống`**.
2. **Loại bỏ chi tiết ngầm:** Không mô tả các thuật toán (Bcrypt, Luhn), truy vấn database hay xử lý token bảo mật.
3. **Tập trung vào Giao diện (UI Display):** Chỉ mô tả hành động tương tác của **Học viên** và những gì **Hệ thống hiển thị** phản hồi cho người dùng (Form nhập, Thông báo lỗi, Modal quyền lợi, Chặn tua video, Banner cảnh báo).

---

## 2. Danh mục Sơ đồ PlantUML (2 Làn: Học viên & Hệ thống)
- **Sơ đồ tổng quan E2E:** [Xem tại ACTIVITY_SWIMLANE.puml#L13](./ACTIVITY_SWIMLANE.puml)
- **US-AUTH-001 (Đăng ký tài khoản):** [Xem tại ACTIVITY_SWIMLANE.puml#L107](./ACTIVITY_SWIMLANE.puml)
- **US-CRS-002 (Xem chi tiết khóa học):** [Xem tại ACTIVITY_SWIMLANE.puml#L162](./ACTIVITY_SWIMLANE.puml)
- **US-ENR-003 (Modal cam kết học thử):** [Xem tại ACTIVITY_SWIMLANE.puml#L202](./ACTIVITY_SWIMLANE.puml)
- **US-PAY-004 (Liên kết thẻ thanh toán):** [Xem tại ACTIVITY_SWIMLANE.puml#L248](./ACTIVITY_SWIMLANE.puml)
- **US-PLAY-005 (Trình phát video 50% & Seek Guard):** [Xem tại ACTIVITY_SWIMLANE.puml#L305](./ACTIVITY_SWIMLANE.puml)
- **US-EXP-006 (Hết hạn học thử 7 ngày):** [Xem tại ACTIVITY_SWIMLANE.puml#L370](./ACTIVITY_SWIMLANE.puml)
