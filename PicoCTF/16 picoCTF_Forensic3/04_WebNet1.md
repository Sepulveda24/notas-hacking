Descripción
Encontramos esta [captura de paquete](https://jupiter.challenges.picoctf.org/static/fbf98e695555a2a48fe42c9a245de376/capture.pcap) y [clave](https://jupiter.challenges.picoctf.org/static/fbf98e695555a2a48fe42c9a245de376/picopico.key). Recupera la bandera.


Hints:
1.⁠Prueba a usar una herramienta como Wireshark.
2.¿Cómo se puede descifrar el flujo TLS?

Solución 1

Con Terminal de linux
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~/Desktop/Retos]
└─$ wget https://jupiter.challenges.picoctf.org/static/fbf98e695555a2a48fe42c9a245de376/picopico.key
--2025-05-02 16:28:29--  https://jupiter.challenges.picoctf.org/static/fbf98e695555a2a48fe42c9a245de376/picopico.key
Resolving jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)... 3.131.60.8
Connecting to jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)|3.131.60.8|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 1704 (1.7K) [application/octet-stream]
Saving to: ‘picopico.key.1’

picopico.key.1      100%[================>]   1.66K  --.-KB/s    in 0s      

2025-05-02 16:28:34 (12.6 MB/s) - ‘picopico.key.1’ saved [1704/1704]

                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~/Desktop/Retos]
└─$ wget https://jupiter.challenges.picoctf.org/static/fbf98e695555a2a48fe42c9a245de376/capture.pcap
--2025-05-02 16:28:42--  https://jupiter.challenges.picoctf.org/static/fbf98e695555a2a48fe42c9a245de376/capture.pcap
Resolving jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)... 3.131.60.8
Connecting to jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)|3.131.60.8|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 92525 (90K) [application/octet-stream]
Saving to: ‘capture.pcap.1’

capture.pcap.1      100%[================>]  90.36K  --.-KB/s    in 0.06s   

2025-05-02 16:28:47 (1.44 MB/s) - ‘capture.pcap.1’ saved [92525/92525]

                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~/Desktop/Retos]
└─$ wireshark capture.pcap.1 b
libGL error: pci id for fd 19: 1ab8:0010, driver (null)
pci id for fd 20: 1ab8:0010, driver (null)
wireshark: Invalid argument: b

Usage: wireshark [options] ... [ <infile> ]

Capture interface:
  -i <interface>, --interface <interface>
                           name or idx of interface (def: first non-loopback)
  -f <capture filter>      packet filter in libpcap filter syntax
  -s <snaplen>, --snapshot-length <snaplen>
                           packet snapshot length (def: appropriate maximum)
  -p, --no-promiscuous-mode
                           don't capture in promiscuous mode
  -k                       start capturing immediately (def: do nothing)
  -S                       update packet display when new packets are captured
  -l                       turn on automatic scrolling while -S is in use
  -I, --monitor-mode       capture in monitor mode, if available
  -B <buffer size>, --buffer-size <buffer size>
                           size of kernel buffer (def: 2MB)
  -y <link type>, --linktype <link type>
                           link layer type (def: first appropriate)
  --time-stamp-type <type> timestamp method for interface
  -D, --list-interfaces    print list of interfaces and exit
  -L, --list-data-link-types
                           print list of link-layer types of iface and exit
  --list-time-stamp-types  print list of timestamp types for iface and exit

Capture stop conditions:
  -c <packet count>        stop after n packets (def: infinite)
  -a <autostop cond.> ..., --autostop <autostop cond.> ...
                           duration:NUM - stop after NUM seconds
                           filesize:NUM - stop this file after NUM KB
                              files:NUM - stop after NUM files
                            packets:NUM - stop after NUM packets
Capture output:
  -b <ringbuffer opt.> ..., --ring-buffer <ringbuffer opt.>
                           duration:NUM - switch to next file after NUM secs
                           filesize:NUM - switch to next file after NUM KB
                              files:NUM - ringbuffer: replace after NUM files
                            packets:NUM - switch to next file after NUM packets
                           interval:NUM - switch to next file when the time is
                                          an exact multiple of NUM secs
Input file:
  -r <infile>, --read-file <infile>
                           set the filename to read from (no pipes or stdin!)

Processing:
  -R <read filter>, --read-filter <read filter>
                           packet filter in Wireshark display filter syntax
  -n                       disable all name resolutions (def: all enabled)
  -N <name resolve flags>  enable specific name resolution(s): "mnNtdv"
  -d <layer_type>==<selector>,<decode_as_protocol> ...
                           "Decode As", see the man page for details
                           Example: tcp.port==8888,http
  --enable-protocol <proto_name>
                           enable dissection of proto_name
  --disable-protocol <proto_name>
                           disable dissection of proto_name
  --enable-heuristic <short_name>
                           enable dissection of heuristic protocol
  --disable-heuristic <short_name>
                           disable dissection of heuristic protocol

User interface:
  -C <config profile>      start with specified configuration profile
  -H                       hide the capture info dialog during packet capture
  -Y <display filter>, --display-filter <display filter>
                           start with the given display filter
  -g <packet number>       go to specified packet number after "-r"
  -J <jump filter>         jump to the first packet matching the (display)
                           filter
  -j                       search backwards for a matching packet after "-J"
  -t a|ad|adoy|d|dd|e|r|u|ud|udoy
                           format of time stamps (def: r: rel. to first)
  -u s|hms                 output format of seconds (def: s: seconds)
  -X <key>:<value>         eXtension options, see man page for details
  -z <statistics>          show various statistics, see man page for details

Output:
  -w <outfile|->           set the output filename (or '-' for stdout)
  --capture-comment <comment>
                           add a capture file comment, if supported
Diagnostic output:
  --log-level <level>      sets the active log level ("critical", "warning", etc.)
  --log-fatal <level>      sets level to abort the program ("critical" or "warning")
  --log-domains <[!]list>  comma separated list of the active log domains
  --log-debug <[!]list>    comma separated list of domains with "debug" level
  --log-noisy <[!]list>    comma separated list of domains with "noisy" level
  --log-file <path>        file to output messages to (in addition to stderr)

Miscellaneous:
  -h, --help               display this help and exit
  -v, --version            display version info and exit
  -P <key>:<path>          persconf:path - personal configuration files
                           persdata:path - personal data files
  -o <name>:<value> ...    override preference or recent setting
  -K <keytab>              keytab file to use for kerberos decryption
  --display <X display>    X display to use
  --fullscreen             start Wireshark in full screen
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~/Desktop/Retos]
└─$ wireshark capture.pcap.1  
libGL error: pci id for fd 19: 1ab8:0010, driver (null)
pci id for fd 20: 1ab8:0010, driver (null)
 ** (wireshark:54466) 16:29:39.677438 [GUI WARNING] -- FIX Add drag reordering to UAT dialog
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~/Desktop/Retos]
└─$ ls
binwalk       capture.pcap.1  myenv         picopico.key.1     vulture.jpg
capture.pcap  dolls.jpg       picopico.key  tunn3l_v1s10n.bmp
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~/Desktop/Retos]
└─$ open vulture.jpg      
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~/Desktop/Retos]
└─$ strings vulture.jpg             
JFIF
Exif
picoCTF{honey.roasted.peanuts}
picoCTF{honey.roasted.peanuts}


Notas adicionales

--------------------


Referencias

https://github.com/payloadbox/xxe-injection-payload-list