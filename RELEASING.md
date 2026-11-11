# Phát hành LumePDF

1. Sửa `version` trong `Cargo.toml` và chạy `cargo check` để cập nhật `Cargo.lock`.
2. Từ thư mục mã nguồn trên Windows, chạy `pwsh -File release/Build-Package.ps1`. Script dùng hai bộ công cụ GNU trong `vendor`, Inno Setup 6, Python 3 và thư mục mẫu Mac của gói 1.0.0. Có thể chỉ đường dẫn khác bằng `-MacTemplate`, `-InnoSetup` và `-OutputRoot`.
3. Kiểm tra hai bộ cài Windows và chạy thử gói macOS nếu có máy Mac. Có thể thêm ghi chú bằng `release/LumePDF-<version>.release.md` trước khi đóng gói.
4. Đưa `LumePDF-<version>.zip`, `LumePDF-<version>.sha256`, ghi chú nếu có, và `release-version.txt` lên thư mục gốc nhánh `main` của `huypx92/LumePDF` trong cùng một commit. Có thể dùng **Add file → Upload files** trên GitHub. Workflow xác minh ZIP và SHA-256, rồi xuất bản release `v<version>` và đặt làm bản mới nhất. Xem **Actions → Publish LumePDF release** để kiểm tra.
5. Nút tải bản mới nhất trên Gumroad trỏ tới `https://github.com/huypx92/LumePDF/releases/latest` nên tự dẫn đến phiên bản mới. Muốn lưu thêm file trực tiếp trên Gumroad thì tải qua **Content** của sản phẩm hiện tại.

LumePDF 1.0.1 trở lên kiểm tra bản phát hành ổn định trên GitHub. Thông báo mở trang tải, còn người dùng chạy bộ cài cho hệ điều hành của họ.
