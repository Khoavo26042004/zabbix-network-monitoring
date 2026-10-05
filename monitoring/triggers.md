Tạo trigger cho trạng thái hoạt động host
+ Trigger thông báo pfsense down.
+ Trigger này giúp cảnh báo cho quản trị viên biết rằng Pfsense bị down bằng cách gửi các gói ping bằng giao thức ICMP liên tục, nếu không phản hồi trong 5p thì sẽ gửi thông báo.
 
Hình 4.9: Trigger thống báo pfsense bị down.
 
Tạo trigger cho trạng thái dịch vụ của host
+ Trigger thông báo dịch vụ SNMP trên pfsense không hoạt động.
Trigger này thông báo cho quản trị viên biết, dịch vụ SNMP được cài đặt trên Pfsense đang không được hoạt động.
 
Hình 4.10: Trigger kiểm tra dịch vụ SNMP không hoạt trên Pfsense.
 
+ Trigger thông báo dịch vụ Zabbix Agent cài trên máy chủ Window không hoạt động
Trigger này giúp cảnh báo cho quản trị viên biết dịch vụ Zabbix Agent đang bị tắt hoặc không còn trên máy chủ Window server.
 
Hình 4.11: Trigger cảnh báo dịch vụ Zabbix Agent không hoạt 
động trên host.
 
Tạo trigger cho việc giám sát tài nguyên của host
+ Trigger cảnh báo mức sử dụng RAM của Window server.
Trigger này cảnh báo việc sử dụng RAM lớn hơn 90% trên máy chủ Window server.
 
Hình 4.12: Trigger cảnh báo mức độ sử dụng RAM của Window server.
 
+ Trigger cảnh báo mức độ sử dụng ổ đĩa của máy chủ Window server.
 
Hình 4.13: Trigger cảnh báo mức độ sử dụng ổ đĩa của Window server.
 
Tạo trigger cho việc giám sát lưu lượng mạng của host.
+ Trigger cảnh báo lưu lượng mạng sử dụng của host Pfsense.
Trigger này dùng để giám sát lưu lượng mạng vào (Inbound traffic) trên interface của pfSense.
 
Hình 4.14: Trigger cảnh báo lưu lượng mạng của host Pfsense
