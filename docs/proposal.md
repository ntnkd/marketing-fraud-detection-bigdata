# PROJECT PROPOSAL  
## Marketing Campaign Analysis & Click Fraud Detection using Big Data (Spark-based)

---

## 1. Bối cảnh & Bài toán

Các nền tảng quảng cáo trực tuyến như Facebook Ads, Google Ads tạo ra hàng triệu bản ghi click mỗi ngày. Doanh nghiệp thường trả tiền theo mô hình CPC (Cost Per Click), nghĩa là trả tiền cho mỗi lượt click vào quảng cáo.

Tuy nhiên, không phải mọi click đều đến từ người dùng thật. Một phần đáng kể có thể đến từ:

- Bot tự động
- Click farm
- Hành vi spam

Click ảo gây ra:

- Lãng phí ngân sách quảng cáo
- Sai lệch chỉ số hiệu quả chiến dịch
- Quyết định marketing không chính xác

Do khối lượng dữ liệu rất lớn, cần xây dựng một hệ thống Big Data để xử lý và phát hiện gian lận một cách hiệu quả.

---

## 2. Mục tiêu đề tài

### Mục tiêu chính

1. Xây dựng hệ thống xử lý dữ liệu click quy mô lớn bằng Apache Spark.
2. Phân tích hiệu quả chiến dịch marketing.
3. Phát hiện click ảo bằng Machine Learning.

### Mục tiêu cụ thể

- Lưu trữ dữ liệu lớn bằng HDFS.
- Thực hiện ETL và làm sạch dữ liệu bằng Spark.
- Phân tích hiệu quả theo channel, app, device.
- Trích xuất đặc trưng hành vi.
- Huấn luyện mô hình phân loại bằng Spark MLlib.
- Tạo báo cáo phục vụ quyết định kinh doanh.

---

## 3. Input & Output hệ thống

### Input

Dataset TalkingData AdTracking Fraud Detection gồm:

- ip
- app
- device
- os
- channel
- click_time
- is_attributed 

Dữ liệu được lưu trữ trên HDFS.

---

### Output

- Kết quả phân loại click thật / click ảo
- Tỷ lệ gian lận theo channel
- Danh sách IP nghi ngờ
- So sánh hiệu quả marketing trước và sau khi lọc click ảo
- Báo cáo và biểu đồ phân tích

---

## 4. Công nghệ sử dụng

- Hadoop (HDFS)
- Apache Spark
- Spark MLlib
- Python (PySpark)
- Định dạng Parquet

---

## 5. Phạm vi & Giới hạn

### Bao gồm

- Xử lý dữ liệu phân tán
- Phân tích marketing
- Machine Learning phân loại

### Không bao gồm

- Streaming real-time
- Kafka
- Triển khai production
- Xây dựng Web App

Đề tài tập trung vào xử lý Big Data offline.

---

## 6. Kết quả mong đợi

Hệ thống giúp:

- Xác định channel quảng cáo hiệu quả
- Phát hiện channel có dấu hiệu gian lận
- Đề xuất tối ưu ngân sách marketing