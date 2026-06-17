# AI Audit Log

## 1. Thông tin chung

| Thông tin | Nội dung |
|---|---|
| Môn học | Software Requirments |
| Mã môn học | SWR302 |
| Lớp | SE20A02 |
| Học kỳ | SU26 |
| Tên bài tập / Project | FitnessTrainingSystem |
| Tên sinh viên / Nhóm | Đặng Phương Nam |
| MSSV / Danh sách MSSV | DE190177 |
| Giảng viên hướng dẫn | TamTTT14 |
| Ngày bắt đầu |  |
| Ngày hoàn thành |  |

---

## 2. Công cụ AI đã sử dụng

Đánh dấu các công cụ AI đã sử dụng trong quá trình thực hiện bài tập/project.

- [ ] ChatGPT
- [x] Gemini
- [x] Claude
- [ ] GitHub Copilot
- [ ] Cursor
- [x] Antigravity
- [x] Perplexity
- [ ] Microsoft Copilot
- [x] Công cụ khác: NotebookLM

---

## 3. Mục tiêu sử dụng AI

Mô tả ngắn gọn sinh viên/nhóm đã sử dụng AI để hỗ trợ những công việc nào.

Ví dụ:

- Phân tích yêu cầu bài toán
- Gợi ý ý tưởng giải pháp
- Thiết kế database
- Thiết kế giao diện
- Viết code mẫu
- Debug lỗi
- Tối ưu code
- Viết test case
- Kiểm tra bảo mật
- Viết báo cáo
- Chuẩn bị slide thuyết trình
- Tìm hiểu công nghệ mới

### Mô tả mục tiêu sử dụng AI

```text
- Tìm kiếm, tóm tắt tài liệu học thuật
- Giải thích, ví dụ lý thuyết
- Liệt kê, phân tích các business trong đề bài
- Chấm điểm bài làm dựa trên góc nhìn của chuyên gia
- Hướng dẫn mindset để xác định đúng yêu cầu
```

## 4. Nhật ký sử dụng AI chi tiết

> Mỗi lần sử dụng AI cho một phần quan trọng của bài tập/project, sinh viên cần ghi lại theo mẫu bên dưới.  
> Sinh viên/nhóm có thể nhân bản mẫu “Lần sử dụng AI” nhiều lần tùy theo số lần sử dụng AI thực tế.

---

### Lần sử dụng AI số 1

| Nội dung | Thông tin |
|---|---|
| Ngày sử dụng | 10/06/2026 |
| Công cụ AI | Claude |
| Mục đích sử dụng | Xác định yêu cầu bài toán |
| Phần việc liên quan | Requirement |
| Mức độ sử dụng | Sinh chính nội dung |

#### 4.1. Prompt đã sử dụng

```text
Dựa trên file docx đề tài tôi đã cung cấp, với vai trò là một kỹ sư phần mềm, bạn hãy chỉ ra các business trong đề bài và giải thích vì sao. Đồng thời bạn cũng phải tạo các use case và use story dựa trên các business mà bạn đã nêu. Câu trả lời của bạn nên chia hai bảng riêng biệt, bảng đầu tiên nêu các business và lí do, bảng thứ hai là các use case và use story bạn tạo dựa trên các business bạn đã nêu.   
```

#### 4.2. Kết quả AI gợi ý

Tóm tắt nội dung AI đã trả lời hoặc gợi ý.

```text
Dựa trên đề bài Fitness Class Booking System, hệ thống có 12 business rule chính xoay quanh việc quản lý sức chứa lớp học và xử lý waitlist tự động khi có chỗ trống, yêu cầu thanh toán online trước khi xác nhận booking, chính sách hoàn tiền theo thời gian hủy (trước 6 giờ), tự động gán trainer khi user không chọn, gửi thông báo xác nhận/nhắc nhở, cơ chế đánh giá và rating trainer, phân quyền giữa Trainer (submit availability, xem participant) và Gym Manager (phê duyệt lịch, giám sát utilization), cùng với yêu cầu bảo mật (encrypted login, login Google) và hỗ trợ người dùng mới qua help section. Từ các quy tắc này, mình đã xây dựng 13 use case tương ứng với user story cho từng actor (Member, Trainer, Gym Manager, System), bao gồm các luồng chính như browse và book lớp, thanh toán, vào waitlist, auto-promote khi có hủy, hủy và nhận refund, auto-assign trainer, nhận thông báo, xem lịch sử và đánh giá, trainer quản lý lịch dạy, manager phê duyệt và theo dõi, đăng nhập bảo mật, và truy cập trợ giúp — nhằm đảm bảo các use case bao quát đầy đủ các nghiệp vụ then chốt của hệ thống.
```

