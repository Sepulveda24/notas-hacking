Descripción
We found this [file](https://jupiter.challenges.picoctf.org/static/ab30fcb7d47364b4190a7d3d40edb551/mystery). Recover the flag.


Hints:
1.⁠ ⁠Try fixing the file header


Solución 1

Con Terminal de Linux
┌──(parallels㉿kali-linux-2022-2)-[~/Desktop]
└─$ wget https://jupiter.challenges.picoctf.org/static/ab30fcb7d47364b4190a7d3d40edb551/mystery
--2025-04-09 14:47:57--  https://jupiter.challenges.picoctf.org/static/ab30fcb7d47364b4190a7d3d40edb551/mystery
Resolving jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)... 3.131.60.8
Connecting to jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)|3.131.60.8|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 202940 (198K) [application/octet-stream]
Saving to: ‘mystery’

mystery             100%[================>] 198.18K  1.10MB/s    in 0.2s    

2025-04-09 14:47:58 (1.10 MB/s) - ‘mystery’ saved [202940/202940]

                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~/Desktop]
└─$ ls
 firefox-esr   mystery  'Parallels Shared Folders'
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~/Desktop]
└─$ file mystery
mystery: data
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~/Desktop]
└─$ hexeditor mystery   
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~/Desktop]
└─$ file mystery     
mystery: PNG image data, 1642 x 1095, 8-bit/color RGB, non-interlaced
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~/Desktop]
└─$ open mystery   
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~/Desktop]
└─$ sudo apt insall pngcheck                    
[sudo] password for parallels: 
E: Invalid operation insall
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~/Desktop]
└─$ sudo apt install pngcheck
Reading package lists... Done
Building dependency tree... Done
Reading state information... Done
The following NEW packages will be installed:
  pngcheck
0 upgraded, 1 newly installed, 0 to remove and 8 not upgraded.
Need to get 62.5 kB of archives.
After this operation, 206 kB of additional disk space will be used.
Err:1 http://http.kali.org/kali kali-rolling/main arm64 pngcheck arm64 3.0.2-2
  404  Not Found [IP: 54.39.128.230 80]
E: Failed to fetch http://http.kali.org/kali/pool/main/p/pngcheck/pngcheck_3.0.2-2_arm64.deb  404  Not Found [IP: 54.39.128.230 80]
E: Unable to fetch some archives, maybe run apt-get update or try with --fix-missing?
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~/Desktop]
└─$ ^[[200~sudo apt update
zsh: bad pattern: ^[[200~sudo
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~/Desktop]
└─$ ~sudo apt update

Command '~sudo' not found, did you mean:
  command 'sudo' from deb sudo
  command 'sudo' from deb sudo-ldap
Try: sudo apt install <deb name>
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~/Desktop]
└─$ sudo apt update 

Get:1 http://kali.download/kali kali-rolling InRelease [41.5 kB]
Err:1 http://kali.download/kali kali-rolling InRelease
  The following signatures were invalid: EXPKEYSIG ED444FF07D8D0BF6 Kali Linux Repository <devel@kali.org>
Fetched 41.5 kB in 1s (69.0 kB/s)
Reading package lists... Done
Building dependency tree... Done
Reading state information... Done
8 packages can be upgraded. Run 'apt list --upgradable' to see them.
W: An error occurred during the signature verification. The repository is not updated and the previous index files will be used. GPG error: http://kali.download/kali kali-rolling InRelease: The following signatures were invalid: EXPKEYSIG ED444FF07D8D0BF6 Kali Linux Repository <devel@kali.org>
W: Failed to fetch http://http.kali.org/kali/dists/kali-rolling/InRelease  The following signatures were invalid: EXPKEYSIG ED444FF07D8D0BF6 Kali Linux Repository <devel@kali.org>
W: Some index files failed to download. They have been ignored, or old ones used instead.
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~/Desktop]
└─$ sudo apt install pngcheck
Reading package lists... Done
Building dependency tree... Done
Reading state information... Done
The following NEW packages will be installed:
  pngcheck
0 upgraded, 1 newly installed, 0 to remove and 8 not upgraded.
Need to get 62.5 kB of archives.
After this operation, 206 kB of additional disk space will be used.
Err:1 http://http.kali.org/kali kali-rolling/main arm64 pngcheck arm64 3.0.2-2
  404  Not Found [IP: 54.39.128.230 80]
E: Failed to fetch http://http.kali.org/kali/pool/main/p/pngcheck/pngcheck_3.0.2-2_arm64.deb  404  Not Found [IP: 54.39.128.230 80]
E: Unable to fetch some archives, maybe run apt-get update or try with --fix-missing?
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~/Desktop]
└─$ cd ..     
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~]
└─$ ls
 Desktop     Downloads   Pictures   Templates   Videos
 Documents   Music       Public    '~.venv'
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~]
└─$ cd Dow      
cd: no such file or directory: Dow
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~]
└─$ cd Dowloads
cd: no such file or directory: Dowloads
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~]
└─$ cd dowloads
cd: no such file or directory: dowloads
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~]
└─$ ls
 Desktop     Downloads   Pictures   Templates   Videos
 Documents   Music       Public    '~.venv'
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~]
└─$ cd Downloads 
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~/Downloads]
└─$ sudo apt install pngcheck
Reading package lists... Done
Building dependency tree... Done
Reading state information... Done
The following NEW packages will be installed:
  pngcheck
