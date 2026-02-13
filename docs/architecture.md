# SYSTEM ARCHITECTURE  
## Marketing Campaign Analysis & Click Fraud Detection (Spark-based)

---

## 1. Tổng quan kiến trúc

Hệ thống được thiết kế theo mô hình Big Data phân tán, tách biệt giữa lưu trữ và xử lý.

TalkingData Dataset (CSV)
        ↓
HDFS (Lưu trữ phân tán)
        ↓
Apache Spark (ETL & Phân tích)
        ↓
Feature Engineering
        ↓
Spark MLlib (Phát hiện gian lận)
        ↓
Reporting & Visualization

---

## 2. Các tầng kiến trúc

### 2.1 Nguồn dữ liệu

- Dataset TalkingData (offline)
- Hàng triệu bản ghi click

---

### 2.2 Tầng lưu trữ – HDFS

- Lưu trữ dữ liệu lớn
- Chia file thành block
- Hỗ trợ xử lý phân tán
- Tách biệt storage và processing

---

### 2.3 Tầng xử lý – Apache Spark

Spark thực hiện:

- Làm sạch dữ liệu (ETL)
- Chuẩn hóa dữ liệu
- Phân tích marketing
- Thống kê và tổng hợp

Xử lý phân tán trên nhiều core.

---

### 2.4 Feature Engineering

Tạo đặc trưng mới:

- Click/IP/phút
- Khoảng thời gian giữa các click
- Encoding biến phân loại

Chuẩn bị dữ liệu cho Machine Learning.

---

### 2.5 Machine Learning – Spark MLlib

Sử dụng:

- Logistic Regression
- Random Forest

Bài toán:

- Phân loại click thật / click ảo

---

### 2.6 Reporting

Xuất kết quả:

- Tỷ lệ click ảo
- Channel gian lận cao
- IP nghi ngờ
- Biểu đồ phân tích

Định dạng:

- Parquet
- CSV
- Dashboard offline

---

## 3. Nguyên tắc thiết kế

- Xử lý phân tán
- Có khả năng mở rộng
- Tách biệt các tầng
- Phù hợp xử lý Big Data offline