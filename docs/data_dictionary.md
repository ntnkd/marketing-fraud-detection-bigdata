# DATA DICTIONARY  
## TalkingData AdTracking Fraud Detection Dataset

---

## 1. Tổng quan Dataset

Dataset gồm hàng triệu bản ghi click quảng cáo.  
Mỗi dòng tương ứng với một sự kiện click.

Được sử dụng cho bài toán phát hiện click ảo.

---

## 2. Mô tả các cột

| Tên cột       | Kiểu dữ liệu | Mô tả |
|---------------|--------------|-------|
| ip            | Integer      | Địa chỉ IP của thiết bị |
| app           | Integer      | ID ứng dụng được quảng cáo |
| device        | Integer      | Loại thiết bị |
| os            | Integer      | Hệ điều hành |
| channel       | Integer      | Kênh quảng cáo |
| click_time    | Timestamp    | Thời điểm click |
| is_attributed | Integer      | Nhãn (1 = có chuyển đổi, 0 = không)|

---

## 3. Phân loại biến

### Nhãn (Label)

- is_attributed
  - 1: Click dẫn đến hành động thật
  - 0: Không có chuyển đổi

Dùng cho bài toán phân loại nhị phân.

---

### Biến hành vi

- ip
- app
- device
- os
- channel
- click_time

Dùng để:

- Phân tích hiệu quả marketing
- Phát hiện bất thường
- Tạo feature cho Machine Learning

---

## 4. Lý do chọn Dataset

- Quy mô lớn → phù hợp Big Data
- Có nhãn sẵn cho supervised learning
- Có thông tin thời gian để phân tích hành vi
- Phù hợp cả phân tích kinh doanh và phát hiện gian lận

---

## 5. Feature có thể tạo (ở các tuần sau)

- Số click/IP/phút
- Khoảng thời gian giữa các click
- Tần suất click theo device
- Tỷ lệ gian lận theo channel