0 upgraded, 1 newly installed, 0 to remove and 8 not upgraded.
Need to get 62.5 kB of archives.
After this operation, 206 kB of additional disk space will be used.
Err:1 http://http.kali.org/kali kali-rolling/main arm64 pngcheck arm64 3.0.2-2
  404  Not Found [IP: 54.39.128.230 80]
E: Failed to fetch http://http.kali.org/kali/pool/main/p/pngcheck/pngcheck_3.0.2-2_arm64.deb  404  Not Found [IP: 54.39.128.230 80]
E: Unable to fetch some archives, maybe run apt-get update or try with --fix-missing?
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~/Downloads]
└─$ cd ..       
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~]
└─$ cd Desktop  
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~/Desktop]
└─$ ls
 firefox-esr   mystery  'Parallels Shared Folders'
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~/Desktop]
└─$ ^[[200~sudo apt update
zsh: bad pattern: ^[[200~sudo
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~/Desktop]
└─$ sudo apt update 

Get:1 http://kali.download/kali kali-rolling InRelease [41.5 kB]
Err:1 http://kali.download/kali kali-rolling InRelease
  The following signatures were invalid: EXPKEYSIG ED444FF07D8D0BF6 Kali Linux Repository <devel@kali.org>
Reading package lists... Done
Building dependency tree... Done
Reading state information... Done
8 packages can be upgraded. Run 'apt list --upgradable' to see them.
W: An error occurred during the signature verification. The repository is not updated and the previous index files will be used. GPG error: http://kali.download/kali kali-rolling InRelease: The following signatures were invalid: EXPKEYSIG ED444FF07D8D0BF6 Kali Linux Repository <devel@kali.org>
W: Failed to fetch http://http.kali.org/kali/dists/kali-rolling/InRelease  The following signatures were invalid: EXPKEYSIG ED444FF07D8D0BF6 Kali Linux Repository <devel@kali.org>
W: Some index files failed to download. They have been ignored, or old ones used instead.
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~/Desktop]
└─$ curl -fsSL https://archive.kali.org/archive-key.asc | sudo gpg --dearmor -o /etc/apt/trusted.gpg.d/kali-archive-keyring.gpg

File '/etc/apt/trusted.gpg.d/kali-archive-keyring.gpg' exists. Overwrite? (y/N) y
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~/Desktop]
└─$ sudo apt update

Get:1 http://kali.download/kali kali-rolling InRelease [41.5 kB]
Get:2 http://kali.download/kali kali-rolling/main arm64 Packages [20.7 MB]
Get:3 http://kali.download/kali kali-rolling/main arm64 Contents (deb) [49.8 MB]
Get:4 http://kali.download/kali kali-rolling/contrib arm64 Packages [102 kB]
Get:5 http://kali.download/kali kali-rolling/contrib arm64 Contents (deb) [246 kB]
Get:6 http://kali.download/kali kali-rolling/non-free arm64 Packages [155 kB]
Get:7 http://kali.download/kali kali-rolling/non-free arm64 Contents (deb) [834 kB]
Fetched 71.9 MB in 27s (2,628 kB/s)                                         
Reading package lists... Done
Building dependency tree... Done
Reading state information... Done
1927 packages can be upgraded. Run 'apt list --upgradable' to see them.
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~/Desktop]
└─$ sudo apt install pngcheck
Reading package lists... Done
Building dependency tree... Done
Reading state information... Done
The following packages were automatically installed and are no longer required:
  libc-devtools libnsl-dev libtirpc-dev