#### 4.3. Phần sinh viên/nhóm đã sử dụng từ AI

Mô tả rõ phần nào được sử dụng lại từ gợi ý của AI.

```text
13 use case tương ứng với user story cho từng actor (Member, Trainer, Gym Manager, System), bao gồm các luồng chính như browse và book lớp, thanh toán, vào waitlist, auto-promote khi có hủy, hủy và nhận refund, auto-assign trainer, nhận thông báo, xem lịch sử và đánh giá, trainer quản lý lịch dạy, manager phê duyệt và theo dõi, đăng nhập bảo mật, và truy cập trợ giúp
```

#### 4.4. Phần sinh viên/nhóm tự chỉnh sửa hoặc cải tiến

Mô tả sinh viên/nhóm đã thay đổi, kiểm tra, sửa lỗi hoặc cải tiến gì so với gợi ý ban đầu của AI.

Dưới đây là phân tích dựa trên đề bài Fitness Class Booking System (Lab7_SWR302), với vai trò kỹ sư phần mềm phân tích yêu cầu.

Bảng 1: Business Rules (Quy tắc nghiệp vụ) và giải thích
| STT | Business Rule	Giải thích | Vì sao đây là business rule |
|---|---|---|
| 1 | Mỗi lớp học có sức chứa (capacity) cố định | Đây là constraint nghiệp vụ giới hạn số học viên/lớp, quyết định khi nào hệ thống phải chuyển sang xử lý waitlist; không phải yêu cầu kỹ thuật mà là chính sách vận hành của trung tâm |
| 2	| Phải thanh toán online trước khi booking được xác nhận | Đảm bảo doanh thu thực tế trước khi giữ chỗ, tránh tình trạng giữ slot "ảo" không thanh toán, ảnh hưởng trực tiếp đến luồng nghiệp vụ booking |
| 3	| Nếu lớp đầy, user được đưa vào waitlist |	Xử lý tình huống cung (capacity) nhỏ hơn cầu (demand), đảm bảo nguyên tắc công bằng theo thứ tự đăng ký |
| 4	| Khi có người hủy, hệ thống tự động promote người đầu waitlist |	Tự động hóa quy trình tận dụng slot trống, giảm thao tác thủ công và đảm bảo phục vụ đúng thứ tự ưu tiên |
| 5	| Hủy trước ít nhất 6 giờ so với giờ bắt đầu lớp mới được hoàn tiền |	Time-based policy nhằm giảm rủi ro tài chính cho trung tâm, đồng thời tạo động lực để học viên hủy sớm, giúp slot được tái sử dụng |
| 6	| Nếu user không chọn trainer, hệ thống tự gán theo loại lớp | Đảm bảo mọi booking đều có trainer phù hợp, giảm friction (rào cản) trong trải nghiệm đặt lớp |
| 7	| Gửi xác nhận và nhắc nhở qua email/app notification |	Quy tắc giao tiếp với khách hàng nhằm giảm tỷ lệ no-show và nâng cao trải nghiệm người dùng |
| 8	| User xem lịch sử lớp, để feedback, rate trainer |	Cơ chế đánh giá chất lượng dịch vụ — là input để Gym Manager giám sát hiệu suất trainer |
| 9	| Trainer submit availability và xem participant list | Trainer là actor có quyền tự quản lý lịch làm việc và thông tin lớp mình phụ trách |
| 10	| Gym Manager phê duyệt lịch trainer và theo dõi class utilization |	Quy tắc về governance/quản trị, đảm bảo có một lớp kiểm soát giữa trainer và hệ thống vận hành |
| 11	| Tài khoản hỗ trợ encrypted login và login qua bên thứ ba (Google) |	Yêu cầu bảo mật dữ liệu người dùng kết hợp tiện lợi đăng nhập, ảnh hưởng đến luồng authentication toàn hệ thống |
| 12	| Có help section hướng dẫn người dùng mới |	Yêu cầu hỗ trợ/usability nhằm giảm rào cản onboarding cho người dùng lần đầu |

