# Danh sách lớp v0 — Đào Duy Hiếu · G10

## DMS (ít nhất 6 lớp)

| # | Lớp / thuộc tính | Giá trị | Để làm gì (chức năng DMS) | Nhìn thấy được trên IR? |
|---|---|---|---|---|
| 1 | eye_left / eye_right | open / closed / unknown | Phát hiện buồn ngủ hoặc nhắm mắt kéo dài | Có, trừ khi mắt bị che hoặc kính phản xạ |
| 2 | gaze_zone | road / mirror_l / mirror_r / mirror_c / cluster / center / lap / other | Phát hiện tài xế mất tập trung và không nhìn đường | Có |
| 3 | glasses | none / clear / sun / unknown | Đánh giá độ tin cậy khi nhận dạng mắt và vùng nhìn | Có, nhưng loại kính có thể khó phân biệt |
| 4 | hand.on_wheel | yes / no / unknown | Xác định tài xế có kiểm soát vô lăng hay không | Có |
| 5 | phone.state | held / mounted / lap | Phát hiện hành vi sử dụng điện thoại gây xao nhãng | Có nếu điện thoại hiện rõ |
| 6 | person.seatbelt | worn_correct / worn_incorrect / not_worn / unknown | Cảnh báo tài xế không thắt hoặc thắt sai dây an toàn | Có, nhưng có thể khó thấy trên quần áo tối |

## OMS (ít nhất 6 lớp)

| # | Lớp / thuộc tính | Giá trị | Để làm gì (chức năng OMS) | Nhìn thấy được trên IR? |
|---|---|---|---|---|
| 1 | person.seat | front_passenger / rear_left / rear_middle / rear_right | Xác định vị trí hành khách để điều khiển cảnh báo và túi khí | Có |
| 2 | person.seatbelt | not_worn / unknown | Cảnh báo hành khách chưa thắt dây an toàn | Có thể thấy, nhưng thường khó trên IR |
| 3 | child_seat | có / không theo ghế | Phát hiện ghế trẻ em và hỗ trợ bảo vệ trẻ | Có qua hình dạng |
| 4 | child_seat.occupied | no / unknown | Xác định khả năng ghế trẻ em đang có người sử dụng | Có, nhưng khi bị che nên dùng unknown |
| 5 | infant_seat.facing | rear / front | Kiểm tra hướng lắp ghế em bé và điều kiện an toàn túi khí | Có qua hình dạng |
| 6 | object.type | bag / box / cup / other | Phân biệt đồ vật với hành khách và phát hiện đồ để quên | Có, nhưng màu sắc không xác định được |

## 2 câu hỏi leo thang

1. Câu hỏi: Khi nhìn thấy mí mắt khép nhưng các mốc mắt khó xác định, có nên đặt `eye_left=closed` đồng thời bật `occluded` cho các điểm mắt không?
   Khung ví dụ: D05.png
   Bạn tạm gán thế nào và vì sao: Giữ `closed` vì quan sát thấy mí mắt khép; đánh dấu ca này cần coach xác nhận quy tắc cờ điểm.
2. Câu hỏi: Khi ảnh IR-sim không đủ rõ để xác định ghế trẻ em có người ngồi, nên ưu tiên thuộc tính nào?
   Khung ví dụ: S02_ir.png
   Bạn tạm gán thế nào và vì sao: Chọn `unknown`, vì guideline không cho phép đoán từ ảnh RGB hoặc từ hình dạng không rõ.
