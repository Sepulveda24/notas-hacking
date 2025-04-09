Descripción
Decode this [message](https://jupiter.challenges.picoctf.org/static/fc1edf07742e98a480c6aff7d2546107/message.wav) from the moon.
Hints:
1.⁠ ⁠How did pictures from the moon landing get sent back to Earth?
2.What is the CMU mascot?, that might help select a RX option

Solución 1

Con Terminal linux
──(parallels㉿kali-linux-2022-2)-[~]
└─$ wget https://jupiter.challenges.picoctf.org/static/fc1edf07742e98a480c6aff7d2546107/message.wav  
--2025-04-08 12:43:16--  https://jupiter.challenges.picoctf.org/static/fc1edf07742e98a480c6aff7d2546107/message.wav
Resolving jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)... 3.131.60.8
Connecting to jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)|3.131.60.8|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 11066998 (11M) [application/octet-stream]
Saving to: ‘message.wav’

message.wav         100%[================>]  10.55M  8.11MB/s    in 1.3s    

2025-04-08 12:43:18 (8.11 MB/s) - ‘message.wav’ saved [11066998/11066998]

                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~]
└─$ ls
 buildings.png   Documents    message.wav      Pictures   '~.venv'
 capture.pcap    Downloads    Music            Public      Videos
 cookies.txt     flag.png     pico_img.png     server.py   webshell.php
 Desktop         garden.jpg   pico_img.png.1   Templates   webshell.png.php
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~]
└─$  file message.wav     
message.wav: RIFF (little-endian) data, WAVE audio, Microsoft PCM, 16 bit, mono 48000 Hz
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~]
└─$ open message.wav
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~]
└─$ cd /opt     
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[/opt]
└─$ sudo git clone $ git clone https://github.com/colaclanth/sstv.git
[sudo] password for parallels: 
fatal: Too many arguments.

usage: git clone [<options>] [--] <repo> [<dir>]

    -v, --verbose         be more verbose
    -q, --quiet           be more quiet
    --progress            force progress reporting
    --reject-shallow      don't clone shallow repository
    -n, --no-checkout     don't create a checkout
    --bare                create a bare repository
    --mirror              create a mirror repository (implies bare)
    -l, --local           to clone from a local repository
    --no-hardlinks        don't use local hardlinks, always copy
    -s, --shared          setup as shared repository
    --recurse-submodules[=<pathspec>]
                          initialize submodules in the clone
    --recursive ...       alias of --recurse-submodules
    -j, --jobs <n>        number of submodules cloned in parallel
    --template <template-directory>
                          directory from which templates will be used
    --reference <repo>    reference repository
    --reference-if-able <repo>
                          reference repository
    --dissociate          use --reference only while cloning
    -o, --origin <name>   use <name> instead of 'origin' to track upstream
    -b, --branch <branch>
                          checkout <branch> instead of the remote's HEAD
    -u, --upload-pack <path>
                          path to git-upload-pack on the remote
    --depth <depth>       create a shallow clone of that depth
    --shallow-since <time>
                          create a shallow clone since a specific time
    --shallow-exclude <revision>
                          deepen history of shallow clone, excluding rev
    --single-branch       clone only one branch, HEAD or --branch
    --no-tags             don't clone any tags, and make later fetches not to follow them
    --shallow-submodules  any cloned submodules will be shallow
    --separate-git-dir <gitdir>
                          separate git dir from working tree
    -c, --config <key=value>
                          set config inside the new repository
    --server-option <server-specific>
                          option to transmit
    -4, --ipv4            use IPv4 addresses only
    -6, --ipv6            use IPv6 addresses only
    --filter <args>       object filtering
    --remote-submodules   any cloned submodules will use their remote-tracking branch
    --sparse              initialize sparse-checkout file to include only files at root

                                                                             
┌──(parallels㉿kali-linux-2022-2)-[/opt]
└─$ ls     
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[/opt]
└─$ cd /sstv
cd: no such file or directory: /sstv
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[/opt]
└─$ sudo git clone $ git clone https://github.com/colaclanth/sstv.git
fatal: Too many arguments.

