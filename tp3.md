# I. Utilisateurs

## 1. Liste des users


🌞 **Afficher la ligne du fichier qui concerne votre utilisateur**
```bash
blaireaux-furtif@vbox:~$ cat /etc/passwd | grep blaireaux-furtif
blaireaux-furtif:x:1000:1000:Blaireaux-Furtif,,,:/home/blaireaux-furtif:/bin/bash
```
🌞 **Afficher la ligne du fichier qui concerne votre utilisateur ET celle de `root` en même temps**
```bash
blaireaux-furtif@vbox:~$ cat /etc/passwd | grep -e blaireaux-furtif -e root  
root:x:0:0:root:/root:/bin/bash  
blaireaux-furtif:x:1000:1000:Blaireaux-Furtif,,,:/home/blaireaux-furtif:/bin/bash  
```
🌞 **Afficher la liste des groupes d'utilisateurs de la *machine***
```bash
blaireaux-furtif@vbox:~$ cat /etc/group  
root:x:0:  
daemon:x:1:  
bin:x:2:  
sys:x:3:  
adm:x:4:  
tty:x:5:  
disk:x:6:  
lp:x:7:  
mail:x:8:  
news:x:9:  
uucp:x:10:  
man:x:12:  
proxy:x:13:  
kmem:x:15:  
dialout:x:20:  
fax:x:21:  
voice:x:22:  
cdrom:x:24:blaireaux-furtif  
floppy:x:25:blaireaux-furtif  
tape:x:26:  
sudo:x:27:blaireaux-furtif  
audio:x:29:pulse,blaireaux-furtif  
dip:x:30:blaireaux-furtif  
www-data:x:33:  
backup:x:34:  
operator:x:37:  
list:x:38:  
irc:x:39:  
src:x:40:  
gnats:x:41:  
shadow:x:42:  
utmp:x:43:  
video:x:44:blaireaux-furtif  
sasl:x:45:  
plugdev:x:46:blaireaux-furtif  
staff:x:50:  
games:x:60:  
users:x:100:  
nogroup:x:65534:  
systemd-journal:x:101:  
systemd-network:x:102:  
systemd-resolve:x:103:  
input:x:104:  
kvm:x:105:  
render:x:106:  
crontab:x:107:  
netdev:x:108:blaireaux-furtif  
messagebus:x:109:  
systemd-timesync:x:110:  
ssh:x:111:  
bluetooth:x:112:blaireaux-furtif  
ssl-cert:x:113:  
avahi-autoipd:x:114:  
rtkit:x:115:  
avahi:x:116:  
lpadmin:x:117:blaireaux-furtif  
pulse:x:118:  
pulse-access:x:119:  
scanner:x:120:saned,blaireaux-furtif  
saned:x:121:  
colord:x:122:  
lightdm:x:123:  
blaireaux-furtif:x:1000:  
systemd-coredump:x:999:  
marmotte:x:1001:  

```

🌞 **Afficher la ligne du fichier qui concerne votre utilisateur ET celle de `root` en même temps**
```bash
blaireaux-furtif@vbox:~$ grep -e blaireaux-furtif -e root /etc/passwd | cut -d: -f1,6  
root:/root  
blaireaux-furtif:/home/blaireaux-furtif  
```
## 2. Hash des passwords


🌞 **Afficher la ligne qui contient le hash du mot de passe de votre utilisateur**
```bash
blaireaux-furtif@vbox:~$ sudo grep blaireaux-furtif /etc/shadow | cut -d: -f1,2,3,4,5,6  
blaireaux-furtif:$y$j9T$Frx8r7zZmtvkbPmkAcJ4x/$ufIggp9ILMtFLrO1zJ7IERH.sWscwAp5FhO4YiYWEdD:20034:0:99999:7
```
## 3. Sudo


