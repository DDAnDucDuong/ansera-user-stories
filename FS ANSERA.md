# ĐẶC TẢ USER STORIES & ACCEPTANCE CRITERIA (ANSERA PLATFORM)
**Tác giả:** Duong Duc An  
**Phiên bản:** 2.1 (Cập nhật mô hình Học thử 7 ngày liên kết thẻ quốc tế, giới hạn 50% thời lượng 3 bài đầu & Thu hồi toàn bộ khi hết hạn)

---

## 1. Phụ lục Thông báo (Message Catalog)

| Mã MSG | Loại | Nội dung thông báo | Điều kiện xuất hiện |
| :--- | :---: | :--- | :--- |
| **MSG-001** | Lỗi | Vui lòng nhập thông tin | Khi người dùng bỏ trống các trường thông tin bắt buộc và bấm gửi |
| **MSG-002** | Cảnh báo | Tên người dùng đã tồn tại | Khi người dùng điền một username đã tồn tại trong hệ thống để đăng ký |
| **MSG-003** | Lỗi | Thông tin chưa hợp lệ | - Khi mật khẩu xác nhận không khớp hoặc dưới 8 ký tự<br>- Khi thông tin thẻ/email sai định dạng (thuật toán Luhn, CVV, ngày hết hạn trong quá khứ) |
| **MSG-004** | Thông báo | Bạn đã đăng ký khóa học này rồi | Khi học viên click "Đăng ký ngay" đối với khóa học đã đăng ký/sở hữu trước đó |
| **MSG-005** | Thông báo | Bạn đã hoàn thành thời lượng học thử của bài học này. Vui lòng mở khóa để xem tiếp toàn bộ nội dung. | Khi video bài học phát chạm mốc 50% thời lượng trong chế độ học thử |
| **MSG-006** | Cảnh báo | Thời gian học thử 7 ngày của bạn cho khóa học này đã kết thúc. Vui lòng thanh toán để tiếp tục học tập. | Khi học viên truy cập vào khóa học sau khi thời hạn học thử 7 ngày đã kết thúc hoặc bị hủy |

---

## 2. Danh mục User Stories tổng quan

| Mã Story | Nội dung User Story (As a / I want / So that) | Độ ưu tiên |
| :--- | :--- | :---: |
| **US-AUTH-001** | **As a** khách truy cập mới<br>**I want to** đăng ký tài khoản bằng username và mật khẩu<br>**So that** tôi sở hữu tài khoản định danh để học tập và lưu tiến trình cá nhân | Must Have (P0) |
| **US-CRS-002** | **As a** học viên đã đăng nhập<br>**I want to** xem chi tiết giáo trình, thông tin giảng viên và nhận diện các bài được học thử 50%<br>**So that** tôi hiểu rõ giá trị khóa học trước khi quyết định đăng ký trải nghiệm | Must Have (P0) |
| **US-ENR-003** | **As a** học viên chưa từng học thử khóa học<br>**I want to** xem thông tin quyền lợi học thử 7 ngày và chuyển sang bước liên kết thẻ<br>**So that** tôi chuẩn bị kích hoạt gói trải nghiệm bài giảng thực tế | High (P1) |
| **US-PAY-004** | **As a** học viên đăng ký trải nghiệm 7 ngày<br>**I want to** nhập thông tin thẻ thanh toán quốc tế (Visa/Mastercard) hợp lệ<br>**So that** hệ thống xác thực thẻ, kích hoạt gói học thử 7 ngày và thiết lập tự động gia hạn sau dùng thử | Must Have (P0) |
| **US-PLAY-005** | **As a** học viên đang trong thời gian học thử 7 ngày<br>**I want to** xem tối đa 50% thời lượng của 3 bài đầu tiên và nhận thông báo mở khóa khi chạm giới hạn<br>**So that** tôi đánh giá chất lượng bài giảng và cân nhắc nâng cấp toàn bộ khóa học | Must Have (P0) |
| **US-EXP-006** | **As a** Quản trị viên vận hành nền tảng ANSERA<br>**I want to** hệ thống tự động thu hồi toàn bộ quyền xem (kể cả 50% 3 bài đầu) khi học viên hết hạn 7 ngày mà không gia hạn thành công<br>**So that** bảo vệ bản quyền khóa học và ngăn chặn hành vi học thử lặp lại | High (P1) |

---

## 3. Chi tiết đặc tả User Stories & Acceptance Criteria

