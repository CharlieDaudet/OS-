

## A. Find me

🌞 **Trouver le chemin vers le répertoire personnel de votre utilisateur**
```bash
blaireaux-furtif@vbox:~$ pwd
/home/blaireaux-furtif
```
🌞 **Vérifier les permissions du répertoire personnel de votre utilisateurs**
```bash
blaireaux-furtif@vbox:~$ ls -l /home/  
total 4  
drwxr-xr-x 15 blaireaux-furtif blaireaux-furtif 4096 Nov 12 08:07 blaireaux-furtif  
```
🌞 **Trouver le chemin du fichier de configuration du serveur SSH**
```bash
root@vbox:~# find / -name sshd_config
/usr/share/openssh/sshd_config
/etc/ssh/sshd_config
```
# 2. Users

## A. Nouveau user

🌞 **Créer un nouvel utilisateur**

```bash
blaireaux-furtif@vbox:~$ su - root
Password:  
root@vbox:~# useradd -m marmotte -d /home/papier_alu   
root@vbox:~# passwd marmotte 
New password:  
Retype new password:  
passwd: password updated successfully  
```


## B. Infos enregistrées par le système:



🌞 **Prouver que cet utilisateur a été créé**
```bash
blaireaux-furtif@vbox:~$ cat /etc/passwd | grep marmotte
marmotte:x:1001:1001::/home/papier_alu:/bin/sh
```
🌞 **Déterminer le *hash* du password de l'utilisateur `marmotte`**  
```bash
blaireaux-furtif@vbox:~$  sudo grep marmotte /etc/shadow | cut -d: -f1,2,3,4,5,6  
marmotte:$y$j9T$SspDOY4DM5DEudC8Z.rQa1$vKzvjTfYgBFyqjx9ZKm2KpQX1qXBTf1stdc9vVjWg0C:20039:0:99999:7  
```



## D. Connexion sur le nouvel utilisateur

🌞 **Tapez une commande pour vous déconnecter : fermer votre session utilisateur**
```bash
root@vbox:~# exit  
logout
```
🌞 **Assurez-vous que vous pouvez vous connecter en tant que l'utilisateur `marmotte`**
```bash
blaireaux-furtif@vbox:~$ su - marmotte  
Password:
$
$ ls
```



🌞 **Lancer un processus `sleep`**
```bash
root@vbox:~# sleep 1000  
root@vbox:~# ps  
    PID TTY          TIME CMD  
   1115 pts/1    00:00:00 su  
   1116 pts/1    00:00:00 bash  
   1119 pts/1    00:00:00 ps  
root@vbox:~#
```
🌞 **Terminez le processus `sleep` depuis le deuxième terminal**
```bash
root@vbox:~# ps aux | grep sleep  
root        1070  0.0  0.0   5364   564 pts/0    S+   16:14   0:00 sleep 1000  
root        1129  0.0  0.0   6240   712 pts/1    S+   16:27   0:00 grep sleep  
root@vbox:~# kill 1070  
root@vbox:~# sleep 1000   
Terminated
```
## B. Tâche de fond

🌞 **Lancer un nouveau processus `sleep`, mais en tâche de fond**
```bash
root@vbox:~# sleep 1000 &  
[1] 1130
```
🌞 **Visualisez la commande en tâche de fond**
```bash
root@vbox:~# ps -ef | grep sleep  
root        1130    1067  0 16:29 pts/0    00:00:00 sleep 1000   
root        1138    1067  0 16:32 pts/0    00:00:00 grep sleep  
```
## C. Find paths


🌞 **Trouver le chemin où est stocké le programme `sleep`**
```bash
root@vbox:~# find / -name sleep  
/usr/lib/klibc/bin/sleep  
/usr/bin/sleep  
```
🌞 Tant qu'on est à chercher des chemins : **trouver les chemins vers tous les fichiers qui s'appellent `.bashrc`**
```bash
root@vbox:~# find / -name .bashrc  
/root/.bashrc  
/home/blaireaux-furtif/gameshell/gameshell/World/.bashrc  
/home/blaireaux-furtif/gameshell/gameshell.2/World/.bashrc  
/home/blaireaux-furtif/gameshell/gameshell.1/World/.bashrc  
/home/blaireaux-furtif/.bashrc  
/home/papier_alu/.bashrc  
/etc/skel/.bashrc  
```
## D. La variable PATH


