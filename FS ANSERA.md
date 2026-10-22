# ĐẶC TẢ USER STORIES & ACCEPTANCE CRITERIA (ANSERA PLATFORM)
**Tác giả:** Duong Duc An  
**Phiên bản:** 2.0 (Cập nhật mô hình Học thử Freemium 7 ngày - Không cần thẻ tín dụng)

---

## 1. Phụ lục Thông báo (Message Catalog)

| Mã MSG | Loại | Nội dung thông báo | Điều kiện xuất hiện |
| :--- | :---: | :--- | :--- |
| **MSG-001** | Lỗi | Vui lòng nhập thông tin | Khi người dùng bỏ trống các trường thông tin bắt buộc và bấm gửi |
| **MSG-002** | Cảnh báo | Tên người dùng đã tồn tại | Khi người dùng điền một username đã tồn tại trong hệ thống để đăng ký |
| **MSG-003** | Lỗi | Thông tin chưa hợp lệ | Khi mật khẩu xác nhận không khớp, mật khẩu dưới 8 ký tự hoặc định dạng dữ liệu không hợp lệ |
| **MSG-004** | Thông báo | Bạn đã đăng ký khóa học này rồi | Khi học viên click "Đăng ký ngay" đối với khóa học đã đăng ký/sở hữu trước đó |
| **MSG-005** | Thông báo | Bạn đã hoàn thành thời lượng học thử của bài học này. Vui lòng mở khóa để xem tiếp toàn bộ nội dung. | Khi video bài học phát chạm mốc 50% thời lượng trong chế độ học thử |
| **MSG-006** | Cảnh báo | Thời gian học thử 7 ngày của bạn cho khóa học này đã kết thúc. Vui lòng thanh toán để tiếp tục học tập. | Khi học viên truy cập vào khóa học sau khi thời hạn học thử 7 ngày đã kết thúc |

---

## 2. Danh mục User Stories tổng quan

| Mã Story | Nội dung User Story (As a / I want / So that) | Độ ưu tiên |
| :--- | :--- | :---: |
| **US-AUTH-001** | **As a** khách truy cập mới<br>**I want to** đăng ký tài khoản bằng username và mật khẩu<br>**So that** tôi sở hữu tài khoản định danh để học tập và lưu tiến trình | Must Have (P0) |
| **US-CRS-002** | **As a** học viên đã đăng nhập<br>**I want to** xem chi tiết giáo trình, thông tin giảng viên và nhận diện các bài được học thử 50%<br>**So that** tôi hiểu rõ giá trị khóa học trước khi quyết định trải nghiệm hoặc mua | Must Have (P0) |
| **US-ENR-003** | **As a** học viên chưa từng học thử khóa học<br>**I want to** kích hoạt trải nghiệm học thử miễn phí trong 7 ngày tức thì không cần thẻ tín dụng<br>**So that** tôi nhanh chóng vào xem bài giảng thực tế mà không lo lắng rủi ro tài chính | High (P1) |
| **US-PLAY-004** | **As a** học viên trong thời gian học thử 7 ngày<br>**I want to** xem 50% thời lượng của 3 bài đầu tiên và nhận thông báo mở khóa khi chạm giới hạn<br>**So that** tôi trải nghiệm cách giảng dạy và đưa ra quyết định nâng cấp khóa học | Must Have (P0) |
| **US-EXP-005** | **As a** hệ thống ANSERA<br>**I want to** tự động thu hồi quyền truy cập học thử khi quá hạn 7 ngày<br>**So that** bảo vệ bản quyền nội dung và thúc đẩy học viên chuyển đổi sang trả phí | High (P1) |
| **US-PAY-006** | **As a** học viên muốn sở hữu khóa học<br>**I want to** thanh toán mở khóa toàn bộ khóa học trọn đời<br>**So that** tôi học không giới hạn 100% thời lượng, làm bài tập và nhận chứng chỉ tốt nghiệp | Must Have (P0) |

---

## 3. Chi tiết đặc tả User Stories & Acceptance Criteria

### 3.1. US-AUTH-001: Đăng ký tài khoản học viên mới bằng Username & Password

**As a** khách truy cập mới chưa có tài khoản trên ANSERA  
**I want to** đăng ký tài khoản bằng username và mật khẩu cá nhân  
**So that** tôi sở hữu tài khoản định danh trên nền tảng, lưu trữ lộ trình học và sử dụng các tính năng học tập cá nhân hóa.

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
  - **When** người dùng nhập `username` chưa tồn tại, `password` hợp lệ (tối thiểu 8 ký tự), `confirm password` trùng khớp 100%, và nhấn "Đăng ký"
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

#### Bảng mô tả thành phần giao diện

