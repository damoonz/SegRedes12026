## Descripción 
A digital ghost has breached my defenses, and my sensitive data has been stolen! 😱💻 Your mission is to uncover how this phantom intruder infiltrated my system and retrieve the hidden flag.To solve this challenge, you'll need to analyze the provided PCAP file and track down the attack method. The attacker has cleverly concealed his moves in well timely manner. Dive into the network traffic, apply the right filters and show off your forensic prowess and unmask the digital intruder!Find the PCAP file here [Network Traffic PCAP file](https://challenge-files.picoctf.net/c_verbal_sleep/4d25aca04e2409ba0d917d8ed27d49c6fb616ff9603fa3926712cce623a3d7f5/myNetworkTraffic.pcap) and try to get the flag.
## Solución 
Se encuentra en el flujo junto a los datos hexa la bandera en base 64
```
┌──(moonz㉿damoonz)-[~/Documentos/picoctf]
└─$ tshark -r myNetworkTraffic.pcap -Y "tcp.len==12" -T fields -e tcp.segment_data | xxd -p -r | base64 -d
tshark: Error loading table 'TLS Decrypt': ssl_keys:5: File '/home/moonz/Documentos/picoctf/forensic/picopico.key' does not exist or access is denied.
picoCTFe10e839_34sy_tnt_th4tbh_4r_8{1t_w4s

                                                                                               
┌──(moonz㉿damoonz)-[~/Documentos/picoctf]
└─$ tshark -r myNetworkTraffic.pcap -Y "tcp.len==12 || tcp.len==4" -T fields -e frame.time -e tcp.segment_data 2>/dev/null | sort -k1 | awk '{print $2}' | xxd -p -r | base64 -d
picoCTF{1t_w4snt_th4t_34sy_tbh_4r_8e10e839}                                                                                               

```
picoCTF{1t_w4snt_th4t_34sy_tbh_4r_8e10e839} 
## Notas
## Referencias