Bảng 2: Use Case và User Story tương ứng
| ID | Use Case | Actor chính | User Story |
|---|---|---|---|
| UC01 |	Browse classes & view trainer profiles |	Member |	As a member, I want to browse upcoming classes and view trainer profiles (expertise, certifications) so that I can choose the class and trainer that fit my needs. |
| UC02 |	Book a class slot |	Member |	As a member, I want to reserve a time slot for a class so that I can secure my spot before it fills up. |
| UC03 |	Complete online payment |	Member | As a member, I want to pay online when booking so that my reservation is confirmed immediately. |
| UC04 |	Join waitlist when class is full |	Member |	As a member, I want to be automatically placed on a waitlist when a class is full so that I still have a chance to attend if a spot opens up. |
| UC05 |	Auto-promote from waitlist |	System | As the system, I want to automatically promote the next waitlisted member when a cancellation occurs so that available slots are filled without manual intervention. |
| UC06 |	Cancel booking & request refund |	Member |	As a member, I want to cancel my booking at least 6 hours before class start time so that I receive a refund according to policy. |
| UC07 |	Auto-assign trainer |	System |	As the system, I want to automatically assign a trainer based on class type when the member doesn't select one so that every class has a qualified trainer. |
| UC08 |	Receive confirmation & reminder notifications |	Member |	As a member, I want to receive booking confirmations and reminders via email or app notification so that I don't forget or miss my class. |
| UC09 |	View history, leave feedback & rate trainer |	Member |	As a member, I want to view my class history and rate my trainer after class so that I can share feedback and help improve service quality. |
| UC10 |	Submit availability & view participants |	Trainer |	As a trainer, I want to submit my available time slots and view the participant list for my classes so that I can plan and prepare accordingly. |
| UC11 |	Approve trainer schedules & monitor utilization |	Gym Manager |	As a gym manager, I want to approve trainer schedules and monitor class utilization so that I can ensure efficient resource allocation and service quality. |
| UC12 |	Register/login (encrypted or via Google) |	Member/Trainer/Manager |	As a user, I want to log in securely with an encrypted password or through Google so that my account stays protected while I have a convenient login option. |
| UC13 |	Access help section |	New user |	As a new user, I want to access a help section so that I can quickly understand how to use the system. |

#### 4.5. Minh chứng

| Loại minh chứng | Nội dung |
|---|---|
| Link commit |  |
| File liên quan |  |
| Screenshot | <img width="2167" height="1321" alt="image" src="https://github.com/user-attachments/assets/6a81608f-77c9-48ee-8b8e-5b253575d09b" />
 |
| Kết quả chạy/test |  |
| Link video demo |  |
| Ghi chú khác |  |

#### 4.6. Nhận xét cá nhân/nhóm

Sinh viên/nhóm học được gì sau lần sử dụng AI này?

```text
Em đã học được cách xác định các business có trong đề bài dựa trên các actor sau đó là use case và user story để ví dụ dễ hiểu business đó xảy ra khi nào
```

---

### Lần sử dụng AI số 2

| Nội dung | Thông tin |
|---|---|
| Ngày sử dụng |  |
| Công cụ AI | Gemini |
| Mục đích sử dụng | Chấm bài vẽ Use Case Diagram |
| Phần việc liên quan | Report |
| Mức độ sử dụng | Hỗ trợ nhiều |

#### 4.1. Prompt đã sử dụng

```text
Với vai trò là một kĩ sư phần mềm tại công ty Microsoft, bạn hãy chấm bài vẽ Use case diagram của mình. Bạn hãy đánh giá theo các tiêu chí sau: Có đầy đủ các Actor không, đã đủ các use case chưa, mối quan hệ đã đúng chưa, 
```

#### 4.2. Kết quả AI gợi ý

```text
Viết tại đây...
```

#### 4.3. Phần sinh viên/nhóm đã sử dụng từ AI

```text
Viết tại đây...
```

#### 4.4. Phần sinh viên/nhóm tự chỉnh sửa hoặc cải tiến

```text
Viết tại đây...
```

#### 4.5. Minh chứng

| Loại minh chứng | Nội dung |
|---|---|
| Link commit |  |
| File liên quan |  |
| Screenshot |  |
| Kết quả chạy/test |  |
| Link video demo |  |
| Ghi chú khác |  |

#### 4.6. Nhận xét cá nhân/nhóm

```text
Viết tại đây...
```

---

### Lần sử dụng AI số 3

| Nội dung | Thông tin |
|---|---|
| Ngày sử dụng |  |
| Công cụ AI | ChatGPT / Gemini / Claude / GitHub Copilot / Cursor / Antigravity / Khác |
| Mục đích sử dụng |  |
| Phần việc liên quan | Requirement / Design / Database / Frontend / Backend / Testing / Debug / Report / Presentation / Other |
| Mức độ sử dụng | Hỗ trợ ý tưởng / Hỗ trợ một phần / Hỗ trợ nhiều / Sinh chính nội dung |

#### 4.1. Prompt đã sử dụng

```text
Dán nguyên văn prompt đã hỏi AI tại đây.
```

#### 4.2. Kết quả AI gợi ý

```text
Viết tại đây...
```

#### 4.3. Phần sinh viên/nhóm đã sử dụng từ AI

