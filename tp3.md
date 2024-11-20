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

- la liste des groupes et de leurs membres c'est dans `/etc/group`
- affichez une seule ligne

🌞 **Créer un deuxième utilisateur**

- il devra s'appeler `imnotbobsorry`
- il devra avoir un mot de passe défini
- il devra appartenir au groupe `imnotbobsorry` ET `stronk_admins`

🌞 **Modifier la configuration de `sudo` pour que**

- les membres du groupes `stronk_admins` ait le droit de taper des commandes `apt` en tant que `root`
- l'utilisateur `imbob` peut taper n'importe quelle commande en tant que `root`

🌞 **Créer le dossier `/home/goodguy`** (avec une commande)

🌞 **Changer le répertoire personnel de `imbob`**

- avec une commande `usermod`, définissez ce dossier comme le *répertoire personnel* de `imbob`
- prouvez que le changement est effectif en affichant le contenu du fichier `passwd`

> "*Répertoire personnel*" ça se dit "*home directory*" en anglais, on dit souvent juste "*homedir*" pour faire court. Sous Windows, pour rappel, les *homedirs* des utilisateurs sont stockés par défaut dans `C:/Users/<USER>`, pour Linux c'est donc `/home/<USER>` par défaut.

🌞 **Créer le dossier `/home/badguy`**

🌞 **Changer le répertoire personnel de `imnotbobsorry`**

- avec une commande `usermod`, définissez ce dossier `/home/badguy` comme le *répertoire personnel* de `imnotbobsorry`
- prouvez que le changement est effectif en affichant le contenu du fichier `passwd`

> Si t'essaies de te connecter en tant que `imbob` là en tapant la commande `su - imbob` il va sûrement se passer des trucs chelous... En tout cas `imbob` ne pourra pas y créer des fichiers. En effet, tu as sûrement du utiliser les droits de `root` pour créer le dossier, donc actuellement, le *répertoire personnel* de `imbob`, il appartient à `root`... Donc `imbob` n'a aucun droit dans son propre *répertoire personnel*, chelou.

🌞 **Prouver que les permissions du dossier `/home/gooduy` sont incohérentes**

- ça n'appartient pas à l'utilisateur `imbob`
- ce qui est chelou, l'utilisateur il peut se connecter, mais il peut pas créer quoique ce soit dans son propre *répertoire personnel*, genre dans son propre dossier "Mes Documents"

🌞 **Modifier les permissions de `/home/goodguy`**

- le dossier doit appartenir à `imbob`
- pareil pour tout son contenu
- avec une commande `chown` (il faudra mettre options et arguments)

🌞 **Modifier les permissions de `/home/badguy`**

- le dossier doit appartenir à `imnotbobsorry`
- pareil pour tout son contenu

🌞 **Connectez-vous sur l'utilisateur `imbob`**

- il faut utiliser la commande `su - <USER>` pour ouvrir une nouvelle session en tant qu'un utilisateur
  - ça doit sortir aucun message d'erreur particulier
- si tu fais `pwd` tu devrais être dans le dossier `/home/goodguy` tout de suite après connexion (le *répertoire personnel* de `imbob` !)
- si tu fais `sudo echo meow` ou n'importe quelle autre commande avec `sudo`, ça devrait fonctionner

🌞 **Connectez-vous sur l'utilisateur `imnotbobsorry`**

- il faut utiliser la commande `su - <USER>` pour ouvrir une nouvelle session en tant qu'un utilisateur
  - ça doit sortir aucun message d'erreur particulier
- si tu fais `pwd` tu devrais être dans le dossier `/home/badguy` tout de suite après 
- si tu fais `sudo echo meow` ou n'importe quelle autre commande avec `sudo`, ça ne devrait fonctionner PAS fonctionner
  - sauf les commandes `sudo apt...`, essaie un `sudo apt update` pour voir ?