### 3.1. US-AUTH-001: Đăng ký tài khoản học viên mới bằng Username & Password

**As a** khách truy cập mới chưa có tài khoản trên ANSERA  
**I want to** đăng ký tài khoản bằng username và mật khẩu cá nhân  
**So that** tôi sở hữu tài khoản định danh trên nền tảng, lưu trữ lộ trình học và sử dụng các tính năng học tập cá nhân hóa.

![US-AUTH-001_ Homepage khi truy cập vào trang trước khi đăng ký](./H%E1%BB%8Dc%20th%E1%BB%AD%20screen./US-AUTH-001_%20Homepage%20khi%20truy%20c%E1%BA%ADp%20v%C3%A0o%20trang%20tr%C6%B0%E1%BB%9Bc%20khi%20%C4%91%C4%83ng%20k%C3%AD.png)

*US-AUTH-001_ Homepage khi truy cập vào trang trước khi đăng ký*

![US-AUTH-001_ Đăng ký tài khoản học viên mới](./H%E1%BB%8Dc%20th%E1%BB%AD%20screen./US-AUTH-001_%20%C4%90%C4%83ng%20k%C3%BD%20t%C3%A0i%20kho%E1%BA%A3n%20h%E1%BB%8Dc%20vi%C3%AAn%20m%E1%BB%9Bi.png)

*US-AUTH-001_ Đăng ký tài khoản học viên mới*

![US-AUTH-001_ Đăng ký (Lỗi validation MSG-001, MSG-002, MSG-003)](./H%E1%BB%8Dc%20th%E1%BB%AD%20screen./US-AUTH-001_%20%C4%90%C4%83ng%20k%C3%BD%20(L%E1%BB%97i%20validation%20MSG-001,%20MSG-002,%20MSG-003).png)

*US-AUTH-001_ Đăng ký (Lỗi validation MSG-001, MSG-002, MSG-003)*

#### Bảng mô tả thành phần giao diện

| STT | Tên thành phần | Type | Được chỉnh sửa | Bắt buộc | Giá trị mặc định | Mô tả |
| :---: | --- | :---: | :---: | :---: | :---: | --- |
| 1 | Button tham gia miễn phí | Button | N/A | N/A | N/A | Nút kêu gọi hành động trên header/banner trang chủ. |
| 2 | Button tham gia miễn phí | Button | N/A | N/A | N/A | Nút kêu gọi hành động ở phần thân trang chủ. |
| 3 | Trường thông tin username | Text | Yes | Yes | N/A | - Bắt buộc nhập.<br>- Bỏ trống và bấm gửi: hiển thị **MSG-001** và đổi viền khung đỏ. |
| 4 | Trường thông tin password | Text | Yes | Yes | N/A | - Mật khẩu bắt buộc nhập, ẩn ký tự dạng `*`.<br>- Tối thiểu 8 ký tự.<br>- Nhấn giữ biểu tượng con mắt để xem mật khẩu.<br>- Bỏ trống: hiển thị **MSG-001**.<br>- Trùng username: hiển thị **MSG-002**. |
| 5 | Trường nhập lại mật khẩu | Text | Yes | Yes | N/A | - Phải trùng khớp 100% với mật khẩu đã nhập.<br>- Bỏ trống: hiển thị **MSG-001**.<br>- Không trùng khớp: hiển thị **MSG-003** và viền đỏ. |
| 6 | Button đăng ký | Button | N/A | N/A | N/A | Gửi thông tin đăng ký tài khoản. Đăng ký thành công điều hướng về trang chủ với trạng thái đăng nhập. |
| 7 | Button đăng ký Google | Button | N/A | N/A | N/A | Chuyển hướng tới đăng ký bằng tài khoản Google. |
| 8 | Button đăng ký Facebook | Button | N/A | N/A | N/A | Chuyển hướng tới đăng ký bằng tài khoản Facebook. |
| 9 | Link đăng nhập | Link | N/A | N/A | N/A | Điều hướng sang trang Đăng nhập nếu đã có tài khoản. |

#### Acceptance Criteria

- **AC1: Đăng ký thành công với thông tin hợp lệ (Happy path)**
  - **Given** người dùng đang ở trang đăng ký tài khoản ANSERA và chưa đăng nhập
  - **When** người dùng nhập `username` chưa tồn tại trong hệ thống, `password` hợp lệ (tối thiểu 8 ký tự), `confirm password` trùng khớp 100%, và nhấn nút "Đăng ký"
  - **Then** hệ thống tạo tài khoản mới ở trạng thái kích hoạt thành công
  - **And** tự động đăng nhập và điều hướng người dùng về trang chủ với trạng thái đã xác thực.
