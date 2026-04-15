[![Open in Visual Studio Code](https://classroom.github.com/assets/open-in-vscode-2e0aaae1b6195c2367325f4f02e2d04e9abb55f0b24a779b69b11b9e10269abc.svg)](https://classroom.github.com/online_ide?assignment_repo_id=23572376&assignment_repo_type=AssignmentRepo)
# Day 10 Lab: Data Pipeline & Data Observability

**Student ID:** 2A202600501
**Student Email:** 26ai.tutn@vinuni.edu.vn
**Name:** Trịnh Ngọc Tú

---

## Mo ta

Bài lab này xây dựng một pipeline ETL tự động để xử lý dữ liệu sản phẩm từ file JSON, bao gồm các bước Extract, Validate, Transform và Load. Ngoài ra, tôi đã thực hiện thí nghiệm để chứng minh tác động của chất lượng dữ liệu đến độ chính xác của AI agent, so sánh kết quả khi sử dụng dữ liệu sạch và dữ liệu rác.

---

## Cach chay (How to Run)

### Prerequisites
```bash
pip install pandas
```

### Chay ETL Pipeline
```bash
python solution.py
```

### Chay Agent Simulation (Stress Test)
```bash
# Mo ta cach ban chay thi nghiem Clean vs Garbage data
python agent_simulation.py
Kiểm tra kết quả nhận được ở terminal
```

---

## Cau truc thu muc

```
├── solution.py              # ETL Pipeline script
├── processed_data.csv       # Output cua pipeline
├── experiment_report.md     # Bao cao thi nghiem
└── README.md                # File nay
```

---

## Ket qua

Pipeline đã xử lý tổng cộng 5 records từ raw_data.json. Trong đó, 3 records hợp lệ được lưu vào processed_data.csv, và 2 records bị loại (1 record có giá âm, 1 record có category rỗng). Thí nghiệm agent simulation cho thấy dữ liệu sạch dẫn đến kết quả chính xác hơn so với dữ liệu rác.
