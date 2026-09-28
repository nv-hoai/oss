# BÁO CÁO THỰC HÀNH: CHUẨN HÓA HỒ SƠ CỘNG ĐỒNG DỰ ÁN OSS

- **Thời gian thực hiện:** 2026-09-28
- **Thư mục dự án:** `/home/nvhoai/projects/personal/opensource/oss`
- **Tài liệu gốc:** `lab_guide_standardizing_oss_community_profile.md`

---

## 1. Tổng hợp kết quả theo yêu cầu

| # | Bước / Yêu cầu | Tệp tin đầu ra | Trạng thái |
| :-: | :--- | :--- | :-: |
| 1 | Kích hoạt giấy phép bản quyền MIT | `LICENSE` | ✅ Hoàn thành |
| 2 | Soạn thảo cẩm nang đóng góp | `CONTRIBUTING.md` | ✅ Hoàn thành |
| 3 | Quy ước ứng xử cộng đồng | `CODE_OF_CONDUCT.md` | ✅ Hoàn thành |
| 4 | Chính sách bảo mật | `SECURITY.md` | ✅ Hoàn thành |
| 5 | Biểu mẫu Issue tự động | `.github/ISSUE_TEMPLATE/bug_report.yml` | ✅ Hoàn thành |
| 6 | Biểu mẫu Pull Request tự động | `.github/PULL_REQUEST_TEMPLATE.md` | ✅ Hoàn thành |
| — | Mặt tiền trang chủ dự án | `README.md` | ✅ Hoàn thành |

> **Kết luận:** 7/7 tệp tin trong cấu trúc hồ sơ cộng đồng hoàn chỉnh đã được tạo đúng vị trí và đúng nội dung theo hướng dẫn.

---

## 2. Chi tiết từng bước

### Bước 1 — `LICENSE` (Giấy phép MIT)

- **Yêu cầu:** Giấy phép MIT, năm 2026, tên đầy đủ của tác giả.
- **Thực hiện:** Tạo tệp `LICENSE` với nội dung chuẩn của MIT License.
- **Thông tin điền:** `Copyright (c) 2026 Nguyen Hoai`
  - Tên tác giả lấy từ cấu hình Git cục bộ (`user.name = nv-hoai`, `user.email = nguyenhoai0990@gmail.com`). *Vui lòng đổi lại nếu muốn dùng tên khác.*
- **Kiểm tra:**
  ```text
  MIT License
  Copyright (c) 2026 Nguyen Hoai
  ```

### Bước 2 — `CONTRIBUTING.md` (Cẩm nang đóng góp)

- **Yêu cầu:** Quy trình workflow (Fork ➔ nhánh `feat/...` ➔ commit Conventional Commits ➔ PR về `main`) và quy chuẩn code C (4 spaces, `snake_case`, comment ở file header).
- **Thực hiện:** Sao chép nguyên khung chuẩn trong tài liệu, giữ nguyên các mục:
  - 🚀 Quy trình làm việc (Workflow) — gồm lệnh `git checkout -b feat/ten-tinh-nang`.
  - 🎨 Quy chuẩn viết code (Coding Standards).

### Bước 3 — `CODE_OF_CONDUCT.md` (Quy ước ứng xử)

- **Yêu cầu:** Chuẩn Contributor Covenant; bảo vệ thành viên khỏi bắt nạt/phân biệt đối xử; có cơ chế thực thi và email báo cáo.
- **Thực hiện:** Tạo 4 mục: Cam kết, Hành vi chuẩn mực, Hành vi không chấp nhận, Cơ chế thực thi.
- **Thông tin điền:** email báo cáo `admin-project@email.com` (giữ theo khung mẫu).

### Bước 4 — `SECURITY.md` (Chính sách bảo mật)

- **Yêu cầu:** Hướng dẫn báo cáo lỗ hổng riêng tư (không mở Issue công khai), bảng phiên bản hỗ trợ, cam kết phản hồi 48h.
- **Thực hiện:** Tạo 3 mục, gồm bảng Supported Versions (`v2.x.x`, `v1.5.x`, `< v1.4.0`).
- **Thông tin điền:** email `security-report@yourdomain.com` (giữ theo khung mẫu — nên đổi thành email thật khi triển khai).