- **AC2: Bỏ trống một hoặc nhiều trường bắt buộc (Validation)**
  - **Given** người dùng đang ở form đăng ký
  - **When** người dùng bỏ trống ít nhất một trong ba trường (`username`, `password`, `confirm password`) và nhấn nút "Đăng ký"
  - **Then** hệ thống chặn gửi dữ liệu và hiển thị thông báo lỗi `MSG-001`: *"Vui lòng nhập thông tin"* tại các trường bị bỏ trống.
- **AC3: Trùng Username đã tồn tại (Negative path / Duplicate)**
  - **Given** tài khoản với username `duc_an2026` đã tồn tại trong hệ thống
  - **When** người dùng mới nhập `username` là `duc_an2026`, điền mật khẩu hợp lệ và nhấn "Đăng ký"
  - **Then** hệ thống không tạo tài khoản mới và hiển thị cảnh báo `MSG-002`: *"Tên người dùng đã tồn tại"*.
- **AC4: Mật khẩu xác nhận không khớp hoặc dưới 8 ký tự (Negative path)**
  - **Given** người dùng đang ở form đăng ký
  - **When** người dùng nhập mật khẩu dưới 8 ký tự HOẶC nhập mật khẩu xác nhận không trùng khớp
  - **Then** hệ thống chặn đăng ký, viền khung đổi màu đỏ và hiển thị lỗi `MSG-003`: *"Thông tin chưa hợp lệ"*.

---

### 3.2. US-CRS-002: Xem chi tiết thông tin khóa học & Nhận diện bài học thử

**As a** học viên đã đăng nhập vào ANSERA  
**I want to** xem chi tiết đề cương khóa học, thông tin giảng viên, đánh giá và nhận biết rõ bài nào được học thử 50%  
**So that** tôi hiểu rõ nội dung, kiến thức đạt được trước khi quyết định trải nghiệm học thử hoặc mua khóa học.

![US-CRS-002_ Chi tiết khóa học (Huy hiệu Học thử 50% & CTA Trải nghiệm 7 ngày)](./H%E1%BB%8Dc%20th%E1%BB%AD%20screen./US-CRS-002_%20Chi%20ti%E1%BA%BFt%20kh%C3%B3a%20h%E1%BB%8Dc%20(Huy%20hi%E1%BB%87u%20H%E1%BB%8Dc%20th%E1%BB%AD%2050%25%20&%20CTA%20Tr%E1%BA%A3i%20nghi%E1%BB%87m%207%20ng%C3%A0y).png)

*US-CRS-002_ Chi tiết khóa học (Huy hiệu Học thử 50% & CTA Trải nghiệm 7 ngày)*

#### Bảng mô tả thành phần giao diện

| STT | Tên thành phần | Type | Được chỉnh sửa | Bắt buộc | Giá trị mặc định | Mô tả |
| :---: | --- | :---: | :---: | :---: | :---: | --- |
| 1 | Card thông tin khóa học | Card | N/A | N/A | N/A | Tên khóa, đơn vị phát hành, xếp hạng rating, số lượng học viên, cấp độ. |
| 2 | Video trailer giới thiệu | Media | N/A | N/A | N/A | Video ngắn giới thiệu tổng quan nội dung và mục tiêu khóa học. |
| 3 | Button Trải nghiệm 7 ngày | Button | N/A | N/A | N/A | Nút CTA chính: Bật popup modal tóm tắt quyền lợi dùng thử 7 ngày (xem 50% 3 bài đầu) và chuyển sang bước liên kết thẻ (US-ENR-003 & US-PAY-004). |
| 4 | Button Mua ngay | Button | N/A | N/A | N/A | Nút CTA phụ: Dẫn thẳng tới trang thanh toán mua đứt khóa học trọn đời. |
| 5 | Huy hiệu [Học thử 50%] | Badge | N/A | N/A | N/A | Gắn cạnh Bài 1, Bài 2, Bài 3 trong danh mục bài học để người dùng nhận diện. |
| 6 | Biểu tượng Khóa 🔒 | Icon | N/A | N/A | N/A | Gắn cạnh Bài 4, Bài 5 và toàn bộ bài tập/quizz (chỉ mở khi thanh toán trả phí). |
| 7 | Accordion bài học | Accordion | N/A | N/A | N/A | Click vào mũi tên để xem mô tả tóm tắt nội dung bài học. |

