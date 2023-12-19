# Jarkom-Modul-5-E19-2023
Laporan Resmi Praktikum Modul 5 Kelompok E19
| Nama               |  NRP       | 
|--------------------|-------------|
| M. Armand Giovani | 5025211054  |
| Afiq Fawwaz Haidar | 5025211246  |

## Topologi

![image](https://github.com/AfiqHaidar/Jarkom-Modul-5-E19-2023/assets/70834506/1c12984b-8361-4c20-ad56-9a6f6fc8f096)

## Pembagian IP

Link pembagian IP https://docs.google.com/spreadsheets/d/1MzAeYkjxnVSKTdKhH7W2RDOhKYu6OOIyPag1VWNo4Js/edit?usp=sharing

![image](https://github.com/AfiqHaidar/Jarkom-Modul-5-E19-2023/assets/70834506/911b6a00-11f4-4fe5-8caa-ea7122ec6189)

## VLSM Tree

![image](https://github.com/AfiqHaidar/Jarkom-Modul-5-E19-2023/assets/70834506/7c28c03a-5ecb-4d5c-8c82-8d5eaba78e0d)

## Konfigurasi Network

- Aura
```sh
auto eth0
iface eth0 inet dhcp

auto eth1
iface eth1 inet static
	address 10.46.0.21
	netmask 255.255.255.252

auto eth2
iface eth2 inet static
	address 10.46.0.1
	netmask 255.255.255.252

```

- Frieren
```sh
auto eth0
iface eth0 inet static
	address 10.46.0.2
	netmask 255.255.255.252

auto eth1
iface eth1 inet static
	address 10.46.0.9
	netmask 255.255.255.252

auto eth2
iface eth2 inet static
	address 10.46.0.5
	netmask 255.255.255.252


```

- Stark
```sh
auto eth0
iface eth0 inet static
	address 10.46.0.2
	netmask 255.255.255.252

auto eth1
iface eth1 inet static
	address 10.46.0.9
	netmask 255.255.255.252

auto eth2
iface eth2 inet static
	address 10.46.0.5
	netmask 255.255.255.252

```

- Himmel
```sh
auto eth0
iface eth0 inet static
	address 10.46.0.10
	netmask 255.255.255.252

auto eth1
iface eth1 inet static
	address 10.46.0.129
	netmask 255.255.255.128

auto eth2
iface eth2 inet static
	address 10.46.2.1
	netmask 255.255.254.0

```

- LaubHills
```sh
auto eth0
iface eth0 inet dhcp
```

- SchwerMountain
```sh
auto eth0
iface eth0 inet dhcp
```

- Fern
```sh
auto eth0
iface eth0 inet static
	address 10.46.0.131
	netmask 255.255.255.128

auto eth2
iface eth2 inet static
	address 10.46.0.13
	netmask 255.255.255.252

auto eth1
iface eth1 inet static
	address 10.46.0.17
	netmask 255.255.255.252

```

- Richter
```sh
auto eth0
iface eth0 inet static
	address 10.46.0.14
	netmask 255.255.255.252
	gateway 10.46.0.13
```

- Revolte
```
auto eth0
iface eth0 inet static
	address 10.46.0.18
	netmask 255.255.255.252
	gateway 10.46.0.17

```

- Heiter
```sh
auto eth0
iface eth0 inet static
	address 10.46.0.22
	netmask 255.255.255.252

auto eth1
iface eth1 inet static
	address 10.46.8.1
	netmask 255.255.248.0

auto eth2
iface eth2 inet static
	address 10.46.4.1
	netmask 255.255.252.0

```

- TurkRegion
```sh
auto eth0
iface eth0 inet dhcp
```

- Sein
```sh
 auto eth0
 iface eth0 inet static
	address 10.46.4.2
	netmask 255.255.252.0
	gateway 10.46.4.1

```

- GrobeForest
```sh
auto eth0
iface eth0 inet dhcp
```

## Routing Network

- Aura
```sh
route add -net 10.46.0.4 netmask 255.255.255.252 gw 10.46.0.2
route add -net 10.46.0.8 netmask 255.255.255.252 gw 10.46.0.2
route add -net 10.46.2.0 netmask 255.255.254.0 gw 10.46.0.2
route add -net 10.46.0.128 netmask 255.255.255.128 gw 10.46.0.2
route add -net 10.46.0.12 netmask 255.255.255.252 gw 10.46.0.2
route add -net 10.46.0.16 netmask 255.255.255.252 gw 10.46.0.2
route add -net 10.46.8.0 netmask 255.255.248.0 gw 10.46.0.22
route add -net 10.46.4.0 netmask 255.255.252.0 gw 10.46.0.22

```

- Frieren
```sh
route add -net 0.0.0.0 netmask 0.0.0.0 gw 10.46.0.1
route add -net 10.46.2.0 netmask 255.255.254.0 gw 10.46.0.10
route add -net 10.46.0.128 netmask 255.255.255.128 gw 10.46.0.10
route add -net 10.46.0.12 netmask 255.255.255.252 gw 10.46.0.10
route add -net 10.46.0.16 netmask 255.255.255.252 gw 10.46.0.10

```

- Himmel
```sh
route add -net 0.0.0.0 netmask 0.0.0.0 gw 10.46.0.9
route add -net 10.46.0.12 netmask 255.255.255.252 gw 10.46.0.131
route add -net 10.46.0.16 netmask 255.255.255.252 gw 10.46.0.131

```

- Fern
```sh
route add -net 0.0.0.0 netmask 0.0.0.0 gw 10.46.0.129

```

- Heiter 
```sh
route add -net 0.0.0.0 netmask 0.0.0.0 gw 10.46.0.21

```

## Konfigurasi DHCP

- Revolte - DHCP Server
```sh
echo nameserver 192.168.122.1 > /etc/resolv.conf

apt-get update
apt install isc-dhcp-server -y

echo "
INTERFACESv4=\"eth0\"
"  > /etc/default/isc-dhcp-server

echo "
subnet 10.46.0.16 netmask 255.255.255.252 {}

subnet 10.46.0.128 netmask 255.255.255.128 {
    range 10.46.0.132 10.46.0.254;
    option routers 10.46.0.131;
    option broadcast-address 10.46.0.255;
    option domain-name-servers 192.168.122.1;
}

subnet 10.46.2.0 netmask 255.255.254.0 {
    range 10.46.2.3 10.46.3.254;
    option routers 10.46.2.1;
    option broadcast-address 10.46.3.255;
    option domain-name-servers 192.168.122.1;
}

subnet 10.46.0.8 netmask 255.255.255.252 {}

subnet 10.46.0.4 netmask 255.255.255.252 {}

subnet 10.46.0.20 netmask 255.255.255.252 {}

subnet 10.46.8.0 netmask 255.255.248.0 {
    range 10.46.8.3 10.46.15.254;
    option routers 10.46.8.1;
    option broadcast-address 10.46.15.255;
      option domain-name-servers 192.168.122.1;
}

subnet 10.46.4.0 netmask 255.255.252.0 {
    range 10.46.4.3 10.46.7.254;
    option routers 10.46.4.1;
    option broadcast-address 10.46.7.255;
       option domain-name-servers 192.168.122.1;
}


" > /etc/dhcp/dhcpd.conf

rm /var/run/dhcpd.pid
service isc-dhcp-server restart


```

- Routers - DHCP Relay
```sh

echo nameserver 192.168.122.1 > /etc/resolv.conf

apt-get update
apt install isc-dhcp-relay -y

echo "
SERVERS=\"10.46.0.18\"
INTERFACESv4=\"eth0 eth1 eth2\"
"  > /etc/default/isc-dhcp-relay

service isc-dhcp-relay restart

```

## Soal 1
> Agar topologi yang kalian buat dapat mengakses keluar, kalian diminta untuk mengkonfigurasi Aura menggunakan iptables, tetapi tidak ingin menggunakan MASQUERADE

### Aura
```sh
IPETH0="$(ip -br a | grep eth0 | awk '{print $NF}' | cut -d'/' -f1)"
iptables -t nat -A POSTROUTING -o eth0 -j SNAT --to-source "$IPETH0" -s 10.46.0.0/20
```

### Testing

![image](https://github.com/AfiqHaidar/Jarkom-Modul-5-E19-2023/assets/70834506/8a708d97-40ad-4e65-9a49-33b9de8f20bf)

![image](https://github.com/AfiqHaidar/Jarkom-Modul-5-E19-2023/assets/70834506/8bc6b53a-3eac-4dab-84af-77d5e76508bf)

## Soal 2
> Kalian diminta untuk melakukan drop semua TCP dan UDP kecuali port 8080 pada TCP.

### Aura
```sh
# Drop all TCP traffic except on port 8080
iptables -A INPUT -p tcp --dport 8080 -j ACCEPT
iptables -A INPUT -p tcp -j DROP

# Drop all UDP traffic
iptables -A INPUT -p udp -j DROP
```

### Testing

![image](https://github.com/AfiqHaidar/Jarkom-Modul-5-E19-2023/assets/70834506/c63aeffd-8ab0-4fa9-b3fc-35ef419e0b8a)

![image](https://github.com/AfiqHaidar/Jarkom-Modul-5-E19-2023/assets/70834506/7511edf3-2e8d-4f65-b080-acdaa8222377)

![image](https://github.com/AfiqHaidar/Jarkom-Modul-5-E19-2023/assets/70834506/03e6cf42-8318-4fb2-8701-d1d78ddbed45)

![image](https://github.com/AfiqHaidar/Jarkom-Modul-5-E19-2023/assets/70834506/d450bea3-1aa1-4654-a2b0-72b94484e576)

## Soal 3
> Kepala Suku North Area meminta kalian untuk membatasi DHCP dan DNS Server hanya dapat dilakukan ping oleh maksimal 3 device secara bersamaan, selebihnya akan di drop.

### Richter - DNS Server & Revolte - DHCP Server
```sh
iptables -A INPUT -p icmp -m connlimit --connlimit-above 3 --connlimit-mask 0 -j DROP
```

### Testing

![image](https://github.com/AfiqHaidar/Jarkom-Modul-5-E19-2023/assets/70834506/89e5cf27-9b25-4d96-91d5-e299efd2020a)

![image](https://github.com/AfiqHaidar/Jarkom-Modul-5-E19-2023/assets/70834506/43c3bf31-5497-400c-b336-6b504adf7f26)

![image](https://github.com/AfiqHaidar/Jarkom-Modul-5-E19-2023/assets/70834506/37773a4f-52a9-4e29-93e9-e33c8edd580c)

![image](https://github.com/AfiqHaidar/Jarkom-Modul-5-E19-2023/assets/70834506/de004e0e-8eec-4a88-afe7-bc2d33dd7bdb)

## Soal 4
> Lakukan pembatasan sehingga koneksi SSH pada Web Server hanya dapat dilakukan oleh masyarakat yang berada pada GrobeForest

### Sein & Stark - Web Server
```sh
sudo iptables -A INPUT --dport 22 -s 10.46.4.3:10.46.7.254 -j ACCEPT
sudo iptables -A INPUT --dport 22 -j DROP
```

### Testing

![image](https://github.com/AfiqHaidar/Jarkom-Modul-5-E19-2023/assets/70834506/b9e9d653-e4e5-4770-9ef3-c8d5268142c7)

![image](https://github.com/AfiqHaidar/Jarkom-Modul-5-E19-2023/assets/70834506/de7b193e-10ab-4368-b6dc-5b5c02218d31)

![image](https://github.com/AfiqHaidar/Jarkom-Modul-5-E19-2023/assets/70834506/e8671856-61c5-4c83-b0ab-ce22c72a1e8e)

![image](https://github.com/AfiqHaidar/Jarkom-Modul-5-E19-2023/assets/70834506/2caf0444-0dd9-489c-9eab-540c75c23c52)





## Soal 5 
> Selain itu, akses menuju WebServer hanya diperbolehkan saat jam kerja yaitu Senin-Jumat pada pukul 08.00-16.00.

### Sein & Stark - Web Server
```sh
iptables -A INPUT -m time --timestart 08:00 --timestop 16:00 --days Mon,Tue,Wed,Thu,Fri -j ACCEPT
iptables -A INPUT -j REJECT
```

### Testing

![image](https://github.com/AfiqHaidar/Jarkom-Modul-5-E19-2023/assets/70834506/941c0f0b-ce2a-4d7b-bdf2-c0ab8bd81884)

![image](https://github.com/AfiqHaidar/Jarkom-Modul-5-E19-2023/assets/70834506/164704e3-3ccd-4ad8-a4a6-12015704d30b)

![image](https://github.com/AfiqHaidar/Jarkom-Modul-5-E19-2023/assets/70834506/269dac78-5ebd-4950-8376-d0fc091ae208)

![image](https://github.com/AfiqHaidar/Jarkom-Modul-5-E19-2023/assets/70834506/7baa3a95-0d73-4424-bbef-1e1c7bd9eb55)


## Soal 6
> Lalu, karena ternyata terdapat beberapa waktu di mana network administrator dari WebServer tidak bisa stand by, sehingga perlu ditambahkan rule bahwa akses pada hari Senin - Kamis pada jam 12.00 - 13.00 dilarang (istirahat maksi cuy) dan akses di hari Jumat pada jam 11.00 - 13.00 juga dilarang (maklum, Jumatan rek).

### Sein & Stark - Web Server
```sh
iptables -A INPUT -m time --timestart 12:00 --timestop 13:00 --weekdays Mon,Tue,Wed,Thu -j REJECT
iptables -A INPUT -m time --timestart 11:00 --timestop 13:00 --weekdays Fri -j REJECT
iptables -A INPUT -m time --timestart 08:00 --timestop 16:00 --weekdays Mon,Tue,Wed,Thu,Fri -j ACCEPT
iptables -A INPUT -j REJECT
```
Penjelasan:
- `iptables -A INPUT -m time --timestart 12:00 --timestop 13:00 --weekdays Mon,Tue,Wed,Thu -j REJECT` : Mengatur akses pada hari Senin - Kamis pada jam 12.00 - 13.00 dilarang
- `iptables -A INPUT -m time --timestart 11:00 --timestop 13:00 --weekdays Fri -j REJECT` : Mengatur akses di hari Jumat pada jam 11.00 - 13.00 juga dilarang
- `iptables -A INPUT -m time --timestart 08:00 --timestop 16:00 --weekdays Mon,Tue,Wed,Thu,Fri -j ACCEPT` : Mengatur akses pada hari Senin - Jumat pada jam 08.00 - 16.00 diperbolehkan
- `iptables -A INPUT -j REJECT` : Mengatur akses pada hari selain Senin - Jumat pada jam selain 08.00 - 16.00 dilarang

### Testing

- Testing jam kerja
```date -u 1214133023```

![image](https://github.com/VanGarman21/PBKK/assets/100523471/c3b2ee80-30b8-4ace-8013-c6cc371cab91)

- Testing jam istirahat
```date -u 1214123023```
![image](https://github.com/VanGarman21/PBKK/assets/100523471/b7e38b36-3183-4a10-b5c3-402ecd031bcc)

## Soal 7
> Karena terdapat 2 WebServer, kalian diminta agar setiap client yang mengakses Sein dengan Port 80 akan didistribusikan secara bergantian pada Sein dan Stark secara berurutan dan request dari client yang mengakses Stark dengan port 443 akan didistribusikan secara bergantian pada Sein dan Stark secara berurutan.

### Heiter
```sh
iptables -A PREROUTING -t nat -p tcp --dport 80 -d 10.46.4.2 -m statistic --mode nth --every 2 --packet 0 -j DNAT --to-destination 10.46.4.2
iptables -A PREROUTING -t nat -p tcp --dport 80 -d 10.46.4.2 -j DNAT --to-destination 10.46.0.6
iptables -A PREROUTING -t nat -p tcp --dport 443 -d 10.46.0.6 -m statistic --mode nth --every 2 --packet 0 -j DNAT --to-destination 10.46.0.6
iptables -A PREROUTING -t nat -p tcp --dport 443 -d 10.46.0.6 -j DNAT --to-destination 10.46.4.2
```

Penjelasan:
- `iptables -A PREROUTING -t nat -p tcp --dport 80 -d 10.46.4.2 -m statistic --mode nth --every 2 --packet 0 -j DNAT --to-destination 10.46.4.2` : Mengatur akses pada port 80 akan didistribusikan secara bergantian pada Sein dan Stark secara berurutan
- `iptables -A PREROUTING -t nat -p tcp --dport 80 -d 10.46.4.2 -j DNAT --to-destination 10.46.0.6` : Mengatur akses pada port 80 akan didistribusikan secara bergantian pada Sein dan Stark secara berurutan
- `iptables -A PREROUTING -t nat -p tcp --dport 443 -d 10.46.0.6 -m statistic --mode nth --every 2 --packet 0 -j DNAT --to-destination 10.46.0.6` : Mengatur akses pada port 443 akan didistribusikan secara bergantian pada Sein dan Stark secara berurutan
- `iptables -A PREROUTING -t nat -p tcp --dport 443 -d 10.46.0.6 -j DNAT --to-destination 10.46.4.2` : Mengatur akses pada port 443 akan didistribusikan secara bergantian pada Sein dan Stark secara berurutan

### Testing

- Gunakan syntaxs berikut pada sein dan stark
```sh
# untuk port 80
Sein :
while true; do nc -l -p 80 -c 'echo "Halo, ini sein"'; done 
Stark :
while true; do nc -l -p 80 -c 'echo "Halo, ini stark"'; done

# untuk port 443
Sein :
while true; do nc -l -p 443 -c 'echo "Halo, ini sein"'; done
while true; do nc -l -p 443 -c 'echo "Halo, ini stark"'; done
```

- Gunakan syntaxs berikut pada client
```sh
# untuk port 80
nc 10.46.4.2 80 

# untuk port 443
nc 10.46.0.6 443
```
- Hasil
![image](https://github.com/VanGarman21/PBKK/assets/100523471/61392fef-d278-4f26-94bb-fb88d96151bf)


![image](https://github.com/VanGarman21/PBKK/assets/100523471/f50647c3-f36a-43d0-b3bc-cf609ca37730)


## Soal 8
> Karena berbeda koalisi politik, maka subnet dengan masyarakat yang berada pada Revolte dilarang keras mengakses WebServer hingga masa pencoblosan pemilu kepala suku 2024 berakhir. Masa pemilu (hingga pemungutan dan penghitungan suara selesai) kepala suku bersamaan dengan masa pemilu Presiden dan Wakil Presiden Indonesia 2024.

### Sein & Stark - Web Server
```sh	
Revolte_Subnet="10.46.0.16/30"

Pemilu_Start=$(date -d "2023-12-19T00:00" +"%Y-%m-%dT%H:%M")

Pemilu_End=$(date -d "2024-03-15T00:00" +"%Y-%m-%dT%H:%M")

iptables -A INPUT -p tcp -s $Revolte_Subnet --dport 80 -m time --datestart "$Pemilu_Start" --datestop "$Pemilu_End" -j DROP
```

Penjelasan:
- `Revolte_Subnet="10.46.0.16/30"` : Mengatur subnet yang akan di drop
- `Pemilu_Start=$(date -d "2023-12-19T00:00" +"%Y-%m-%dT%H:%M")` : Mengatur waktu awal pemilu
- `Pemilu_End=$(date -d "2024-03-15T00:00" +"%Y-%m-%dT%H:%M")` : Mengatur waktu akhir pemilu
- `iptables -A INPUT -p tcp -s $Revolte_Subnet --dport 80 -m time --datestart "$Pemilu_Start" --datestop "$Pemilu_End" -j DROP` : Mengatur akses pada subnet yang akan di drop

### Testing
```sh
date -u 0110120024
nmap 10.46.4.2 80 #pada Revolte & GrobeForest
```
- Hasil

![image](https://github.com/VanGarman21/PBKK/assets/100523471/5f81f8a4-4ba8-404f-9e22-1a0d89079ea4)

## Soal 9
> Sadar akan adanya potensial saling serang antar kubu politik, maka WebServer harus dapat secara otomatis memblokir  alamat IP yang melakukan scanning port dalam jumlah banyak (maksimal 20 scan port) di dalam selang waktu 10 menit. 
(clue: test dengan nmap)

### Sein & Stark - Web Server
```sh
iptables -F

iptables -N scan_port
iptables -A INPUT -m recent --name scan_port --update --seconds 600 --hitcount 20 -j DROP
iptables -A FORWARD -m recent --name scan_port --update --seconds 600 --hitcount 20 -j DROP
iptables -A INPUT -m recent --name scan_port --set -j ACCEPT
iptables -A FORWARD -m recent --name scan_port --set -j ACCEPT
```

Penjelasan:
- `iptables -F` : Menghapus semua rule yang ada
- `iptables -N scan_port` : Membuat chain baru dengan nama scan_port
- `iptables -A INPUT -m recent --name scan_port --update --seconds 600 --hitcount 20 -j DROP` : Mengatur akses pada input yang melakukan scanning port dalam jumlah banyak (maksimal 20 scan port) di dalam selang waktu 10 menit
- `iptables -A FORWARD -m recent --name scan_port --update --seconds 600 --hitcount 20 -j DROP` : Mengatur akses pada forward yang melakukan scanning port dalam jumlah banyak (maksimal 20 scan port) di dalam selang waktu 10 menit
- `iptables -A INPUT -m recent --name scan_port --set -j ACCEPT` : Mengatur akses pada input yang melakukan scanning port dalam jumlah banyak (maksimal 20 scan port) di dalam selang waktu 10 menit
- `iptables -A FORWARD -m recent --name scan_port --set -j ACCEPT` : Mengatur akses pada forward yang melakukan scanning port dalam jumlah banyak (maksimal 20 scan port) di dalam selang waktu 10 menit

### Testing
> Lakukan Ping ke Sein atau Stark


![image](https://github.com/VanGarman21/PBKK/assets/100523471/9767a863-4b28-4258-924a-836cea68c808)

![image](https://github.com/VanGarman21/PBKK/assets/100523471/d427922f-776e-448c-a0e5-0fe8b9aa8cd4)


## Soal 10
> Karena kepala suku ingin tau paket apa saja yang di-drop, maka di setiap node server dan router ditambahkan logging paket yang di-drop dengan standard syslog level

### Sein & Stark - Web Server
```sh
iptables -A INPUT -j LOG --log-level debug --log-prefix "Packet Dropped:"
```

Penjelasan:
- `iptables -A INPUT -j LOG --log-level debug --log-prefix "Packet Dropped:"` : Mengatur log pada input
- `-A INPUT` : Menambahkan aturan ke rantai INPUT, yang mengatur paket-paket yang masuk ke sistem.
- `-j LOG` : Mengarahkan paket yang memenuhi aturan ini ke target LOG. Ini berarti informasi tentang paket-paket tersebut akan dicatat dalam log sistem.
- `--log-level debug` : Menentukan tingkat log yang diinginkan. Dalam contoh ini, tingkat log ditetapkan sebagai "debug".
- `--log-prefix "Packet Dropped:"` : Menentukan awalan pesan log yang akan ditambahkan ke setiap catatan log yang dihasilkan oleh aturan ini. Dalam contoh ini, awalan "Packet Dropped: " akan ditambahkan ke setiap catatan log.

### Testing
> Jalankan syntaxs berikut pada sein atau stark
```sh
iptables -L
```

![image](https://github.com/VanGarman21/PBKK/assets/100523471/bcbdfe35-6974-4f60-9497-ae95cafad9f0)

![image](https://github.com/VanGarman21/PBKK/assets/100523471/c902092e-fd23-45b1-983f-acd5bcd8377f)