Use 'sudo apt autoremove' to remove them.
The following additional packages will be installed:
  libc-bin libc-dev-bin libc-l10n libc6 libc6-dev libcryptsetup12
  libnss-systemd libpam-systemd libssl3t64 libsystemd-shared libsystemd0
  libzstd1 linux-sysctl-defaults locales openssh-client openssh-server
  openssh-sftp-server openssl-provider-legacy runit-helper systemd
  systemd-cryptsetup systemd-timesyncd
Suggested packages:
  libc-devtools glibc-doc libnss-nis libnss-nisplus libtss2-rc0t64
  libarchive13t64 libbpf1 libdw1t64 libelf1t64 libpwquality1 keychain
  libpam-ssh monkeysphere ssh-askpass molly-guard ufw systemd-container
  systemd-homed systemd-userdbd systemd-boot systemd-resolved
  systemd-repart
The following packages will be REMOVED:
  libssl3
The following NEW packages will be installed:
  libssl3t64 libsystemd-shared linux-sysctl-defaults
  openssl-provider-legacy pngcheck systemd-cryptsetup
The following packages will be upgraded:
  libc-bin libc-dev-bin libc-l10n libc6 libc6-dev libcryptsetup12
  libnss-systemd libpam-systemd libsystemd0 libzstd1 locales openssh-client
  openssh-server openssh-sftp-server runit-helper systemd systemd-timesyncd
17 upgraded, 6 newly installed, 1 to remove and 1910 not upgraded.
Need to get 20.2 MB of archives.
After this operation, 19.0 MB of additional disk space will be used.
Do you want to continue? [Y/n] y
Get:1 http://kali.download/kali kali-rolling/main arm64 libc-l10n all 2.40-3 [724 kB]
Get:2 http://kali.download/kali kali-rolling/main arm64 libc6 arm64 2.40-3 [2,453 kB]
Get:7 http://kali.darklab.sh/kali kali-rolling/main arm64 runit-helper all 2.16.4 [7,296 B]
Get:3 http://kali.download/kali kali-rolling/main arm64 libc-bin arm64 2.40-3 [540 kB]
Get:4 http://kali.download/kali kali-rolling/main arm64 locales all 2.40-3 [3,903 kB]
Get:11 http://kali.darklab.sh/kali kali-rolling/main arm64 libsystemd0 arm64 257.3-1 [419 kB]
Get:5 http://kali.download/kali kali-rolling/main arm64 openssl-provider-legacy arm64 3.4.1-1 [300 kB]
Get:6 http://kali.download/kali kali-rolling/main arm64 openssh-client arm64 1:9.9p2-1 [906 kB]
Get:8 http://kali.download/kali kali-rolling/main arm64 openssh-server arm64 1:9.9p2-1 [475 kB]
Get:9 http://kali.download/kali kali-rolling/main arm64 libssl3t64 arm64 3.4.1-1 [2,636 kB]
Get:10 http://kali.download/kali kali-rolling/main arm64 libsystemd-shared arm64 257.3-1 [1,907 kB]
Get:12 http://kali.download/kali kali-rolling/main arm64 systemd arm64 257.3-1 [2,922 kB]
Get:19 http://kali.darklab.sh/kali kali-rolling/main arm64 libc-dev-bin arm64 2.40-3 [50.9 kB]
Get:13 http://http.kali.org/kali kali-rolling/main arm64 libzstd1 arm64 1.5.6+dfsg-2 [261 kB]
Get:14 http://kali.download/kali kali-rolling/main arm64 openssh-sftp-server arm64 1:9.9p2-1 [60.4 kB]
Get:15 http://kali.download/kali kali-rolling/main arm64 libcryptsetup12 arm64 2:2.7.5-1 [232 kB]
Get:16 http://kali.download/kali kali-rolling/main arm64 systemd-timesyncd arm64 257.3-1 [88.1 kB]
Get:17 http://kali.download/kali kali-rolling/main arm64 libnss-systemd arm64 257.3-1 [199 kB]
Get:18 http://kali.download/kali kali-rolling/main arm64 libpam-systemd arm64 257.3-1 [273 kB]
Get:20 http://kali.download/kali kali-rolling/main arm64 libc6-dev arm64 2.40-3 [1,591 kB]
Get:21 http://kali.download/kali kali-rolling/main arm64 linux-sysctl-defaults all 4.11 [5,244 B]
Get:22 http://http.kali.org/kali kali-rolling/main arm64 pngcheck arm64 3.0.3-3+b1 [62.5 kB]
Get:23 http://kali.download/kali kali-rolling/main arm64 systemd-cryptsetup arm64 257.3-1 [160 kB]
Fetched 20.2 MB in 4s (4,797 kB/s)       
Preconfiguring packages ...
(Reading database ... 322716 files and directories currently installed.)
Preparing to unpack .../libc-l10n_2.40-3_all.deb ...
Unpacking libc-l10n (2.40-3) over (2.33-6) ...
Preparing to unpack .../locales_2.40-3_all.deb ...
Unpacking locales (2.40-3) over (2.33-6) ...
dpkg: considering deconfiguration of systemd, which would be broken by installation of libc6:arm64 ...
dpkg: yes, will deconfigure systemd (broken by libc6:arm64)
Preparing to unpack .../libc6_2.40-3_arm64.deb ...
De-configuring systemd (250.4-1), to allow installation of libc6:arm64 (2.40-3) ...
debconf: unable to initialize frontend: Dialog
debconf: (Dialog frontend requires a screen at least 13 lines tall and 31 columns wide.)
debconf: falling back to frontend: Readline
Checking for services that may need to be restarted...
Checking init scripts...
Unpacking libc6:arm64 (2.40-3) over (2.33-6) ...
Setting up libc6:arm64 (2.40-3) ...
debconf: unable to initialize frontend: Dialog
debconf: (Dialog frontend requires a screen at least 13 lines tall and 31 columns wide.)
debconf: falling back to frontend: Readline
Checking for services that may need to be restarted...
Checking init scripts...
Configuring libc6:arm64
-----------------------