#### Acceptance Criteria

- **AC1: Hiển thị đầy đủ thông tin khóa học và phân loại bài học (Happy path)**
  - **Given** học viên đã đăng nhập và xem trang chi tiết khóa học
  - **When** trang tải hoàn tất
  - **Then** hệ thống hiển thị đầy đủ thông tin khóa học, thông tin giảng viên, đánh giá
  - **And** hiển thị huy hiệu `[Học thử 50%]` tại Bài 1, 2, 3 và biểu tượng 🔒 tại các bài từ số 4 trở đi kèm nút CTA *"Trải nghiệm 7 ngày"*.
- **AC2: Mở rộng tóm tắt bài học qua Accordion (Interaction)**
  - **Given** học viên đang ở mục danh mục bài học
  - **When** học viên click vào biểu tượng mũi tên xổ xuống tại một bài học
  - **Then** hệ thống bung mở bản tóm tắt nội dung bài học mà không tải lại trang.
- **AC3: Đã sở hữu khóa học bấm Đăng ký ngay (Negative path)**
  - **Given** học viên đã thanh toán mua khóa học này trước đó
  - **When** học viên vào trang chi tiết khóa học và click nút mua
  - **Then** hệ thống không mở luồng thanh toán và hiển thị thông báo `MSG-004`: *"Bạn đã đăng ký khóa học này rồi"*.

---

### 3.3. US-ENR-003: Đăng ký trải nghiệm học thử miễn phí trong 7 ngày

**As a** học viên đã đăng nhập và chưa từng tham gia khóa học đang chọn  
**I want to** mở xem thông tin chi tiết gói học thử 7 ngày và chuyển sang màn hình liên kết thẻ thanh toán  
**So that** tôi hiểu rõ phạm vi học thử (50% của 3 bài đầu) và chính sách gia hạn trước khi cung cấp thông tin thẻ.

![US-ENR-003_ Modal cam kết trải nghiệm học thử 7 ngày](./H%E1%BB%8Dc%20th%E1%BB%AD%20screen./US-ENR-003_%20Modal%20cam%20k%E1%BA%BFt%20tr%E1%BA%A3i%20nghi%E1%BB%87m%20h%E1%BB%8Dc%20th%E1%BB%AD%207%20ng%C3%A0y.png)

*US-ENR-003_ Modal cam kết trải nghiệm học thử 7 ngày*

#### Bảng mô tả thành phần giao diện

| STT | Tên thành phần | Type | Được chỉnh sửa | Bắt buộc | Giá trị mặc định | Mô tả |
| :---: | --- | :---: | :---: | :---: | :---: | --- |
| 1 | Button Trải nghiệm 7 ngày | Button | N/A | N/A | N/A | Click để mở popup modal tóm tắt quyền lợi và chính sách học thử. |
| 2 | Modal cam kết học thử | Modal | N/A | N/A | N/A | Hộp thoại thông báo: Quyền lợi xem 50% thời lượng của 3 bài đầu trong 7 ngày, miễn phí 0đ trong 7 ngày đầu, tự động gia hạn sau 7 ngày nếu không hủy. |
| 3 | Button Bắt đầu dùng thử miễn phí | Button | N/A | N/A | N/A | Nằm trong popup modal. Click để xác nhận và chuyển hướng sang màn hình nhập thông tin thẻ (US-PAY-004). |

#### Acceptance Criteria

- **AC1: Hiển thị modal đặc quyền học thử và điều hướng sang trang liên kết thẻ (Happy path)**
  - **Given** học viên đang xem chi tiết khóa học chưa từng học thử hoặc đăng ký
  - **When** học viên nhấn nút "Trải nghiệm 7 ngày"
  - **Then** hệ thống hiển thị modal thông báo đặc quyền học thử: thời hạn 7 ngày, quyền xem 50% thời lượng của 3 bài đầu, cam kết 0đ trong 7 ngày và chính sách tự động gia hạn
  - **And** khi học viên click nút "Bắt đầu dùng thử miễn phí", hệ thống chuyển hướng đến màn hình điền thông tin thẻ thanh toán (US-PAY-004).