usage: git clone [<options>] [--] <repo> [<dir>]

    -v, --verbose         be more verbose
    -q, --quiet           be more quiet
    --progress            force progress reporting
    --reject-shallow      don't clone shallow repository
    -n, --no-checkout     don't create a checkout
    --bare                create a bare repository
    --mirror              create a mirror repository (implies bare)
    -l, --local           to clone from a local repository
    --no-hardlinks        don't use local hardlinks, always copy
    -s, --shared          setup as shared repository
    --recurse-submodules[=<pathspec>]
                          initialize submodules in the clone
    --recursive ...       alias of --recurse-submodules
    -j, --jobs <n>        number of submodules cloned in parallel
    --template <template-directory>
                          directory from which templates will be used
    --reference <repo>    reference repository
    --reference-if-able <repo>
                          reference repository
    --dissociate          use --reference only while cloning
    -o, --origin <name>   use <name> instead of 'origin' to track upstream
    -b, --branch <branch>
                          checkout <branch> instead of the remote's HEAD
    -u, --upload-pack <path>
                          path to git-upload-pack on the remote
    --depth <depth>       create a shallow clone of that depth
    --shallow-since <time>
                          create a shallow clone since a specific time
    --shallow-exclude <revision>
                          deepen history of shallow clone, excluding rev
    --single-branch       clone only one branch, HEAD or --branch
    --no-tags             don't clone any tags, and make later fetches not to follow them
    --shallow-submodules  any cloned submodules will be shallow
    --separate-git-dir <gitdir>
                          separate git dir from working tree
    -c, --config <key=value>
                          set config inside the new repository
    --server-option <server-specific>
                          option to transmit
    -4, --ipv4            use IPv4 addresses only
    -6, --ipv6            use IPv6 addresses only
    --filter <args>       object filtering
    --remote-submodules   any cloned submodules will use their remote-tracking branch
    --sparse              initialize sparse-checkout file to include only files at root

                                                                             
┌──(parallels㉿kali-linux-2022-2)-[/opt]
└─$ ls
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[/opt]
└─$ cd /sstv                                                         
cd: no such file or directory: /sstv
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[/opt]
└─$ sudo git clone git clone https://github.com/colaclanth/sstv.git 
fatal: Too many arguments.

usage: git clone [<options>] [--] <repo> [<dir>]

    -v, --verbose         be more verbose
    -q, --quiet           be more quiet
    --progress            force progress reporting
    --reject-shallow      don't clone shallow repository
    -n, --no-checkout     don't create a checkout
    --bare                create a bare repository
    --mirror              create a mirror repository (implies bare)
    -l, --local           to clone from a local repository
    --no-hardlinks        don't use local hardlinks, always copy
    -s, --shared          setup as shared repository
    --recurse-submodules[=<pathspec>]
                          initialize submodules in the clone
    --recursive ...       alias of --recurse-submodules
    -j, --jobs <n>        number of submodules cloned in parallel
    --template <template-directory>
                          directory from which templates will be used
    --reference <repo>    reference repository
    --reference-if-able <repo>
                          reference repository
    --dissociate          use --reference only while cloning
    -o, --origin <name>   use <name> instead of 'origin' to track upstream
    -b, --branch <branch>
                          checkout <branch> instead of the remote's HEAD
    -u, --upload-pack <path>
                          path to git-upload-pack on the remote
    --depth <depth>       create a shallow clone of that depth
    --shallow-since <time>
                          create a shallow clone since a specific time
    --shallow-exclude <revision>
                          deepen history of shallow clone, excluding rev
    --single-branch       clone only one branch, HEAD or --branch
    --no-tags             don't clone any tags, and make later fetches not to follow them
    --shallow-submodules  any cloned submodules will be shallow
    --separate-git-dir <gitdir>
                          separate git dir from working tree
    -c, --config <key=value>
                          set config inside the new repository
    --server-option <server-specific>
                          option to transmit
    -4, --ipv4            use IPv4 addresses only
    -6, --ipv6            use IPv6 addresses only
    --filter <args>       object filtering
    --remote-submodules   any cloned submodules will use their remote-tracking branch
    --sparse              initialize sparse-checkout file to include only files at root

                                                                             
