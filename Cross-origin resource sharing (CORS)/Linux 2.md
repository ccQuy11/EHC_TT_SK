Task 1: 

Giới thiệu và mô tả những cái sẽ học trong phần này

Task 2:

Kiến thức về SSH và cách hoạt động

SSH ( secure shell ) là giao thức giữa 2 thiết bị được mã hóa, sử dụng thuật toán để gửi những gì con người đọc được thành mã hóa để đi qua network nơi mà sẽ được mở khóa khi ở 1 thiết bị remote khác

Cho phép ta ra lệnh trên các thiết bị remote khác 

Ví dụ ssh tryhackme@10.10.137.96 

Task 3:

Giới thiệu flag và chuyển đổi 

Hiểu thì là các extensions đi theo các command 

Ví dụ ls -a show tất cả folder hay ls -l show ra cái folder đấy có quyền gì

Có thể kiểm tra bằng man + command muốn tra 

Task 4:

Giới thiệu về filesystem interaction

Các commands cơ bản

touch: tạo file

mkdir: tạo folder

cp: copy nội dung 

mv: di chuyển

rm: xóa

file: định nghĩa loại file

Task 5:

Giới thiệu về quyền

Có thể thay đổi quyền của file đấy bằng lệnh chmod xxx ( với x là các số từ 0 đến 7)

<img width="967" height="523" alt="image" src="https://github.com/user-attachments/assets/5e6f6ea8-52cf-4989-8719-3bca21a26b15" />

Mở ls -l để xem file có quyền gì

XXX đấy tượng trưng cho 3 nhóm 

Theo từ trái sang phải sẽ là quyền của user, group và public 

Chuyển giữa các user: sử dụng lệnh su -l ( cái này chắc để tạo biến môi trường mới và các thứ tương tự)

Task 6:

Thư mục cơ bản:

/etc: là thư mục gốc, quan trọng nhất. Có 2 loại là /etc/passwd và /etc/shadow nhưng khi muốn tìm pass thì sẽ thường vào passwd nhiều hơn do passwd chứa mật khẩu ( tệp văn bản) còn shadow sẽ chứa hash của mật khẩu đó ( mã hóa bằng sha512) 

Đọc thêm: https://unix.stackexchange.com/questions/461022/what-is-the-difference-between-etc-shadow-and-etc-passwd

/var: thư mục trong linux, chứa dữ liệu thường xuyên vào hoặc viết bởi ứng dụng chạy trên hệ thống 

Ví dụ: các file log kiểu /var/log không cần thiết xuất hiện với người dùng cụ thể kiểu databases

/root: là thư mục gốc, phải có mật khẩu của user mới vào được, các user tạo sau không được vào