- **AC2: Đã từng sử dụng gói học thử cho khóa học này (Negative path)**
  - **Given** học viên đã từng kích hoạt gói học thử 7 ngày cho khóa học này trước đây (đang hoạt động hoặc đã hết hạn)
  - **When** học viên truy cập trang chi tiết khóa học
  - **Then** nút "Trải nghiệm 7 ngày" bị vô hiệu hóa (disabled) kèm ghi chú giải thích quyền học thử chỉ áp dụng 1 lần duy nhất cho mỗi khóa học, chỉ hiển thị nút "Mua ngay".

---

### 3.4. US-PAY-004: Liên kết thẻ thanh toán quốc tế và thiết lập tự động gia hạn sau dùng thử

**As a** học viên đăng ký trải nghiệm học thử 7 ngày  
**I want to** nhập thông tin thẻ thanh toán quốc tế (Visa/Mastercard) hợp lệ  
**So that** tôi hoàn tất xác thực 0đ, kích hoạt quyền học thử 7 ngày và hệ thống tự động gia hạn thuê bao sau 7 ngày nếu tôi không hủy bỏ.

![US-PAY-004_ Liên kết thẻ thanh toán quốc tế & Kích hoạt học thử 7 ngày](./H%E1%BB%8Dc%20th%E1%BB%AD%20screen./US-PAY-004_%20Li%C3%AAn%20k%E1%BA%BFt%20th%E1%BA%BB%20thanh%20to%C3%A1n%20qu%E1%BB%91c%20t%E1%BA%BF%20&%20K%C3%ADch%20ho%E1%BA%A1t%20h%E1%BB%8Dc%20th%E1%BB%AD%207%20ng%C3%A0y.png)

*US-PAY-004_ Liên kết thẻ thanh toán quốc tế & Kích hoạt học thử 7 ngày*

![US-PAY-004_ Điền thẻ thanh toán (Lỗi validation AC2 MSG-001 & AC3 MSG-003)](./H%E1%BB%8Dc%20th%E1%BB%AD%20screen./US-PAY-004_%20%C4%90i%E1%BB%81n%20th%E1%BA%BB%20thanh%20to%C3%A1n%20(L%E1%BB%97i%20validation%20AC2%20MSG-001%20&%20AC3%20MSG-003).png)

*US-PAY-004_ Điền thẻ thanh toán (Lỗi validation AC2 MSG-001 & AC3 MSG-003)*

![US-PAY-004_ Điền thẻ thanh toán (Lỗi thẻ bị từ chối AC4 Gateway Decline)](./H%E1%BB%8Dc%20th%E1%BB%AD%20screen./US-PAY-004_%20%C4%90i%E1%BB%81n%20th%E1%BA%BB%20thanh%20to%C3%A1n%20(L%E1%BB%97i%20th%E1%BA%BB%20b%E1%BB%8B%20t%E1%BB%AB%20ch%E1%BB%91i%20AC4%20Gateway%20Decline).png)

*US-PAY-004_ Điền thẻ thanh toán (Lỗi thẻ bị từ chối AC4 Gateway Decline)*

#### Bảng mô tả thành phần giao diện

| STT | Tên thành phần | Type | Được chỉnh sửa | Bắt buộc | Giá trị mặc định | Mô tả |
| :---: | --- | :---: | :---: | :---: | :---: | --- |
| 1 | Trường Họ và tên trên thẻ | Text | Yes | Yes | N/A | - Nhập họ tên in trên thẻ (không chứa số hoặc ký tự đặc biệt).<br>- Bỏ trống: hiển thị **MSG-001**.<br>- Chứa số/ký tự sai: hiển thị **MSG-003**. |
| 2 | Trường Email | Text | Yes | Yes | N/A | - Địa chỉ email nhận thông báo gia hạn và biên lai.<br>- Bỏ trống: hiển thị **MSG-001**.<br>- Sai cú pháp: hiển thị **MSG-003**. |
| 3 | Droplist Quốc gia | List | Yes | Yes | N/A | Danh sách quốc gia cư trú / phát hành thẻ. |
| 4 | Trường Số thẻ | Text | Yes | Yes | N/A | - Nhập dãy số thẻ Visa/Mastercard.<br>- Bỏ trống: hiển thị **MSG-001**.<br>- Sai cấu trúc hoặc sai thuật toán Luhn: hiển thị **MSG-003**. |
| 5 | Trường Ngày hết hạn | Text | Yes | Yes | N/A | - Định dạng chuẩn placeholder `MM/YY` (thời điểm trong tương lai).<br>- Bỏ trống: hiển thị **MSG-001**.<br>- Sai định dạng hoặc ngày trong quá khứ: hiển thị **MSG-003**. |
| 6 | Trường Mã bảo vệ (CVV) | Text | Yes | Yes | N/A | - 3 chữ số bảo mật ở mặt sau thẻ.<br>- Bỏ trống: hiển thị **MSG-001**.<br>- Không đúng 3 số: hiển thị **MSG-003**. |
| 7 | Button Kích hoạt học thử 7 ngày | Button | N/A | N/A | N/A | Gửi dữ liệu xác thực thẻ qua cổng thanh toán, thiết lập subscription tự động gia hạn sau 7 ngày và kích hoạt khóa học sang trạng thái `TRIAL_ACTIVE`. |

