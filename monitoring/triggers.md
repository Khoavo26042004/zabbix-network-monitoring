## Tạo trigger cho trạng thái hoạt động host
+ **Trigger thông báo pfsense down**:
Trigger này giúp cảnh báo cho quản trị viên biết rằng Pfsense bị down bằng cách gửi các gói ping bằng giao thức ICMP liên tục, nếu không phản hồi trong 5p thì sẽ gửi thông báo.

<img width="915" height="614" alt="image" src="https://github.com/user-attachments/assets/3d66f4f4-2940-4b2a-b31a-ec9b2ca75947" />

## Tạo trigger cho trạng thái dịch vụ của host
+ **Trigger thông báo dịch vụ SNMP trên pfsense không hoạt động**:
Trigger này thông báo cho quản trị viên biết, dịch vụ SNMP được cài đặt trên Pfsense đang không được hoạt động.

<img width="915" height="611" alt="image" src="https://github.com/user-attachments/assets/838cb54e-3407-4adc-a17c-87c0e0ba7a11" />

+ **Trigger thông báo dịch vụ Zabbix Agent cài trên máy chủ Window không hoạt động**:
Trigger này giúp cảnh báo cho quản trị viên biết dịch vụ Zabbix Agent đang bị tắt hoặc không còn trên máy chủ Window server.
<img width="915" height="605" alt="image" src="https://github.com/user-attachments/assets/ca6cc8c9-583a-4a5c-a211-2e3221e328e3" />

## Tạo trigger cho việc giám sát tài nguyên của host
+ T**rigger cảnh báo mức sử dụng RAM của Window server**:
Trigger này cảnh báo việc sử dụng RAM lớn hơn 90% trên máy chủ Window server.

<img width="915" height="611" alt="image" src="https://github.com/user-attachments/assets/a6bedd67-bc53-438b-bc04-ce4ca4a9ab87" />

+ **Trigger cảnh báo mức độ sử dụng ổ đĩa của máy chủ Window server**

<img width="915" height="619" alt="image" src="https://github.com/user-attachments/assets/d6ecad63-4c5b-425c-94dd-d8a9022a016d" />

## Tạo trigger cho việc giám sát lưu lượng mạng của host.
+ **Trigger cảnh báo lưu lượng mạng sử dụng của host Pfsense**:
Trigger này dùng để giám sát lưu lượng mạng vào (Inbound traffic) trên interface của pfSense.

<img width="915" height="645" alt="image" src="https://github.com/user-attachments/assets/1788ac66-696b-4799-9e17-6c8d9f0854e1" />
