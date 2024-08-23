# Data-governance-aws
Nội dung ở đây tập trung ở phần lý thuyết, các slide nói về data governance mình kiếm được của aws. Tập trung service Data Lakeformation 
1. What is it ? 
Data Governance là một trong những kiến thức rất quan trọng khi làm việc với data platform. Phần lớn thời gian doanh nghiệp lãng phí là để quản lý dữ liệu trong doanh nghiệp sao cho dữ liệu được tin cậy và xác định đúng người có quyền truy cập gì để tối ưu hiệu quả BI và không để rò rỉ những dữ liệu quan trọng khách hàng như PII.
2. What aws help to solve data governance ?
![Untitled](https://github.com/user-attachments/assets/6fbfcb16-745f-4a44-a27f-2739f0fef8dc)
- AWS hỗ trợ việc quản lý bảo mật dữ liệu thông qua chủ yếu các service monitoring như CloudTrail, CloudWatch và Data Lakeformation.  
3. Challanges with building data lake with data governance ?
![Untitled (3)](https://github.com/user-attachments/assets/52b863c8-0245-4dca-bee6-405565e66b7b)
-Data Lake không chỉ là nơi bỏ tất cả dữ liệu vào mà nó cần phải đáp ứng nhu cầu phân tích dữ liệu. Các dữ liệu trong Data Lake cần phải được tách biệt và đóng khối theo mục tiêu của consumers. 

-Chính vì thế mà ta cần phải có các vùng (zones) để thoả các yêu cầu theo loại dữ liệu, mức độ quality của dữ liệu, mục tiêu phân tích:  Landing/raw zones, Standardrized zone, Consumption zone, Exploratory zone 

+ Landing/raw zone: điểm đầu tiên quản lý các dữ liệu ở định dạng gốc cho trường hợp Batch và Streaming. Dữ liệu tại lớp này sẽ được xác định giữ lại trong bao lâu.
+ Standarized zone:  lớp biến đổi dữ liệu thực hiện những phương pháp biến đổi để đáp ứng nhu cầu hiệu suất và phân tích khác nhau.
+ Consumption zone: data product
![Untitled (3)](https://github.com/user-attachments/assets/914461f4-812e-4616-b51d-6517c39b203f)
