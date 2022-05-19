# OSCP-Prep-Notes

## İlk taramalar

nmap -sS -sV -v IP -p- #Tüm portlara stealth scan at.


gobuster dir -u http://192.168.174.101/ -w /usr/share/wordlists/dirbuster/directory-list-2.3-medium.txt -t 20 #dir taraması

#-x php,txt,py,c,js,bak,gz,tar,html,db,php.bak,key,jsp,asp # extension taraması

#-b 404 -s 201 # status code özelleştirme




## Privilege Escalation

wget "https://github.com/carlospolop/PEASS-ng/releases/latest/download/linpeas.sh" -O linpeas.sh

sudo -l
