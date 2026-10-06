# Zabbix Network Monitoring & Alerting System

Hệ thống giám sát mạng và cảnh báo sự cố được xây dựng với **Zabbix, pfSense, Windows Server và Ubuntu Server**.

## Tổng quan

Đây là một **Dự án nghiên cứu cá nhân** tập trung vào việc nghiên cứu, thiết kế và triển khai hệ thống **Giám sát mạng & cảnh báo sự cố** sử dụng Zabbix.

Dự án nghiên cứu cách sử dụng **infrastructure monitoring** để phát hiện các sự cố liên quan đến network và server, thu thập dữ liệu giám sát, xác định các trạng thái bất thường và gửi thông báo đến quản trị viên theo thời gian thực.

## Công nghệ

* Zabbix
* Ubuntu Server 24.04
* pfSense
* Windows Server 2022
* SNMP
* Zabbix Agent
* ICMP
* Telegram Bot
* VMware
* DNS
* Active Directory

## Triển khai chính

* Triển khai **Zabbix monitoring server** trên Ubuntu Server.
* Cấu hình **Zabbix Agent** để giám sát Windows Server.
* Cấu hình **SNMP-based monitoring** cho pfSense.
* Giám sát trạng thái hoạt động của network và interface.
* Giám sát CPU, memory, disk usage và network traffic.
* Xây dựng các **trigger-based incident detection scenarios**.
* Tích hợp **Telegram** để gửi thông báo sự cố theo thời gian thực.
* Xây dựng **virtualized network environment** để mô phỏng hạ tầng mạng trong môi trường doanh nghiệp.

## Mô hình thực nghiệm
 
**Mô hình hệ thống sử dụng Zabbix để giám sát**

<img width="856" height="756" alt="image" src="https://github.com/user-attachments/assets/56cccdba-f177-430d-b092-6f5010b87a82" />

### Trong mô hình các thành phần trong hệ thống mạng được quy hoạch theo bảng sau, bao gồm:

#### Bảng quy hoạch thành phần trong sơ đồ mạng.

| Vùng | Host name | IP | OS | Mục đích |
|:---:|:---:|:---:|:---:|---|
| DMZ | `pfsense.home.arpa` | `192.168.204.1/24` | FreeBSD | Firewall dùng để thiết lập rule, cung cấp các dịch vụ mạng như DHCP, DNS, NAT. |
| DMZ | `zabbix-server` | `192.168.204.129/24` | Ubuntu Server 24.04 | Máy chủ giám sát tài nguyên các server. |
| DMZ | `FTP-server` | `192.168.204.131/24` | Windows Server 2022 | Máy chủ lưu trữ các file tài liệu. |
| Internet | `Kali` | `192.168.74.132/24` | Kali Linux | Máy tính đóng vai trò người tấn công vào hệ thống mạng. |
| Internal | `Windows 10` | `192.168.200.0/24` | Windows | Máy tính nội bộ. |

## Kịch bản giám sát

Hệ thống được thiết kế để phát hiện các tình huống như:

* **Host unavailable**
* **Windows Server agent unavailable**
* **High CPU utilization**
* **High memory utilization**
* **Low disk space**
* **WAN interface failure**
* **Abnormal network traffic**
* **Network connectivity problems**

## Kết quả 
### Giám sát trạng thái hoạt động
Tại phần giao diện monitoring có thể thấy trạng thái của host hiện tại là màu đỏ tức là đang không hoạt động hay đang gặp sự cố nào đó mà không thể kết nối được, còn màu xanh thì host vẫn đang hoạt động bình thường. Cụ thể trong hình đang dùng giao thức SNMP trên Zabbix để giám sát thông qua port 161 và báo lỗi là: cannot retrieve OID: '.1.3.6.1.2.1.2.2.1.13' from [[192.168.204.1]:161]: timed out. 

**Theo dõi trạng thái của host Pfsense**

<img width="915" height="442" alt="image" src="https://github.com/user-attachments/assets/cfc0602e-e4a4-4510-9858-a720193be041" />

### Giám sát trạng thái Interface
**Giám sát tài nguyên CPU của host Window server**
<img width="915" height="316" alt="image" src="https://github.com/user-attachments/assets/003b517f-cc4a-4dee-9c7c-31311942afae" />

## Giám sát tài nguyên
### Giám sát tài nguyên CPU
**Giám sát tài nguyên CPU của host Window server**

<img width="915" height="216" alt="image" src="https://github.com/user-attachments/assets/6434c6aa-09e9-43d5-aee2-b731bdfe5dac" />

+ Trước đó ta có tạo một trigger về mức sử dụng tài nguyên CPU ở “mục 4.3.2. Tạo trigger cho host”. Ta có thể thấy có một đường nét đứt màu vàng là đường ngưỡng CPU đạt 90%.

### Giám sát tài nguyên ô đĩa (Disk)
**Giám sát tài nguyên ổ đĩa của host Window server**

<img width="915" height="195" alt="image" src="https://github.com/user-attachments/assets/a4ad90a7-1eb6-49dd-a852-cc66717212e0" />

+ Ta có thể thấy rõ các thống số như tổng dung lượng ổ đĩa, đã sử dụng và số dung lượng còn trống.

### Giám sát lưu lượng mạng
**Biểu đồ lưu lượng mạng trên 1 interface của host Pfsense**

<img width="915" height="255" alt="image" src="https://github.com/user-attachments/assets/cc8901e1-95f9-4741-abdc-686e93f6f0db" />

### Cảnh báo sự cố
**Cảnh báo trạng thái host thay đổi của host qua Telegram**

<img width="752" height="266" alt="image" src="https://github.com/user-attachments/assets/b7f6cb5f-9d5b-441e-9781-3b387d373620" />

**Cảnh báo mức sử dụng tài nguyên CPU vượt ngưỡng 90% của host Window server qua Telegram**

<img width="794" height="581" alt="image" src="https://github.com/user-attachments/assets/fa288edd-1393-4bca-a8f6-33e95090b1a9" />

