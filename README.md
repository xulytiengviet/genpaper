# GenPaper

Bàn viết bài báo khoa học bằng tiếng Việt. Tải [index.html](./index.html) về máy, mở bằng Chrome hoặc Edge và giữ tab mở đến khi xuất xong. Ứng dụng chỉ gồm một tệp HTML, không cần máy chủ hay cài gói phụ thuộc.

## Viết một bản thảo

1. Nhập câu hỏi nghiên cứu và nhật ký thực nghiệm. Để tạo biểu đồ, nhập thêm hai cột gồm tên điều kiện và giá trị đo, ghi đơn vị trong tiêu đề cột.
2. Điền nhan đề, tác giả, cơ quan, email, tài trợ và lời cảm ơn. Có thể chỉnh các trường này trước khi xuất.
3. Nhập khóa DeepSeek của chính tác giả và tên mô hình được cấp quyền. Nhấn **Tạo bản thảo**. Trình duyệt cần kết nối Internet cho DeepSeek và Crossref. Khóa được gửi tới api.deepseek.com, không được ghi vào tệp, bộ nhớ lưu trữ trình duyệt hay tài liệu xuất.
4. Mở nhật ký tác nhân để đọc dàn ý, nguồn đối chiếu và nhận xét. Chọn **Chỉnh nội dung** để sửa từng mục. Trường nhan đề trong thông tin công bố được ưu tiên hơn nhan đề đề xuất.
5. Tải Word (.docx), LaTeX (.tex, biên dịch bằng XeLaTeX với font DejaVu Serif), hoặc chọn **In / Lưu PDF** và chọn **Save as PDF** trong hộp thoại in.

## Quy trình tác nhân

Lead Researcher lập dàn ý và đề xuất truy vấn. Literature Review Agent nhận tối đa sáu bản ghi từ Crossref, gồm DOI, nhan đề và tóm tắt nếu có. Khi tra cứu thất bại, hệ thống ghi rõ khoảng trống nguồn. Plotting Agent đặt chú thích cho hình được mã JavaScript dựng từ số liệu tác giả nhập. Lead Researcher viết bản đầu, Reviewer Agent đối chiếu với bằng chứng và Lead Researcher trả bản sửa.

Bản thảo, khóa và các chỉnh sửa được giữ trong phiên làm việc. Xuất tài liệu trước khi đóng hoặc tải lại tab. Một lần chạy dùng năm yêu cầu DeepSeek, hoặc sáu nếu có số liệu vẽ hình. Nút Dừng hủy yêu cầu đang chờ ở phía trình duyệt. Tác giả cần kiểm tra DOI, mức độ phù hợp của từng trích dẫn và các diễn giải so với nhật ký gốc.

GenPaper chạy trong trang riêng. Liên kết [demo chính thức](https://cdn.deepseek.com/chat-demo) mở giao diện chat do DeepSeek vận hành. Phần điều phối tác nhân gọi [API chat completions](https://api-docs.deepseek.com/) trực tiếp từ trình duyệt.
