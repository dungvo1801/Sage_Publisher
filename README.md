# Sage_Publisher
1. Yêu cầu nhiệm vụ:
Crawl dữ liệu của các tạp chí thuộc nhà xuất bản SAGE tại đường dẫn
https://journals.sagepub.com/. Trong đó, yêu cầu lấy ra toàn bộ 1193 danh mục các tạp chí
hiện có, tên viết tắt, tin tên tạp chí, issn, eissn, chỉ số impact factor trong 2 năm theo hình
mô tả. Sau đó xuất ra file Excel và sử dụng các thư viện của ngôn ngữ Python để thực
hiện nhiệm vụ này.
2. Ý tưởng triển khai:
Đầu tiên, em sẽ quan sát cấu trúc của trang web để hiểu cách các tạp chí được tổ chức và
truy cập. Kiểm tra cấu trúc URL của từng trang và tìm hiểu cách trang web hiển thị danh
sách tạp chí.
Với yêu cầu lấy ra toàn bộ 1193 danh mục các tạp chí hiện có tại đường dẫn
https://journals.sagepub.com/action/showPublications, em quan sát thấy đường dẫn này
bao gồm 120 trang, mỗi trang sẽ có từ 9 đến 10 tạp chí, vậy để lấy được đường dẫn cụ thể
đến 1193 tạp chí, em cần lặp qua 120 trang để có thể lấy được toàn bộ đường dẫn này.
Tuy nhiên, em sẽ thay đổi pageSize của trang web để có thể load 100 tạp chí trong 1 lần
thay vì 10 như mặc định, việc này sẽ giúp giảm thiểu thời gian chạy và chi phí.
Sau khi đã có 1193 đường dẫn của từng tạp chí, em sẽ xây dựng vòng lặp truy cập đến
từng đường dẫn trên để lấy ra các thông tin chi tiết như yêu cầu. Riêng chỉ số Impact
Factor, em chỉ lấy trong 2 năm theo yêu cầu.
3.Kết quả đạt được:
- Crawl các dữ liệu được yêu cầu và trình bày theo mẫu. Các dữ liệu không có sẽ
được để trống.
- File kết quả được lưu dưới dạng Excel.
