# AirPlay Server VI — bản Việt hóa dành cho ZEUS H01

Dự án Việt hóa [AirPlay Server](https://github.com/jqssun/android-airplay-server) theo mã nguồn gốc **v0.0.30**, giấy phép **GPL-3.0**.

- Thiết bị mục tiêu: ZEUS H01 / GlocalMe K1 — Android 8.1 (API 27), Qualcomm MSM8909, ARM32 (armeabi-v7a).
- Phạm vi thay đổi: giao diện tiếng Việt (145 chuỗi và 5 mục danh sách). **Không sửa thuật toán AirPlay, Bluetooth, audio, mạng hoặc firmware.**
- Bản phát triển thử nghiệm dùng `applicationIdSuffix = ".vi"` để cài riêng cạnh bản AirPlay Server gốc. **Không mở hai bản cùng lúc**, do chúng cùng cung cấp dịch vụ AirPlay và có thể tranh chấp cổng mạng.
- Chỉ sử dụng APK tạo bởi workflow sau khi báo trạng thái **Success**. Chưa xác nhận chạy trên H01 cho đến khi thử thực tế.

## Build APK trên GitHub Actions

1. Mở tab **Actions** của repo, chọn **Build AirPlay Server VI (H01)**.
2. Chọn **Run workflow**, hoặc xem lượt chạy tự động khi thay đổi workflow/bản dịch.
3. Khi job hoàn tất xanh, mở run → **Artifacts** → tải `AirPlay_Server_VI_H01_APK`.
4. Giải nén, lấy `app-debug.apk` hoặc `AirPlay_Server_VI_H01.apk`, chép sang H01 để thử.

APK debug được ký bằng khóa debug của GitHub runner, không phải chữ ký của upstream. Số lượng ABI được giới hạn còn **armeabi-v7a** trong bản test.

**Sao lưu dữ liệu, giữ nguyên APK gốc và thử phản chiếu từ iPhone trước.** Nếu bản Việt hóa hoạt động, có thể nghiên cứu phát hành APK với khóa ký ổn định.

## Nguồn, ghi nhận và giấy phép

- Mã nguồn gốc: https://github.com/jqssun/android-airplay-server (tag v0.0.30)
- Giấy phép gốc: https://github.com/jqssun/android-airplay-server/blob/v0.0.30/LICENSE
- Phần dịch tiếng Việt: `translations/strings_vi.xml`
- GitHub Actions tự tải mã nguồn gốc cùng các submodule, thay thế giao diện ngôn ngữ và build bằng Gradle.
- Bản điều chỉnh nguồn là dẫn xuất theo **GPL-3.0**; giữ các thông báo nguồn gốc và cung cấp mã nguồn tương ứng.

© Phần dịch tiếng Việt, 2026. Không liên kết với Apple.
