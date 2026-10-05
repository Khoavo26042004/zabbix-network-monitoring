Thiết lập cảnh báo qua Telegram.
+ Bước 1: Trên giao diện Zabbix truy cập đến Alerts -> Media types -> Tìm dịch vụ telegram và enable.
 
Hình 4.15: Enable dịch vụ thông báo qua Telegram.
+ Bước 2: Để có thể sử dụng thống báo qua telegram ta cần lấy các thông số sau: Token bot, ID Bot và Group ID bot. Đăng nhập vào tài khoản Telegram làm các bước sau:
	- Tạo một bot mới và lấy token thông qua sử dụng BotFather của Telegram.
 
Hình 4.16: Tạo Bot mới của Telegram.
 
Hình 4.17: Đặt tên cho bot mới.
 
Hình 4.18: Tạo username cho bot mới và lấy token.
	
 
- Tại thanh search của telegram, ta tìm @IDBot và lấy ID của username bot đã tạo ở bước trên.
 
Hình 4.19: Lấy ID của bot.
	- Tạo group để nhận thông báo và add IDBot và Bot vừa mới tạo vào group. Sau đó lấy Group ID. Đây là nơi mà thông báo sẽ trả về từ Zabbix nếu gặp sự cố.
 
Hình 4.20: Thêm member cần thiết vào group.
 
Hình 4.21: Lấy Group ID.
Sau khi thực hiện các bước ở trên ta lấy được các thông tin như bảng sau.
Zabbix-token	8704848176:AAEJBvK2WyWYO7lg8lfDLClOf43QhGW-efw
Bot ID	7270124369
Group ID:	-5259771955

 
+ Bước 3: Ta trở lại bước 1, chọn vào Telegram để nhập các Parameters. Sử dụng API_Token và Group ID lấy ở bước một dán vào trường api_token và api_chat_id.
 
Hình 4.22: Thiết lập các thống số để chạy dịch vụ.
+ Bước 4: Truy cập Users -> Users chọn Admin và chuyển hướng sang thành Media để tạo kênh media qua dịch vụ Telegram với Bot ID lấy ở bước 2.
 
Hình 4.23: Thêm media cho Admin
