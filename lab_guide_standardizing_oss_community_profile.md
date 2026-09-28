# THỰC HÀNH: CHUẨN HÓA HỒ SƠ CỘNG ĐỒNG DỰ ÁN OSS

- **Thời lượng:** 50 phút
- **Môi trường yêu cầu:** Tài khoản GitHub, một kho lưu trữ (Repository) cá nhân bất kỳ đã có sẵn code thô trên GitHub để làm phôi nâng cấp.
- **Mục tiêu:** Tạo lập và cấu hình hoàn chỉnh bộ hồ sơ: `LICENSE`, `CONTRIBUTING.md`, `CODE_OF_CONDUCT.md`, `SECURITY.md` và hệ thống tự động hóa biểu mẫu `.github/ISSUE_TEMPLATE`.

---

## HƯỚNG DẪN CHI TIẾT

### Bước 1: Kích hoạt Giấy phép Bản quyền LICENSE

Một dự án mã nguồn mở không có file `LICENSE` thì về mặt pháp lý doanh nghiệp sẽ không ai dám tải về dùng vì sợ vi phạm bản quyền. Trong bài Lab này, chúng ta sẽ áp dụng giấy phép MIT (Tự do, gọn nhẹ).

1. Truy cập vào kho lưu trữ của bạn trên giao diện Web GitHub.
2. Bấm vào nút **Add file** ➔ Chọn **Create new file**.
3. Tại ô đặt tên file, gõ chính xác chữ: `LICENSE` (viết hoa toàn bộ).
4. GitHub sẽ hiển thị một nút xanh có tên là **"Choose a license template"** ở bên phải. Bấm vào nút này.
5. Chọn **MIT License** từ danh sách bên trái. Ở cột bên phải, kiểm tra lại thông tin năm (2026) và tên đầy đủ của bạn (Ví dụ: DUT).
6. Bấm **Review and submit** ➔ Bấm **Commit changes** để đẩy file thẳng lên nhánh `main`.

---

### Bước 2: Soạn thảo Cẩm nang đóng góp CONTRIBUTING.md

File này đóng vai trò như một cuốn "Sách hướng dẫn luật chơi" dành cho các Contributor muốn vào sửa code, tránh việc họ viết code lộn xộn phá vỡ cấu trúc dự án.

1. Bấm **Add file** ➔ **Create new file**. Đặt tên tệp tin là `CONTRIBUTING.md`.
2. Sao chép và điền nội dung theo khung chuẩn sau:

```markdown
# 🤝 Hướng dẫn đóng góp mã nguồn cho dự án

Chào mừng bạn đã đến với dự án! Chúng tôi rất hào hứng khi nhận được sự hỗ trợ từ phía cộng đồng. Để đảm bảo chất lượng mã nguồn, vui lòng tuân thủ quy trình sau:

## 🚀 Quy trình làm việc (Workflow)

1. **Fork** kho lưu trữ này về tài khoản cá nhân của bạn.
2. Tạo một nhánh tính năng mới đi ra từ nhánh `main` sạch:
   ```bash
   git checkout -b feat/ten-tinh-nang
   ```
3. Tiến hành viết code, đảm bảo code đã chạy qua hệ thống test cục bộ.
4. Commit mã nguồn theo chuẩn Conventional Commits (Ví dụ: `feat(core): add json support`).
5. Đẩy nhánh lên GitHub của bạn và mở một Pull Request (PR) hướng về nhánh `main` của kho gốc.

## 🎨 Quy chuẩn viết code (Coding Standards)

- **Ngôn ngữ C:** Thụt lề bằng 4 khoảng trắng (Spaces), tuyệt đối không dùng phím Tab.
- **Đặt tên biến:** Sử dụng chuẩn `snake_case` (Ví dụ: `user_id`, `max_length`).
- Mọi hàm mới bổ sung bắt buộc phải có comment đặc tả giải thích ở file header.
```

3. Bấm **Commit changes** để lưu lại.

