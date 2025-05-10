Descripción
A group of underground hackers might be using this legit site to communicate. Use your forensic techniques to uncover their message

Additional details will be available after launching your challenge instance.


Hints:
1.⁠ ⁠In the country that doesn't exist, the flag persists

Solución 1

Con terminal linux
                                                                             ┌──(parallels㉿kali-linux-2022-2)-[~]
└─$ cd Desktop                              
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~/Desktop]
└─$ ls        
 firefox-esr  'Parallels Shared Folders'   Retos
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~/Desktop]
└─$ cd Retos  
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~/Desktop/Retos]
└─$ ls      
binwalk         dolls.jpg  picopico.key    tunn3l_v1s10n.bmp
capture.pcap    Forensic4  picopico.key.1  vulture.jpg
capture.pcap.1  myenv      TareaForensic3
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~/Desktop/Retos]
└─$ cd TareaForensic3 
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~/Desktop/Retos/TareaForensic3]
└─$ ls
secretOfThePolyglot  stepic
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~/Desktop/Retos/TareaForensic3]
└─$ cd s                  
cd: no such file or directory: s
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~/Desktop/Retos/TareaForensic3]
└─$ cd stepic 
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~/Desktop/Retos/TareaForensic3/stepic]
└─$ ls
upz.png
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~/Desktop/Retos/TareaForensic3/stepic]
└─$ stepic           
zsh: command not found: stepic
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~/Desktop/Retos/TareaForensic3/stepic]
└─$ sudo install stepic
[sudo] password for parallels: 
Sorry, try again.
[sudo] password for parallels: 
install: missing destination file operand after 'stepic'
Try 'install --help' for more information.
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~/Desktop/Retos/TareaForensic3/stepic]
└─$ sudo apt update
sudo apt install python3-pip

Get:1 https://packages.microsoft.com/repos/code stable InRelease [3,590 B]
Get:3 https://packages.microsoft.com/repos/code stable/main arm64 Packages [19.5 kB]
Get:4 https://packages.microsoft.com/repos/code stable/main armhf Packages [19.6 kB]
Get:5 https://packages.microsoft.com/repos/code stable/main amd64 Packages [19.3 kB]
Get:2 http://kali.download/kali kali-rolling InRelease [41.5 kB]            
Err:2 http://kali.download/kali kali-rolling InRelease                      
  The following signatures couldn't be verified because the public key is not available: NO_PUBKEY ED65462EC8D5E4C5
