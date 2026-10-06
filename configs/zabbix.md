# 1. Các yêu cầu cần cài đặt:
	- OS version: Ubuntu 24.04.2 64bit.
	- Zabbix version 7.4.6.
	- Database: MySQL.
	- Web server: Apache2.
	- PHP, net-snmp: LTS version.
**+ Cài đặt Ubuntu:**

  <img width="753" height="728" alt="image" src="https://github.com/user-attachments/assets/a1106761-b029-40db-b560-0817b8c7f7ef" />

**Xem thông tin phiên bản đang dùng**

<img width="915" height="374" alt="image" src="https://github.com/user-attachments/assets/c3f97067-846c-4a6a-a394-a94afa32eb4b" />

# 2. Cài đặt Zabbix Server 
**Chuẩn bị môi trường.**
+ Bước 1: Cập nhật hệ thống.
 <img width="915" height="33" alt="image" src="https://github.com/user-attachments/assets/39d0ebe9-a13b-4c46-9197-393af5be774d" />

+ Bước 2: Cài đặt Database (MySQL/ MariaDB).
 <img width="915" height="46" alt="image" src="https://github.com/user-attachments/assets/57f32165-471e-4639-b09a-7cdc17b853d1" />

**Tải file cài đặt.**
+ Bước 1: Lên trang chủ Zabbix và tải file cài đặt từ package.
+ Bước 2: Cài đặt và cấu hình cho Zabbix.
 <img width="915" height="36" alt="image" src="https://github.com/user-attachments/assets/5cd686b5-ff2d-4af7-b29c-fd99d9e2329a" />

+ Bước 3: Tạo database
- Bao gồm các bước: Login database -> Tạo database với tên ‘zabbix’ -> gán quyền cho user zabbix với mật khẩu là ‘password’ -> áp dụng thay đổi và thoát database.
 <img width="915" height="183" alt="image" src="https://github.com/user-attachments/assets/5829ecf6-b769-4d84-b59b-b2827aede859" />

+ Bước 4: Cấu hình database cho Zabbix server.
 <img width="915" height="64" alt="image" src="https://github.com/user-attachments/assets/5760e76a-68ed-4843-b9a4-24800e52a3d5" />

 <img width="915" height="376" alt="image" src="https://github.com/user-attachments/assets/49803159-b96b-4b63-87d3-ba3d43005da9" />

+ Bước 5: Khởi Zabbix server và agent..
 <img width="915" height="98" alt="image" src="https://github.com/user-attachments/assets/8f1ef2b8-7379-40f4-917e-443faf2ea3cb" />

# 3. Thiết lập giao diện Web frontend của zabbix.
+ Bước 1: Truy cập vào http://ipserverUbuntu/zabbix. Tại trang bắt đầu ấn vào Next step để chuyển hướng trang.
 <img width="915" height="547" alt="image" src="https://github.com/user-attachments/assets/a336ce79-0a3b-47c7-b17e-edc0d19d51ed" />

+ Bước 2: Tại trang này, kiểm tra thông số config php, đảm bảo ổn hết rồi ấn Next step để chuyển hướng.
 <img width="915" height="559" alt="image" src="https://github.com/user-attachments/assets/72c731e6-ba21-48a1-af52-e3c6ad77d7b2" />

+ Bước 3: Nhập thông tin về database Zabbix đã được thiết lập, Nhất Next step.
 <img width="915" height="540" alt="image" src="https://github.com/user-attachments/assets/64b362a5-313a-49b8-9798-334bf79e8b95" />

+ Bước 4: Nhập thông tin của Zabbix server, nhấn Next step.
 <img width="915" height="544" alt="image" src="https://github.com/user-attachments/assets/3cb323b9-ccf4-4ccb-864e-4f4abe7fb10c" />

+ Bước 5: Xác nhận thông tin đã thiết lập trước đó, ấn Next step.
 <img width="915" height="543" alt="image" src="https://github.com/user-attachments/assets/089c20c1-6ad4-48f6-bc93-12b50039ca01" />

+ Bước 6: Kết thúc quá trình thiết lập, ấn Finish.
 <img width="915" height="544" alt="image" src="https://github.com/user-attachments/assets/1895ecb0-bae2-4440-858a-8693a0b20fa5" />

+ Bước 7: Đăng nhập tài khoản mặt định zabbix cấp, ấn Sign in.
 <img width="576" height="592" alt="image" src="https://github.com/user-attachments/assets/d3bccd5f-8b91-43f6-aca8-81dc4aa2d455" />

<img width="915" height="453" alt="image" src="https://github.com/user-attachments/assets/a81e0059-6875-4cf1-9511-8f5f6ca79f63" />

# 4. Cài đặt Zabbix Agent
**Cài đặt Zabbix agent cho window server 2022.**
+ Bước 1: Tải zabbix agent bằng dòng lệnh.
 <img width="915" height="79" alt="image" src="https://github.com/user-attachments/assets/25ca93b2-161a-48c0-8bb1-92829649d5f1" />

+ Bước 2: Xác nhận đã cài đặt được file Zabbix agent
 <img width="915" height="79" alt="image" src="https://github.com/user-attachments/assets/c79c3e63-152a-4d3e-976e-43db8250c361" />
 
+ Bước 3: Mở port 10050 cho Zabbix agent trên window server 2022.
 <img width="915" height="88" alt="image" src="https://github.com/user-attachments/assets/09e44f7d-7559-4de3-85d6-bcdac3f56a92" />

+ Bước 4: Cài đặt Zabbix agent.
 <img width="915" height="130" alt="image" src="https://github.com/user-attachments/assets/16c6818a-97c4-4c84-b36b-f3ef85c119a3" />

**Cài đặt giao thức SNMP cho Pfsense trên Zabbix.**
+ Bước 1: Cài đặt package SNMP trên pfsense. Chọn theo đường dẫn System → Package Manager → Available Packages → search net-snmp.

<img width="915" height="120" alt="image" src="https://github.com/user-attachments/assets/b797e36b-cc87-4e4d-9c64-c249753ef12c" />

<img width="915" height="346" alt="image" src="https://github.com/user-attachments/assets/fd228ff5-c21b-4776-8876-099f7deeb12f" />

<img width="833" height="390" alt="image" src="https://github.com/user-attachments/assets/a6e37f6d-16e6-463d-bbea-61c8da6c163e" />

+ Bước 2: Bật SNMP Service, cấu hình community string “zabbix” và bật SNMP Trap.
 <img width="915" height="603" alt="image" src="https://github.com/user-attachments/assets/9a909d13-caf8-4114-ba6d-ff7a5dfb9d10" />

