## NMAP
1) **Full TCP port, service version detect, default script scan**: nmap -Pn -p- -sV -sC <IP> -oA <path/filename>    
2) **Full UDP port, service version detect, default script scan**: nmap -Pn -sU -p- -sV -sC <IP> -oA <path/filename>    
3) **NMAP scripts for SMB enumeration**: cd /usr/share/nmap/scripts; ls |  grep smb    
4) **NMAP SMB enumeration example**: nmap --script smb-os-discovery.nse -p445 <target>    


