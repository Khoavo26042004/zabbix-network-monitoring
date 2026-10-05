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

# Triển khai chính

* Triển khai **Zabbix monitoring server** trên Ubuntu Server.
* Cấu hình **Zabbix Agent** để giám sát Windows Server.
* Cấu hình **SNMP-based monitoring** cho pfSense.
* Giám sát trạng thái hoạt động của network và interface.
* Giám sát CPU, memory, disk usage và network traffic.
* Xây dựng các **trigger-based incident detection scenarios**.
* Tích hợp **Telegram** để gửi thông báo sự cố theo thời gian thực.
* Xây dựng **virtualized network environment** để mô phỏng hạ tầng mạng trong môi trường doanh nghiệp.

# Mô hình thực nghiệm
 
Hình 4.2: Mô hình hệ thống sử dụng Zabbix để giám sát.

<img width="856" height="756" alt="image" src="https://github.com/user-attachments/assets/56cccdba-f177-430d-b092-6f5010b87a82" />

Trong mô hình các thành phần trong hệ thống mạng được quy hoạch theo bảng sau, bao gồm:

### Bảng quy hoạch thành phần trong sơ đồ mạng.

| Vùng | Host name | IP | OS | Mục đích |
|:---:|:---:|:---:|:---:|---|
| DMZ | `pfsense.home.arpa` | `192.168.204.1/24` | FreeBSD | Firewall dùng để thiết lập rule, cung cấp các dịch vụ mạng như DHCP, DNS, NAT. |
| DMZ | `zabbix-server` | `192.168.204.129/24` | Ubuntu Server 24.04 | Máy chủ giám sát tài nguyên các server. |
| DMZ | `FTP-server` | `192.168.204.131/24` | Windows Server 2022 | Máy chủ lưu trữ các file tài liệu. |
| Internet | `Kali` | `192.168.74.132/24` | Kali Linux | Máy tính đóng vai trò người tấn công vào hệ thống mạng. |
| Internal | `Windows 10` | `192.168.200.0/24` | Windows | Máy tính nội bộ. |

# Kịch bản giám sát

Hệ thống được thiết kế để phát hiện các tình huống như:

* **Host unavailable**
* **Windows Server agent unavailable**
* **High CPU utilization**
* **High memory utilization**
* **Low disk space**
* **WAN interface failure**
* **Abnormal network traffic**
* **Network connectivity problems**
