1. Thiết lập thống số cho Zabbix
Trong đồ án sử dụng phần mềm ảo hóa VMWare để thiết lập cho các hệ thống server trong mô hình.
+ Các yêu cầu cần cài đặt:
	- OS version: Ubuntu 24.04.2 64bit.
	- Zabbix version 7.4.6.
	- Database: MySQL.
	- Web server: Apache2.
	- PHP, net-snmp: LTS version.
+ Cài đặt Ubuntu:
 
Hình 1.1: Thiết lập thông số cho hệ điều hành Ubuntu.
 
Hình 1.2: Thông tin về Ubuntu.
Cấu trúc thư mục 
+ Thư mục cấu hình /etc/zabbix, gồm:
 
	- zabbix_server.conf: File cấu hình của Zabbix Server.
	- zabbix_agentd.conf: File cấu hình Zabbix Agent.
+ Thư mục log /var/log/zabbix/, gồm:
 
+ Thư mục giao diện web /usr/share/zabbix/: nơi chứa mã nguồn giao diện WebUI:
 
+ Thư mục chứa script /usr/lib/zabbix/.
 
2. Cài đặt Zabbix Server 
Chuẩn bị môi trường.
+ Bước 1: Cập nhật hệ thống.
 
+ Bước 2: Cài đặt Database (MySQL/ MariaDB).
 
Tải file cài đặt.
+ Bước 1: Lên trang chủ Zabbix và tải file cài đặt từ package.
+ Bước 2: Cài đặt và cấu hình cho Zabbix.
 
 
+ Bước 3: Tạo database
- Bao gồm các bước: Login database -> Tạo database với tên ‘zabbix’ -> gán quyền cho user zabbix với mật khẩu là ‘password’ -> áp dụng thay đổi và thoát database.
 
+ Bước 4: Cấu hình database cho Zabbix server.
 
 
+ Bước 5: Khởi Zabbix server và agent..
 
3. Thiết lập giao diện Web frontend của zabbix.
+ Bước 1: Truy cập vào http://ipserverUbuntu/zabbix. Tại trang bắt đầu ấn vào Next step để chuyển hướng trang.
 
Hình 3.1: Giao diện web zabbix thiết lập lần đầu. 
 
+ Bước 2: Tại trang này, kiểm tra thông số config php, đảm bảo ổn hết rồi ấn Next step để chuyển hướng.
 
Hình 3.2: Kiểm tra thông số config php.
+ Bước 3: Nhập thông tin về database Zabbix đã được thiết lập, Nhất Next step.
 
Hình 3.3: Nhập thông tin database Zabbix.
 
+ Bước 4: Nhập thông tin của Zabbix server, nhấn Next step.
 
Hình 3.4: Thiết lập thông tin Zabbix server.
+ Bước 5: Xác nhận thông tin đã thiết lập trước đó, ấn Next step.
 
Hình 3.5: Tổng thông tin đã cài đặt.
 
+ Bước 6: Kết thúc quá trình thiết lập, ấn Finish.
 
Hình 3.6: Hoàn thành quá trình thiết lập.

+ Bước 7: Đăng nhập tài khoản mặt định zabbix cấp, ấn Sign in.
 
Hình 3.7: Đăng nhập vào web.
 
Hình 3.8: Giảo diện web của Zabbix.
