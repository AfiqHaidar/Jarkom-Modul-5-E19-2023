# Jarkom-Modul-3-E19-2023
Laporan Resmi Praktikum Modul 3 Kelompok E19
| Nama               |  NRP       | 
|--------------------|-------------|
| M. Armand Giovani | 5025211054  |
| Afiq Fawwaz Haidar | 5025211246  |

## Topologi

![image](https://github.com/AfiqHaidar/Jarkom-Modul-5-E19-2023/assets/70834506/1c12984b-8361-4c20-ad56-9a6f6fc8f096)

## Pembagian IP

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

## Soal 3
> Kepala Suku North Area meminta kalian untuk membatasi DHCP dan DNS Server hanya dapat dilakukan ping oleh maksimal 3 device secara bersamaan, selebihnya akan di drop.

### Richter - DNS Server & Revolte - DHCP Server
```sh
iptables -A INPUT -p icmp -m connlimit --connlimit-above 3 --connlimit-mask 0 -j DROP
```

### Testing

## Soal 4
> Lakukan pembatasan sehingga koneksi SSH pada Web Server hanya dapat dilakukan oleh masyarakat yang berada pada GrobeForest

### Sein & Stark - Web Server
```sh
sudo iptables -A INPUT --dport 22 -s 10.46.4.3:10.46.7.254 -j ACCEPT
sudo iptables -A INPUT --dport 22 -j DROP
```

### Testing

## Soal 5 
> Selain itu, akses menuju WebServer hanya diperbolehkan saat jam kerja yaitu Senin-Jumat pada pukul 08.00-16.00.

### Sein & Stark - Web Server
```sh
iptables -A INPUT -m time --timestart 08:00 --timestop 16:00 --days Mon,Tue,Wed,Thu,Fri -j ACCEPT
```

### Testing

## Soal 6
> Lalu, karena ternyata terdapat beberapa waktu di mana network administrator dari WebServer tidak bisa stand by, sehingga perlu ditambahkan rule bahwa akses pada hari Senin - Kamis pada jam 12.00 - 13.00 dilarang (istirahat maksi cuy) dan akses di hari Jumat pada jam 11.00 - 13.00 juga dilarang (maklum, Jumatan rek).

### Konfigurasi

### Testing

## Soal 7
> Karena terdapat 2 WebServer, kalian diminta agar setiap client yang mengakses Sein dengan Port 80 akan didistribusikan secara bergantian pada Sein dan Stark secara berurutan dan request dari client yang mengakses Stark dengan port 443 akan didistribusikan secara bergantian pada Sein dan Stark secara berurutan.

### Konfigurasi

### Testing

## Soal 8
> Karena berbeda koalisi politik, maka subnet dengan masyarakat yang berada pada Revolte dilarang keras mengakses WebServer hingga masa pencoblosan pemilu kepala suku 2024 berakhir. Masa pemilu (hingga pemungutan dan penghitungan suara selesai) kepala suku bersamaan dengan masa pemilu Presiden dan Wakil Presiden Indonesia 2024.

### Konfigurasi

### Testing

## Soal 9
> Sadar akan adanya potensial saling serang antar kubu politik, maka WebServer harus dapat secara otomatis memblokir  alamat IP yang melakukan scanning port dalam jumlah banyak (maksimal 20 scan port) di dalam selang waktu 10 menit. 
(clue: test dengan nmap)

### Konfigurasi

### Testing

## Soal 10
> Karena kepala suku ingin tau paket apa saja yang di-drop, maka di setiap node server dan router ditambahkan logging paket yang di-drop dengan standard syslog level

### Konfigurasi

### Testing











