# Báo cáo thực hành: chuẩn hóa hồ sơ cộng đồng dự án OSS

- Ngày thực hiện: 28/09/2026
- Repo: https://github.com/nv-hoai/oss (public, nhánh mặc định `main`)

## Tóm tắt

Repo `oss` đã có đủ bộ hồ sơ cộng đồng theo yêu cầu: `LICENSE`, `CONTRIBUTING.md`, `CODE_OF_CONDUCT.md`, `SECURITY.md`, `README.md`, và hai mẫu tự động nằm trong thư mục `.github` là `ISSUE_TEMPLATE/bug_report.yml` với `PULL_REQUEST_TEMPLATE.md`. Toàn bộ đã được commit và push lên nhánh `main`.

## Chi tiết từng file

### LICENSE

Dùng giấy phép MIT. Mình ghi năm 2026 và tên người giữ bản quyền là Nguyen Hoai, lấy theo git config trên máy (nếu muốn tên khác chỉ cần sửa lại dòng Copyright).

### CONTRIBUTING.md

Giữ đúng khung trong đề bài: quy trình fork repo, tạo nhánh `feat/...`, commit theo Conventional Commits rồi mở PR về `main`; phần quy chuẩn code nhắc viết C với 4 khoảng trắng, đặt tên `snake_case` và bắt buộc có comment mô tả cho hàm mới.

### CODE_OF_CONDUCT.md

Viết theo tinh thần Contributor Covenant, chia làm 4 phần: cam kết, hành vi nên làm, hành vi không chấp nhận, và cách xử lý khi có vi phạm. Email nhận báo cáo tạm để theo mẫu là `admin-project@email.com`.

### SECURITY.md

Hướng dẫn báo lỗ hổng riêng tư thay vì mở Issue công khai, kèm bảng các phiên bản còn được hỗ trợ (`v2.x.x`, `v1.5.x`, và các bản cũ hơn `< v1.4.0`) và cam kết phản hồi trong 48 giờ. Email tạm để theo mẫu là `security-report@yourdomain.com`.

### .github/ISSUE_TEMPLATE/bug_report.yml

Biểu mẫu dạng YAML của GitHub Issue Forms, tự hiện khi bấm New Issue. Có tiêu đề `[BUG]`, nhãn `type/bug` và `triage-needed`, cùng 3 trường bắt buộc: mô tả lỗi, các bước tái hiện, và chọn hệ điều hành.

### .github/PULL_REQUEST_TEMPLATE.md

Mẫu PR gồm 4 phần: tổng quan thay đổi, danh sách thay đổi chi tiết, hướng dẫn kiểm thử, và checklist để tác giả tự tick trước khi gửi.

### README.md

Trang chủ liệt kê các file hồ sơ cộng đồng kèm liên kết tới từng file.

## Cấu trúc repo sau khi hoàn thành

```text
oss
├── .github/
│   ├── ISSUE_TEMPLATE/
│   │   └── bug_report.yml
│   └── PULL_REQUEST_TEMPLATE.md
├── screenshots/
│   ├── 01-repo-overview.png
│   ├── 02-license.png
│   ├── 03-contributing.png
│   ├── 04-code-of-conduct.png
│   ├── 05-security-policy.png
│   ├── 06-issue-template.png
│   ├── 07-pr-template.png
│   ├── 08-community-standards.png
│   └── 09-github-tree.png
├── BAO_CAO_THUC_HANH.md
├── CODE_OF_CONDUCT.md
├── CONTRIBUTING.md
├── LICENSE
├── README.md
└── SECURITY.md
```

## Ảnh chụp màn hình

Mấy ảnh dưới được chụp trực tiếp từ repo đang chạy, lưu trong thư mục `screenshots/`.

- `01-repo-overview.png`: trang chủ repo, thấy đủ các file và badge MIT license / Code of conduct / Contributing / Security policy.
- `02-license.png`: nội dung `LICENSE`.
- `03-contributing.png`: nội dung `CONTRIBUTING.md`.
- `04-code-of-conduct.png`: nội dung `CODE_OF_CONDUCT.md`.
- `05-security-policy.png`: nội dung `SECURITY.md`.
- `06-issue-template.png`: file `bug_report.yml`.
- `07-pr-template.png`: file `PULL_REQUEST_TEMPLATE.md`.
- `08-community-standards.png`: trang Community Standards, cả 8 mục đều đã tick xanh.
- `09-github-tree.png`: cây thư mục `.github/` chứa cả hai mẫu.

![Trang chủ repo](screenshots/01-repo-overview.png)

![LICENSE](screenshots/02-license.png)

![CONTRIBUTING](screenshots/03-contributing.png)

![CODE_OF_CONDUCT](screenshots/04-code-of-conduct.png)

![SECURITY](screenshots/05-security-policy.png)

![Issue template](screenshots/06-issue-template.png)

![PR template](screenshots/07-pr-template.png)

![Community Standards](screenshots/08-community-standards.png)

![Cây thư mục .github](screenshots/09-github-tree.png)
