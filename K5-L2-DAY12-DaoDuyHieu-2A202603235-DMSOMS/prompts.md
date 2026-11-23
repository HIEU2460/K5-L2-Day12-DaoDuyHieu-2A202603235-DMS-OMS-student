# Khai báo dùng AI — Đào Duy Hiếu

| # | Công cụ | Bạn hỏi gì (tóm tắt) | Bạn dùng kết quả thế nào | Bạn có kiểm lại không? Bằng gì? |
|---|---|---|---|---|
| 1 | ChatGPT/Codex | Đọc project và xác định các sản phẩm E1–E5 cần nộp | Lập checklist thực hiện và đóng gói bài | Có; đối chiếu README, GUIDE, SUBMISSION và RUBRIC |
| 2 | ChatGPT/Codex | Kiểm tra cấu trúc các file export CVAT | Xác nhận đúng định dạng CVAT for images 1.1, đủ 22 ảnh và không kèm ảnh | Có; chạy `zipfile` và `cabin_check.py` |
| 3 | ChatGPT/Codex | Tạo checkpoint A/B và kiểm tra bản final | Tạo `check_cpA.txt`, `check_cpB.txt`, `check_final.txt` | Có; đọc lại số ảnh, ERROR và WARN trong từng file |
| 4 | ChatGPT/Codex | So sánh export của mình với export review chéo | Tạo `disagreement_log.csv` và xác định 5 bất đồng ở D05 | Có; đối chiếu GUIDE §4.5–4.6 và giữ ca chưa rõ để hỏi coach |
| 5 | ChatGPT/Codex | Góp ý câu chữ cho class list và self-review | Hoàn thiện bản nháp các báo cáo | Có; tự đọc lại và đối chiếu với nhãn đã dùng |

Không cung cấp ảnh cabin hoặc ảnh tài xế cho AI; công cụ chỉ đọc tài liệu, metadata và dữ liệu annotation.
