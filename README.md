# LFI2RCE

Local File Inclusion to Remote Code Execution  
Automated proof of concept tool to poison ssh and apache2 log files  
linux ssh (/var/log/auth.log)  
linux apache2 (/var/log/apache2/access.log)  
windows xampp/apache (C:/xampp/apache/logs/access.log)
use --windows option for windows hosts

# Change listener parameters in source code that are hardcoded
<pre>
#########################################################
attacker_ip="10.0.2.15"   # CHANGE ME BY ATTACKER IP    #
attacker_port="4444"      # CHANGE ME BY ATTACKER PORT  #
#########################################################
</pre>

# Pre-Requisites: 
* You must be able to read files in the system(Local File Inclusion) and you must know the target url  
* Services log files must be readable,writeable and executable by every user in the system.  

# Screenshots
![alt text](https://github.com/0bfxGH0ST/LFI2RCE/blob/main/screenshots/screenshot0000.png)  
ssh auth.log case  
![alt text](https://github.com/0bfxGH0ST/LFI2RCE/blob/main/screenshots/screenshot001.png)  
apache2 access.log case  
![alt text](https://github.com/0bfxGH0ST/LFI2RCE/blob/main/screenshots/screenshot002.png)  
Valid for Windows too if enable --windows option (you should tune folders)
![alt text](https://github.com/0bfxGH0ST/LFI2RCE/blob/main/screenshots/screenshot003.png)  

Note: Windows payload was tested with Windows Defender disabled for testing purposes, if you want bypass antivirus you must to learn how to obfuscate code.
