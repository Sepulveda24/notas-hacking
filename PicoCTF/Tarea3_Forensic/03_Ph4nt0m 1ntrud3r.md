Descripción
A digital ghost has breached my defenses, and my sensitive data has been stolen! 😱💻 Your mission is to uncover how this phantom intruder infiltrated my system and retrieve the hidden flag.To solve this challenge, you'll need to analyze the provided PCAP file and track down the attack method. The attacker has cleverly concealed his moves in well timely manner. Dive into the network traffic, apply the right filters and show off your forensic prowess and unmask the digital intruder!Find the PCAP file here [Network Traffic PCAP file](https://challenge-files.picoctf.net/c_verbal_sleep/a917f567b9cc0f1a730a7801b309955df4d2234a8114326857b9759e9e5d0453/myNetworkTraffic.pcap) and try to get the flag.


Hints:
1.⁠ ⁠Filter your packets to narrow down your search.
2.Attacks were done in timely manner.
3.Time is essential

Solución 1

Con Wireshark y cyberchef

Analizamos el trafico de redes en wireshark y sacamos los valores de TCP payload y reclutando los mejores tiempos y transformandolos a hexadecimal y luego a base 64 nos empieza a dar la bandera

cyberchef 
input:63476c6a62304e5552673d3d
657a46305833633063773d3d
626e52666447673064413d3d
587a4d3063336c6664413d3d
596d68664e484a664f513d3d
4e546c6d4e54426b4d773d3d
66513d3d
Recipe:from 64, from hex
output:picoCTF{1t_w4snt_th4t_34sy_tbh_4r_959f50d3}


Notas adicionales

--------------------


Referencias


https://gchq.github.io/CyberChef/#recipe=From_Base64('A-Za-z0-9%2B/%3D',true,false)&input=Y0dsamIwTlVSbnQwYUdWZmJUTjBZV1JoZEdGZk1YTmZiVzlrYVdacFpXUjk