Fetched 103 kB in 11s (9,684 B/s)                                           
Reading package lists... Done
Building dependency tree... Done
Reading state information... Done
1516 packages can be upgraded. Run 'apt list --upgradable' to see them.
W: An error occurred during the signature verification. The repository is not updated and the previous index files will be used. GPG error: http://kali.download/kali kali-rolling InRelease: The following signatures couldn't be verified because the public key is not available: NO_PUBKEY ED65462EC8D5E4C5
W: Failed to fetch http://http.kali.org/kali/dists/kali-rolling/InRelease  The following signatures couldn't be verified because the public key is not available: NO_PUBKEY ED65462EC8D5E4C5
W: Some index files failed to download. They have been ignored, or old ones used instead.
Reading package lists... Done
Building dependency tree... Done
Reading state information... Done
python3-pip is already the newest version (25.0.1+dfsg-1).
The following packages were automatically installed and are no longer required:
  apt-file attr base58 binutils-mingw-w64-i686 binutils-mingw-w64-x86-64
  blt cython3 distro-info-data espeak-ng-data ettercap-common
  ettercap-graphical faraday-angular-frontend figlet finger fonts-lyx
  fonts-noto-color-emoji freetds-common gcc-mingw-w64-base
  gcc-mingw-w64-i686-win32 gcc-mingw-w64-i686-win32-runtime
  gcc-mingw-w64-x86-64-win32 gcc-mingw-w64-x86-64-win32-runtime gdal-data
  gdal-plugins gir1.2-atk-1.0 gir1.2-atspi-2.0
  gir1.2-ayatanaappindicator3-0.1 gir1.2-freedesktop gir1.2-gdkpixbuf-2.0
  gir1.2-glib-2.0 gir1.2-gstreamer-1.0 gir1.2-gtk-3.0 gir1.2-gtksource-3.0
  gir1.2-harfbuzz-0.0 gir1.2-javascriptcoregtk-4.0 gir1.2-nm-1.0
  gir1.2-pango-1.0 gir1.2-soup-2.4 gir1.2-vte-2.91 gir1.2-webkit2-4.0
  gir1.2-wnck-3.0 gir1.2-xfconf-0 hwloc icu-devtools isympy-common isympy3
  kismet-capture-common kismet-capture-linux-bluetooth
  kismet-capture-linux-wifi kismet-capture-nrf-51822
  kismet-capture-nrf-52840 kismet-capture-nrf-mousejack
  kismet-capture-nxp-kw41z kismet-capture-rz-killerbee
  kismet-capture-ti-cc-2531 kismet-capture-ti-cc-2540
  kismet-capture-ubertooth-one kismet-core kismet-logtools ldap-utils
  libaec0 libao-common libao4 libapache2-mod-php libapt-pkg-perl
  libarmadillo11 libarpack2t64 libatk-adaptor libblosc1 libbrlapi0.8
  libbtbb1 libc-devtools libcfitsio9 libct4 libdotconf0 libespeak-ng1
  libev4 libexpat1-dev libexporter-tiny-perl libffi-dev libfreexl1 libfyba0
  libgdal31 libgeos-c1v5 libgeos3.11.0 libgeotiff5 libgirepository-1.0-1
  libhdf4-0-alt libhdf5-103-1 libhdf5-hl-100 libheif1 libhiredis1.1.0
  libicu-dev libimagequant0 libiw30 libjq1 libjs-jquery-ui libjs-skeleton
  libkmlbase1 libkmldom1 libkmlengine1 liblbfgsb0 liblist-moreutils-perl
  liblist-moreutils-xs-perl liblouis-data liblouis20 libluajit-5.1-2
  libluajit-5.1-common libmotif-common libmpdec3 libncurses-dev libnetcdf19
  libnsl-dev libodbc2 libodbcinst2 libogdi4.1 libonig5 libopusfile0
  libpangoxft-1.0-0 libpcaudio0 libportmidi0 libproj25 libprotobuf23
  libpython3-dev libpython3.10 libpython3.10-dev libpython3.10-minimal
  libpython3.10-stdlib libpython3.9-minimal libpython3.9-stdlib
  libqhull-r8.0 libqt5designer5 libqt5help5 libqt5sql5 libqt5sql5-sqlite
  libqt5test5 libraqm0 libregexp-assemble-perl librtlsdr0 librttopo1
  libsdl2-image-2.0-0 libsdl2-mixer-2.0-0 libsdl2-ttf-2.0-0 libsonic0
  libsoup-gnome2.4-1 libspatialite7 libspeechd2 libsuperlu5 libsybdb5
  libsz2 libtinfo-dev libtirpc-dev libtk8.6 libubertooth1 liburiparser1
  libvte-2.91-0 libvte-2.91-common libwebsockets16 libxdo3 libxerces-c3.2
  libxm4 libxml2-dev libyara9 libz3-dev llvm-11 llvm-11-runtime llvm-13
  llvm-13-runtime medusa mingw-w64-common mingw-w64-i686-dev
  mingw-w64-x86-64-dev node-normalize.css onboard-common postgresql
  proj-bin proj-data pwgen python-apt-common python-babel-localedata
  python-matplotlib-data python-mpltoolkits.basemap-data
  python-pastedeploy-tpl python-tables-data python3-adblockparser
  python3-advancedhttpserver python3-aioconsole python3-aiofiles
  python3-aiomultiprocess python3-aioredis python3-aiosignal python3-ajpy
  python3-aniso8601 python3-apispec python3-appdirs python3-apscheduler
  python3-asciitree python3-async-timeout python3-asysocks python3-babel
  python3-backcall python3-backoff python3-base58 python3-bidict
  python3-bluepy python3-boltons python3-bottle python3-brlapi python3-cbor
  python3-cli-helpers python3-commonmark python3-configobj
  python3-defusedxml python3-dicttoxml python3-distro python3-docopt
  python3-donut python3-ecdsa python3-engineio python3-et-xmlfile
  python3-exifread python3-feedparser python3-filedepot python3-flatbuffers
  python3-frozenlist python3-fs python3-geojson python3-git python3-gitdb
  python3-h2 python3-hiredis python3-hpack python3-html2text
  python3-httpagentparser python3-humanize python3-hupper
  python3-hyperframe python3-importlib-resources python3-iniconfig
  python3-ipy python3-jaraco.context python3-jdcal python3-jedi python3-jq
  python3-kaitaistruct python3-limiter python3-louis python3-lz4
  python3-markdown python3-matplotlib-inline python3-maxminddb
  python3-minidump python3-mistune0 python3-mnemonic python3-mpmath
  python3-multidict python3-mypy-extensions python3-mysqldb python3-neobolt
  python3-netaddr python3-ntlm-auth python3-odf python3-pampy python3-parso
  python3-passlib python3-pastedeploy-tpl python3-pefile python3-pexpect
  python3-phonenumbers python3-pickleshare python3-plaster python3-pluggy
  python3-pluginbase python3-png python3-psycopg2 python3-ptyprocess
  python3-publicsuffix2 python3-publicsuffixlist python3-py
  python3-pydispatch python3-pyfiglet python3-pyinotify python3-pylnk3
  python3-pyminifier python3-pymssql python3-pymysql python3-pyotp
  python3-pypdf2 python3-pyperclip python3-pyqrcode python3-pyrsistent
  python3-pyshp python3-pytz python3-pytz-deprecation-shim python3-pytzdata
  python3-redis python3-repoze.lru python3-routes python3-ruamel.yaml
  python3-ruamel.yaml.clib python3-rx python3-secure python3-serial
  python3-setproctitle python3-sgmllib3k python3-simplekv python3-smmap
  python3-smoke-zephyr python3-snappy python3-sniffio python3-socketio
  python3-sortedcontainers python3-speaklater python3-speechd
  python3-sqlparse python3-sympy python3-syslog-rfc5424-formatter
  python3-tabulate python3-tdb python3-tempita python3-termcolor
  python3-terminaltables python3-texttable python3-tld python3-token-bucket
  python3-toml python3-tornado python3-tqdm python3-traitlets
  python3-translationstring python3-trie python3-tz python3-tzlocal
  python3-u-msgpack python3-ubjson python3-ujson python3-unicodecsv
  python3-unicodedata2 python3-unidecode python3-venusian python3-webob
  python3-websocket python3-winacl python3-wsaccel python3-wtforms
  python3-xdg python3-xlrd python3-xlutils python3-xlwt python3-xmltodict
  python3-yaswfp python3-zipp python3-zlib-wrapper python3.10
  python3.10-dev python3.10-minimal python3.9 python3.9-minimal
  qtbase5-dev-tools qtchooser ruby-cms-scanner ruby-ethon
  ruby-get-process-mem ruby-opt-parse-validator ruby-progressbar
  ruby-typhoeus ruby-yajl rwho rwhod samba-dsdb-modules samba-vfs-modules
  sound-icons sparta-scripts speech-dispatcher
  speech-dispatcher-audio-plugins speech-dispatcher-espeak-ng sqsh
  subversion tdb-tools tk8.6-blt2.5 toilet-fonts unicode-data
  unixodbc-common wireless-tools xdotool xkbset xsltproc