🌞 **Faites en sorte que votre utilisateur puisse taper** 
```bash
blaireaux-furtif@vbox:~$ sudo usermod -aG sudo blaireaux-furtif  
blaireaux-furtif@vbox:~$ sudo su blaireaux-furtif
blaireaux-furtif@vbox:~$ sudo whoami  
root  
```
### B. Practice

🌞 **Créer un groupe d'utilisateurs**  
```bash
blaireaux-furtif@vbox:~$ sudo groupadd stronk_admins
```

🌞 **Créer un utilisateur**
```bash
blaireaux-furtif@vbox:~$ sudo useradd -m imbob -d /home/stronk_admins  
blaireaux-furtif@vbox:~$ sudo passwd imbob  
New password:  
Retype new password:  
passwd: password updated successfully
```
🌞 **Prouver que l'utilisateur `imbob` est créé**
```bash
blaireaux-furtif@vbox:~$ cat /etc/passwd | grep imbob  
imbob:x:1002:1003::/home/stronk_admins:/bin/sh
```
🌞 **Prouver que l'utilisateur `imbob` a un password défini**
```bash
blaireaux-furtif@vbox:~$ sudo grep imbob /etc/shadow | cut -d: -f1,2,3,4,5,6  
imbob:$y$j9T$WPLFhAkvp88M6EPmZ4Aa4.$.nVeAUwEXIgUOdb2mxUUA3Wb0b8zkWMiqYtUHNoMUS4:20042:0:99999:7
```

🌞 **Prouver que l'utilisateur `imbob` appartient au groupe `stronk_admins`**

```bash
blaireaux-furtif@vbox:~$ sudo cat  /etc/group | grep imbob
imbob:x:1003:
```

🌞 **Créer un deuxième utilisateur**

```bash
blaireaux-furtif@vbox:~$ sudo useradd imnotbobsorry
blaireaux-furtif@vbox:~$ sudo passwd imnotbobsorry
New password:
Retype new password:
passwd: password updated successfully
``` 

🌞 **Modifier la configuration de `sudo` pour que**



🌞 **Créer le dossier `/home/goodguy`** (avec une commande)
```bash
blaireaux-furtif@vbox:~$ sudo mkdir goodguy

```
🌞 **Changer le répertoire personnel de `imbob`**
```bash
blaireaux-furtif@vbox:~$ sudo usermod -d /home/goodguy imbob
blaireaux-furtif@vbox:~$ cat /etc/passwd | grep imbob
imbob:x:1002:1003::/home/goodguy:/bin/sh

```
🌞 **Créer le dossier `/home/badguy`**
```bash
blaireaux-furtif@vbox:~$ sudo mkdir badguy
```
🌞 **Changer le répertoire personnel de `imnotbobsorry`**
```bash
blaireaux-furtif@vbox:~$ sudo usermod -d /home/badguy imnotbobsorry
blaireaux-furtif@vbox:~$ cat /etc/passwd | grep imnotbobsorry
imnotbobsorry:x:1003:1004::/home/badguy:/bin/sh
```
🌞 **Prouver que les permissions du dossier `/home/gooduy` sont incohérentes**



🌞 **Modifier les permissions de `/home/goodguy`**

```bash
blaireaux-furtif@vbox:~$ ls -l | grep goodguy
drwxr-xr-x 2 root             root             4096 Nov 20 11:58 goodguy
blaireaux-furtif@vbox:~$ sudo chown imbob:imbob goodguy -R
[sudo] password for blaireaux-furtif:
blaireaux-furtif@vbox:~$ ls -l | grep goodguy
drwxr-xr-x 2 imbob            imbob            4096 Nov 20 11:58 goodguy
blaireaux-furtif@vbox:~$
```
🌞 **Modifier les permissions de `/home/badguy`**

```bash 
blaireaux-furtif@vbox:~$ sudo chown imnotbobsorry:imnotbobsorry badguy/ -R
blaireaux-furtif@vbox:~$ ls -l | grep badguy
drwxr-xr-x 2 imnotbobsorry    imnotbobsorry    4096 Nov 20 12:20 badguy

```