```text
Viết tại đây...
```

#### 4.4. Phần sinh viên/nhóm tự chỉnh sửa hoặc cải tiến

```text
Viết tại đây...
```

#### 4.5. Minh chứng

| Loại minh chứng | Nội dung |
|---|---|
| Link commit |  |
| File liên quan |  |
| Screenshot |  |
| Kết quả chạy/test |  |
| Link video demo |  |
| Ghi chú khác |  |

#### 4.6. Nhận xét cá nhân/nhóm

```text
Viết tại đây...
```

---

## 5. Bảng tổng hợp mức độ sử dụng AI

Đánh dấu mức độ AI hỗ trợ ở từng hạng mục.

| Hạng mục | Không dùng AI | AI hỗ trợ ít | AI hỗ trợ nhiều | AI sinh chính | Ghi chú |
|---|:---:|:---:|:---:|:---:|---|
| Phân tích yêu cầu |  |  |  |  |  |
| Viết user story/use case |  |  |  |  |  |
| Thiết kế database |  |  |  |  |  |
| Thiết kế kiến trúc hệ thống |  |  |  |  |  |
| Thiết kế giao diện |  |  |  |  |  |
| Code frontend |  |  |  |  |  |
| Code backend |  |  |  |  |  |
| Debug lỗi |  |  |  |  |  |
| Viết test case |  |  |  |  |  |
| Kiểm thử sản phẩm |  |  |  |  |  |
| Tối ưu code |  |  |  |  |  |
| Viết báo cáo |  |  |  |  |  |
| Làm slide thuyết trình |  |  |  |  |  |

---

## 6. Các lỗi hoặc hạn chế từ AI

Ghi lại các trường hợp AI trả lời sai, thiếu, chưa phù hợp hoặc sinh code không chạy.

| STT | Lỗi/hạn chế từ AI | Cách phát hiện | Cách xử lý/cải tiến |
|---:|---|---|---|
| 1 |  |  |  |
| 2 |  |  |  |
| 3 |  |  |  |

---

## 7. Kiểm chứng kết quả AI

Mô tả cách sinh viên/nhóm kiểm tra lại kết quả do AI gợi ý.

Có thể bao gồm:

- Chạy thử chương trình
- Viết test case
- So sánh với yêu cầu đề bài
- Kiểm tra output
- Đối chiếu tài liệu môn học
- Hỏi lại giảng viên
- Review cùng thành viên nhóm
- Kiểm tra lỗi bảo mật
- Kiểm tra bằng dữ liệu mẫu
- So sánh trước và sau khi dùng AI

### Nội dung kiểm chứng

```text
Viết tại đây...
```

---

## 8. Đóng góp cá nhân hoặc đóng góp nhóm

### 8.1. Đối với bài cá nhân

Mô tả phần sinh viên tự làm, phần AI hỗ trợ và phần đã tự cải tiến.

```text
Viết tại đây...
```

### 8.2. Đối với bài nhóm

| Thành viên | MSSV | Nhiệm vụ chính | Có sử dụng AI không? | Minh chứng đóng góp |
|---|---|---|---|---|
|  |  |  | Có / Không |  |
|  |  |  | Có / Không |  |
|  |  |  | Có / Không |  |
|  |  |  | Có / Không |  |

---

## 9. Reflection cuối bài

### 9.1. AI đã hỗ trợ em/nhóm ở điểm nào?

```text
Viết tại đây...
```

### 9.2. Phần nào em/nhóm không sử dụng theo gợi ý của AI? Vì sao?

```text
Viết tại đây...
```

### 9.3. Em/nhóm đã kiểm tra tính đúng đắn của kết quả AI như thế nào?

```text
Viết tại đây...
```

### 9.4. Nếu không có AI, phần nào sẽ khó khăn nhất?

```text
Viết tại đây...
```

### 9.5. Sau bài tập/project này, em/nhóm học được gì về môn học?

```text
Viết tại đây...
```

### 9.6. Sau bài tập/project này, em/nhóm học được gì về cách sử dụng AI có trách nhiệm?

```text
Viết tại đây...
```

---

## 10. Cam kết học thuật

Sinh viên/nhóm cam kết rằng:

- Nội dung AI hỗ trợ đã được ghi nhận trung thực.
- Không nộp nguyên văn kết quả AI mà không kiểm tra.
- Có khả năng giải thích các phần đã nộp.
- Chịu trách nhiệm về tính đúng đắn của sản phẩm cuối cùng.
- Hiểu rằng việc sử dụng AI không khai báo có thể ảnh hưởng đến kết quả đánh giá.

| Đại diện sinh viên/nhóm | Ngày xác nhận |
|---|---|
|  |  |