Use 'sudo apt autoremove' to remove them.
0 upgraded, 0 newly installed, 0 to remove and 1516 not upgraded.
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~/Desktop/Retos/TareaForensic3/stepic]
└─$ pip install stepic

error: externally-managed-environment

× This environment is externally managed
╰─> To install Python packages system-wide, try apt install
    python3-xyz, where xyz is the package you are trying to
    install.
    
    If you wish to install a non-Debian-packaged Python package,
    create a virtual environment using python3 -m venv path/to/venv.
    Then use path/to/venv/bin/python and path/to/venv/bin/pip. Make
    sure you have python3-full installed.
    
    If you wish to install a non-Debian packaged Python application,
    it may be easiest to use pipx install xyz, which will manage a
    virtual environment for you. Make sure you have pipx installed.
    
    See /usr/share/doc/python3.13/README.venv for more information.

note: If you believe this is a mistake, please contact your Python installation or OS distribution provider. You can override this, at the risk of breaking your Python installation or OS, by passing --break-system-packages.
hint: See PEP 668 for the detailed specification.
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~/Desktop/Retos/TareaForensic3/stepic]
└─$ pip3 install stepic

error: externally-managed-environment

× This environment is externally managed
╰─> To install Python packages system-wide, try apt install
    python3-xyz, where xyz is the package you are trying to
    install.
    
    If you wish to install a non-Debian-packaged Python package,
    create a virtual environment using python3 -m venv path/to/venv.
    Then use path/to/venv/bin/python and path/to/venv/bin/pip. Make
    sure you have python3-full installed.
    
    If you wish to install a non-Debian packaged Python application,
    it may be easiest to use pipx install xyz, which will manage a
    virtual environment for you. Make sure you have pipx installed.
    
    See /usr/share/doc/python3.13/README.venv for more information.

