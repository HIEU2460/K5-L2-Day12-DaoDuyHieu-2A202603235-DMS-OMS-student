# Tự đánh giá — Đào Duy Hiếu · G10

## 1. Tự rà soát 4 cảnh

| Ảnh | Đối tượng | Loại lỗi | Ghi chú | Đã sửa? |
|---|---|---|---|---|
| S01_rgb.png | các đối tượng OMS | ok | Kiểm tra lại tên ghế theo phía của xe và `frame_meta` | Có |
| S02_ir.png | child_seat | wrong_class | Ban đầu đặt `occupied=yes`, trong khi guideline yêu cầu `unknown` hoặc `no` | Có |
| D02.png | frame_meta | missing | Checkpoint B phát hiện thiếu tag `frame_meta` | Có |
| D05.png | face13 / eye_left | flag | Trạng thái mắt và cờ `occluded` khác với bản review chéo | Giữ nguyên và ghi giải thích |

## 2. Lỗi mình lặp lại nhiều nhất hôm nay

Lỗi: Chọn thuộc tính theo suy đoán thay vì giới hạn giá trị của guideline.

Vì sao mình mắc: Một số chi tiết trên ảnh IR khó nhìn rõ nên dễ chọn giá trị quá chắc chắn.

Lần sau tránh bằng cách: Kiểm tra lại guideline và dùng `unknown` khi bằng chứng hình ảnh không đủ rõ trước khi chuyển sang ảnh tiếp theo.

## 3. Ghi chú về disagreement_log

Bản review chéo cho thấy trạng thái mắt và cờ điểm phải được xét cùng nhau. Mình học được rằng cần ghi rõ lý do khi giữ một nhãn khác với bạn review và đưa ca guideline chưa rõ cho coach xác nhận.