| STT | Tên thành phần | Type | Được chỉnh sửa | Bắt buộc | Giá trị mặc định | Mô tả |
| :---: | --- | :---: | :---: | :---: | :---: | --- |
| 1 | Card thông tin khóa học | Card | N/A | N/A | N/A | Tên khóa, đơn vị phát hành, xếp hạng rating, số lượng học viên, cấp độ. |
| 2 | Video trailer giới thiệu | Media | N/A | N/A | N/A | Video ngắn giới thiệu tổng quan nội dung và mục tiêu khóa học. |
| 3 | Button Học thử 7 ngày miễn phí | Button | N/A | N/A | N/A | CTA chính: Kích hoạt trải nghiệm 7 ngày không cần thẻ tín dụng (Dẫn tới US-ENR-003). |
| 4 | Button Mua khóa học | Button | N/A | N/A | N/A | CTA phụ: Dẫn tới trang thanh toán mua đứt khóa học trọn đời (US-PAY-006). |
| 5 | Huy hiệu [Học thử 50%] | Badge | N/A | N/A | N/A | Gắn cạnh Bài 1, Bài 2, Bài 3 trong danh mục bài học để người dùng nhận diện. |
| 6 | Biểu tượng Khóa 🔒 | Icon | N/A | N/A | N/A | Gắn cạnh Bài 4, Bài 5 và toàn bộ bài tập/quizz (chỉ mở khi thanh toán trả phí). |
| 7 | Accordion bài học | Accordion | N/A | N/A | N/A | Click vào mũi tên để xem mô tả tóm tắt nội dung bài học. |

#### Acceptance Criteria

- **AC1: Hiển thị đầy đủ thông tin khóa học và phân loại bài học (Happy path)**
  - **Given** học viên đã đăng nhập và xem trang chi tiết khóa học
  - **When** trang tải hoàn tất
  - **Then** hệ thống hiển thị đầy đủ thông tin khóa học, thông tin giảng viên, đánh giá
  - **And** hiển thị huy hiệu `[Học thử 50%]` tại Bài 1, 2, 3 và biểu tượng 🔒 tại các bài từ số 4 trở đi kèm nút CTA *"Học thử 7 ngày miễn phí (Không cần thẻ)"*.
- **AC2: Mở rộng tóm tắt bài học qua Accordion (Interaction)**
  - **Given** học viên đang ở mục danh mục bài học
  - **When** học viên click vào biểu tượng mũi tên xổ xuống tại một bài học
  - **Then** hệ thống bung mở bản tóm tắt nội dung bài học mà không tải lại trang.
- **AC3: Đã sở hữu khóa học bấm Đăng ký ngay (Negative path)**
  - **Given** học viên đã thanh toán mua khóa học này trước đó
  - **When** học viên vào trang chi tiết khóa học và click nút mua
  - **Then** hệ thống không mở luồng thanh toán và hiển thị thông báo `MSG-004`: *"Bạn đã đăng ký khóa học này rồi"*.

---

### 3.3. US-ENR-003: Kích hoạt trải nghiệm học thử 7 ngày không cần thẻ tín dụng

**As a** học viên đã đăng nhập và chưa từng học thử khóa học đang chọn  
**I want to** kích hoạt gói học thử 7 ngày chỉ với 1 click mà không cần nhập thẻ thanh toán  
**So that** tôi có thể trải nghiệm ngay chất lượng bài giảng một cách nhanh chóng, thuận tiện và an tâm tuyệt đối.

#### Bảng mô tả thành phần giao diện

| STT | Tên thành phần | Type | Được chỉnh sửa | Bắt buộc | Giá trị mặc định | Mô tả |
| :---: | --- | :---: | :---: | :---: | :---: | --- |
| 1 | Button Học thử 7 ngày miễn phí | Button | N/A | N/A | N/A | Nút kích hoạt trên trang chi tiết khóa học. |
| 2 | Modal cam kết học thử | Modal | N/A | N/A | N/A | Hộp thoại thông báo: Quyền lợi xem 50% của 3 bài đầu trong 7 ngày, hoàn toàn miễn phí, không phát sinh chi phí ngầm. |
| 3 | Button Bắt đầu học ngay | Button | N/A | N/A | N/A | Nằm trong modal. Click để xác nhận kích hoạt và vào thẳng Bài 1. |
| 4 | Banner đếm ngược thời gian | Banner | N/A | N/A | N/A | Thanh thông báo trên đầu trình phát bài học hiển thị thời gian học thử còn lại (ví dụ: Còn 6 ngày 23 giờ). |

#### Acceptance Criteria