---

### Bước 3: Kích hoạt Quy ước ứng xử CODE_OF_CONDUCT.md

Để bảo vệ các thành viên khỏi nạn bắt nạt mạng, phân biệt đối xử và giữ cho không gian thảo luận luôn văn minh (Mục 10.3), chúng ta sử dụng chuẩn quốc tế Contributor Covenant.

1. Bấm **Add file** ➔ **Create new file**. Đặt tên tệp tin là `CODE_OF_CONDUCT.md`.
2. Truy cập trang web [https://www.contributor-covenant.org/](https://www.contributor-covenant.org/) để lấy bản dịch mới nhất, hoặc sử dụng khung sườn cốt lõi sau:

```markdown
# 📜 Quy ước ứng xử cộng đồng

## 1. Cam kết của chúng tôi

Nhằm mục đích nuôi dưỡng một môi trường cởi mở và thân thiện, chúng tôi với tư cách là những nhà quản trị dự án cam kết làm cho việc tham gia dự án trở thành một trải nghiệm không bị quấy rối cho tất cả mọi người, bất kể tuổi tác, giới tính, trình độ hay tôn giáo.

## 2. Các hành vi chuẩn mực (Hành vi tích cực)

- Sử dụng ngôn từ lịch sự, mang tính chất xây dựng kỹ thuật.
- Tôn trọng các quan điểm và ý kiến trái chiều của các thành viên khác.
- Thể hiện sự đồng cảm và cổ vũ đối với những lập trình viên mới tham gia.

## 3. Các hành vi không thể chấp nhận (Hành vi độc hại)

- Ngôn từ mang tính chất lăng mạ, công kích cá nhân, xúc phạm trình độ.
- Quấy rối, spam hoặc gửi các nội dung không liên quan vào mục thảo luận.

## 4. Cơ chế thực thi

Mọi hành vi vi phạm quy ước này sẽ bị Ban quản trị xử lý nghiêm khắc thông qua các hình thức: Ẩn bình luận, cảnh báo bằng email, hoặc **Khóa tài khoản vĩnh viễn** khỏi dự án. Để báo cáo vi phạm, vui lòng gửi thư về email: `admin-project@email.com`.
```

3. Bấm **Commit changes** để hoàn tất.

---

### Bước 4: Cấu hình Chính sách Bảo mật SECURITY.md

> **Tư duy quản trị:** Lỗi thông thường (bug) thì có thể mở Issue công khai. Nhưng nếu phát hiện ra lỗi bảo mật nghiêm trọng (như rò rỉ dữ liệu, hở mã khóa), việc mở Issue công khai sẽ vô tình "mách nước" cho các hacker vào tấn công hệ thống trước khi bạn kịp vá. `SECURITY.md` sinh ra để hướng dẫn người dùng cách báo cáo bảo mật một cách âm thầm (Private Reporting).

1. Tại giao diện thư mục gốc của kho lưu trữ trên GitHub, bấm **Add file** ➔ **Create new file**.
2. Đặt tên tệp tin chính xác là: `SECURITY.md` (viết hoa toàn bộ).
3. Sao chép và biên soạn nội dung theo biểu mẫu an ninh mạng dưới đây:

```markdown
# 🛡️ Chính sách Bảo mật (Security Policy)

Chúng tôi cực kỳ coi trọng an ninh an toàn của hệ thống. Nếu bạn phát hiện ra bất kỳ lỗ hổng bảo mật nào, xin vui lòng KHÔNG mở Issue công khai. Hãy làm theo hướng dẫn dưới đây để báo cáo an toàn.

## 1. Các phiên bản được hỗ trợ bảo trì (Supported Versions)

Chúng tôi chỉ tiến hành vá lỗi bảo mật cho các phiên bản phần mềm nằm trong danh sách dưới đây:

| Phiên bản (Version) | Được hỗ trợ bảo mật? |
| :--- | :---: |
| v2.x.x | 🟢 Có |
| v1.5.x | 🟢 Có |
| < v1.4.0 | ❌ Không (Vui lòng nâng cấp lên bản mới nhất) |

## 2. Quy trình báo cáo lỗ hổng (Reporting a Vulnerability)

Khi phát hiện lỗ hổng bảo mật (Ví dụ: Lỗi tràn bộ nhớ, rò rỉ Token cấp quyền):

1. **Phương thức 1 (Khuyến khích):** Truy cập vào tab **Security** trên kho lưu trữ GitHub này ➔ Chọn **Vulnerability reporting** ➔ Bấm **Report a vulnerability** để gửi báo cáo mã hóa riêng tư cho Ban quản trị.
2. **Phương thức 2:** Gửi email trực tiếp mô tả chi tiết lỗi kèm theo code kiểm thử mã độc (PoC) về hòm thư: `security-report@yourdomain.com`.

## 3. Cam kết phản hồi của Ban quản trị

- Chúng tôi sẽ phản hồi xác nhận đã tiếp nhận thông tin trong vòng **48 tiếng**.
- Lỗ hổng sẽ được giữ bí mật tuyệt đối trong quá trình đội ngũ kỹ sư tiến hành viết bản vá (Hotfix).
- Sau khi bản vá được phát hành chính thức, chúng tôi sẽ vinh danh tên của bạn tại bảng tin **Release Notes** của dự án để tri ân đóng góp cho cộng đồng.
```

4. Bấm **Commit changes** để lưu lại file.

---

### Bước 5: Tự động hóa Biểu mẫu Issue Template

Để ép người dùng phải khai báo lỗi chi tiết theo chuẩn (như bài thực hành trước), chúng ta sẽ tạo biểu mẫu tự động. Khi người dùng bấm nút "New Issue", biểu mẫu này sẽ tự động hiện ra cho họ điền.

1. Bấm **Add file** ➔ **Create new file**.
2. Tại ô đặt tên, bạn tạo một thư mục ẩn bằng cách gõ chính xác đường dẫn sau:  
   `.github/ISSUE_TEMPLATE/bug_report.yml`
3. Sao chép đoạn mã cấu hình biểu mẫu dạng YAML chuẩn sau vào file:

```yaml
name: 🐛 Báo cáo lỗi kỹ thuật (Bug Report)
description: Khởi tạo một biểu mẫu chuẩn hóa để báo cáo lỗi cho các kỹ sư lập trình.
title: "[BUG]: <Tóm tắt ngắn gọn lỗi của bạn>"
labels: ["type/bug", "triage-needed"]
body:
  - type: markdown
    attributes:
      value: |
        Cảm ơn bạn đã dành thời gian báo lỗi để giúp dự án hoàn thiện hơn!
  - type: textarea
    id: bug-description
    attributes:
      label: 1. Mô tả chi tiết lỗi
      description: Điều gì đang xảy ra với phần mềm của bạn?
      placeholder: Viết mô tả lỗi tại đây...
    validations:
      required: true
  - type: textarea
    id: steps-to-reproduce
    attributes:
      label: 2. Các bước tái hiện lỗi
      description: Liệt kê thứ tự các bước để kỹ sư có thể làm chạy lại lỗi này trên máy của họ.
      placeholder: |
        1. Chạy lệnh...
        2. Nhập tham số...
    validations:
      required: true
  - type: dropdown
    id: operating-system
    attributes:
      label: 3. Hệ điều hành đang sử dụng
      options:
        - Ubuntu Linux (24.04/26.04)
        - Windows 11
        - macOS Sequoia
    validations:
      required: true
```

4. Bấm **Commit changes**.

> **KIỂM TRA KẾT QUẢ:** Bây giờ, bạn bấm vào tab **Issues** của repo ➔ Bấm nút **New Issue**. Bạn sẽ thấy một giao diện biểu mẫu chuyên nghiệp xuất hiện thay thế cho khung nhập text trống ngày trước. Đồng thời, quay trở lại trang chủ dự án, góc phải màn hình mục **Community Profile** của dự án trên GitHub đã chính thức chuyển sang màu xanh lá cây đạt điểm 100% Khỏe mạnh.

---

### Bước 6: Tự động hóa Biểu mẫu Pull Request Template

> **Tư duy quản trị:** Để ép tất cả các Contributor khi mở đơn xin gộp code (Pull Request) đều phải viết tài liệu mạch lạc, có đầy đủ checklist kiểm tra như chúng ta đã học ở bài thực hành trước, bạn cần tạo ra một file khuôn mẫu. Mỗi khi có ai đó bấm nút "Create Pull Request", biểu mẫu này sẽ tự động hiện ra trong khung nhập liệu của họ.

1. Bấm **Add file** ➔ **Create new file**.
2. Tại ô đặt tên, gõ chính xác đường dẫn thư mục ẩn và tên file sau:  
   `.github/PULL_REQUEST_TEMPLATE.md`  
   *(Lưu ý: Viết hoa toàn bộ tên file `PULL_REQUEST_TEMPLATE.md` và đặt trong thư mục `.github/`)*.
3. Sao chép đoạn mã Markdown chuẩn dưới đây vào file:

```markdown
## 🎯 1. Tổng quan sự thay đổi (Overview)

- **Bản chất thay đổi:** [Ví dụ: Sửa lỗi tràn bộ nhớ trong module quản lý chuỗi]
- **Liên kết Issue:** Liên quan đến Issue số #

## 🛠️ 2. Danh sách các thay đổi chi tiết (Detailed Changes)

- File `src/...`: Thêm hàm...
- File `tests/...`: Bổ sung dữ liệu kiểm thử...

## 🧪 3. Hướng dẫn kiểm thử (How to Test)

Chạy câu lệnh sau tại Terminal để xác nhận tính năng hoạt động sạch lỗi:

```bash
make test
```

## ✅ 4. Checklist tự kiểm tra của Tác giả

Vui lòng đánh dấu [x] vào các ô sau khi bạn đã hoàn thành kiểm tra:

- [ ] Code của tôi đã chạy qua hệ thống test cục bộ và hiện màu xanh (All tests passed).
- [ ] Tôi đã viết comment đặc tả đầy đủ cho các hàm mới bổ sung.
- [ ] Tôi không đẩy các file cấu hình môi trường cá nhân hoặc file rác hệ thống lên Git.
- [ ] Tôi đã viết thông điệp Commit đúng chuẩn định dạng Semantic (`feat:`, `fix:`, `docs:`).
```

4. Bấm **Commit changes** để hoàn tất.

---

## CẤU TRÚC THƯ MỤC DỰ ÁN HOÀN CHỈNH

Sau khi hoàn thành toàn bộ các bước, cấu trúc thư mục quản trị cộng đồng (DevSecOps) trong kho lưu trữ của bạn sẽ hiển thị như sau:

```text
dự-án-của-bạn (Root)
├── .github/
│   ├── ISSUE_TEMPLATE/
│   │   └── bug_report.yml          (Biểu mẫu báo lỗi tự động)
│   └── PULL_REQUEST_TEMPLATE.md    (Biểu mẫu kiểm duyệt code tự động)
├── CODE_OF_CONDUCT.md              (Luật ứng xử văn minh)
├── CONTRIBUTING.md                 (Cẩm nang hướng dẫn viết code)
├── LICENSE                         (Giấy phép bản quyền MIT)
├── SECURITY.md                     (Chính sách bảo mật riêng tư)
└── README.md                       (Mặt tiền trang chủ dự án)
```

**Kiểm tra thực tế:** Hãy liên hệ với thành viên cùng nhóm thử đóng vai một người ngoài để bấm nút mở một Pull Request vào kho lưu trữ này.

---

## BÁO CÁO THỰC HÀNH

Cung cấp link repo và chụp màn hình kết quả các bước thực hiện và kiểm tra.