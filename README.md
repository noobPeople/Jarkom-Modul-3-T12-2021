﻿# Jarkom-Modul-3-T12-2021

Nama Kelompok :  
- Ian Felix Jonathan Simanjuntak
- Muhammad Zakky Ghufron
- Muhammad Naufal Imantyasto

### Gambar Topologi
![image](https://user-images.githubusercontent.com/50267676/141628788-d83842a9-69af-40f9-ad40-1b98899b6788.png)

### Nomor 1
Luffy bersama Zoro berencana membuat peta tersebut dengan kriteria EniesLobby sebagai DNS Server, Jipangu sebagai DHCP Server, Water7 sebagai Proxy Server

### Jawaban Nomor 1
Untuk soal nomor 1 akan dijelaskan selagi kami mengerjakan soal soal berikutnya

### Nomor 2
dan Foosha sebagai DHCP Relay (2)

### Jawaban Nomor 2
Pada Foosha, kami menjalankan beberapa perintah sebagai berikut
```bash
apt-get update -y
apt-get install nano -y
iptables -t nat -A POSTROUTING -o eth0 -j MASQUERADE -s 192.217.0.0/16
apt-get install isc-dhcp-relay -y
service isc-dhcp-relay restart
```
Dari perintah diatas kami pertama sekali melakukan update, lalu menjalankan IPTABLES. Setelah menjalankan IPTABLES kami melakukan download isc-dhcp-relay. Ketika melakukan download dhcp-relay, kami menjadikan Jipangu (192.217.2.4) sebagai dhcp-server dan interfaces yang kami gunakan adalah `eth1 eth2 eth3` seperti gambar dibawah ini
![image](https://user-images.githubusercontent.com/50267676/141637521-8923463f-741c-4139-bbbe-1cf457905f49.png)