🌞 **Vérifier que**
```bash
root@vbox:~# which ssh  
/usr/bin/ssh  
root@vbox:~# which ping  
/usr/bin/ping  
root@vbox:~# which sleep  
/usr/bin/sleep  
```
# 2. Paquets



🌞 **Installer le paquet `firefox`**

```bash
root@vbox:~# apt install firefox  
Reading package lists... Done  
Building dependency tree... Done  
Reading state information... Done  
Package firefox is not available, but is referred to by another package.  
This may mean that the package is missing, has been obsoleted, or
is only available from another source  

E: Package 'firefox' has no installation candidate
```

🌞 **Utiliser une commande pour lancer Firefox**
```bash
root@vbox:~# find / -name firefox  
/usr/share/bash-completion/completions/firefox  
/usr/bin/firefox  
```
🌞 **Mais aussi déterminer...**
```bash
root@vbox:~# cd /etc/  
root@vbox:/etc# ls  
adduser.conf            dhcp                    ifplugd          mailcap.order   protocols          subgid
adjtime                 dictionaries-common     init.d           manpath.config  pulse              subgid-
alsa                    discover.conf.d         initramfs-tools  mime.types      python3            subuid
alternatives            discover-modprobe.conf  inputrc          mke2fs.conf     python3.9          subuid-
anacrontab              dpkg                    ipp-usb          modprobe.d      rc0.d              sudo.conf
apache2                 e2scrub.conf            iproute2         modules         rc1.d              sudoers
apparmor                emacs                   issue            modules-load.d  rc2.d              sudoers.d
apparmor.d              environment             issue.net        motd            rc3.d              sudo_logsrvd.conf
apt                     environment.d           kernel           mtab            rc4.d              sv
avahi                   ethertypes              kernel-img.conf  nanorc          rc5.d              sysctl.conf
bash.bashrc             firefox-esr             ldap             netconfig       rc6.d              sysctl.d
bash_completion         fonts                   ld.so.cache      network         rcS.d              systemd
bindresvport.blacklist  fstab                   ld.so.conf       NetworkManager  reportbug.conf     terminfo
binfmt.d                fuse.conf               ld.so.conf.d     networks        resolv.conf        timezone
bluetooth               gai.conf                libao.conf       nftables.conf   rmt                timidity
ca-certificates         ghostscript             libaudit.conf    nsswitch.conf   rpc                tmpfiles.d
ca-certificates.conf    gimp                    libblockdev      openal          rsyslog.conf       ucf.conf
chatscripts             glvnd                   libnl-3          openni2         rsyslog.d          udev
console-setup           groff                   libpaper.d       opt             runit              udisks2
cron.d                  group                   libreoffice      os-release      sane.d             ufw
cron.daily              group-                  lightdm          PackageKit      security           update-motd.d
cron.hourly             grub.d                  lighttpd         pam.conf        selinux            UPower
cron.monthly            gshadow                 locale.alias     pam.d           sensors3.conf      usb_modeswitch.conf
crontab                 gshadow-                locale.gen       papersize       sensors.d          usb_modeswitch.d
cron.weekly             gss                     localtime        passwd          services           vdpau_wrapper.cfg
cups                    gtk-2.0                 logcheck         passwd-         shadow             vim
cupshelpers             gtk-3.0                 login.defs       perl            shadow-            vulkan
dbus-1                  hddtemp.db              logrotate.conf   pipewire        shells             wgetrc
dconf                   host.conf               logrotate.d      plymouth        skel               wpa_supplicant
debconf.conf            hostname                machine-id       polkit-1        snmp               X11
debian_version          hosts                   magic            ppp             speech-dispatcher  xattr.conf
default                 hosts.allow             magic.mime       profile         ssh                xdg
deluser.conf            hosts.deny              mailcap          profile.d       ssl                xfce4
root@vbox:/etc# find /etc -name apt  
/etc/logrotate.d/apt  
/etc/apt  
```
# IV. Poupée russe