### Bước 5 — `.github/ISSUE_TEMPLATE/bug_report.yml` (Issue Form)

- **Yêu cầu:** Biểu mẫu YAML chuẩn GitHub Issue Forms, tự hiện khi bấm **New Issue**.
- **Thực hiện:** Tạo đúng đường dẫn thư mục ẩn; nội dung gồm:
  - `name`, `description`, `title: "[BUG]: ..."`, `labels: ["type/bug", "triage-needed"]`.
  - Các trường bắt buộc: `bug-description`, `steps-to-reproduce`, `operating-system` (dropdown 3 hệ điều hành).
- **Kiểm tra cấu trúc:** Đã xác nhận các field id và thuộc tính `validations.required: true`.

### Bước 6 — `.github/PULL_REQUEST_TEMPLATE.md` (PR Template)

- **Yêu cầu:** Biểu mẫu tự hiện khi mở Pull Request, gồm 4 phần: Tổng quan, Thay đổi chi tiết, Hướng dẫn kiểm thử, Checklist tác giả.
- **Thực hiện:** Tạo đúng tên viết hoa `PULL_REQUEST_TEMPLATE.md` trong thư mục `.github/`, giữ nguyên checklist 4 ô `[ ]`.

---

## 3. Cấu trúc thư mục dự án hoàn chỉnh (thực tế)

```text
oss (Root)
├── .github/
│   ├── ISSUE_TEMPLATE/
│   │   └── bug_report.yml          ✅ Biểu mẫu báo lỗi tự động
│   └── PULL_REQUEST_TEMPLATE.md    ✅ Biểu mẫu kiểm duyệt code tự động
├── CODE_OF_CONDUCT.md              ✅ Luật ứng xử văn minh
├── CONTRIBUTING.md                 ✅ Cẩm nang hướng dẫn viết code
├── LICENSE                         ✅ Giấy phép bản quyền MIT
├── README.md                       ✅ Mặt tiền trang chủ dự án
├── SECURITY.md                     ✅ Chính sách bảo mật riêng tư
└── lab_guide_standardizing_oss_community_profile.md   (tài liệu gốc)
```

Lệnh kiểm tra đã chạy:

```bash
find . -type f -not -path './.git/*' | sort
```

---

## 4. Phần cần thực hiện trên giao diện GitHub (chưa tự động hóa được)

Các thao tác sau bắt buộc phải làm trên Web GitHub và cần tài khoản/quyền truy cập, nên **chưa được thực thi** trong môi trường này:

- [ ] Tạo repository cá nhân trên GitHub và push 7 tệp tin vừa tạo lên nhánh `main`:
  ```bash
  git init
  git add .
  git commit -m "docs: add OSS community profile files"
  git branch -M main
  git remote add origin <repo-url>
  git push -u origin main
  ```
- [ ] (Tùy chọn) Tạo `LICENSE` bằng nút **Choose a license template** để GitHub tự điền metadata giấy phép.
- [ ] Mở tab **Issues ➔ New Issue** để xác nhận biểu mẫu Bug Report tự hiện.
- [ ] Mở thử một Pull Request để xác nhận `PULL_REQUEST_TEMPLATE.md` tự hiện.
- [ ] Kiểm tra **Community Profile** (Insights ➔ Community Standards) đạt **100% – màu xanh lá**.
- [ ] Chụp màn hình minh chứng các bước và dán kèm link repo theo yêu cầu phần "BÁO CÁO THỰC HÀNH".

---

## 5. Ghi chú

- Nội dung tất cả tệp tin được sao chép **nguyên văn** từ khung chuẩn trong tài liệu, chỉ thay các giá trị điền được (`LICENSE` năm + tên).
- Hai email trong khung mẫu (`admin-project@email.com`, `security-report@yourdomain.com`) là placeholder — nên cập nhật email thật trước khi công bố dự án.
- Môi trường hiện tại không có trình phân tích YAML (`pyyaml`/`ruby`), nên `bug_report.yml` được kiểm tra bằng đối chiếu cấu trúc schema GitHub Issue Forms thay vì parse tự động. Nội dung trùng khớp 100% với mẫu chuẩn trong tài liệu.