┌──(parallels㉿kali-linux-2022-2)-[/opt]
└─$ ls
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[/opt]
└─$ sudo git clone https://github.com/colaclanth/sstv.git
Cloning into 'sstv'...
remote: Enumerating objects: 221, done.
remote: Counting objects: 100% (59/59), done.
remote: Compressing objects: 100% (10/10), done.
remote: Total 221 (delta 51), reused 49 (delta 49), pack-reused 162 (from 1)
Receiving objects: 100% (221/221), 1.01 MiB | 2.20 MiB/s, done.
Resolving deltas: 100% (139/139), done.
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[/opt]
└─$ ls
sstv
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[/opt]
└─$ cd sstv 
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[/opt/sstv]
└─$ python setup.py install
running install
/usr/lib/python3/dist-packages/setuptools/command/install.py:34: SetuptoolsDeprecationWarning: setup.py install is deprecated. Use build and pip and other standards-based tools.
  warnings.warn(
/usr/lib/python3/dist-packages/setuptools/command/easy_install.py:158: EasyInstallDeprecationWarning: easy_install command is deprecated. Use build and pip and other standards-based tools.
  warnings.warn(
error: can't create or remove files in install directory

The following error occurred while trying to add or remove files in the
installation directory:

    [Errno 13] Permission denied: '/usr/local/lib/python3.10/dist-packages/test-easy-install-3654.write-test'

The installation directory you specified (via --install-dir, --prefix, or
the distutils default setting) was:

    /usr/local/lib/python3.10/dist-packages/

Perhaps your account does not have write access to this directory?  If the
installation directory is a system-owned directory, you may need to sign in
as the administrator or "root" account.  If you do not have administrative
access to this machine, you may wish to choose a different installation
directory, preferably one that is listed in your PYTHONPATH environment
variable.

For information on other options, you may wish to consult the
documentation at:

  https://setuptools.pypa.io/en/latest/deprecated/easy_install.html

Please make the appropriate changes for your system and try again.

                                                                             
┌──(parallels㉿kali-linux-2022-2)-[/opt/sstv]
└─$ ls
examples  LICENSE  README.md  setup.py  sstv  test
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[/opt/sstv]
└─$ python setup.py install
running install
/usr/lib/python3/dist-packages/setuptools/command/install.py:34: SetuptoolsDeprecationWarning: setup.py install is deprecated. Use build and pip and other standards-based tools.
  warnings.warn(
/usr/lib/python3/dist-packages/setuptools/command/easy_install.py:158: EasyInstallDeprecationWarning: easy_install command is deprecated. Use build and pip and other standards-based tools.
  warnings.warn(
error: can't create or remove files in install directory

The following error occurred while trying to add or remove files in the
installation directory:

    [Errno 13] Permission denied: '/usr/local/lib/python3.10/dist-packages/test-easy-install-3842.write-test'

The installation directory you specified (via --install-dir, --prefix, or
the distutils default setting) was:

    /usr/local/lib/python3.10/dist-packages/

Perhaps your account does not have write access to this directory?  If the
installation directory is a system-owned directory, you may need to sign in
as the administrator or "root" account.  If you do not have administrative
access to this machine, you may wish to choose a different installation
directory, preferably one that is listed in your PYTHONPATH environment
variable.

For information on other options, you may wish to consult the
documentation at:

  https://setuptools.pypa.io/en/latest/deprecated/easy_install.html

Please make the appropriate changes for your system and try again.

                                                                             
┌──(parallels㉿kali-linux-2022-2)-[/opt/sstv]
└─$ python3 setup.py install
running install
/usr/lib/python3/dist-packages/setuptools/command/install.py:34: SetuptoolsDeprecationWarning: setup.py install is deprecated. Use build and pip and other standards-based tools.
  warnings.warn(
/usr/lib/python3/dist-packages/setuptools/command/easy_install.py:158: EasyInstallDeprecationWarning: easy_install command is deprecated. Use build and pip and other standards-based tools.
  warnings.warn(
error: can't create or remove files in install directory

The following error occurred while trying to add or remove files in the
installation directory:

    [Errno 13] Permission denied: '/usr/local/lib/python3.10/dist-packages/test-easy-install-4265.write-test'

The installation directory you specified (via --install-dir, --prefix, or
the distutils default setting) was:

    /usr/local/lib/python3.10/dist-packages/

Perhaps your account does not have write access to this directory?  If the
installation directory is a system-owned directory, you may need to sign in
as the administrator or "root" account.  If you do not have administrative
access to this machine, you may wish to choose a different installation
directory, preferably one that is listed in your PYTHONPATH environment
variable.

For information on other options, you may wish to consult the
documentation at:

  https://setuptools.pypa.io/en/latest/deprecated/easy_install.html

Please make the appropriate changes for your system and try again.

                                                                             
┌──(parallels㉿kali-linux-2022-2)-[/opt/sstv]
└─$ sudo python3 setup.py install
running install
/usr/lib/python3/dist-packages/setuptools/command/install.py:34: SetuptoolsDeprecationWarning: setup.py install is deprecated. Use build and pip and other standards-based tools.
  warnings.warn(
/usr/lib/python3/dist-packages/setuptools/command/easy_install.py:158: EasyInstallDeprecationWarning: easy_install command is deprecated. Use build and pip and other standards-based tools.
  warnings.warn(
/usr/lib/python3/dist-packages/pkg_resources/__init__.py:116: PkgResourcesDeprecationWarning: 1.16.0-unknown is an invalid version and will not be supported in a future release
  warnings.warn(
/usr/lib/python3/dist-packages/pkg_resources/__init__.py:116: PkgResourcesDeprecationWarning: 1.12.1-git20200711.33e2d80-dfsg1-0.6 is an invalid version and will not be supported in a future release
  warnings.warn(
running bdist_egg
running egg_info
creating sstv.egg-info
writing sstv.egg-info/PKG-INFO
writing dependency_links to sstv.egg-info/dependency_links.txt
writing entry points to sstv.egg-info/entry_points.txt
writing requirements to sstv.egg-info/requires.txt
writing top-level names to sstv.egg-info/top_level.txt
writing manifest file 'sstv.egg-info/SOURCES.txt'
reading manifest file 'sstv.egg-info/SOURCES.txt'
adding license file 'LICENSE'
writing manifest file 'sstv.egg-info/SOURCES.txt'
installing library code to build/bdist.linux-aarch64/egg
running install_lib
running build_py
creating build
creating build/lib
creating build/lib/sstv
copying sstv/__init__.py -> build/lib/sstv
copying sstv/__main__.py -> build/lib/sstv
copying sstv/spec.py -> build/lib/sstv
copying sstv/common.py -> build/lib/sstv
copying sstv/command.py -> build/lib/sstv
copying sstv/decode.py -> build/lib/sstv
creating build/bdist.linux-aarch64
creating build/bdist.linux-aarch64/egg
creating build/bdist.linux-aarch64/egg/sstv
copying build/lib/sstv/__init__.py -> build/bdist.linux-aarch64/egg/sstv
copying build/lib/sstv/__main__.py -> build/bdist.linux-aarch64/egg/sstv
copying build/lib/sstv/spec.py -> build/bdist.linux-aarch64/egg/sstv
copying build/lib/sstv/common.py -> build/bdist.linux-aarch64/egg/sstv
copying build/lib/sstv/command.py -> build/bdist.linux-aarch64/egg/sstv
copying build/lib/sstv/decode.py -> build/bdist.linux-aarch64/egg/sstv
byte-compiling build/bdist.linux-aarch64/egg/sstv/__init__.py to __init__.cpython-310.pyc
byte-compiling build/bdist.linux-aarch64/egg/sstv/__main__.py to __main__.cpython-310.pyc
byte-compiling build/bdist.linux-aarch64/egg/sstv/spec.py to spec.cpython-310.pyc
byte-compiling build/bdist.linux-aarch64/egg/sstv/common.py to common.cpython-310.pyc
byte-compiling build/bdist.linux-aarch64/egg/sstv/command.py to command.cpython-310.pyc
byte-compiling build/bdist.linux-aarch64/egg/sstv/decode.py to decode.cpython-310.pyc
creating build/bdist.linux-aarch64/egg/EGG-INFO
copying sstv.egg-info/PKG-INFO -> build/bdist.linux-aarch64/egg/EGG-INFO
copying sstv.egg-info/SOURCES.txt -> build/bdist.linux-aarch64/egg/EGG-INFO
copying sstv.egg-info/dependency_links.txt -> build/bdist.linux-aarch64/egg/EGG-INFO
copying sstv.egg-info/entry_points.txt -> build/bdist.linux-aarch64/egg/EGG-INFO
copying sstv.egg-info/requires.txt -> build/bdist.linux-aarch64/egg/EGG-INFO
copying sstv.egg-info/top_level.txt -> build/bdist.linux-aarch64/egg/EGG-INFO
zip_safe flag not set; analyzing archive contents...
creating dist
creating 'dist/sstv-0.1-py3.10.egg' and adding 'build/bdist.linux-aarch64/egg' to it
removing 'build/bdist.linux-aarch64/egg' (and everything under it)
Processing sstv-0.1-py3.10.egg
Copying sstv-0.1-py3.10.egg to /usr/local/lib/python3.10/dist-packages
Adding sstv 0.1 to easy-install.pth file
Installing sstv script to /usr/local/bin

Installed /usr/local/lib/python3.10/dist-packages/sstv-0.1-py3.10.egg
Processing dependencies for sstv==0.1
Searching for PySoundFile
Reading https://pypi.org/simple/PySoundFile/
/usr/lib/python3/dist-packages/pkg_resources/__init__.py:116: PkgResourcesDeprecationWarning:  is an invalid version and will not be supported in a future release
  warnings.warn(
Downloading https://files.pythonhosted.org/packages/2a/b3/0b871e5fd31b9a8e54b4ee359384e705a1ca1e2870706d2f081dc7cc1693/PySoundFile-0.9.0.post1-py2.py3-none-any.whl#sha256=db14f84f4af1910f54766cf0c0f19d52414fa80aa0e11cb338b5614946f39947
Best match: PySoundFile 0.9.0.post1
Processing PySoundFile-0.9.0.post1-py2.py3-none-any.whl
Installing PySoundFile-0.9.0.post1-py2.py3-none-any.whl to /usr/local/lib/python3.10/dist-packages
Adding PySoundFile 0.9.0.post1 to easy-install.pth file

Installed /usr/local/lib/python3.10/dist-packages/PySoundFile-0.9.0.post1-py3.10.egg
Searching for scipy==1.7.3
Best match: scipy 1.7.3
Adding scipy 1.7.3 to easy-install.pth file

Using /usr/lib/python3/dist-packages
Searching for numpy==1.21.5
Best match: numpy 1.21.5
Adding numpy 1.21.5 to easy-install.pth file
Installing f2py script to /usr/local/bin
Installing f2py3 script to /usr/local/bin
Installing f2py3.9 script to /usr/local/bin
Installing f2py3.10 script to /usr/local/bin

Using /usr/lib/python3/dist-packages
Searching for Pillow==9.1.1
Best match: Pillow 9.1.1
Adding Pillow 9.1.1 to easy-install.pth file

Using /usr/lib/python3/dist-packages
Searching for cffi==1.15.0
Best match: cffi 1.15.0
Adding cffi 1.15.0 to easy-install.pth file

Using /usr/lib/python3/dist-packages
Finished processing dependencies for sstv==0.1
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[/opt/sstv]
└─$ ls                           
build  examples  README.md  sstv           test
dist   LICENSE   setup.py   sstv.egg-info
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[/opt/sstv]
└─$ cdss
cdss: command not found
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[/opt/sstv]
└─$ cd     
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~]
└─$ cd /opt/sstv   
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[/opt/sstv]
└─$ ls
build  examples  README.md  sstv           test
dist   LICENSE   setup.py   sstv.egg-info
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[/opt/sstv]
└─$ cd sstv     
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[/opt/sstv/sstv]
└─$ cd ..  
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[/opt/sstv]
└─$ sstv --help                  
usage: sstv [-h] [-d AUDIO_FILE] [-o OUTPUT_FILE] [-s SKIP] [-V]
            [--list-modes] [--list-audio-formats] [--list-image-formats]

options:
  -h, --help            show this help message and exit
  -d AUDIO_FILE, --decode AUDIO_FILE
                        decode SSTV audio file
  -o OUTPUT_FILE, --output OUTPUT_FILE
                        save output image to custom location
  -s SKIP, --skip SKIP  time in seconds to start decoding signal at
  -V, --version         show program's version number and exit
  --list-modes          list supported SSTV modes
  --list-audio-formats  list supported audio file formats
  --list-image-formats  list supported image file formats

examples:
  Decode local SSTV audio file named 'audio.ogg' to 'result.png':
    $ sstv -d audio.ogg

  Decode SSTV audio file in /tmp to './image.jpg':
    $ sstv -d /tmp/signal.wav -o ./image.jpg

  Start decoding SSTV signal at 50.5 seconds into the audio
    $ sstv -d audio.ogg -s 50.50
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[/opt/sstv]
└─$ sstv -d message -o flag.png
usage: sstv [-h] [-d AUDIO_FILE] [-o OUTPUT_FILE] [-s SKIP] [-V]
            [--list-modes] [--list-audio-formats] [--list-image-formats]
sstv: error: argument -d/--decode: can't open 'message': [Errno 2] No such file or directory: 'message'
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[/opt/sstv]
└─$ ls
build  examples  README.md  sstv           test
dist   LICENSE   setup.py   sstv.egg-info
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[/opt/sstv]
└─$ cd ..
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[/opt]
└─$ cd ..
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[/]
└─$ ls
0    boot  etc   lib         media  opt   root  sbin  sys  usr
bin  dev   home  lost+found  mnt    proc  run   srv   tmp  var
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[/]
└─$ cd ~ 
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~]
└─$ ls
 buildings.png   Documents    message.wav      Pictures   '~.venv'
 capture.pcap    Downloads    Music            Public      Videos
 cookies.txt     flag.png     pico_img.png     server.py   webshell.php
 Desktop         garden.jpg   pico_img.png.1   Templates   webshell.png.php
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~]
└─$ sstv -d message -o flag.png
usage: sstv [-h] [-d AUDIO_FILE] [-o OUTPUT_FILE] [-s SKIP] [-V]
            [--list-modes] [--list-audio-formats] [--list-image-formats]
sstv: error: argument -d/--decode: can't open 'message': [Errno 2] No such file or directory: 'message'
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~]
└─$ sstv -d message.wav -o flag.png
[sstv] Searching for calibration header... Found!    
[sstv] Detected SSTV mode Scottie 1
[sstv] Decoding image...   [###########################################] 100%
[sstv] Drawing image data...
[sstv] ...Done!
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~]
└─$ ls
 buildings.png   Documents    message.wav      Pictures   '~.venv'
 capture.pcap    Downloads    Music            Public      Videos
 cookies.txt     flag.png     pico_img.png     server.py   webshell.php
 Desktop         garden.jpg   pico_img.png.1   Templates   webshell.png.php
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~]
└─$ open flag.png 



picoCTF{beep_boop_im_in_space}



Notas adicionales

--------------------


Referencias

https://jupiter.challenges.picoctf.org/static/fc1edf07742e98a480c6aff7d2546107/message.wav 
https://github.com/colaclanth/sstv.git