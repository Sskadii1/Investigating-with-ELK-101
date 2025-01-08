# Investigating-with-ELK-101
Test ELK101 

Elastic Stack là tập hợp các thành phần nguồn mở khác nhau được liên kết với nhau để giúp người dùng lấy dữ liệu từ bất kỳ nguồn nào và ở bất kỳ định dạng nào, sau đó thực hiện tìm kiếm, phân tích và trực quan hóa dữ liệu theo thời gian thực.

bao gồm:
**Elestic search
Logstash
beats
kibana**

**Elasticsearch** là một công cụ tìm kiếm và phân tích toàn văn bản được sử dụng để lưu trữ các tài liệu định dạng JSON. Elasticsearch là một thành phần quan trọng được sử dụng để lưu trữ, phân tích, thực hiện tương quan trên dữ liệu, v.v. 

**Elasticsearch hỗ trợ RESTFul API để tương tác với dữ liệu.*

**Logstash** Logstash là một công cụ xử lý dữ liệu được sử dụng để lấy dữ liệu từ nhiều nguồn khác nhau, áp dụng bộ lọc hoặc chuẩn hóa dữ liệu, sau đó gửi đến đích có thể là Kibana hoặc cổng lắng nghe. Tệp cấu hình logstash được chia thành ba phần:

Input{}: là nơi người dùng xác định nguồn mà dữ liệu đang được thu thập. Logstash hỗ trợ nhiều plugin đầu vào như được hiển thị trong tài liệu tham khảo.

https://www.elastic.co/guide/en/logstash/8.1/input-plugins.html

Filter{}: là nơi người dùng chỉ định các tùy chọn bộ lọc để chuẩn hóa nhật ký đã nhập ở trên. Logstash hỗ trợ nhiều plugin bộ lọc như được hiển thị trong tài liệu tham khảo.

https://www.elastic.co/guide/en/logstash/8.1/filter-plugins.html

Output{}: là nơi người dùng muốn dữ liệu đã lọc được gửi đi. Nó có thể là một cổng lắng nghe, Giao diện Kibana, cơ sở dữ liệu elasticsearch, một tệp, v.v. Logstash hỗ trợ nhiều plugin Output như được hiển thị trong tài liệu tham khảo.

https://www.elastic.co/guide/en/logstash/8.1/output-plugins.html

**Beats** là một tác nhân dựa trên máy chủ được gọi là Data-shippers được sử dụng để vận chuyển/chuyển dữ liệu từ các điểm cuối đến elasticsearch. Mỗi beat là một tác nhân có mục đích duy nhất gửi dữ liệu cụ thể đến elasticsearch. 

Beats có Filebeat, Metricbeat, Packetbeat, Winlogbeat, auditbeat, Heartbeat, Functionbeat. 

**Kibana** à một công cụ trực quan hóa dữ liệu dựa trên web hoạt động với elasticsearch để phân tích, điều tra và trực quan hóa luồng dữ liệu theo thời gian thực. Công cụ này cho phép người dùng tạo nhiều hình ảnh trực quan và bảng thông tin để có khả năng hiển thị tốt hơn.

**Elastic Stack** Hoạt động như sau: 

1. Beats là một tập hợp các tác nhân vận chuyển dữ liệu khác nhau được sử dụng để thu thập dữ liệu từ nhiều tác nhân.

2. Logstash thu thập dữ liệu từ các nhịp, cổng hoặc tệp, v.v., phân tích/chuẩn hóa dữ liệu thành các cặp giá trị trường và lưu trữ chúng vào elasticsearch.

3. Elasticsearch hoạt động như một cơ sở dữ liệu được sử dụng để tìm kiếm và phân tích dữ liệu.

4. Kibana chịu trách nhiệm hiển thị và trực quan hóa dữ liệu được lưu trữ trong elasticsearch. Dữ liệu được lưu trữ trong elasticseach có thể dễ dàng được định hình thành các hình ảnh trực quan, biểu đồ thời gian, đồ họa thông tin, v.v. khác nhau bằng cách sử dụng Kibana.






