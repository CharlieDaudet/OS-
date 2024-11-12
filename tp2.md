

## A. Find me

🌞 **Trouver le chemin vers le répertoire personnel de votre utilisateur**

blaireaux-furtif@vbox:~$ pwd
/home/blaireaux-furtif

🌞 **Vérifier les permissions du répertoire personnel de votre utilisateurs**

blaireaux-furtif@vbox:~$ ls -l /home/
total 4
drwxr-xr-x 15 blaireaux-furtif blaireaux-furtif 4096 Nov 12 08:07 blaireaux-furtif

🌞 **Trouver le chemin du fichier de configuration du serveur SSH**

root@vbox:~# find / -name sshd_config
/usr/share/openssh/sshd_config
/etc/ssh/sshd_config

# 2. Users

## A. Nouveau user

🌞 **Créer un nouvel utilisateur**

blaireaux-furtif@vbox:~$ su - root
Password:
root@vbox:~# useradd -m marmotte -d /home/papier_alu
useradd: user 'marmotte' already exists
root@vbox:~# userdel 'marmotte'
root@vbox:~# useradd -m marmotte -d /home/papier_alu
root@vbox:~# passwd
New password:
Retype new password:
passwd: password updated successfully

## B. Infos enregistrées par le système:



🌞 **Prouver que cet utilisateur a été créé**

root@vbox:~# cat /home/papier_alu | grep marmotte
cat: /home/papier_alu: Is a directory

🌞 **Déterminer le *hash* du password de l'utilisateur `marmotte`**

root@vbox:~# cat /home/papier_alu/ | grep hash
cat: /home/papier_alu/: Is a directory



## D. Connexion sur le nouvel utilisateur

🌞 **Tapez une commande pour vous déconnecter : fermer votre session utilisateur**

root@vbox:~# exit
logout

🌞 **Assurez-vous que vous pouvez vous connecter en tant que l'utilisateur `marmotte`**

blaireaux-furtif@vbox:~$ su - marmotte
Password:
$
$ ls




🌞 **Lancer un processus `sleep`**

root@vbox:~# sleep 1000
root@vbox:~# ps
    PID TTY          TIME CMD
   1115 pts/1    00:00:00 su
   1116 pts/1    00:00:00 bash
   1119 pts/1    00:00:00 ps
root@vbox:~#

🌞 **Terminez le processus `sleep` depuis le deuxième terminal**

root@vbox:~# ps aux | grep sleep
root        1070  0.0  0.0   5364   564 pts/0    S+   16:14   0:00 sleep 1000
root        1129  0.0  0.0   6240   712 pts/1    S+   16:27   0:00 grep sleep
root@vbox:~# kill 1070
root@vbox:~# sleep 1000
Terminated
## B. Tâche de fond

🌞 **Lancer un nouveau processus `sleep`, mais en tâche de fond**

root@vbox:~# sleep 1000 &
[1] 1130

🌞 **Visualisez la commande en tâche de fond**

root@vbox:~# ps -ef | grep sleep
root        1130    1067  0 16:29 pts/0    00:00:00 sleep 1000
root        1138    1067  0 16:32 pts/0    00:00:00 grep sleep

## C. Find paths


🌞 **Trouver le chemin où est stocké le programme `sleep`**

root@vbox:~# find / -name sleep
/usr/lib/klibc/bin/sleep
/usr/bin/sleep

🌞 Tant qu'on est à chercher des chemins : **trouver les chemins vers tous les fichiers qui s'appellent `.bashrc`**

root@vbox:~# find / -name .bashrc
/root/.bashrc
/home/blaireaux-furtif/gameshell/gameshell/World/.bashrc
/home/blaireaux-furtif/gameshell/gameshell.2/World/.bashrc
/home/blaireaux-furtif/gameshell/gameshell.1/World/.bashrc
/home/blaireaux-furtif/.bashrc
/home/papier_alu/.bashrc
/etc/skel/.bashrc

## D. La variable PATH


🌞 **Vérifier que**
root@vbox:~# which ssh
/usr/bin/ssh
root@vbox:~# which ping
/usr/bin/ping
root@vbox:~# which sleep
/usr/bin/sleep
# 2. Paquets



🌞 **Installer le paquet `firefox`**

root@vbox:~# apt install firefox
Reading package lists... Done
Building dependency tree... Done
Reading state information... Done
Package firefox is not available, but is referred to by another package.
This may mean that the package is missing, has been obsoleted, or
is only available from another source

E: Package 'firefox' has no installation candidate
root@vbox:~#

🌞 **Utiliser une commande pour lancer Firefox**

root@vbox:~# find / -name firefox
/usr/share/bash-completion/completions/firefox
/usr/bin/firefox

🌞 **Mais aussi déterminer...**

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