#### Acceptance Criteria

- **AC1: Xác thực thẻ thành công và tạo subscription tự động gia hạn (Happy path)**
  - **Given** học viên đang ở màn hình điền thông tin thẻ của gói học thử
  - **When** học viên nhập đầy đủ: Họ tên trên thẻ, Email hợp lệ, Quốc gia, Số thẻ Visa/Mastercard hợp lệ, Ngày hết hạn hợp lệ (MM/YY trong tương lai), CVV hợp lệ (3 số), và nhấn "Kích hoạt học thử 7 ngày"
  - **Then** cổng thanh toán xác thực thẻ thành công (thực hiện pre-authorization 0đ), mã hóa an toàn (tokenization) thông tin thẻ và hệ thống khởi tạo lịch trình tự động gia hạn trừ tiền sau 168 giờ (7 ngày)
  - **And** trạng thái khóa học của học viên chuyển sang `TRIAL_ACTIVE`, kích hoạt đồng hồ đếm ngược 7 ngày, gửi email xác nhận và điều hướng học viên vào Bài học số 1 (US-PLAY-005).
- **AC2: Bỏ trống một hoặc nhiều trường thông tin thanh toán (Validation)**
  - **Given** học viên đang ở màn hình thanh toán
  - **When** học viên để trống bất kỳ trường nào trong các trường bắt buộc và nhấn gửi
  - **Then** hệ thống chặn gửi dữ liệu và hiển thị thông báo lỗi `MSG-001`: *"Vui lòng nhập thông tin"* tại các trường bị bỏ trống.
- **AC3: Nhập sai định dạng dữ liệu hoặc thông tin thẻ không hợp lệ (Negative path)**
  - **Given** học viên đang ở màn hình thanh toán
  - **When** học viên nhập email sai cú pháp, họ tên chứa số/ký tự đặc biệt, số thẻ sai thuật toán Luhn hoặc ngày hết hạn trong quá khứ và bấm gửi
  - **Then** hệ thống chặn gửi dữ liệu và hiển thị thông báo lỗi `MSG-003`: *"Thông tin chưa hợp lệ"*.
- **AC4: Thẻ bị từ chối từ ngân hàng phát hành (Negative path / Gateway Decline)**
  - **Given** thông tin thẻ đúng định dạng nhưng thẻ bị khóa, không hỗ trợ giao dịch online hoặc không đủ điều kiện xác thực từ ngân hàng
  - **When** học viên gửi yêu cầu xác thực
  - **Then** cổng thanh toán trả về lỗi, hệ thống không tạo subscription và hiển thị thông báo hướng dẫn học viên kiểm tra lại tình trạng thẻ hoặc sử dụng thẻ khác.

---

### 3.5. US-PLAY-005: Trải nghiệm học thử 50% thời lượng 3 bài đầu & Chặn tua (Seek Guard)

**As a** học viên đang trong thời gian học thử 7 ngày  
**I want to** xem được 50% thời lượng của 3 bài đầu tiên và hiển thị Paywall khi chạm giới hạn  
**So that** tôi cảm nhận được chất lượng giảng dạy và quyết định duy trì gói trả phí hoặc mua khóa học.

![US-PLAY-005_ Trình phát video học thử 50% & Chặn tua (Seek Guard)](./H%E1%BB%8Dc%20th%E1%BB%AD%20screen./US-PLAY-005_%20Tr%C3%ACnh%20ph%C3%A1t%20video%20h%E1%BB%8Dc%20th%E1%BB%AD%2050%25%20&%20Ch%E1%BA%B7n%20tua%20(Seek%20Guard).png)