- **AC1: Kích hoạt học thử thành công tức thì không cần thẻ (Happy path)**
  - **Given** học viên đã đăng nhập và chưa từng tham gia học thử khóa học này
  - **When** học viên nhấn nút *"Học thử 7 ngày miễn phí"* và xác nhận *"Bắt đầu học ngay"* trên Modal
  - **Then** hệ thống lập tức chuyển trạng thái khóa học của học viên sang `TRIAL_ACTIVE`
  - **And** kích hoạt đồng hồ đếm ngược 168 giờ (7 ngày), điều hướng trực tiếp học viên vào màn hình phát Bài học số 1 mà không yêu cầu bất kỳ thông tin thanh toán nào.
- **AC2: Đã từng học thử khóa học này trước đây (Negative path)**
  - **Given** học viên đã từng kích hoạt gói học thử 7 ngày cho khóa học này (đang diễn ra hoặc đã kết thúc)
  - **When** học viên truy cập trang chi tiết khóa học
  - **Then** nút *"Học thử 7 ngày miễn phí"* chuyển sang trạng thái disabled với dòng chữ *"Bạn đã dùng quyền học thử của khóa học này"*, chỉ hiển thị nút *"Mua khóa học ngay"*.
- **AC3: Chưa đăng nhập bấm học thử (Edge case)**
  - **Given** khách truy cập chưa đăng nhập đang xem khóa học
  - **When** khách nhấn *"Học thử 7 ngày miễn phí"*
  - **Then** hệ thống điều hướng đến trang Đăng nhập / Đăng ký kèm tham số lưu trang đích (`redirect_url`), sau khi đăng nhập thành công tự động kích hoạt học thử.

---

### 3.4. US-PLAY-004: Trải nghiệm học thử 50% thời lượng 3 bài đầu & Chặn tua (Seek Guard)

**As a** học viên đang trong thời gian học thử 7 ngày  
**I want to** xem được 50% thời lượng của 3 bài đầu tiên và hiển thị Paywall khi chạm giới hạn  
**So that** tôi cảm nhận được giá trị kiến thức thực tế và quyết định nâng cấp gói trả phí.

#### Bảng mô tả thành phần giao diện

| STT | Tên thành phần | Type | Được chỉnh sửa | Bắt buộc | Giá trị mặc định | Mô tả |
| :---: | --- | :---: | :---: | :---: | :---: | --- |
| 1 | Khung trình phát video | Video | N/A | N/A | N/A | Phát video bài giảng với các nút điều khiển chuẩn. |
| 2 | Thanh tiến trình tua (Seek-bar) | Slider | Yes | N/A | 00:00 | Được phân tách trực quan: 50% đầu có màu nổi bật (cho phép phát), 50% sau bị mờ kèm vạch ngăn ranh giới học thử. |
| 3 | Paywall Modal Overlay | Modal | N/A | N/A | N/A | Lớp phủ bật lên khi video đạt 50% hoặc click bài bị khóa, hiển thị ưu đãi và các tính năng mở rộng khi mua khóa học. |
| 4 | Button Mở khóa toàn bộ khóa học | Button | N/A | N/A | N/A | Nút CTA chính trên Paywall Modal dẫn tới màn hình thanh toán. |
| 5 | Button Xem lại đoạn học thử | Button | N/A | N/A | N/A | Nút phụ trên Paywall Modal cho phép tua lại video về mốc 00:00 để nghe lại. |

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

### 3.5. US-EXP-005: Tự động hết hạn học thử sau 7 ngày & Thu hồi quyền truy cập

**As a** hệ thống ANSERA  
**I want to** tự động chuyển trạng thái hết hạn và khóa toàn bộ nội dung khi quá thời hạn 7 ngày học thử  
**So that** đảm bảo bảo mật quyền lợi nội dung và thúc đẩy học viên thanh toán để tiếp tục học tập.

#### Bảng mô tả thành phần giao diện

| STT | Tên thành phần | Type | Được chỉnh sửa | Bắt buộc | Giá trị mặc định | Mô tả |
| :---: | --- | :---: | :---: | :---: | :---: | --- |
| 1 | Banner thông báo hết hạn | Banner | N/A | N/A | N/A | Banner cảnh báo hiển thị trên đầu khóa học: *"Thời gian học thử 7 ngày đã kết thúc"*. |
| 2 | Biểu tượng Khóa 🔒 toàn bộ | Icon | N/A | N/A | N/A | Toàn bộ danh mục bài học (kể cả Bài 1, 2, 3) đều chuyển sang biểu tượng khóa 🔒. |
| 3 | Button Mua khóa học để tiếp tục | Button | N/A | N/A | N/A | CTA duy nhất trên giao diện dẫn tới thanh toán mua khóa học. |

#### Acceptance Criteria

