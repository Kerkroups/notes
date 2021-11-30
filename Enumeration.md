## NMAP
**Full TCP port, service version detect, default script scan**: nmap -Pn -p- -sV -sC <IP> -oA <path/filename>
**Full UDP port, service version detect, default script scan**: nmap -Pn -sU -p- -sV -sC <IP> -oA <path/filename>
**NMAP scripts for SMB enumeration**: cd /usr/share/nmap/scripts; ls |  grep smb
**NMAP SMB enumeration example**: nmap --script smb-os-discovery.nse -p445 <target>


