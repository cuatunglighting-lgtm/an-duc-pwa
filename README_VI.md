# AN ĐỨC – PWA Android + iPhone

## Mục tiêu
Bộ này tạo một **lớp PWA tĩnh** có icon AN ĐỨC chuẩn và nhúng Web App Apps Script hiện tại bên trong. Không sửa nghiệp vụ, đăng nhập, Google Sheets hoặc các hàm `google.script.run` của hệ thống hiện tại.

## Trước khi triển khai
Mở `config.js` và thay:

`PASTE_YOUR_APPS_SCRIPT_WEB_APP_EXEC_URL_HERE`

bằng URL Web App đang chạy, ví dụ:

`https://script.google.com/macros/s/DEPLOYMENT_ID/exec`

Dùng URL `/exec`, không dùng `/dev`.

## Hosting
Đưa toàn bộ thư mục này lên một static host HTTPS. GitHub Pages là lựa chọn đơn giản. Sau khi publish, mở URL của PWA bằng Chrome (Android) hoặc Safari (iPhone).

## Android
Chrome → mở URL PWA → menu ⋮ → **Thêm vào màn hình chính** / **Cài đặt ứng dụng**.

## iPhone
Safari → mở URL PWA → **Chia sẻ** → **Thêm vào Màn hình chính**.

## Backend Apps Script
Code.gs hiện tại đã có `setXFrameOptionsMode(HtmlService.XFrameOptionsMode.ALLOWALL)`, nên Web App có thể được nhúng bởi lớp PWA này. Không thêm `setFaviconUrl()`.

## Quan trọng
PNG trong thư mục `./` được phục vụ trực tiếp từ static host HTTPS. Google Drive chỉ giữ bản gốc, không được dùng làm nguồn icon runtime.


## BACKEND ĐÃ CẤU HÌNH
URL Apps Script /exec:
https://script.google.com/macros/s/AKfycbxDKM-6FmrqYXFJJukWuQzC2DF0YpTpx2o9GjAARXRVkCFPEThjmM1rKIyLZmgRubA/exec