There are services installed on your system which need to be restarted when 
certain libraries, such as libpam, libc, and libssl, are upgraded. Since 
these restarts may cause interruptions of service for the system, you will 
normally be prompted on each upgrade for the list of services you wish to 
restart.  You can choose this option to avoid being prompted; instead, all 
necessary restarts will be done for you automatically so you can avoid being 
asked questions on each library upgrade.
[More] 


Restart services during package upgrades without asking? [yes/no] y



Restarting services possibly affected by the upgrade:
  cron: restarting...done.

Services restarted successfully.
(Reading database ... 322720 files and directories currently installed.)
Preparing to unpack .../libc-bin_2.40-3_arm64.deb ...
Unpacking libc-bin (2.40-3) over (2.33-6) ...
Setting up libc-bin (2.40-3) ...
dpkg: libssl3:arm64: dependency problems, but removing anyway as you requested:
 wpasupplicant depends on libssl3 (>= 3.0.0).
 vboot-utils depends on libssl3 (>= 3.0.0).
 vboot-kernel-utils depends on libssl3 (>= 3.0.0).
 tnftp depends on libssl3 (>= 3.0.0).
 thc-ipv6 depends on libssl3 (>= 3.0.0).
 tcpdump depends on libssl3 (>= 3.0.0).
 stunnel4 depends on libssl3 (>= 3.0.0).
 ssldump depends on libssl3 (>= 3.0.0).
 socat depends on libssl3 (>= 3.0.0).
 snmp depends on libssl3 (>= 3.0.0).
 skipfish depends on libssl3 (>= 3.0.0).
 samdump2 depends on libssl3 (>= 3.0.0).
 rsync depends on libssl3 (>= 3.0.0).
 proxytunnel depends on libssl3 (>= 3.0.0).
 ppp depends on libssl3 (>= 3.0.0).
 postgresql-client-14 depends on libssl3 (>= 3.0.0).
 postgresql-14 depends on libssl3 (>= 3.0.0).
 php8.1-common depends on libssl3 (>= 3.0.0).
 php8.1-cli depends on libssl3 (>= 3.0.0).
 perl-openssl-defaults:arm64 depends on libssl3 (>= 3.0.0).
 passing-the-hash depends on libssl3 (>= 3.0.0).
 ophcrack-cli depends on libssl3 (>= 3.0.0).
 ophcrack depends on libssl3 (>= 3.0.0).
 openvpn depends on libssl3 (>= 3.0.0).
 openssl depends on libssl3 (>= 3.0.3).
 openssh-sftp-server depends on libssl3 (>= 3.0.0).
 openssh-server depends on libssl3 (>= 3.0.3).
 openssh-client depends on libssl3 (>= 3.0.3).
 openfortivpn depends on libssl3 (>= 3.0.0).
 nginx-core depends on libssl3 (>= 3.0.0).
 network-manager-l2tp-gnome depends on libssl3 (>= 3.0.0).
 network-manager-l2tp depends on libssl3 (>= 3.0.0).
 ncrack depends on libssl3 (>= 3.0.0).
 mtd-utils depends on libssl3 (>= 3.0.0).
 metasploit-framework depends on libssl3 (>= 3.0.0).
 medusa depends on libssl3 (>= 3.0.0).
 mariadb-server-core-10.6 depends on libssl3 (>= 3.0.0).
 mariadb-server-10.6 depends on libssl3 (>= 3.0.0).
 mariadb-client-core-10.6 depends on libssl3 (>= 3.0.0).
 mariadb-client-10.6 depends on libssl3 (>= 3.0.0).
 linux-kbuild-5.18 depends on libssl3 (>= 3.0.0).
 libzip4:arm64 depends on libssl3 (>= 3.0.0).
 libyara9:arm64 depends on libssl3 (>= 3.0.0).
 libxmlsec1-openssl:arm64 depends on libssl3 (>= 3.0.0).
 libwinpr2-2:arm64 depends on libssl3 (>= 3.0.0).
 libwebsockets16:arm64 depends on libssl3 (>= 3.0.0).
 libtss2-esys-3.0.2-0:arm64 depends on libssl3 (>= 3.0.0).
 libssh2-1:arm64 depends on libssl3 (>= 3.0.0).
 libssh-4:arm64 depends on libssl3 (>= 3.0.0).
 libsnmp40:arm64 depends on libssl3 (>= 3.0.0).
 libshout3:arm64 depends on libssl3 (>= 3.0.0).
 libserf-1-1:arm64 depends on libssl3 (>= 3.0.0).
 librabbitmq4:arm64 depends on libssl3 (>= 3.0.0).
 libpython3.9-minimal:arm64 depends on libssl3 (>= 3.0.0).
 libpython3.10-minimal:arm64 depends on libssl3 (>= 3.0.0).
 libpq5:arm64 depends on libssl3 (>= 3.0.0).
 libpkcs11-helper1:arm64 depends on libssl3 (>= 3.0.0).
 libpipewire-0.3-modules:arm64 depends on libssl3 (>= 3.0.0).
 libopusfile0:arm64 depends on libssl3 (>= 3.0.0).
 libnet-ssleay-perl:arm64 depends on libssl3 (>= 3.0.0).
 libnet-dns-sec-perl depends on libssl3 (>= 3.0.0).
 libmongocrypt0:arm64 depends on libssl3 (>= 3.0.0).
 libmongoc-1.0-0 depends on libssl3 (>= 3.0.0).
 libmariadb3:arm64 depends on libssl3 (>= 3.0.0).
 libkrb5-3:arm64 depends on libssl3 (>= 3.0.0).
 libkmod2:arm64 depends on libssl3 (>= 3.0.0).
 libisc-export1105:arm64 depends on libssl3 (>= 3.0.0).
 libimobiledevice6:arm64 depends on libssl3 (>= 3.0.0).
 libhdf5-103-1:arm64 depends on libssl3 (>= 3.0.0).
 libgdal31 depends on libssl3 (>= 3.0.0).
 libfreerdp2-2:arm64 depends on libssl3 (>= 3.0.0).
 libfido2-1:arm64 depends on libssl3 (>= 3.0.0).
 libevent-openssl-2.1-7:arm64 depends on libssl3 (>= 3.0.0).
 libdns-export1110 depends on libssl3 (>= 3.0.0).
 libcurl4:arm64 depends on libssl3 (>= 3.0.0).
 libcryptsetup12:arm64 depends on libssl3 (>= 3.0.0).
 libcrypt-ssleay-perl depends on libssl3 (>= 3.0.0).
 libaprutil1:arm64 depends on libssl3 (>= 3.0.0).
 libapache2-mod-php8.1 depends on libssl3 (>= 3.0.0).
 libafflib0v5:arm64 depends on libssl3 (>= 3.0.0).
 kmod depends on libssl3 (>= 3.0.0).
 john depends on libssl3 (>= 3.0.0).
 ike-scan depends on libssl3 (>= 3.0.0).
 hydra depends on libssl3 (>= 3.0.0).
 gstreamer1.0-plugins-bad:arm64 depends on libssl3 (>= 3.0.0).
 galera-4 depends on libssl3 (>= 3.0.0).
 bind9-libs:arm64 depends on libssl3 (>= 3.0.0).
 axel depends on libssl3 (>= 3.0.0).
 apache2-utils depends on libssl3 (>= 3.0.0).
 apache2-bin depends on libssl3 (>= 3.0.0).

