# Zabbix Network Monitoring & Alerting System

Hệ thống giám sát mạng và cảnh báo sự cố được xây dựng với **Zabbix, pfSense, Windows Server và Ubuntu Server**.

## Tổng quan

Đây là một **personal technical research project** tập trung vào việc nghiên cứu, thiết kế và triển khai hệ thống **network monitoring và incident alerting** sử dụng Zabbix.

Project nghiên cứu cách sử dụng **infrastructure monitoring** để phát hiện các sự cố liên quan đến network và server, thu thập dữ liệu giám sát, xác định các trạng thái bất thường và gửi thông báo đến administrator theo thời gian thực.

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
