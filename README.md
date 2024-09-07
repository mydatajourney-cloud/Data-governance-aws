# Data Governance Fundamentals and on AWS

Nội dung ở đây tập trung vào lý thuyết về quản lý dữ liệu và các slide về data governance từ AWS, đặc biệt là dịch vụ **Data Lake Formation**.

## Table of Contents

1. [Data Governance là gì?](#1-data-governance-l%C3%A0-g%C3%AC)
2. [Lợi ích của Data Governance](#2-l%E1%BB%A3i-%C3%ADch-c%E1%BB%A7a-data-governance)
3. [Quy tắc chính của Data Governance](#3-quy-t%E1%BA%AFc-ch%C3%ADnh-c%E1%BB%A7a-data-governance)
4. [AWS và Quản lý Dữ liệu](#4-aws-v%C3%A0-qu%E1%BA%A3n-l%C3%BD-d%E1%BB%A5-li%E1%BB%87u)
5. [Thách thức trong việc xây dựng Data Lake với Data Governance](#5-th%C3%A1ch-th%E1%BB%A9c-trong-vi%E1%BB%87c-x%C3%A2y-d%E1%BB%B1ng-data-lake-v%E1%BB%9Bi-data-governance)

## 1. Data Governance là gì?

**Data Governance** là một yếu tố quan trọng khi làm việc với các nền tảng dữ liệu. Doanh nghiệp thường lãng phí thời gian quản lý dữ liệu để đảm bảo dữ liệu tin cậy và xác định quyền truy cập hợp lý nhằm tối ưu hóa hiệu quả BI và ngăn ngừa rò rỉ thông tin quan trọng như PII (Personally Identifiable Information).

## 2. Lợi ích của Data Governance

- **Bảo mật dữ liệu**: Bảo mật dữ liệu trong nội bộ công ty, giữa các phòng ban và từ bên ngoài. Chỉ những phòng ban được phép mới có quyền truy cập dữ liệu.
- **Đảm bảo tiêu chuẩn**: Giúp dữ liệu đáp ứng các tiêu chuẩn của công ty và quy định quốc gia.
- **Cải thiện chất lượng dữ liệu**: Đảm bảo dữ liệu chính xác và đáng tin cậy.
- **Đồng nhất dữ liệu**: Tránh sự không đồng nhất giữa các phòng ban.
- **Tăng tính tin cậy**: Nhờ vào các quy trình và quy tắc được triển khai.
- **Cải thiện phân tích và ra quyết định**: Hỗ trợ việc phân tích dữ liệu và đưa ra quyết định tốt hơn cho công ty.

## 3. Quy tắc chính của Data Governance

![Quy tắc chính của Data Governance](https://github.com/user-attachments/assets/edc67889-a75e-4c07-8104-54d222ed3db1)

- **“My data” → “Our data”**: Dữ liệu nên được chia sẻ giữa các phòng ban trong công ty, không chỉ riêng mỗi phòng ban. Tuy nhiên, cần thận trọng với dữ liệu nhạy cảm (ví dụ: dữ liệu phòng ban HR).
  - Cần có cấu trúc để chia sẻ dữ liệu theo nhu cầu phân tích và quyền truy cập.
- **Xác định trách nhiệm**: Trách nhiệm không chỉ thuộc về bộ phận IT mà còn các bộ phận khác. Mọi người cần biết dữ liệu nào có thể sử dụng và dữ liệu nào không.
- **Quản lý dữ liệu**: Đội quản lý dữ liệu cần làm việc với các bên trong và ngoài công ty để đảm bảo dữ liệu tuân thủ quy chuẩn.
- **Chất lượng dữ liệu**: Đảm bảo dữ liệu luôn chính xác để đưa ra quyết định đúng.

### Các tiêu chuẩn đánh giá

- **Accessibility**: Dữ liệu có được truy cập bởi đúng người không?
- **Accuracy**: Tính chính xác của dữ liệu.
- **Completeness**: Dữ liệu có đầy đủ không? Cần thu thập thêm không?
- **Consistency**: Dữ liệu có đồng nhất không?
- **Relevance**: Dữ liệu có được cập nhật không? Dữ liệu lưu trữ có cần thiết không? Có cần nén dữ liệu không?
- **Timeliness**: Dữ liệu có thể truy cập kịp thời không?
- **Uniqueness**: Dữ liệu có bị trùng lặp không? Nguồn dữ liệu có duy nhất không?

⇒ Khi xây dựng một chương trình quản lý dữ liệu, cần phải xem xét các vấn đề trong công ty và liên kết với các nguyên tắc trên.

Tìm hiểu thêm: [Defining Data Governance Core Principles – TDAN.com](https://tdan.com/defining-data-governance-core-principles/17087)

## 4. AWS và Quản lý Dữ liệu

![AWS Data Governance](https://github.com/user-attachments/assets/6fbfcb16-745f-4a44-a27f-2739f0fef8dc)

- AWS hỗ trợ việc quản lý bảo mật dữ liệu chủ yếu qua các dịch vụ như **CloudTrail**, **CloudWatch** và **Data Lake Formation**.

## 5. Thách thức trong việc xây dựng Data Lake với Data Governance

![Data Lake Challenges](https://github.com/user-attachments/assets/52b863c8-0245-4dca-bee6-405565e66b7b)

- **Data Lake** không chỉ là nơi lưu trữ tất cả dữ liệu mà còn cần đáp ứng nhu cầu phân tích. Dữ liệu trong Data Lake cần được phân chia và tổ chức theo mục tiêu của người sử dụng.
  
  - **Landing/Raw Zone**: Điểm đầu tiên quản lý dữ liệu ở định dạng gốc cho cả Batch và Streaming. Xác định thời gian lưu trữ dữ liệu.
  - **Standardized Zone**: Lớp biến đổi dữ liệu để đáp ứng các nhu cầu về hiệu suất và phân tích khác nhau.
  - **Consumption Zone**: Dữ liệu sản phẩm (Data Product).

![Data Lake Zones](https://github.com/user-attachments/assets/54a6bace-176b-4edc-b6a6-a597d4dca181)
