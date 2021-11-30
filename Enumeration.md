## NMAP
1) **Full TCP port, service version detect, default script scan**: nmap -Pn -p- -sV -sC <IP> -oA <path/filename>    
2) **Full UDP port, service version detect, default script scan**: nmap -Pn -sU -p- -sV -sC <IP> -oA <path/filename>    
3) **NMAP scripts for SMB enumeration**: cd /usr/share/nmap/scripts; ls |  grep smb    
4) **NMAP SMB enumeration example**: nmap --script smb-os-discovery.nse -p445 <target>    
                                     nmap -sU -sS --script smb-enum-shares.nse -p U:137,T:139 <host>    
## SMB
1) **Enumerate hostname**: nmblookup -A [ip]    
2) **List shares**:    
      smbmap -H [ip/hostname]    
      smbmap -H [ip] -d [domain] -u [user] -p [password]    
      smbclient -L //[ip] -N    
      nmap --script smb-enum-shares -p 139,445 [ip]    
3) **Null session**:    
      rpcclient -U "" -N [ip]    
      smbclient \\\\[ip]\\[share name]    
4) **Overall Scan**:    
      enum4linux -a [ip]    
## Web
1) **Common scan**:
  - nikto -h [hostname/ip]
  - **Directory recon**:     
                         gobuster dir -u [http://ip/hostname] -w wordlist.txt    
                         ffuf -w wordlist:FUZZ -u [http://ip/hostname]/FUZZ    
  - **Virtual host recon**:     
                         gobuster vhost -u [http://ip/hostname] -w wordlist.txt    
                         ffuf -w wordlist:FUZZ -u [http://ip/] -H "FUZZ.hostname.com" -fs/fc    
  - **CMS tools**:    
    - wpscan    
    - droopescan    
  
