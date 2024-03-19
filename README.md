How to install Zabbix Server for Ubuntu:

Version: 6.4
OS: Ubuntu Server 22.04 (Jammy) LTS
Zabbix Components: Server / Frontend / Agent
Database: MySQL
Web Server: Apache


Install and configure Zabbix for your platform:

1. Install Zabbix repository:
# wget https://repo.zabbix.com/zabbix/6.4/ubuntu/pool/main/z/zabbix-release/zabbix-release_6.4-1+ubuntu22.04_all.deb
# dpkg -i zabbix-release_6.4-1+ubuntu22.04_all.deb
# apt update

2. Install Zabbix server, frontend, agent:
# apt install zabbix-server-mysql zabbix-frontend-php zabbix-apache-conf zabbix-sql-scripts zabbix-agent

(Aditional):
Check status Zabbix Server and Agent services:
# systemctl status zabbix-server.service
# systemctl status zabbix-agent.service
///
Start Zabbix Server and Agent service:
# systemctl start zabbix-server.service
# systemctl start zabbix-agent.service

(Recommended):
To keep running Zabbix services, if server reboot:
# systemctl enable zabbix-server.service
# systemctl enable zabbix-agent.service