note: If you believe this is a mistake, please contact your Python installation or OS distribution provider. You can override this, at the risk of breaking your Python installation or OS, by passing --break-system-packages.
hint: See PEP 668 for the detailed specification.
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~/Desktop/Retos/TareaForensic3/stepic]
└─$ python3 -m venv venv

                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~/Desktop/Retos/TareaForensic3/stepic]
└─$ source venv/bin/activate

                                                                             
┌──(venv)─(parallels㉿kali-linux-2022-2)-[~/Desktop/Retos/TareaForensic3/stepic]
└─$ pip install stepic

Collecting stepic
  Downloading stepic-0.5.0.tar.gz (219 kB)
  Installing build dependencies ... done
  Getting requirements to build wheel ... done
  Preparing metadata (pyproject.toml) ... done
Collecting pillow (from stepic)
  Downloading pillow-11.2.1-cp313-cp313-manylinux_2_28_aarch64.whl.metadata (8.9 kB)
Downloading pillow-11.2.1-cp313-cp313-manylinux_2_28_aarch64.whl (4.5 MB)
   ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 4.5/4.5 MB 26.1 MB/s eta 0:00:00
Building wheels for collected packages: stepic
  Building wheel for stepic (pyproject.toml) ... done
  Created wheel for stepic: filename=stepic-0.5.0-py3-none-any.whl size=12506 sha256=c867555982e9ace856b6cb00ac45837f7b7987da10adcf40878f216a64934b5e
  Stored in directory: /home/parallels/.cache/pip/wheels/f7/4c/a1/2791c89a230cdc97ab0c5ad4b7893b2b4ad6f71374f4ce8352
Successfully built stepic
Installing collected packages: pillow, stepic
Successfully installed pillow-11.2.1 stepic-0.5.0
                                                                             
┌──(venv)─(parallels㉿kali-linux-2022-2)-[~/Desktop/Retos/TareaForensic3/stepic]
└─$ stepic                 
usage: stepic [-h] [--version] [--debug] [-d] [-e] [-f FORMAT] [-i FILE]
              [-t FILE] [-o FILE]
Choose either encode (-e) or decode (-d).
                                                                             
┌──(venv)─(parallels㉿kali-linux-2022-2)-[~/Desktop/Retos/TareaForensic3/stepic]
└─$ stepic -d upz.png 
usage: stepic [-h] [--version] [--debug] [-d] [-e] [-f FORMAT] [-i FILE]
              [-t FILE] [-o FILE]
stepic: error: unrecognized arguments: upz.png
                                                                             
┌──(venv)─(parallels㉿kali-linux-2022-2)-[~/Desktop/Retos/TareaForensic3/stepic]
└─$ ls
upz.png  venv
                                                                             
┌──(venv)─(parallels㉿kali-linux-2022-2)-[~/Desktop/Retos/TareaForensic3/stepic]
└─$ stepic -d -i upz.png
/home/parallels/Desktop/Retos/TareaForensic3/stepic/venv/lib/python3.13/site-packages/PIL/Image.py:3442: DecompressionBombWarning: Image size (150658990 pixels) exceeds limit of 89478485 pixels, could be decompression bomb DOS attack.
  warnings.warn(
picoCTF{fl4g_h45_fl4g1a2a9157}                                                                             
┌──(venv)─(parallels㉿kali-linux-2022-2)-[~/Desktop/Retos/TareaForensic3/stepic]



picoCTF{fl4g_h45_fl4g1a2a9157}  

Notas adicionales

--------------------


Referencias

Terminal linux