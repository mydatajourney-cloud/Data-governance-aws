# Data-governance-fundemental and on aws 
Nội dung ở đây tập trung ở phần lý thuyết, các slide nói về data governance mình kiếm được của aws. Tập trung service Data Lakeformation 
1. Data governance là gì ?
- Data Governance là một trong những kiến thức rất quan trọng khi làm việc với data platform. Phần lớn thời gian doanh nghiệp lãng phí là để quản lý dữ liệu trong doanh nghiệp sao cho dữ liệu được tin cậy và xác định đúng người có quyền truy cập gì để tối ưu hiệu quả BI và không để rò rỉ những dữ liệu quan trọng khách hàng như PII.
2. Lợi ích data governance ?
- Bảo mật dữ liệu: bảo mật dữ liệu ở bên trong công ty, giữa các phòng ban và từ bên ngoài. Chỉ những phòng ban được cho phép mới có thể access dữ liệu
- Giúp đảm bảo đáp dữ liệu đáp ứng những tiêu chuẩn công ty và quốc gia sở tại.
- Cải thiện chất lượng dữ liệu.
- Tránh trường hợp dữ liệu không đồng nhất giữa các phòng ban.
- Tăng tính tin cậy của dữ liệu nhờ vào các quy trình, quy tắc được triển khai.
- Cải thiện việc phân tích và đưa ra quyết định công ty
3. Quy tắc chính của data governance ?
![Untitled (4)](https://github.com/user-attachments/assets/edc67889-a75e-4c07-8104-54d222ed3db1)
- “My data” → “Our data”: Dữ liệu nên được chia sẻ với nhau giữa các phòng ban trong công ty chứ không chỉ riêng mỗi phòng ban. Tất nhiên việc chia sẻ những dữ liệu nhạy cảm (ví dụ như phòng ban HR sẽ không phù hợp). 
⇒ Nên có một cấu trúc để dữ liệu có thể được chia sẻ tuỳ theo như cầu phân tích và quyền truy cập dữ liệu.
- Xác định trách nhiệm: trách nhiệm của data gorvenance không chỉ nằm ở bộ phận IT mà còn bộ phận khác. Mọi người cần phải biết dữ liệu nào dùng để làm gì và dữ liệu nào không được phép dùng để làm gì. Để nhằm chia sẻ nhằm dữ liệu ra bên ngoài .
- Đội quản lý dữ liệu cần phải làm việc với các bên ở trong và ở ngoài để chắc rằng dữ liệu tuân theo quy chuẩn, quy tắc.
- Chất lượng dữ liệu cần phải luôn đúng để đưa ra các quyết định đúng.

*Quy tắc trên được đánh giá dựa trên các tiêu chuẩn sau: 
- Accessibility: liệu rằng dữ liệu có được truy cập bởi đúng người.
- Accuracy: tính chính xác của dữ liệu.
- Completeness: liệu rằng dữ liệu có đủ hoàn thiện chưa hay cần phải thu thập thêm.
- Consistency:
- Relevance: liệu rằng dữ liệu của ta có luôn được cập nhật không, dữ liệu đang được lưu trữ có cần thiết không. Hoặc là có dữ liệu nào cần được nén lại không.
- Timeliness: liệu rằng dữ liệu ta cần có thể truy cập được kịp thời không.
- Uniqueless: khi đo lường những bộ dữ liệu đang có ta cần phải xem dữ liệu ta có bị trùng lặp không và phải chắc rằng nguồn mà ta lấy phải unique

⇒ Khi xây dựng một chương trình data governance ta cần phải xem liệu rằng các vấn đề ở trong công ty có thể kết nối tới những principle nào phía trên.

Tìm hiểu thêm: [Defining Data Governance Core Principles – TDAN.com](https://tdan.com/defining-data-governance-core-principles/17087)
4. What aws help to solve data governance ?
![Untitled](https://github.com/user-attachments/assets/6fbfcb16-745f-4a44-a27f-2739f0fef8dc)
- AWS hỗ trợ việc quản lý bảo mật dữ liệu thông qua chủ yếu các service monitoring như CloudTrail, CloudWatch và Data Lakeformation.  
3. Challanges with building data lake with data governance ?
![Untitled (3)](https://github.com/user-attachments/assets/52b863c8-0245-4dca-bee6-405565e66b7b)
-Data Lake không chỉ là nơi bỏ tất cả dữ liệu vào mà nó cần phải đáp ứng nhu cầu phân tích dữ liệu. Các dữ liệu trong Data Lake cần phải được tách biệt và đóng khối theo mục tiêu của consumers. 

-Chính vì thế mà ta cần phải có các vùng (zones) để thoả các yêu cầu theo loại dữ liệu, mức độ quality của dữ liệu, mục tiêu phân tích:  Landing/raw zones, Standardrized zone, Consumption zone, Exploratory zone 

+ Landing/raw zone: điểm đầu tiên quản lý các dữ liệu ở định dạng gốc cho trường hợp Batch và Streaming. Dữ liệu tại lớp này sẽ được xác định giữ lại trong bao lâu.
+ Standarized zone:  lớp biến đổi dữ liệu thực hiện những phương pháp biến đổi để đáp ứng nhu cầu hiệu suất và phân tích khác nhau.
+ Consumption zone: data product
![Untitled (1)](https://github.com/user-attachments/assets/54a6bace-176b-4edc-b6a6-a597d4dca181)