(Reading database ... 322720 files and directories currently installed.)
Removing libssl3:arm64 (3.0.3-8) ...
Selecting previously unselected package openssl-provider-legacy.
(Reading database ... 322708 files and directories currently installed.)
Preparing to unpack .../0-openssl-provider-legacy_3.4.1-1_arm64.deb ...
Unpacking openssl-provider-legacy (3.4.1-1) ...
Preparing to unpack .../1-openssh-client_1%3a9.9p2-1_arm64.deb ...
Unpacking openssh-client (1:9.9p2-1) over (1:9.0p1-1+b1) ...
Preparing to unpack .../2-runit-helper_2.16.4_all.deb ...
Unpacking runit-helper (2.16.4) over (2.13.1) ...
dpkg: warning: unable to delete old directory '/lib/runit-helper': Directory not empty
Preparing to unpack .../3-openssh-server_1%3a9.9p2-1_arm64.deb ...
/bin/systemd-tty-ask-password-agent: error while loading shared libraries: libcrypto.so.3: cannot open shared object file: No such file or directory
Unpacking openssh-server (1:9.9p2-1) over (1:9.0p1-1+b1) ...
Selecting previously unselected package libssl3t64:arm64.
Preparing to unpack .../4-libssl3t64_3.4.1-1_arm64.deb ...
Unpacking libssl3t64:arm64 (3.4.1-1) ...
Selecting previously unselected package libsystemd-shared:arm64.
Preparing to unpack .../5-libsystemd-shared_257.3-1_arm64.deb ...
Unpacking libsystemd-shared:arm64 (257.3-1) ...
Preparing to unpack .../6-libsystemd0_257.3-1_arm64.deb ...
Unpacking libsystemd0:arm64 (257.3-1) over (250.4-1) ...
Setting up libsystemd0:arm64 (257.3-1) ...
(Reading database ... 322736 files and directories currently installed.)
Preparing to unpack .../libzstd1_1.5.6+dfsg-2_arm64.deb ...
Unpacking libzstd1:arm64 (1.5.6+dfsg-2) over (1.5.2+dfsg-1) ...
Setting up libzstd1:arm64 (1.5.6+dfsg-2) ...
Setting up openssl-provider-legacy (3.4.1-1) ...
Setting up libssl3t64:arm64 (3.4.1-1) ...
Setting up libsystemd-shared:arm64 (257.3-1) ...
(Reading database ... 322736 files and directories currently installed.)
Preparing to unpack .../00-systemd_257.3-1_arm64.deb ...
Unpacking systemd (257.3-1) over (250.4-1) ...
dpkg: warning: unable to delete old directory '/lib/systemd/system/user-.slice.d': Directory not empty
dpkg: warning: unable to delete old directory '/lib/systemd/system/timers.target.wants': Directory not empty
dpkg: warning: unable to delete old directory '/lib/systemd/system/systemd-localed.service.d': Directory not empty
dpkg: warning: unable to delete old directory '/lib/systemd/system/rc-local.service.d': Directory not empty
dpkg: warning: unable to delete old directory '/lib/systemd/system/local-fs.target.wants': Directory not empty
dpkg: warning: unable to delete old directory '/lib/systemd/system/getty.target.wants': Directory not empty
Preparing to unpack .../01-openssh-sftp-server_1%3a9.9p2-1_arm64.deb ...
Unpacking openssh-sftp-server (1:9.9p2-1) over (1:9.0p1-1+b1) ...
Preparing to unpack .../02-libcryptsetup12_2%3a2.7.5-1_arm64.deb ...
Unpacking libcryptsetup12:arm64 (2:2.7.5-1) over (2:2.4.3-1+b1) ...
Preparing to unpack .../03-systemd-timesyncd_257.3-1_arm64.deb ...
Unpacking systemd-timesyncd (257.3-1) over (250.4-1) ...
dpkg: warning: unable to delete old directory '/lib/systemd/ntp-units.d': Directory not empty
Preparing to unpack .../04-libnss-systemd_257.3-1_arm64.deb ...
Unpacking libnss-systemd:arm64 (257.3-1) over (250.4-1) ...
Preparing to unpack .../05-libpam-systemd_257.3-1_arm64.deb ...
Unpacking libpam-systemd:arm64 (257.3-1) over (250.4-1) ...
Preparing to unpack .../06-libc-dev-bin_2.40-3_arm64.deb ...
Unpacking libc-dev-bin (2.40-3) over (2.33-6) ...
Preparing to unpack .../07-libc6-dev_2.40-3_arm64.deb ...
Unpacking libc6-dev:arm64 (2.40-3) over (2.33-6) ...
Selecting previously unselected package linux-sysctl-defaults.
Preparing to unpack .../08-linux-sysctl-defaults_4.11_all.deb ...
Unpacking linux-sysctl-defaults (4.11) ...
Selecting previously unselected package pngcheck.
Preparing to unpack .../09-pngcheck_3.0.3-3+b1_arm64.deb ...
Unpacking pngcheck (3.0.3-3+b1) ...
Selecting previously unselected package systemd-cryptsetup.
Preparing to unpack .../10-systemd-cryptsetup_257.3-1_arm64.deb ...
Unpacking systemd-cryptsetup (257.3-1) ...
Setting up runit-helper (2.16.4) ...
Setting up pngcheck (3.0.3-3+b1) ...
Setting up libc-l10n (2.40-3) ...
Setting up openssh-client (1:9.9p2-1) ...
Installing new version of config file /etc/ssh/ssh_config ...
Setting up systemd (257.3-1) ...
Installing new version of config file /etc/systemd/journald.conf ...
Installing new version of config file /etc/systemd/logind.conf ...
Installing new version of config file /etc/systemd/networkd.conf ...
Installing new version of config file /etc/systemd/pstore.conf ...
Installing new version of config file /etc/systemd/sleep.conf ...
Installing new version of config file /etc/systemd/system.conf ...
Installing new version of config file /etc/systemd/user.conf ...
Created symlink '/run/systemd/system/tmp.mount' → '/dev/null'.
/usr/lib/tmpfiles.d/legacy.conf:14: Duplicate line for path "/run/lock", ignoring.
Removing obsolete conffile /etc/systemd/resolved.conf ...
Setting up locales (2.40-3) ...
Installing new version of config file /etc/locale.alias ...
debconf: unable to initialize frontend: Dialog
debconf: (Dialog frontend requires a screen at least 13 lines tall and 31 columns wide.)
debconf: falling back to frontend: Readline
Generating locales (this might take a while)...
  en_US.UTF-8... done
