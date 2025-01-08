# So sánh hệ thống phiên bản tập trung và phân tán

Khi nói về hệ thống quản lý phiên bản, "tập trung" và "phân tán" là hai mô hình phổ biến. Dưới đây là sự so sánh giữa hai mô hình này:

| **Tiêu chí**                  | **Hệ thống tập trung**                          | **Hệ thống phân tán**                             |
|-------------------------------|------------------------------------------------|--------------------------------------------------|
| **Định nghĩa**               | Tất cả dữ liệu và lịch sử phiên bản được lưu trữ trên một máy chủ trung tâm. | Mỗi máy người dùng có một bản sao đầy đủ của kho lưu trữ, bao gồm toàn bộ lịch sử phiên bản. |
| **Ví dụ phổ biến**            | Subversion (SVN)                    | Git                                 |
| **Cách hoạt động**           | Người dùng làm việc trực tiếp với máy chủ trung tâm để lấy và đẩy thay đổi. | Người dùng làm việc với bản sao cục bộ và chỉ đồng bộ với kho trung tâm khi cần thiết. |
| **Phụ thuộc vào máy chủ**    | Máy chủ trung tâm là điểm duy nhất. Nếu máy chủ không hoạt động, tất cả người dùng bị gián đoạn. | Không phụ thuộc hoàn toàn vào máy chủ trung tâm; người dùng có thể làm việc ngoại tuyến. |
| **Hiệu suất làm việc**       | Chậm hơn nếu kết nối mạng kém, do phải truy cập máy chủ thường xuyên. | Nhanh hơn do các thao tác phần lớn được thực hiện trên bản sao cục bộ. |
| **Làm việc ngoại tuyến**     | Không thể làm việc nếu không có kết nối đến máy chủ. | Có thể làm việc ngoại tuyến, vì tất cả dữ liệu có sẵn cục bộ. |
| **Lịch sử và thay đổi**       | Lịch sử phiên bản được lưu trên máy chủ trung tâm. | Lịch sử đầy đủ được lưu trữ trên từng bản sao cục bộ. |
| **Xung đột**                 | Xung đột được phát hiện khi người dùng đẩy thay đổi lên máy chủ. | Xung đột có thể được phát hiện và xử lý trong quá trình hợp nhất (merge). |


## Khi nào nên dùng từng loại:

### Hệ thống tập trung
- Khi bạn làm việc với một nhóm nhỏ.
- Khi bạn cần kiểm soát chặt chẽ hơn và một quy trình làm việc đơn giản.
- Khi mọi người luôn làm việc trong môi trường kết nối mạng tốt.

### Hệ thống phân tán
- Khi bạn cần hỗ trợ cho nhóm lớn hoặc làm việc từ xa.
- Khi bạn cần làm việc ngoại tuyến.
- Khi bạn cần khả năng hợp nhất thay đổi phức tạp hơn.

## Tóm lại
- **Hệ thống tập trung** phù hợp với các dự án nhỏ, đơn giản.
- **Hệ thống phân tán** mang lại tính linh hoạt cao và khả năng làm việc độc lập mạnh mẽ hơn, đặc biệt phù hợp với các dự án hiện đại và nhóm lớn.