*US-PLAY-005_ Trình phát video học thử 50% & Chặn tua (Seek Guard)*

![US-PLAY-005_ Lớp phủ Paywall Modal khi chạm mốc 50% (MSG-005)](./H%E1%BB%8Dc%20th%E1%BB%AD%20screen./US-PLAY-005_%20L%E1%BB%9Bp%20ph%E1%BB%A7%20Paywall%20Modal%20khi%20ch%E1%BA%A1m%20m%E1%BB%91c%2050%25%20(MSG-005).png)

*US-PLAY-005_ Lớp phủ Paywall Modal khi chạm mốc 50% (MSG-005)*

#### Bảng mô tả thành phần giao diện

| STT | Tên thành phần | Type | Được chỉnh sửa | Bắt buộc | Giá trị mặc định | Mô tả |
| :---: | --- | :---: | :---: | :---: | :---: | --- |
| 1 | Khung trình phát video | Video | N/A | N/A | N/A | Phát video bài giảng với các nút điều khiển chuẩn. |
| 2 | Thanh tiến trình tua (Seek-bar) | Slider | Yes | N/A | 00:00 | Phân tách trực quan: 50% đầu có màu xanh (cho phép phát), 50% sau bị mờ xám sọc chéo kèm vạch phân chia ranh giới học thử. |
| 3 | Banner đếm ngược thời gian | Banner | N/A | N/A | N/A | Dải thông báo trên đầu trình phát hiển thị thời gian học thử còn lại (ví dụ: Còn 5 ngày 14 giờ) kèm lời nhắc ngày tự động gia hạn. |
| 4 | Paywall Modal Overlay | Modal | N/A | N/A | N/A | Lớp phủ bật lên khi video đạt 50% hoặc khi click bài bị khóa, hiển thị ưu đãi và các tính năng mở khóa toàn bộ. |
| 5 | Button Mở khóa toàn bộ khóa học | Button | N/A | N/A | N/A | Nút CTA chính trên Paywall Modal dẫn tới xác nhận mở khóa ngay lập tức. |
| 6 | Button Xem lại đoạn học thử | Button | N/A | N/A | N/A | Nút phụ trên Paywall Modal cho phép tua lại video về mốc 00:00 để học lại phần 50% miễn phí. |

#### Acceptance Criteria

- **AC1: Tự động dừng tại mốc 50% thời lượng và hiển thị Paywall (Happy path)**
  - **Given** học viên có trạng thái khóa học là `TRIAL_ACTIVE` đang xem Bài 1, 2 hoặc 3
  - **When** video phát đến mốc chính xác $50\%$ tổng thời lượng bài giảng (ví dụ mốc 05:00 đối với bài dài 10:00)
  - **Then** video tự động tạm dừng (pause), hệ thống hiển thị thông báo `MSG-005` và bật **Paywall Modal Overlay** mời học viên mở khóa trọn bộ khóa học.
- **AC2: Kiểm soát hành vi kéo tua vượt mốc 50% - Seek Guard (Edge case)**
  - **Given** học viên đang xem bài học thử
  - **When** học viên cố tình kéo thanh tua (seek-bar) vượt quá mốc $50\%$ thời lượng
  - **Then** trình phát tự động kéo ngược thời gian phát về đúng mốc $50\%$, chặn tải luồng dữ liệu video sau mốc $50\%$ và hiển thị Paywall Modal.
- **AC3: Click vào bài từ số 4 trở đi hoặc bài tập (Restricted)**
  - **Given** học viên đang ở trạng thái `TRIAL_ACTIVE`
  - **When** học viên click vào Bài 4, Bài 5 hoặc bài tập ôn tập trong danh sách bài học
  - **Then** hệ thống không mở trình phát và lập tức hiển thị Paywall Modal thông báo nội dung này chỉ dành cho học viên trả phí.
- **AC4: Cho phép xem lại đoạn học thử (Repeat play)**
  - **Given** Paywall Modal đang hiển thị khi chạm mốc 50%
  - **When** học viên click nút *"Xem lại đoạn học thử"*
  - **Then** Paywall Modal đóng lại, video tua về mốc 00:00 và học viên có thể xem lại trong phạm vi 50% ban đầu mà không bị giới hạn số lần xem lại trong 7 ngày.

---

