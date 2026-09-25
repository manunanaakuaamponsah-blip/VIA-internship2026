# Metasploitable2 Exploitation Report

**Name:**   MANU NANA AKUA AMPONSAH**
Index Number:** <Your Index Number>
**Date:** <Today's Date>
**Target IP:** 192.168.30.4
**Attacker OS / Tools:** Kali Linux, nmap 7.99,  mount (NFS client)

---

## Reconnaissance Summary

Command used: `nmap -sV 192.168.30.4`

This scan found 23 open ports on the target, revealing a wide range of outdated and
misconfigured services — including an FTP server with a known backdoor, an
unauthenticated NFS export of the whole filesystem, a raw root shell left open on
a non-standard port, an old Samba version vulnerable to remote code execution, and
a database with no root password. Full output below:
Nmap scan report for 192.168.30.4
Host is up (0.018s latency).
Not shown: 977 closed tcp ports (reset)
PORT STATE SERVICE VERSION
21/tcp open ftp vsftpd 2.3.4
22/tcp open ssh OpenSSH 4.7p1 Debian 8ubuntu1 (protocol 2.0)
23/tcp open telnet Linux telnetd
25/tcp open smtp Postfix smtpd
53/tcp open domain ISC BIND 9.4.2
80/tcp open http Apache httpd 2.2.8 ((Ubuntu) DAV/2)
111/tcp open rpcbind 2 (RPC 
#100000)
139/tcp open netbios-ssn Samba smbd 3.X - 4.X (workgroup: WORKGROUP)
445/tcp open netbios-ssn Samba smbd 3.X - 4.X (workgroup: WORKGROUP)
512/tcp open exec netkit-rsh rexecd
513/tcp open login
514/tcp open shell Netkit rshd
1099/tcp open java-rmi GNU Classpath grmiregistry
1524/tcp open bindshell Metasploitable root shell
2049/tcp open nfs 2-4 (RPC 
#100003)
2121/tcp open ftp ProFTPD 1.3.1
3306/tcp open mysql MySQL 5.0.51a-3ubuntu5
5432/tcp open postgresql PostgreSQL DB 8.3.0 - 8.3.7
5900/tcp open vnc VNC (protocol 3.3)
6000/tcp open X11 (access denied)
6667/tcp open irc UnrealIRCd
8009/tcp open ajp13 Apache Jserv (Protocol v1.3)
8180/tcp open http Apache Tomcat/Coyote JSP engine 1.1
MAC Address: 08:00:27:DD:2B:4D (Oracle VirtualBox virtual NIC)
Service Info: Hosts: metasploitable.localdomain, irc.Metasploitable.LAN; OSs: Unix, Linux
