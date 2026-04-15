# Experiment Report: Data Quality Impact on AI Agent

**Student ID:** 2A202600501
**Name:** Trịnh Ngọc Tú
**Date:** 14/04/2026

---

## 1. Ket qua thi nghiem

Chay `agent_simulation.py` voi 2 bo du lieu va ghi lai ket qua:

| Scenario | Agent Response | Accuracy (1-10) | Notes |
|----------|----------------|-----------------|-------|
| Clean Data (`processed_data.csv`) | Based on my data, the best choice is Laptop at $1200 | | |
| Garbage Data (`garbage_data.csv`) | Based on my data, the best choice is Nuclear Reactor at $999999 | | |

---

## 2. Phan tich & nhan xet

### Tại sao Agent trả lời sai khi dùng Garbage Data?

Agent trả lời sai khi dùng garbage data vì dữ liệu bị hỏng làm ảnh hưởng đến cả cách tạo đầu vào và cách mô hình hiệu chỉnh kết quả. Duplicate IDs có thể làm sai lệch trong tính toán doanh số.
Wrong data types làm không thể so sánh và sắp xếp chính xác.
Outliers làm giá trị không hợp lệ vượt xa mức bình thường.
Null values khiến thông tin thiếu nghĩa.
Khi dữ liệu không sạch, agent nhầm lẫn thông tin và đưa ra giải pháp sai vì nó xem dữ liệu là hợp lệ và có thể là dấu hiệu quan trọng. Các vấn đề như ID trùng lặp, kiểu dữ liệu sai, giá trị ngoại lệ và giá trị null đều góp phần làm giảm độ tin cậy của kết quả AI, dẫn đến quyết định sai lầm trong phân tích dữ liệu.

(Hãy phân tích các vấn đề như Duplicate IDs, wrong data types, outliers, null values
và giải thích tại sao chúng ảnh hưởng đến kết quả của Agent.)

---

## 3. Ket luan

**Quality Data > Quality Prompt?** (Dong y hay khong? Giai thich ngan gon.)

Đồng ý. Dữ liệu chất lượng cao quan trọng hơn prompt tốt vì dữ liệu sai sẽ làm mô hình AI đưa ra kết quả không chính xác, ngay cả khi prompt được thiết kế kỹ lưỡng. Việc xử lý dữ liệu đúng từ đầu đảm bảo độ tin cậy của kết quả hơn là chỉ dựa vào prompt.
