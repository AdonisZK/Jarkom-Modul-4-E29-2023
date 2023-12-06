# Jarkom-Modul-4-E29-2023
## Anggota
Kelompok E29
| Nama | NRP |
| --- | --- |
| Sony Hermawan | 5025211226 |
| Sekar Ambar Arum | 5025211041 |

# Laporan Resmi
* [Topologi](#Topologi)
* [VLSM](#VLSM)
  * [Subnetting](#Subnetting)
  * [Rute](#Rute)
  * [Tree](#Tree)
  * [Pembagian IP](#Pembagian-IP)
  * [Konfigurasi](#Konfigurasi)
  * [Testing-CPT](#Testing-CPT)
* [CIDR](#CIDR)
  * [Penggabungan IP](#Penggabungan-IP)
  * [Tree CIDR](#Tree-CIDR)
  * [Pembagian IP CIDR](#Pembagian-IP-CIDR)
  * [Config](#Config)
  * [Testing-GNS](#Testing-GNS)

## Topologi

![Screenshot 2023-11-28 235649](https://github.com/AdonisZK/Jarkom-Modul-4-E29-2023/assets/90591077/70cf4226-8b98-4198-a6a0-817ece9d6a74)

## VLSM
### Subnetting
Melakukan subnetting untuk dapat menentukan rute. 

![WhatsApp Image 2023-12-05 at 16 05 00](https://github.com/AdonisZK/Jarkom-Modul-4-E29-2023/assets/90591077/ee5fb45d-3b1e-49e2-b1fb-ecc73a314eca)

### Rute
Rute yang didapat setelah melakukan subnetting.

![Cuplikan layar 2023-12-05 160155](https://github.com/AdonisZK/Jarkom-Modul-4-E29-2023/assets/90591077/32bfb63a-c662-401f-abfc-638af0c12fd0)

### Tree
Membuat tree untuk dapat menentukan pembagian IP.

![WhatsApp Image 2023-12-02 at 19 12 49](https://github.com/AdonisZK/Jarkom-Modul-4-E29-2023/assets/90591077/f88799c3-f6ea-4626-bcf3-793a64773f3e)

### Pembagian IP
Pembagian IP berdasarkan tree yang telah dibuat.

![image](https://github.com/AdonisZK/Jarkom-Modul-4-E29-2023/assets/90591077/53437903-8db1-454f-a7f6-dd84c80bc33c)

### Konfigurasi Network

### Testing-CPT
https://github.com/AdonisZK/Jarkom-Modul-4-E29-2023/assets/48209612/fd3cd4a5-6b2a-4864-9123-0e936d59159d

## CIDR
### Penggabungan IP

<img width="2500" alt="cidr" src="https://github.com/AdonisZK/Jarkom-Modul-4-E29-2023/assets/90591077/d925e28c-2da9-4e80-b7d9-dc53e48f696e">

![Cuplikan layar 2023-12-05 173547](https://github.com/AdonisZK/Jarkom-Modul-4-E29-2023/assets/90591077/d1a5abea-918d-42ae-aca4-5db48322e91a)

![Cuplikan layar 2023-12-05 173555](https://github.com/AdonisZK/Jarkom-Modul-4-E29-2023/assets/90591077/f8e1d89c-8efb-4f8b-b3c5-dd28d1bc98d5)

![Cuplikan layar 2023-12-05 173605](https://github.com/AdonisZK/Jarkom-Modul-4-E29-2023/assets/90591077/ff832ebf-b030-4b16-b958-b49a5fcb4703)

![Cuplikan layar 2023-12-05 173716](https://github.com/AdonisZK/Jarkom-Modul-4-E29-2023/assets/90591077/4c742f18-44f5-4f74-a248-13beee1656ad)

### Tree CIDR
Membuat tree untuk dapat menentukan pembagian IP.

![Tree](https://github.com/AdonisZK/Jarkom-Modul-4-E29-2023/assets/90591077/d12a9a30-5228-4cc0-8524-292c2353be05)

### Pembagian IP CIDR
Pembagian IP berdasarkan tree yang telah dibuat.

![Cuplikan layar 2023-12-06 180333](https://github.com/AdonisZK/Jarkom-Modul-4-E29-2023/assets/90591077/22a69a76-c491-4442-8b21-e04acab9ce08)

### Config

* Aura
```
auto eth0
iface eth0 inet dhcp

auto eth1
iface eth1 inet static
	address 10.51.73.49
	netmask 255.255.255.252

auto eth2
iface eth2 inet static
	address 10.51.73.53
	netmask 255.255.255.252

auto eth3
iface eth3 inet static
	address 10.51.73.45
	netmask 255.255.255.252
```
* Eisen
```
auto eth0
iface eth0 inet static
	address 10.51.73.50
	netmask 255.255.255.252
	gateway 10.51.73.49

auto eth1
iface eth1 inet static
	address 10.51.73.41
	netmask 255.255.255.248

auto eth2
iface eth2 inet static
	address 10.51.73.33
	netmask 255.255.255.252

auto eth3
iface eth3 inet static
	address 10.51.50.1
	netmask 255.255.255.252

auto eth4
iface eth4 inet static
	address 10.51.69.1
	netmask 255.255.255.252
```  
* Denken
```
auto eth0
iface eth0 inet static
	address 10.51.73.54
	netmask 255.255.255.252
	gateway 10.51.73.53

auto eth1
iface eth1 inet static
	address 10.51.72.1
	netmask 255.255.255.0
```
* Frieren
```
auto eth0
iface eth0 inet static
	address 10.51.73.46
	netmask 255.255.255.252
	gateway 10.51.73.45

auto eth1
iface eth1 inet static
	address 10.51.73.1
	netmask 255.255.255.252

auto eth2
iface eth2 inet static
	address 10.51.20.33
	netmask 255.255.255.224
```
* LakeKorridor
```
auto eth0
iface eth0 inet static
	address 10.51.73.2
	netmask 255.255.255.224
	gateway 10.51.73.1
```
* Flamme
```
auto eth0
iface eth0 inet static
	address 10.51.20.34
	netmask 255.255.255.252
	gateway 10.51.20.33

auto eth1
iface eth1 inet static
	address 10.51.8.1
	netmask 255.255.255.252

auto eth2
iface eth2 inet static
	address 10.51.16.1
	netmask 255.255.252.0

auto eth3
iface eth3 inet static
	address 10.51.20.17
	netmask 255.255.255.252
```
* Fern
```
auto eth0
iface eth0 inet static
	address 10.51.8.2
	netmask 255.255.255.252
	gateway 10.51.8.1

auto eth1
iface eth1 inet static
	address 10.51.0.1
	netmask 255.255.248.0
```
* PC-RohrRoad
```
auto eth0
iface eth0 inet static
	address 10.51.16.2
	netmask 255.255.252.0
	gateway 10.51.16.1
```
* Himmel
```
auto eth0
iface eth0 inet static
	address 10.51.20.18
	netmask 255.255.255.252
	gateway 10.51.20.17

auto eth1
iface eth1 inet static
	address 10.51.20.1
	netmask 255.255.255.248
```
* PC-LaubHills
```
auto eth0
iface eth0 inet static
	address 10.51.0.2
	netmask 255.255.248.0
	gateway 10.51.0.1
```
* PC-AppetitRegion
 ```
auto eth0
iface eth0 inet static
	address 10.51.0.3
	netmask 255.255.248.0
	gateway 10.51.0.1
```
* PC-SchwerMountains
```
auto eth0
iface eth0 inet static
	address 10.51.20.2
	netmask 255.255.255.248
	gateway 10.51.20.1
```
* Stark
```
auto eth0
iface eth0 inet static
	address 10.51.73.42
	netmask 255.255.255.252
	gateway 10.51.73.41
```
* Lugner
```
auto eth0
iface eth0 inet static
	address 10.51.69.2
	netmask 255.255.255.252
	gateway 10.51.69.1

auto eth1
iface eth1 inet static
	address 10.51.68.1
	netmask 255.255.252.0

auto eth2
iface eth2 inet static
	address 10.51.64.1
	netmask 255.255.255.0
```
* Linie
```
auto eth0
iface eth0 inet static
	address 10.51.50.2
	netmask 255.255.255.252
	gateway 10.51.50.1

auto eth1
iface eth1 inet static
	address 10.51.40.1
	netmask 255.255.255.252

auto eth2
iface eth2 inet static
	address 10.51.48.1
	netmask 255.255.254.0
```
* Ritcher
```
auto eth0
iface eth0 inet static
	address 10.51.73.34
	netmask 255.255.255.248
	gateway 10.51.73.33
```
* Revolte
```
auto eth0
iface eth0 inet static
	address 10.51.73.35
	netmask 255.255.255.248
	gateway 10.51.73.33
```
* TurkRegion
```
auto eth0
iface eth0 inet static
	address 10.51.64.2
	netmask 255.255.252.0
	gateway 10.51.64.1
```
* GrobeForest
```
auto eth0
iface eth0 inet static
	address 10.51.68.2
	netmask 255.255.255.0
	gateway 10.51.68.1
```
* Lawine
```
auto eth0
iface eth0 inet static
	address 10.51.40.2
	netmask 255.255.255.252
	gateway 10.51.40.1

auto eth1
iface eth1 inet static
	address 10.51.36.1
	netmask 255.255.255.192
```
* GranzChannel
```
auto eth0
iface eth0 inet static
	address 10.51.48.2
	netmask 255.255.254.0
	gateway 10.51.48.1
```
* BredtRegion
```
auto eth0
iface eth0 inet static
	address 10.51.36.2
	netmask 255.255.255.192
	gateway 10.51.36.1
```
* Heiter
```
auto eth0
iface eth0 inet static
	address 10.51.36.3
	netmask 255.255.255.192
	gateway 10.51.36.1

auto eth1
iface eth1 inet static
	address 10.51.32.1
	netmask 255.255.252.0
```
* RiegelCanyon
```
auto eth0
iface eth0 inet static
	address 10.51.32.2
	netmask 255.255.252.0
	gateway 10.51.32.1
```
* Sein
```
auto eth0
iface eth0 inet static
	address 10.51.32.3
	netmask 255.255.252.0
	gateway 10.51.32.1
```
* PC-RoyalCapital
```
auto eth0
iface eth0 inet static
	address 10.51.72.2
	netmask 255.255.255.252
	gateway 10.51.72.1
```
* PC-WilleRegion
```
auto eth0
iface eth0 inet static
	address 10.51.72.3
	netmask 255.255.255.252
	gateway 10.51.72.1
```

### Testing-GNS
https://github.com/AdonisZK/Jarkom-Modul-4-E29-2023/assets/90591077/b7387ca0-2a5f-4ef2-8fed-18211197306d