- **AC1: Tự động chuyển đổi trạng thái khi hết 7 ngày (System logic)**
  - **Given** khóa học của học viên đang ở trạng thái `TRIAL_ACTIVE`
  - **When** thời gian trôi qua đủ 168 giờ (7 ngày) kể từ thời điểm kích hoạt mà học viên chưa thanh toán mua khóa học
  - **Then** hệ thống tự động cập nhật trạng thái khóa học sang `TRIAL_EXPIRED`.
- **AC2: Thu hồi toàn bộ quyền truy cập nội dung học thử (Negative path)**
  - **Given** khóa học đã chuyển sang trạng thái `TRIAL_EXPIRED`
  - **When** học viên truy cập vào khóa học hoặc click vào bất kỳ bài nào (kể cả 3 bài đầu)
  - **Then** hệ thống chặn hoàn toàn việc xem video, hiển thị cảnh báo `MSG-006`: *"Thời gian học thử 7 ngày của bạn cho khóa học này đã kết thúc. Vui lòng thanh toán để tiếp tục học tập"* và bật modal hướng dẫn thanh toán.
- **AC3: Không cho phép kích hoạt học thử lần 2 (Business rule)**
  - **Given** khóa học của học viên ở trạng thái `TRIAL_EXPIRED`
  - **When** học viên tải lại trang chi tiết khóa học
  - **Then** nút *"Học thử 7 ngày miễn phí"* bị ẩn hoàn toàn, chỉ hiển thị nút *"Mua khóa học ngay"*.

---

### 3.6. US-PAY-006: Thanh toán mở khóa toàn bộ khóa học trọn đời

**As a** học viên muốn học trọn vẹn kiến thức  
**I want to** thực hiện thanh toán mua khóa học một lần dễ dàng  
**So that** tôi mở khóa vĩnh viễn 100% thời lượng toàn bộ bài giảng, nộp bài tập ôn tập và nhận chứng chỉ tốt nghiệp.

#### Bảng mô tả thành phần giao diện

| STT | Tên thành phần | Type | Được chỉnh sửa | Bắt buộc | Giá trị mặc định | Mô tả |
| :---: | --- | :---: | :---: | :---: | :---: | --- |
| 1 | Thông tin đơn hàng | Text | N/A | N/A | N/A | Tên khóa học, giá niêm yết, số tiền thanh toán cuối cùng. |
| 2 | Trường Họ và tên | Text | Yes | Yes | N/A | Tên người mua hiển thị trên hóa đơn và chứng chỉ. Bỏ trống báo **MSG-001**. |
| 3 | Trường Email | Text | Yes | Yes | N/A | Email nhận biên lai và tài liệu khóa học. Sai cú pháp báo **MSG-003**. |
| 4 | Phương thức thanh toán | Radio | Yes | Yes | Thẻ quốc tế | Lựa chọn phương thức: Thẻ quốc tế (Visa/Mastercard) hoặc Chuyển khoản QR / Ví điện tử. |
| 5 | Button Xác nhận thanh toán | Button | N/A | N/A | N/A | Gửi lệnh thanh toán sang cổng thanh toán đối tác. |

#### Acceptance Criteria

- **AC1: Thanh toán thành công và mở khóa 100% nội dung (Happy path)**
  - **Given** học viên đang ở màn hình thanh toán khóa học
  - **When** học viên điền đầy đủ thông tin hợp lệ, chọn phương thức thanh toán và hoàn tất giao dịch thành công qua cổng thanh toán
  - **Then** hệ thống cập nhật trạng thái đơn hàng `PAID`, nâng cấp trạng thái khóa học của học viên sang `ENROLLED`
  - **And** gỡ bỏ toàn bộ biểu tượng ổ khóa 🔒 trên tất cả các bài học (từ Bài 1 đến hết), mở khóa 100% thời lượng tua video và kích hoạt mục bài tập ôn tập kèm gửi email hóa đơn.
- **AC2: Bỏ trống trường thông tin bắt buộc (Validation)**
  - **Given** học viên đang ở form thanh toán
  - **When** học viên để trống họ tên hoặc email và bấm xác nhận
  - **Then** hệ thống chặn gửi dữ liệu và hiển thị lỗi `MSG-001`: *"Vui lòng nhập thông tin"*.
- **AC3: Giao dịch thanh toán bị hủy hoặc thất bại (Negative path)**
  - **Given** học viên đang thực hiện giao dịch tại cổng thanh toán
  - **When** giao dịch bị ngân hàng từ chối hoặc học viên bấm hủy thanh toán
  - **Then** hệ thống hiển thị thông báo thanh toán không thành công, giữ nguyên trạng thái khóa học cũ và cho phép học viên thử lại.