🌞 **Récupérer le fichier `meow`**
```bash
blaireaux-furtif@vbox:~/Downloads$ wget https://gitlab.com/it4lik/b1-os/-/raw/main/tp/2/meow
--2024-11-13 10:18:27--  https://gitlab.com/it4lik/b1-os/-/raw/main/tp/2/meow  
Resolving gitlab.com (gitlab.com)... 172.65.251.78, 2606:4700:90:0:f22e:fbec:5bed:a9b9
Connecting to gitlab.com (gitlab.com)|172.65.251.78|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 18016947 (17M) [application/octet-stream]
Saving to: ‘meow’

meow                          100%[=================================================>]  17.18M  14.0MB/s    in 1.2s

2024-11-13 10:18:29 (14.0 MB/s) - ‘meow’ saved [18016947/18016947]

blaireaux-furtif@vbox:~/Downloads$ ls  
meow
```
🌞 **Trouver le dossier `dawa/`**
```bash
blaireaux-furtif@vbox:~/Downloads$ file meow  
meow: Zip archive data, at least v2.0 to extract  
blaireaux-furtif@vbox:~/Downloads$ mv meow meow.zip  
blaireaux-furtif@vbox:~/Downloads$ ls  
meow.zip  
blaireaux-furtif@vbox:~/Downloads$ unzip meow.zip  
Archive:  meow.zip  
  inflating: meow   
 blaireaux-furtif@vbox:~/Downloads$ ls  
meow.zip   
blaireaux-furtif@vbox:~/Downloads$ file meow.zip  
meow.zip: XZ compressed data  
blaireaux-furtif@vbox:~/Downloads$ mv meow.zip meow.xz  
blaireaux-furtif@vbox:~/Downloads$ ls  
meow.xz  
blaireaux-furtif@vbox:~/Downloads$ xz -d meow.xz  
blaireaux-furtif@vbox:~/Downloads$ ls  
meow  
blaireaux-furtif@vbox:~/Downloads$ file meow  
meow: bzip2 compressed data, block size = 900k  
blaireaux-furtif@vbox:~/Downloads$ mv meow meow.bzip2  
blaireaux-furtif@vbox:~/Downloads$ ls  
meow.bzip2  
blaireaux-furtif@vbox:~/Downloads$ bzip2 -d meow.bzip2  
bzip2: Can't guess original name for meow.bzip2 -- using meow.bzip2.out  
meow.out: RAR archive data, v5
blaireaux-furtif@vbox:~/Downloads$ sudo apt install unrar-free
blaireaux-furtif@vbox:~/Downloads$ unrar meow.out

unrar-free 0.1.3  Copyright (C) 2004  Ben Asselstine, Jeroen Dekkers


Extracting from /home/crea/Downloads/meow.out

Extracting  meow                                                      OK        
All OK
blaireaux-furtif@vbox:~/Downloads$ file meow
meow: gzip compressed data, from Unix, original size modulo 2^32 145049600 gzip compressed data, reserved method, has CRC, extra field, has comment, from FAT filesystem (MS-DOS, OS/2, NT), original size modulo 2^32 145049600
blaireaux-furtif@vbox:~/Downloads$ mv meow.gzip meow.gz
blaireaux-furtif@vbox:~/Downloads$ gzip -d meow.gz
blaireaux-furtif@vbox:~/Downloads$ file meow
meow: POSIX tar archive (GNU)
blaireaux-furtif@vbox:~/Downloads$ mv meow meow.tar
blaireaux-furtif@vbox:~/Downloads$ tar -xvf meow.tar 
```


🌞 **Dans le dossier `dawa/`, déterminer le chemin vers**
```bash
blaireaux-furtif@vbox:~/Downloads$ find dawa/ -type f -size 15M
dawa/folder31/19/file39  
blaireaux-furtif@vbox:~/Downloads$ find dawa/ -type f -name "cookie"  
dawa/folder14/25/cookie  
blaireaux-furtif@vbox:~/Downloads$ find dawa/ -type f -name ".*"
dawa/folder32/14/.hidden_file    
blaireaux-furtif@vbox:~/Downloads$ find dawa/ -type f -path "*/*/*/*/*/*"  
dawa/folder37/45/23/43/54/file43    
blaireaux-furtif@vbox:~/Downloads$ find dawa/ -type f -newermt 2014-01-01 ! -newermt 2015-01-01  
dawa/folder36/40/file43
blaireaux-furtif@vbox:~/Downloads$ find dawa/ -type f | xargs grep -L '[^7]'  
dawa/folder43/38/file41
```
