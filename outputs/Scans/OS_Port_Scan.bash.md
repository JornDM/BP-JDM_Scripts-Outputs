# Uitvoer 1: OS en Poort Scan
```bash
# nmap -O 192.168.50.0/24 -T3
Starting Nmap 7.92 ( https://nmap.org ) at 2023-05-14 13:55 EDT
Stats: 0:00:07 elapsed; 253 hosts completed (2 up), 2 undergoing SYN Stealth Scan
SYN Stealth Scan Timing: About 76.27% done; ETC: 13:55 (0:00:02 remaining)
Nmap scan report for bp-2223-jorn.hogent (192.168.50.2)
Host is up (0.00042s latency).
Not shown: 985 closed tcp ports (reset)
PORT     STATE SERVICE
22/tcp   open  ssh
53/tcp   open  domain
80/tcp   open  http
88/tcp   open  kerberos-sec
135/tcp  open  msrpc
139/tcp  open  netbios-ssn
389/tcp  open  ldap
443/tcp  open  https
445/tcp  open  microsoft-ds
464/tcp  open  kpasswd5
593/tcp  open  http-rpc-epmap
636/tcp  open  ldapssl
1723/tcp open  pptp
3268/tcp open  globalcatLDAP
3269/tcp open  globalcatLDAPssl
MAC Address: 08:00:27:79:C5:C4 (Oracle VirtualBox virtual NIC)
Device type: general purpose|specialized
Running: Microsoft Windows 2012|10|2016|Vista|7|2008 (92%)
OS CPE: cpe:/o:microsoft:windows_server_2012:r2 cpe:/o:microsoft:windows_10 cpe:/o:microsoft:windows_server_2016 cpe:/o:microsoft:windows_10:1511 cpe:/o:microsoft:windows_vista::sp1:home_premium cpe:/o:microsoft:windows_7 cpe:/o:microsoft:windows_server_2008
Aggressive OS guesses: Microsoft Windows Server 2012 R2 (92%), Microsoft Windows 10 1709 - 1909 (89%), Microsoft Windows Server 2016 (87%), Microsoft Windows 10 1511 (86%), Microsoft Windows Vista Home Premium SP1, Windows 7, or Windows Server 2008 (86%), Microsoft Windows Server 2012 Data Center (86%), Microsoft Windows 7 SP1 (86%), Microsoft Windows 10 1709 - 1803 (86%), Microsoft Windows 7 SP1 or Windows Server 2008 SP2 (86%), Microsoft Windows Windows 7 SP1 (86%)
No exact OS matches for host (test conditions non-ideal).
Network Distance: 1 hop

Nmap scan report for client.bp-2223-jorn.hogent (192.168.50.101)
Host is up (0.00034s latency).
Not shown: 996 closed tcp ports (reset)
PORT    STATE SERVICE
22/tcp  open  ssh
135/tcp open  msrpc
139/tcp open  netbios-ssn
445/tcp open  microsoft-ds
MAC Address: 08:00:27:13:A4:2E (Oracle VirtualBox virtual NIC)
Device type: general purpose
Running: Microsoft Windows 10
OS CPE: cpe:/o:microsoft:windows_10
OS details: Microsoft Windows 10 1709 - 1909
Network Distance: 1 hop

Nmap scan report for 192.168.50.5
Host is up (0.000026s latency).
Not shown: 999 closed tcp ports (reset)
PORT   STATE SERVICE
22/tcp open  ssh
Device type: general purpose
Running: Linux 2.6.X
OS CPE: cpe:/o:linux:linux_kernel:2.6.32
OS details: Linux 2.6.32
Network Distance: 0 hops

OS detection performed. Please report any incorrect results at https://nmap.org/submit/ .
Nmap done: 256 IP addresses (3 hosts up) scanned in 15.25 seconds
```