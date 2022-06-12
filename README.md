# OSCP-Prep-Notes

## İlk taramalar

nmap -sS -sV -v IP -p- #Tüm portlara stealth scan at.


gobuster dir -u http://192.168.174.101/ -w /usr/share/wordlists/dirbuster/directory-list-2.3-medium.txt -t 20 #dir taraması

#-x php,txt,py,c,js,bak,gz,tar,html,db,php.bak,key,jsp,asp # extension taraması

#-b 404 -s 201 # status code özelleştirme

## BOF

!mona config -set workingfolder c:\mona\%p

!mona bytearray -b "\x00"

!mona compare -f C:\mona\<PATH>\bytearray.bin -a <ESP_ADDRESS/EBX_ADDRESS>


## Privilege Escalation

wget "https://github.com/carlospolop/PEASS-ng/releases/latest/download/linpeas.sh" -O linpeas.sh

sudo -l
