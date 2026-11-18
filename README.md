# Định dạng văn bản hành chính — Phiên bản 2

Ứng dụng web của **Tổ Chuyển đổi số Trường Đại học Tiền Giang**, dùng để trình bày lại thể thức một văn bản Word (.docx) theo:

- **Nghị định 30/2020/NĐ-CP** về công tác văn thư (văn bản hành chính);
- **Hướng dẫn 05-HD/VPTW ngày 27/5/2026** của Văn phòng Trung ương Đảng về thể thức và kỹ thuật trình bày văn bản của Đảng (thay Hướng dẫn 36-HD/VPTW).

> Bản thử nghiệm. Văn bản xuất ra cần người soạn rà soát lại trước khi trình ký.

## Có gì mới ở phiên bản 2

- **Bộ thể thức văn bản của Đảng**: tiêu đề “ĐẢNG CỘNG SẢN VIỆT NAM”, dấu sao dưới tên cơ quan, số ký hiệu dạng `Số 05-CV/ĐU`, trích yếu công văn in nghiêng cỡ 12, dòng `-----` dưới trích yếu, quyền hạn ký T/M, K/T, T/L, “Nơi nhận” gạch chân, giãn dòng Exactly 18–22 pt. Văn bản có tiêu đề Đảng được tự chuyển sang bộ thể thức này.
- **Kiểm tra chính tả**: phát hiện từ ghép vần sai (ví dụ “nghành”), dấu thanh đặt sai chỗ (“qủa”), lỗi thường gặp (“sử lý”, “đề suất”), viết hoa sai theo Phụ lục II NĐ 30 (“Ủy Ban Nhân Dân”), lặp từ (“của của”), thiếu khoảng trắng sau dấu câu. Có nút **Sửa**, **Bỏ qua** và **Sửa tất cả**.
- Logo Trường ở đầu trang.

## Tính năng

- Tải lên file **.docx**. File được xử lý ngay trên trình duyệt, **không gửi lên máy chủ nào**.
- Tự nhận diện các thành phần thể thức: tên cơ quan chủ quản và cơ quan ban hành, số ký hiệu, địa danh và ngày tháng, tên loại, trích yếu, kính gửi, nội dung, quyền hạn và chức vụ người ký, họ tên người ký, nơi nhận.
- Đọc được cả văn bản trình bày phần đầu và phần chữ ký bằng bảng hoặc bằng phím Tab.
- Có ô để sửa từng thành phần và bản xem trước khổ A4.
- Tự chuẩn hóa:
  - thêm số 0 cho ngày dưới 10 và tháng 1, 2;
  - viết số ký hiệu liền, không có khoảng trắng thừa;
  - thêm dấu “-” ở đầu và dấu “;” hoặc “.” ở cuối các dòng kính gửi, nơi nhận;
  - bỏ khoảng trắng thừa và khoảng trắng đứng trước dấu câu.
- Kiểm tra và báo các thành phần còn thiếu hoặc chưa đúng dạng.
- Xuất file **.docx**: khổ A4, chữ Times New Roman, lề và cỡ chữ theo NĐ 30, có đường kẻ dưới tên cơ quan và tiêu ngữ, đánh số trang ở giữa phía trên và bỏ số ở trang đầu.

## Cách dùng

1. Mở trang web.
2. Kéo thả file .docx vào, hoặc bấm “Thử với công văn mẫu”.
3. Kiểm tra và sửa các ô bên trái nếu nhận diện sai.
4. Bấm **Tải về .docx**.

## Hạn chế hiện tại

- Chưa giữ được hình ảnh, chú thích cuối trang và số thứ tự đánh tự động.
- Bảng có ô gộp có thể bị lệch.
- Chưa hỗ trợ file .doc cũ (mở bằng Word rồi lưu lại thành .docx).
- Kiểm tra chính tả dựa trên quy tắc và danh sách lỗi thường gặp, không phải từ điển đầy đủ: không bắt được từ đúng chính tả nhưng dùng sai nghĩa.

## Cấu trúc

```
index.html          giao diện và toàn bộ xử lý
assets/logo-tgu.svg logo Trường Đại học Tiền Giang
lib/docx.iife.js    thư viện docx (giấy phép MIT), dùng để tạo file .docx
lib/jszip.min.js    thư viện JSZip (giấy phép MIT hoặc GPLv3), dùng để đọc file .docx
```

Đây là trang tĩnh, không cần máy chủ xử lý. Có thể chạy trên GitHub Pages hoặc bất kỳ web server nào.
