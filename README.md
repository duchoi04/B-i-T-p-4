Bài tập 04 của SV: K225480106085 - Hoàng Đức Hội- HQTCSDL

bai tap 4: (sql server) yêu cầu bài toán:

Tạo csdl cho TKB hệ thống (đã nghe học, đã xem cách làm)
Nguồn dữ liệu: TMS.tnut.edu.vn
Tạo các bảng tuỳ ý (3nf)
Tạo truy vấn ra thông tin gồm 4 cột: họ tên gv, môn dạy, giờ vào lớp, giờ ra. trả lời câu hỏi: trong khoảng thời gian từ datetime1 tới datetime2 thì có những gv nào đang bận giảng dạy.
các bước thực hiện:

Tạo mới repo github: đặt tên tuỳ ý (có liên quan đến bài tập này)
tạo tập tin readme.md, chỉnh sửa trực tuyến: dán những ảnh chụp màn hình nhập văn bản mô tả cho ảnh đó
Gợi ý: sử dụng tms => dữ liệu thô => tiền xử lý => dữ liệu như ý (3nf) tạo các bảng với struct phù hợp chèn nhiều hàng từ excel vào cửa sổ chỉnh sửa bảng dữ liệu 1 (quan sát thì sẽ làm đc)

hạn chót: 15/4/2025
a
Tạo cơ sở dữ liệu cho TKB hệ thống:

hình ảnh

Dựa vào nguồn dữ liệu: TMS.tnut.edu.vn để tạo các bảng với các thuộc tính phù hợp(đã đạt tiêu chuẩn 3NF), đặt loại dữ liệu cho các thuộc tính sao cho tối ưu:

Bảng GV:
hình ảnh

Bảng LOP:

hình ảnh

Bảng MON:

hình ảnh

Bảng PHONG:

hình ảnh

Bảng LICH (lịch dạy):

hình ảnh

Đặt khóa chính cho các bảng và liên kết các khóa ngoại lệ:

Ngoại trừ các khóa liên kết bảng:

hình ảnh

Sau khi đặt các khóa chính và các khóa liên kết ngoại trừ ta được sơ đồ liên kết sau ( sơ đồ cơ sở dữ liệu):

hình ảnh

Lấy thông tin từ nguồn TMS.tnut.edu.vn dán vào Excel và tiền xử lý dữ liệu (đọc các vòng lặp dữ liệu trong một số bảng) ------> Sao chép các dữ liệu đã được xử lý từ Excel vào mục Chỉnh sửa của bảng

Bảng GV:
hình ảnh

Bảng LOP:

hình ảnh

Bảng MON:

hình ảnh

Bảng PHONG:

hình ảnh

Bảng LICH:

hình ảnh

Truy vấn thông tin gồm 4 cột: họ tên gv, môn dạy, giờ vào lớp, giờ ra (em bổ sung thêm ngày):

hình ảnh

Trả lời cho câu hỏi: rong khoảng thời gian từ datetime1 tới datetime2 thì có những gv nào đang bận giảng dạy.

Em tạo 1 truy cập vẫn giữa thời điểm này và thời điểm kia để so sánh giờ vào và giờ ra:

hình ảnh

Ngoài ra, ta cũng có thể đóng gói thành phần 1 cho những lần sau không cần truy vấn quá dài:

hình ảnh

Đóng gói chức năng và truy vấn ngắn gọn:

hình ảnh
