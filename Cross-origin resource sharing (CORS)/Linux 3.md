Giới thiệu VIM và NANO

VIM sẽ tiên tiến hơn NANO

Giới thiệu về wget: dùng để tải tệp từ 1 trang web nào đó về 

Transferring Files From Your Host - SCP (SSH): là một phương tiện sao chép tệp an toàn, cho phép truyền tệp giữa 2 máy tính bằng giao thức SSH để cung cấp cả xác thực và mã hóa.

<img width="905" height="660" alt="image" src="https://github.com/user-attachments/assets/e087d77a-c16f-49a4-b2e2-c6fc702f4e1d" />

<img width="1256" height="592" alt="image" src="https://github.com/user-attachments/assets/5e318444-f936-4ac9-a9ad-5416b932a968" />

Serving Files From Your Host - WEB: ubuntu được cài sẵn python3 

Cái này cần mở 2 term 1 dùng để mở port listen ( sẵn là 8000 và 2 là wget) 

<img width="1067" height="897" alt="image" src="https://github.com/user-attachments/assets/4f3c0149-92e7-441d-b794-e40300a1e9b9" />

Process 101:

Sử dụng lệnh ps để cung cấp danh sách các tiến trình đang chạy dưới dạng phiên của người dùng và một số thông tin bổ sung như mã trạng thái, phiên đang chạy tiến trình đó, thời gian sử dụng CPU mà tiến trình đó đang sử dụng và tên của chương trình hoặc lệnh thực tế đang được thực thi:

<img width="308" height="193" alt="image" src="https://github.com/user-attachments/assets/d33ad610-0bf0-41df-bee3-1679954c63ac" />

ps à một lệnh trong Unix/Linux (Process Status) dùng để liệt kê và hiển thị thông tin về các tiến trình (process) đang chạy trên hệ thống.

Muốn full thì là ps aux

          a = hiển thị các tiến trình cho tất cả người dùng
          
          u = hiển thị người dùng/chủ sở hữu của tiến trình
          
          x = cũng hiển thị các tiến trình không được kết nối với thiết bị đầu cuối

Cách duyệt khác là dùng top 

Có thể gửi tín hiệu để chấm dứt tiến trình. VD dùng lệnh Kill để chấm dứt PID 1337 sẽ là kill 1337

              SIGTERM - Kết thúc tiến trình, nhưng cho phép nó thực hiện một số tác vụ dọn dẹp trước
              
              SIGKILL - Giết tiến trình - không thực hiện bất kỳ dọn dẹp nào sau đó
              
              SIGSTOP - Dừng/tạm dừng một tiến trình

🍌 Getting Processes/Services to Start on Boot

Nhập systemctl để tương tác systemd

systemctl [option] [service] Ví dụ  systemctl start apache2

Có 4 options: 

            Start
            
            Stop

            Enable

            Disable

fg: đưa một tiến trình đang ở chế độ nền trước đó trở lại chế độ nền

😽 Maintaining Your System: Automation

          crontab -e

Crontab đơn giản là một tệp đặc biệt có định dạng được quy rình nhận dạng để thực thi từng dòng lệnh theo từng bước. Crontab yêu cầu 6 giá trị cụ thể:

           MIN	What minute to execute at

           HOUR     What hour to execute at

           DOM      What day of the month to execute at

           MON      What month of the year to execute at

           DOW      What day of the week to execute at

           CMD      The actual command that will be executed.

Ví dụ về việc sao lưu tệp. Muốn sao lưu "Documents" của "cmnatic" cứ sau 12 giờ.. Chúng ta sẽ sử dụng định dạng sau: 

             0 */12 * * * cp -R /home/cmnatic/Documents /var/backups/

Hỗ trợ ký tự đại diện hoặc dấu sao ( *).

💣Maintaining Your System: Package Management

apt install ........ để cài đặt 

add-apt-repository --remove ppa:PPA_Name/ppa  

apt remove sublime-text

🚒Maintaining Your System: Logs

Này chủ yếu nói về tập tin /var/log

Có thể vào để kiểm tra người dùng truy cập ip và file nào 
