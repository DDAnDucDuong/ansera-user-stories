# ĐẶC TẢ SƠ ĐỒ HOẠT ĐỘNG PHÂN LÀN (ACTIVITY SWIMLANE SPECIFICATION)
## Tính năng: Gói học thử 7 ngày (Trial 50% 3 bài đầu & Xác thực thẻ thanh toán)
**Dự án:** Nền tảng học trực tuyến ANSERA  
**Phiên bản:** 1.0.0  
**Tệp nguồn PlantUML:** [ACTIVITY_SWIMLANE.puml](./ACTIVITY_SWIMLANE.puml)  
**Tài liệu tham chiếu:** [User Story Specification.md](./User%20Story%20Specification.md) | [USER_FLOW.md](./USER_FLOW.md)  
**Quy chuẩn áp dụng:** BA-Kit Standard / `rules/17-actor-role-definition.md` / `/activity-swimlane`

---

## 1. Bảng định nghĩa các Làn trách nhiệm (Swimlane Roles)

Theo quy tắc chuẩn `rules/17-actor-role-definition.md`, sơ đồ hoạt động phân làn tách biệt rõ ràng trách nhiệm giữa các tác nhân:

| Tên Làn (Swimlane) | Phân loại Actor | Trách nhiệm chính trong hệ thống |
| :--- | :--- | :--- |
| **Học viên (Khách / Đã định danh)** | Primary Actor | Trực tiếp tương tác giao diện, nhập liệu form, chọn bài học, xem video. |
| **Frontend Web App / Player UI** | Client Presentation | Render giao diện, bắt sự kiện, validate client-side, thực thi chặn tua Seek Guard. |
| **Backend Platform Service** | Core System | Xử lý logic nghiệp vụ, quản lý token JWT, quản lý gói dùng thử, điều phối thanh toán. |
| **Cổng thanh toán quốc tế (Gateway)** | External System | Thực hiện kiểm tra thẻ sống 0đ (Zero-Auth / Pre-auth), mã hóa token chuẩn PCI-DSS, xử lý auto-charge. |
| **Cơ sở dữ liệu (Database / CDN)** | Data & Media Store | Lưu trữ người dùng, quyền enrollment, streaming video an toàn theo mốc thời gian. |
| **Hệ thống Cron Scheduler** | Automated Actor | Chạy tác vụ quét ngầm định kỳ (quét hạn dùng thử, kích hoạt gia hạn hoặc thu hồi quyền). |

---

## 2. Toàn văn mã PlantUML cho từng User Story

Tất cả các diagram đều đã được compile và lưu trữ tại file: [`ACTIVITY_SWIMLANE.puml`](./ACTIVITY_SWIMLANE.puml).
