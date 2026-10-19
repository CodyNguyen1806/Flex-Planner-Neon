FLEX PLANNER NEON — BẢN ĐỘC LẬP · GitHub Pages
================================================
TẤT CẢ FILE CHO MỘT REPOSITORY GITHUB MỚI:
- index.html                 ứng dụng đầy đủ; đã tích hợp CSS dark mode
- manifest.webmanifest       cấu hình PWA riêng
- sw.js                     offline service worker với cache riêng
- icon-192.png / icon-512.png  icon PWA

CÀI ĐẶT:
1. Tạo repository GitHub MỚI, ví dụ flex-planner-neon.
2. Upload toàn bộ file trong ZIP trực tiếp vào THƯ MỤC GỐC (không tạo thư mục con).
3. Settings > Pages > Deploy from a branch > main / (root).
4. Mở https://<ten-github>.github.io/flex-planner-neon/
5. Trên iPhone dùng Safari > Add to Home Screen; Samsung dùng Chrome > Install app.

QUAN TRỌNG — AN TOÀN DỮ LIỆU:
- Bản này dùng localStorage keys tiền tố flex-neon-independent-v1::.
- Không tự đọc / ghi dữ liệu của Flex Rolling 7 Days bản gốc trên GitHub Pages.
- Bản gốc có dữ liệu mẫu khởi đầu. Bản Neon cũng giữ nguyên chế độ mẫu đó.
- Khi mới mở, ứng dụng mới có dữ liệu độc lập. Muốn chuyển dữ liệu, hãy XUẤT Backup JSON từ bản gốc, rồi NHẬP Backup JSON vào bản Neon.
- Trước khi nhập dữ liệu, lưu bản backup dự phòng.
- Supabase chỉ kết nối nếu tự cài cấu hình; không tự đồng bộ với bản gốc.
- Service worker có cache name riêng; không xóa cache của bản gốc.

GIỮ NGUYÊN TOÀN BỘ CHỨC NĂNG (mã nguồn gốc 18/10):
- Rolling 7 Days, 40h, reserve, IO, tự chuyển ngày, OUT, 14-day forecast;
- upload Schedule/Earnings, review, OCR, history, mark reserve, undo;
- income Paid, Tips pending, Base, Tips, Adjustment, Additional Tips, Healthcare;
- chống nhập trùng, xóa từng ngày/từng chuyến/xóa toàn bộ, Backup JSON;
- Healthcare Q4 / as-of / ngày nghỉ / Buffer / EST.

CHỈ thay đổi: CSS, tiêu đề / menu điều hướng, vị trí hiển thị các phần,
phân vùng localStorage và tên PWA/cache độc lập. KHÔNG thay thuật toán tính.

LƯU Ý: không thêm tính năng mới giả định có dữ liệu Amazon trực tiếp.
Các số trong ảnh thiết kế là minh họa. Giá trị khi chạy lấy từ dữ liệu
của chính thiết bị hoặc Backup JSON của bạn.