Generation complete.
Setting up linux-sysctl-defaults (4.11) ...
Setting up systemd-timesyncd (257.3-1) ...
Installing new version of config file /etc/dhcp/dhclient-exit-hooks.d/timesyncd ...
Installing new version of config file /etc/systemd/timesyncd.conf ...
systemd-time-wait-sync.service is a disabled or a static unit not running, not starting it.
Setting up libpam-systemd:arm64 (257.3-1) ...
debconf: unable to initialize frontend: Dialog
debconf: (Dialog frontend requires a screen at least 13 lines tall and 31 columns wide.)
debconf: falling back to frontend: Readline
Setting up libcryptsetup12:arm64 (2:2.7.5-1) ...
Setting up libc-dev-bin (2.40-3) ...
Setting up openssh-sftp-server (1:9.9p2-1) ...
Setting up openssh-server (1:9.9p2-1) ...
Installing new version of config file /etc/pam.d/sshd ...
Installing new version of config file /etc/ssh/moduli ...
debconf: unable to initialize frontend: Dialog
debconf: (Dialog frontend requires a screen at least 13 lines tall and 31 columns wide.)
debconf: falling back to frontend: Readline
Replacing config file /etc/ssh/sshd_config with new version
ssh.service is a disabled or a static unit not running, not starting it.
ssh.socket is a disabled or a static unit not running, not starting it.
Setting up libnss-systemd:arm64 (257.3-1) ...
Setting up systemd-cryptsetup (257.3-1) ...
Setting up libc6-dev:arm64 (2.40-3) ...
Processing triggers for libc-bin (2.40-3) ...
Processing triggers for man-db (2.10.2-1) ...
Processing triggers for dbus (1.14.0-1) ...
Processing triggers for shared-mime-info (2.2-1) ...
Processing triggers for kali-menu (2022.3.0) ...
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~/Desktop]
└─$ pngcheck -v mystery
zlib warning:  different version (expected 1.3.1, using 1.2.11)

