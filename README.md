# security
Домашнее задание к занятию «Уязвимости и атаки на информационные системы»
# 1. Какие сетевые службы разрешены на Metasploitable?
На виртуальной машине Metasploitable обнаружены следующие сетевые службы:

Порт	Служба	Версия
21/tcp	FTP	vsftpd 2.3.4

22/tcp	SSH	OpenSSH 4.7p1

23/tcp	Telnet	Linux telnetd

25/tcp	SMTP	Postfix smtpd

53/tcp	DNS	ISC BIND 9.4.2

80/tcp	HTTP	Apache 2.2.8

111/tcp	RPC	rpcbind 2

139/tcp	NetBIOS	Samba smbd 3.X - 4.X

445/tcp	SMB	Samba smbd 3.X - 4.X

512/tcp	rexec	netkit-rsh rexecd

513/tcp	rlogin	OpenBSD rlogind

514/tcp	rsh	rshd (tcpwrapped)

1099/tcp	RMI	GNU Classpath grmiregistry

1524/tcp	bindshell	Metasploitable root shell

2049/tcp	NFS	nfs 2-4

2121/tcp	FTP	ProFTPD 1.3.1

3306/tcp	MySQL	MySQL 5.0.51a

5432/tcp	PostgreSQL	PostgreSQL 8.3.0 - 8.3.7

5900/tcp	VNC	VNC (protocol 3.3)

6000/tcp	X11	X Window System

6667/tcp	IRC	UnrealIRCd

8009/tcp	AJP	Apache Jserv 1.3

8180/tcp	HTTP	Apache Tomcat/Coyote 1.1

# 2. Обнаруженные уязвимости (три примера)
Уязвимость 1: vsftpd 2.3.4 - Backdoor Command Execution
Описание: В версии FTP-сервера vsftpd 2.3.4 был обнаружен бэкдор. При отправке строки, содержащей последовательность :) в имени пользователя, на порту 6200 открывается командная оболочка с правами root.

Ссылка на Exploit-DB: https://www.exploit-db.com/exploits/17491

EDB-ID: 17491

Уязвимость 2: UnrealIRCd 3.2.8.1 - Backdoor Command Execution
Описание: В IRC-сервере UnrealIRCd 3.2.8.1 обнаружен бэкдор. При отправке команды, содержащей системный вызов (например, AB; <команда>), сервер выполняет её в системе с правами пользователя, под которым запущен IRC-сервер.

Ссылка на Exploit-DB: https://www.exploit-db.com/exploits/16922

EDB-ID: 16922

Уязвимость 3: Samba 3.X - Usermap Script (CVE-2007-2447)
Описание: В Samba версий с 3.0.20 по 3.0.25rc3 существует уязвимость удаленного выполнения кода. Злоумышленник может передать команду через параметр username map script, что позволяет выполнить произвольные команды с правами суперпользователя.

Ссылка на Exploit-DB: https://www.exploit-db.com/exploits/16320

EDB-ID: 16320


<img width="883" height="740" alt="image" src="https://github.com/user-attachments/assets/7165e4b6-c1dd-4375-9b21-4d44d38aa5e3" />
