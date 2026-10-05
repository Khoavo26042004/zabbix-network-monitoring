# Thiết lập cảnh báo qua Telegram.
+ Bước 1: Trên giao diện Zabbix truy cập đến Alerts -> Media types -> Tìm dịch vụ telegram và enable.

<img width="915" height="31" alt="image" src="https://github.com/user-attachments/assets/c8cd9e58-1241-49c7-8b55-65d71ccf4a74" />

+ Bước 2: Để có thể sử dụng thống báo qua telegram ta cần lấy các thông số sau: Token bot, ID Bot và Group ID bot. Đăng nhập vào tài khoản Telegram làm các bước sau:
	- Tạo một bot mới và lấy token thông qua sử dụng BotFather của Telegram.

**Tạo Bot mới của Telegram.**

<img width="915" height="759" alt="image" src="https://github.com/user-attachments/assets/81b4f5cc-117f-4ffe-a7c8-8f7689048622" />

**Đặt tên cho bot mới.**

<img width="915" height="271" alt="image" src="https://github.com/user-attachments/assets/d5a6f69c-1df9-4cf4-9b92-91fec1ea56eb" />

**Tạo username cho bot mới và lấy token.**

<img width="915" height="489" alt="image" src="https://github.com/user-attachments/assets/64ad9ead-360c-460f-a6ad-922656220a08" />
 
	- Tại thanh search của telegram, ta tìm @IDBot và lấy ID của username bot đã tạo ở bước trên.
<img width="860" height="715" alt="image" src="https://github.com/user-attachments/assets/ada5e1bb-fc05-446b-b9e4-e10ce740e328" />

	- Tạo group để nhận thông báo và add IDBot và Bot vừa mới tạo vào group. Sau đó lấy Group ID. Đây là nơi mà thông báo sẽ trả về từ Zabbix nếu gặp sự cố.

**Thêm member cần thiết vào group.**

<img width="915" height="132" alt="image" src="https://github.com/user-attachments/assets/e044e89d-7483-4b4f-b84c-7a5c07c17087" />

**Lấy Group ID.**

<img width="915" height="354" alt="image" src="https://github.com/user-attachments/assets/5694541f-1c4f-4b26-a94a-fdc126b95a26" />

**Sau khi thực hiện các bước ở trên ta lấy được các thông tin như bảng sau.**

| Zabbix-token | 8704848176:AAEJBvK2WyWYO7lg8lfDLClOf43QhGW-efw
|Bot ID | 7270124369
| Group ID | -5259771955

+ Bước 3: Ta trở lại bước 1, chọn vào Telegram để nhập các Parameters. Sử dụng API_Token và Group ID lấy ở bước một dán vào trường api_token và api_chat_id.

**Thiết lập các thống số để chạy dịch vụ.**

<img width="915" height="890" alt="image" src="https://github.com/user-attachments/assets/b623f8ce-01e1-4a6a-a5d9-eef782d77dfb" />

+ Bước 4: Truy cập Users -> Users chọn Admin và chuyển hướng sang thành Media để tạo kênh media qua dịch vụ Telegram với Bot ID lấy ở bước 2.

**Thêm media cho Admin**

<img width="915" height="466" alt="image" src="https://github.com/user-attachments/assets/03fffddb-9031-4ce4-b34b-d7887b94d852" />