File: mystery (202940 bytes)
  chunk IHDR at offset 0x0000c, length 13
    1642 x 1095 image, 24-bit RGB, non-interlaced
  chunk sRGB at offset 0x00025, length 1
    rendering intent = perceptual
  chunk gAMA at offset 0x00032, length 4: 0.45455
  chunk pHYs at offset 0x00042, length 9: 2852132389x5669 pixels/meter
  CRC error in chunk pHYs (computed 38d82c82, expected 495224f0)
ERRORS DETECTED in mystery
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~/Desktop]
└─$ hexeditor mystery        
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~/Desktop]
└─$ pngcheck -v mystery      
zlib warning:  different version (expected 1.3.1, using 1.2.11)

File: mystery (202940 bytes)
  chunk IHDR at offset 0x0000c, length 13
    1642 x 1095 image, 24-bit RGB, non-interlaced
  chunk sRGB at offset 0x00025, length 1
    rendering intent = perceptual
  chunk gAMA at offset 0x00032, length 4: 0.45455
  chunk pHYs at offset 0x00042, length 9: 5669x5669 pixels/meter (144 dpi)
:  invalid chunk length (too large)
ERRORS DETECTED in mystery
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~/Desktop]
└─$ hexeditor mystery        
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~/Desktop]
└─$ pngcheck -v mystery
zlib warning:  different version (expected 1.3.1, using 1.2.11)