🌞 **Connectez-vous sur l'utilisateur `imbob`**


🌞 **Connectez-vous sur l'utilisateur `imnotbobsorry`**



# II. Processes

## 1. Jouer avec la commande ps

🌞 **Affichez les processus `bash`**
```bash
blaireaux-furtif@vbox:~$ ps -ef | grep bash
blairea+    1065    1064  0 11:40 pts/1    00:00:00 -bash
blairea+    1092    1087  0 11:42 pts/0    00:00:00 bash
blairea+    1277    1276  0 12:38 pts/2    00:00:00 -bash
blairea+    1323    1277  0 12:50 pts/2    00:00:00 grep bash
```
🌞 **Affichez tous les processus lancés par votre utilisateur**

```bash
blaireaux-furtif@vbox:~$ ps -ef | grep blaireaux-furtif
root        1058     630  0 11:40 ?        00:00:00 sshd-session: blaireaux-furtif [priv]
blairea+    1064    1058  0 11:40 ?        00:00:01 sshd-session: blaireaux-furtif@pts/1
root        1270     630  0 12:38 ?        00:00:00 sshd-session: blaireaux-furtif [priv]
blairea+    1276    1270  0 12:38 ?        00:00:00 sshd-session: blaireaux-furtif@pts/2
blairea+    1325    1277  0 12:51 pts/2    00:00:00 grep blaireaux-furtif
```

🌞 **Affichez le top 5 des processus qui utilisent le plus de RAM**

```bash
blaireaux-furtif@vbox:~$ ps aux --sort=-rss | head -n 6 | tail -n 5 | tr -s ' ' | cut -d ' ' -f 11,6
90640 /usr/sbin/lightdm-gtk-greeter
74976 xfwm4
73148 /usr/lib/xorg/Xorg
56356 /usr/lib/xorg/Xorg
46916 xfdesktop
```


🌞 **Affichez le *PID* du processus du service SSH**

```bash
blaireaux-furtif@vbox:~$ ps -ef | grep sshd
root         630       1  0 11:37 ?        00:00:00 sshd: /usr/sbin/sshd -D [listener] 0 of 10-100 startups
root        1058     630  0 11:40 ?        00:00:00 sshd-session: blaireaux-furtif [priv]
blairea+    1064    1058  0 11:40 ?        00:00:01 sshd-session: blaireaux-furtif@pts/1
root        1270     630  0 12:38 ?        00:00:00 sshd-session: blaireaux-furtif [priv]
blairea+    1276    1270  0 12:38 ?        00:00:00 sshd-session: blaireaux-furtif@pts/2
blairea+    1333    1277  0 12:54 pts/2    00:00:00 grep sshd
```

🌞 **Affichez le nom du processus avec l'identifiant le plus petit**

```bash
blaireaux-furtif@vbox:~$ ps -ef --sort pid | head -2
UID          PID    PPID  C STIME TTY          TIME CMD
root           1       0  0 11:37 ?        00:00:00 /sbin/init
```

## 2. Parent, enfant, et meurtre



🌞 **Déterminer le *PID* de votre shell actuel**
```bash
blaireaux-furtif@vbox:~$ ps -ef | grep bash
blairea+     759     754  0 08:29 pts/0    00:00:00 -bash
```
🌞 **Déterminer le *PPID* de votre shell actuel**

```bash
blaireaux-furtif@vbox:~$ ps -p 1157
    PID TTY          TIME CMD

```

🌞 **Déterminer le nom de ce *processus***



🌞 **Lancer un *processus* `sleep 9999` en tâche de fond**

```bash
blaireaux-furtif@vbox:~$ ps -ef | grep sleep
blairea+     777     759  0 08:39 pts/0    00:00:00 grep sleep
```

🌞 **Fermez votre session SSH**

```bash
blaireaux-furtif@vbox:~$ exit
logout
Connection to 192.168.63.20 closed.
```



