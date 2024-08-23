# Data-governance-aws
Nội dung ở đây tập trung ở phần lý thuyết, các slide nói về data governance mình kiếm được của aws. Tập trung service Data Lakeformation 
1. What is it ? 
Data Governance là một trong những kiến thức rất quan trọng khi làm việc với data platform. Phần lớn thời gian doanh nghiệp lãng phí là để quản lý dữ liệu trong doanh nghiệp sao cho dữ liệu được tin cậy và xác định đúng người có quyền truy cập gì để tối ưu hiệu quả BI và không để rò rỉ những dữ liệu quan trọng khách hàng như PII.
2. What aws help to solve data governance ?
![Untitled](https://github.com/user-attachments/assets/6fbfcb16-745f-4a44-a27f-2739f0fef8dc)
- AWS hỗ trợ việc quản lý bảo mật dữ liệu thông qua chủ yếu các service monitoring như CloudTrail, CloudWatch và Data Lakeformation.  
3. Challanges with building data lake with data governance ?
![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/f00c4aab-69cd-4657-92af-51b4d5db5334/a8df1392-bcee-4895-8a85-e6c77f40eff7/Untitled.png)
4. Data lake zone in AWS
-Data Lake không chỉ là nơi bỏ tất cả dữ liệu vào mà nó cần phải đáp ứng nhu cầu phân tích dữ liệu. Các dữ liệu trong Data Lake cần phải được tách biệt và đóng khối theo mục tiêu của consumers. 

-Chính vì thế mà ta cần phải có các vùng (zones) để thoả các yêu cầu theo loại dữ liệu, mức độ quality của dữ liệu, mục tiêu phân tích:  Landing/raw zones, Standardrized zone, Consumption zone, Exploratory zone 

+ Landing/raw zone: điểm đầu tiên quản lý các dữ liệu ở định dạng gốc cho trường hợp Batch và Streaming. Dữ liệu tại lớp này sẽ được xác định giữ lại trong bao lâu.
+ Standarized zone:  lớp biến đổi dữ liệu thực hiện những phương pháp biến đổi để đáp ứng nhu cầu hiệu suất và phân tích khác nhau.
+ Consumption zone: data product
![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/f00c4aab-69cd-4657-92af-51b4d5db5334/a89939c3-905e-4353-85e6-7d95e0a7ff40/Untitled.png)
