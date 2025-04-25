Bài tập 04 của SV: K225480106085 - HOÀNG ĐỨC HỘI - HQTCSDL

bai tap 4: (sql server) yêu cầu bài toán:

Tạo csdl cho hệ thống TKB (đã nghe học, đã xem cách làm)
Nguồn dữ liệu: TMS.tnut.edu.vn
Tạo các bảng tuỳ ý (3nf)
Tạo truy vấn ra thông tin gồm 4 cột: họ tên gv, môn dạy, giờ vào lớp, giờ ra. trả lời câu hỏi: trong khoảng thời gian từ datetime1 tới datetime2 thì có những gv nào đang bận giảng dạy.
các bước thực hiện:

Tạo mới repo github: đặt tên tuỳ ý (có liên quan đến bài tập này)
tạo tập tin readme.md, chỉnh sửa trực tuyến: dán những ảnh chụp màn hình nhập văn bản mô tả cho ảnh đó
Gợi ý: sử dụng tms => dữ liệu thô => tiền xử lý => dữ liệu như ý (3nf) tạo các bảng với struct phù hợp chèn nhiều hàng từ excel vào cửa sổ chỉnh sửa bảng dữ liệu 1 (quan sát thì sẽ làm được)
hạn chót: 15/4/2025

1.Tạo cơ sở dữ liệu cho TKB hệ thống:

![Screenshot 2025-04-24 210720](https://github.com/user-attachments/assets/cefbb1be-2a2f-432b-9a49-b43aa617ebe7)


2. Dựa vào nguồn dữ liệu: TMS.tnut.edu.vn để tạo các bảng với các thuộc tính phù hợp(đã đạt tiêu chuẩn 3NF), đặt loại dữ liệu cho các thuộc tính sao cho tối ưu:

- Bảng GV:


![Screenshot 2025-04-24 211909](https://github.com/user-attachments/assets/e298a900-3423-4047-b581-348b18f6e563)


- Bảng LOP:

![Screenshot 2025-04-24 212255](https://github.com/user-attachments/assets/3e47c011-6420-4b33-a0a8-a94913dac75c)

- Bảng MON:

![Screenshot 2025-04-24 211919](https://github.com/user-attachments/assets/ebe22110-0d06-4faa-abe2-f645efd9184b)

- Bảng PHONG:

![Screenshot 2025-04-24 211925](https://github.com/user-attachments/assets/f3f5e808-fe73-4157-a534-8f2178dc4eee)


- Bảng LICH (lịch dạy):

![Screenshot 2025-04-24 211931](https://github.com/user-attachments/assets/8a4597d5-4f62-40bc-8ceb-839b353941a4)


3. Đặt khóa chính cho các bảng và liên kết các khóa ngoại lệ:

Ngoại trừ các khóa liên kết bảng:

![Screenshot 2025-04-24 213115](https://github.com/user-attachments/assets/dff1a523-54f5-463e-bf3f-8705dab18a86)


- Sau khi đặt các khóa chính và các khóa liên kết ngoại trừ ta được sơ đồ liên kết sau ( sơ đồ cơ sở dữ liệu):

![Screenshot 2025-04-24 213811](https://github.com/user-attachments/assets/7f45ebdd-d77a-42d2-ab33-30472176cb9e)


4. Lấy thông tin từ nguồn TMS.tnut.edu.vn dán vào Excel và tiền xử lý dữ liệu (đọc các vòng lặp dữ liệu trong một số bảng) ------> Sao chép các dữ liệu đã được xử lý từ Excel vào mục Chỉnh sửa của bảng

- Bảng GV:

![Screenshot 2025-04-24 225001](https://github.com/user-attachments/assets/bb7b3a5d-ea54-42cb-8be2-236c0821eb51)


- Bảng LOP:

![Screenshot 2025-04-24 232820](https://github.com/user-attachments/assets/5697f2ce-1122-4043-b20c-492a9dca9475)


- Bảng MON:

![Screenshot 2025-04-25 232144](https://github.com/user-attachments/assets/26b140b9-be31-4b57-95d9-e300990646b1)


- Bảng PHONG:

![Screenshot 2025-04-25 232130](https://github.com/user-attachments/assets/21f4d0dc-55a3-4929-8c90-feb2a2601658)


- Bảng LICH:

![Screenshot 2025-04-25 000954](https://github.com/user-attachments/assets/1722d1e4-a0db-416d-9723-3143772d30e8)


Truy vấn thông tin gồm 4 cột: họ tên gv, môn dạy, giờ vào lớp, giờ ra (em bổ sung thêm ngày):

![Screenshot 2025-04-25 233005](https://github.com/user-attachments/assets/f1c78f88-bebd-4db6-9e6e-a433278224f6)


Trả lời cho câu hỏi: rong khoảng thời gian từ datetime1 tới datetime2 thì có những gv nào đang bận giảng dạy.

Em tạo 1 truy cập vẫn giữa thời điểm này và thời điểm kia để so sánh giờ vào và giờ ra:

![Screenshot 2025-04-25 233751](https://github.com/user-attachments/assets/fa0e9d7c-44eb-435b-bc6b-b1fcc232b5e3)


Ngoài ra, ta cũng có thể đóng gói thành phần 1 cho những lần sau không cần truy vấn quá dài:

![Screenshot 2025-04-26 000322](https://github.com/user-attachments/assets/01f53f15-0816-479d-aa97-0c4a30841764)


Đóng gói chức năng và truy vấn ngắn gọn:

![Screenshot 2025-04-26 000553](https://github.com/user-attachments/assets/7be17fdc-4922-4819-88a2-139cd8309a4e)