File: mystery (202940 bytes)
  chunk IHDR at offset 0x0000c, length 13
    1642 x 1095 image, 24-bit RGB, non-interlaced
  chunk sRGB at offset 0x00025, length 1
    rendering intent = perceptual
  chunk gAMA at offset 0x00032, length 4: 0.45455
  chunk pHYs at offset 0x00042, length 9: 5669x5669 pixels/meter (144 dpi)
:  invalid chunk length (too large)
ERRORS DETECTED in mystery
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~/Desktop]
└─$ hexeditor mystery  
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~/Desktop]
└─$ pngcheck -v mystery
zlib warning:  different version (expected 1.3.1, using 1.2.11)

File: mystery (202940 bytes)
  chunk IHDR at offset 0x0000c, length 13
    1642 x 1095 image, 24-bit RGB, non-interlaced
  chunk sRGB at offset 0x00025, length 1
    rendering intent = perceptual
  chunk gAMA at offset 0x00032, length 4: 0.45455
  chunk pHYs at offset 0x00042, length 9: 5669x5669 pixels/meter (144 dpi)
  chunk IDAT at offset 0x00057, length 65445
    zlib: deflated, 32K window, fast compression
  chunk IDAT at offset 0x10008, length 65524
  chunk IDAT at offset 0x20008, length 65524
  chunk IDAT at offset 0x30008, length 6304
  chunk IEND at offset 0x318b4, length 0
No errors detected in mystery (9 chunks, 96.3% compression).
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~/Desktop]
└─$ open mystery 
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~/Desktop]
└─$ 



picoCTF{c0rrupt10n_1847995}



Notas adicionales

--------------------


Referencias

https://es.wikipedia.org/wiki/Portable_Network_Graphics