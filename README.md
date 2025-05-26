# Elevate-Labs-Internship
Contains the daily tasks assigned for the internship at Elevate Labs.

Day1
Installed Nmap and ran a scan on personal ip address
ip address- 192.168.1.7
ports: 
PORT     STATE SERVICE
135/tcp  open  msrpc
139/tcp  open  netbios-ssn
445/tcp  open  microsoft-ds
5357/tcp open  wsdapi

Services and potential security risks:

135/tcp (msrpc)
Used for Microsoft RPC (Remote Procedure Call).  
Risk: Can be used in DCOM exploits or lateral movement in internal networks.

139/tcp (netbios-ssn)
NetBIOS Session Service, used for Windows file and printer sharing.  
Risk: May expose file shares; often targeted in SMB relay or brute-force attacks.

445/tcp (microsoft-ds)  
Used for SMB over TCP, Windows file sharing.  
Risk: Vulnerable to exploits like EternalBlue (used in WannaCry). Disable if not needed.

5357/tcp (wsdapi)  
Web Services for Devices API. Enables automatic device discovery in a network.  
Risk: Not critical but could reveal device info to attackers.
