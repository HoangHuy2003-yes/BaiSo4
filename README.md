# BaiSo4
Sinh Viên: Chu Hoàng Huy, MSV K2154801076

Yêu cầu bài toán 
- Tạo csdl cho hệ thống TKB (đã nghe giảng, đã xem cách làm)
Nguồn dữ liệu: TMS.tnut.edu.vn
Tạo các bảng tuỳ ý (3nf)
Tạo được query truy vấn ra thông tin gồm 4 cột: họ tên gv, môn dạy, giờ vào lớp, giờ ra. trả lời câu hỏi: trong khoảng thời gian từ datetime1 tới datetime2 thì có những gv nào đang bận giảng dạy.

Các bước thực hiên
- Tạo github repo mới: đặt tên tuỳ ý (có liên quan đến bài tập này)
tạo file readme.md, edit online nó: paste những ảnh chụp màn hình gõ text mô tả cho ảnh đó

Tạo CSDL cho hệ thống 

 tạo bảng giảng viên khóa chính là MaGV
 
 ![image](https://github.com/user-attachments/assets/1a20512b-1640-4b33-a8c5-d94f2f7815e3)
 
 tạo bảng môn học khóa chính là MaMH
 
 ![image](https://github.com/user-attachments/assets/4577a3e9-42b4-4198-9199-4b152981505a)
 
 tạo bảng lớp học khóa chính là MaLop
 
 ![image](https://github.com/user-attachments/assets/06d3e6cc-3a1a-41a1-ba86-10cc99208df8)
 
 tạo bảng TKB tuần khóa chính là MaTKB 
 
 ![image](https://github.com/user-attachments/assets/aad4dbb1-d4ce-4a38-b776-a0e031dd448b)

 bảng liên kết thực thể 
  1. Thực thể GiangVien
MaGV: Mã giảng viên (Khóa chính)
HoTenGV: Họ tên giảng viên
 Quan hệ:
Một giảng viên có thể dạy nhiều buổi học → Liên kết với ThoiKhoaBieu qua MaGV (1:N).
 2. Thực thể MonHoc
MaMH: Mã môn học (Khóa chính)
TenMH: Tên môn học
Quan hệ:
Một môn học có thể có nhiều lớp học khác nhau → liên kết với LopHoc qua MaMH.
 3. Thực thể LopHoc
MaLop: Mã lớp học (Khóa chính)
MaMH: Mã môn học (Khóa ngoại từ bảng MonHoc)
 Quan hệ:
Một lớp học thuộc một môn học (N:1 với MonHoc).
Một lớp học xuất hiện nhiều lần trong thời khóa biểu → liên kết với ThoiKhoaBieu qua MaLop (1:N).
 4. Thực thể ThoiKhoaBieu
MaTKB: Mã TKB (Khóa chính)
MaLop: Mã lớp học (Khóa ngoại từ LopHoc)
MaGV: Mã giảng viên (Khóa ngoại từ GiangVien)
Thu: Thứ trong tuần
GioBatDau: Giờ bắt đầu
GioKetThuc: Giờ kết thúc
Ngay: Ngày học cụ thể
bảng này sẽ mô tả chi tiết từng buổi học: ai dạy, dạy môn nào, vào thời gian nào.

![image](https://github.com/user-attachments/assets/7037d98e-66da-43c5-92e6-2c25bbdff029)

câu lệnh dùng để tìm giảng viên đang giảng dậy trong một thời gian 

![image](https://github.com/user-attachments/assets/150ad28b-a5ae-4b02-81d6-9795169c47e5)




 


 


  