### 3.6. US-EXP-006: Tự động hết hạn học thử sau 7 ngày & Thu hồi toàn bộ quyền truy cập

**As a** Quản trị viên vận hành nền tảng ANSERA  
**I want to** hệ thống tự động chuyển trạng thái sang hết hạn và khóa toàn bộ nội dung (kể cả 50% của 3 bài đầu) khi học viên hết hạn 7 ngày mà không thanh toán/gia hạn thành công  
**So that** bảo đảm bản quyền nội dung, ngăn chặn trục lợi học thử và thúc đẩy người dùng thanh toán.

![US-EXP-006_ Chi tiết khóa học khi Hết hạn học thử 7 ngày (MSG-006 & Khóa toàn bộ 🔒)](./H%E1%BB%8Dc%20th%E1%BB%AD%20screen./US-EXP-006_%20Chi%20ti%E1%BA%BFt%20kh%C3%B3a%20h%E1%BB%8Dc%20khi%20H%E1%BA%BFt%20h%E1%BA%A1n%20h%E1%BB%8Dc%20th%E1%BB%AD%207%20ng%C3%A0y%20(MSG-006%20&%20Kh%C3%B3a%20to%C3%A0n%20b%E1%BB%99%20%F0%9F%94%92).png)

*US-EXP-006_ Chi tiết khóa học khi Hết hạn học thử 7 ngày (MSG-006 & Khóa toàn bộ 🔒)*

#### Bảng mô tả thành phần giao diện

| STT | Tên thành phần | Type | Được chỉnh sửa | Bắt buộc | Giá trị mặc định | Mô tả |
| :---: | --- | :---: | :---: | :---: | :---: | --- |
| 1 | Banner thông báo hết hạn | Banner | N/A | N/A | N/A | Banner cảnh báo hiển thị trên đầu khóa học: *"Thời gian học thử 7 ngày đã kết thúc"*. |
| 2 | Biểu tượng Khóa 🔒 toàn bộ | Icon | N/A | N/A | N/A | Toàn bộ danh mục bài học (kể cả Bài 1, 2, 3 đã học thử) đều chuyển sang biểu tượng khóa 🔒 với nhãn *"Đã khóa sau học thử"*. |
| 3 | Button Thanh toán để tiếp tục học | Button | N/A | N/A | N/A | CTA duy nhất trên giao diện dẫn tới màn hình thanh toán để mở khóa lại khóa học. |
| 4 | Nút học thử bị vô hiệu hóa | Button | N/A | N/A | N/A | Nút học thử chuyển sang trạng thái disabled: *"Đã sử dụng quyền học thử (1 lần duy nhất)"*. |

#### Acceptance Criteria

- **AC1: Tự động chuyển đổi trạng thái khi hết 7 ngày không gia hạn thành công (System logic)**
  - **Given** khóa học của học viên đang ở trạng thái `TRIAL_ACTIVE`
  - **When** thời gian trôi qua đủ 168 giờ (7 ngày) kể từ thời điểm kích hoạt và xảy ra một trong các trường hợp: (1) Học viên chủ động bấm hủy gia hạn trước ngày thứ 7, hoặc (2) Cổng thanh toán quét trừ tiền gia hạn tự động thất bại sau 3 lần retry
  - **Then** hệ thống tự động cập nhật trạng thái khóa học của học viên sang `TRIAL_EXPIRED`.
- **AC2: Thu hồi toàn bộ quyền truy cập nội dung học thử (Negative path)**
  - **Given** khóa học đã chuyển sang trạng thái `TRIAL_EXPIRED`
  - **When** học viên truy cập vào khóa học hoặc click vào bất kỳ bài nào (kể cả 50% thời lượng của Bài 1, 2, 3 trước đó)
  - **Then** hệ thống chặn hoàn toàn việc phát video, hiển thị cảnh báo `MSG-006`: *"Thời gian học thử 7 ngày của bạn cho khóa học này đã kết thúc. Vui lòng thanh toán để tiếp tục học tập"* và bật modal hướng dẫn thanh toán.
- **AC3: Không cho phép kích hoạt học thử lần 2 (Business rule)**
  - **Given** khóa học của học viên ở trạng thái `TRIAL_EXPIRED`
  - **When** học viên tải lại trang chi tiết khóa học
  - **Then** nút học thử bị vô hiệu hóa hoàn toàn, chỉ hiển thị nút *"Thanh toán để tiếp tục học (399.000đ)"*.
