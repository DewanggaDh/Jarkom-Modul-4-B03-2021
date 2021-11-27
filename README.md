# Jarkom-Modul-4-B03-2021

Nama Anggota :
1. Dewangga Dharmawan (05111940000029)
2. Ahmad Syafiq Aqil Wafi (05111940000089)

# Cisco Packet Tracer - VLSM

## Topologi CPT

1. Topologi keseluruhan

![image](https://user-images.githubusercontent.com/73766205/143469409-119aab67-35c8-4563-b55b-05094d3aef2c.png)

2. Dari Jipangu, Courtyard, dan Clambelt ke Foosha

![image](https://user-images.githubusercontent.com/73766205/143469714-b511d701-a181-4fff-9e98-e4a2f4f82a47.png)

3. Dari Foosha ke Dorki dan Jorge dan Guanhao

![image](https://user-images.githubusercontent.com/73766205/143469902-f6b96782-e3ba-4db3-9250-118d055aceb0.png)

4. Dari Guanhao ke Jabra, EnniesLobby, Elena, dan Fukurou

![image](https://user-images.githubusercontent.com/73766205/143470071-dcef5683-f228-49ae-b89e-ef74ba83500c.png)

## Tabel perhitungan Subnetting

![image](https://user-images.githubusercontent.com/73766205/143471730-c555b29e-8166-4367-b855-28bab3f47ea6.png)

## Tree Pembagian Subnetting

![image](https://user-images.githubusercontent.com/73766205/143472149-47f5af80-de36-4ff5-88e9-c6e6afd09f84.png)

## End Device :

- Calmbelt

![image](https://user-images.githubusercontent.com/73766205/143472840-902195f2-fab1-49ca-88cc-7b29d5c00e09.png)

- Courtyard

![image](https://user-images.githubusercontent.com/73766205/143472985-006310a3-8e12-46bf-ae51-9b747494c762.png)

- Jipangu

![image](https://user-images.githubusercontent.com/73766205/143473113-b1b4a3bc-c22b-4b38-980c-0b83b9620021.png)

- Cipher

![image](https://user-images.githubusercontent.com/73766205/143473171-79c22c06-7aa2-4967-a3e5-0734b93bc7dc.png)

- Blueno

![image](https://user-images.githubusercontent.com/73766205/143473231-4be4f851-427f-4c80-b480-c2bfdadc55cc.png)

- Jabra

![image](https://user-images.githubusercontent.com/73766205/143473316-d9fb4db0-b79b-4e4a-b07f-2033de9d73c3.png)

- Maingate

![image](https://user-images.githubusercontent.com/73766205/143473361-1370bfdf-963d-4a06-9b1c-7d36ff6436b1.png)

- Jorge

![image](https://user-images.githubusercontent.com/73766205/143473444-e2a06204-d0d8-4007-87ac-8714cf4cd9a9.png)

- EnniesLobby

![image](https://user-images.githubusercontent.com/73766205/143473519-92fb8b10-3f9d-4299-a610-cff9e014b0b5.png)

- Elena

![image](https://user-images.githubusercontent.com/73766205/143473566-716fed8b-417d-4697-8c12-1895e67d151e.png)

## Router :

- Pucci
```
Interface
Fa0/0 (Ke Water7) :
IP : 192.178.0.2/30
Fa0/1 (Ke Jipangu) :
IP : 192.178.0.129/25
Fa1/0 (Ke Calmbelt-Courtyard) :
IP : 192.178.24.1/21
```
```
Routing Network Address :
0.0.0.0/0 via 192.178.0.1
192.178.4.0/22 via 192.178.0.1
192.178.8.0/22 via 192.178.0.1
192.178.12.0/22 via 192.178.0.1
192.178.16.0/22 via 192.178.0.1
192.178.2.0/23 via 192.178.0.1
192.178.1.0/24 via 192.178.0.1
192.178.0.32/28 via 192.178.0.1
192.178.0.4/30 via 192.178.0.1
192.178.0.8/30 via 192.178.0.1
192.178.0.12/30 via 192.178.0.1
192.178.0.16/30 via 192.178.0.1
192.178.0.20/30 via 192.178.0.1
```
- Water7
```
Interface
Fa0/0 (Ke Foosha) :
IP : 192.178.0.6/30
Fa0/1 (Ke Pucci) :
IP : 192.178.0.1/30
Fa1/0 (Ke Cipher) :
IP : 192.178.12.1/22
```
```
Routing Network Address :
0.0.0.0/0 via 192.178.0.2
192.178.0.128/25 via 192.178.0.2
192.178.24.0/21 via 192.178.0.2
192.178.4.0/22 via 192.178.0.5
192.178.8.0/22 via 192.178.0.5
192.178.12.0/22 via 192.178.0.5
192.178.16.0/22 via 192.178.0.5
192.178.2.0/23 via 192.178.0.5
192.178.1.0/24 via 192.178.0.5
192.178.0.32/28 via 192.178.0.5
192.178.0.8/30 via 192.178.0.5
192.178.0.12/30 via 192.178.0.5
192.178.0.16/30 via 192.178.0.5
192.178.0.20/30 via 192.178.0.5
```
- Foosha
```
Interface
Fa0/0 (Ke Water7) :
IP : 192.178.0.5/30
Fa0/1 (Ke Blueno) :
IP : 192.178.4.1/22
Fa1/0 (Ke Guanhao) :
IP : 192.178.0.9/30
Fa1/1 (Ke Dorki) :
IP : 192.178.0.17/30
Console (Ke Cloud)
```
```
Routing Network Address :
0.0.0.0/0 via 192.178.0.6
192.178.0.0/30 via 192.178.0.6
192.178.12.0/22 via 192.178.0.6
192.178.24.0/21 via 192.178.0.6
0.0.0.0/0 via 192.178.0.10
192.178.2.0/23 via 192.178.0.10
192.178.0.32/28 via 192.178.0.10
192.178.16.0/22 via 192.178.0.10
192.178.0.12/30 via 192.178.0.10
192.178.0.20/30 via 192.178.0.10
192.178.1.0/24 via 192.178.0.10
192.178.8.0/22 via 192.178.0.10
```
- Guanhao
```
Interface
Fa0/0 (Ke Oimo) :
IP : 192.178.0.13/30
Fa0/1 (Ke Foosha) :
IP : 192.178.0.10/30
Fa1/0 (Ke Jabra) :
IP : 192.178.16.1/22
Fa1/1 (ke Maingate dan Alabasta)
IP : 192.178.2.1/23
```
```
Routing Network Address :
0.0.0.0/0 via 192.178.0.14
192.178.0.20/30 via 192.178.0.14
192.178.1.0/24 via 192.178.0.14
192.178.8.0/22 via 192.178.0.14
192.178.0.32/28 via 192.178.2.3
0.0.0.0/0 via 192.178.0.9
192.178.0.16/30 via 192.178.0.9
192.178.4.0/22 via 192.178.0.9
192.178.0.4/30 via 192.178.0.9
192.178.12.0/22 via 192.178.0.9
192.178.0.0/30 via 192.178.0.9
192.178.0.128/25 via 192.178.0.9
192.178.24.0/21 via 192.178.0.9
192.178.2.0/23 via 192.178.2.2
0.0.0.0/0 via 192.178.2.3
```
- Oimo
```
Interface
Fa0/0 (Ke Guanhao) :
IP : 192.178.0.14/30
Fa0/1 (Ke EnniesLobby dan Seastone) :
IP : 192.178.1.1/24
Fa1/0 (Ke Fukurou) :
IP : 192.178.0.21/30
```
```
Routing Network Address :
0.0.0.0/0 via 192.178.1.3
0.0.0.0/0 via 192.178.0.13
192.178.24.0/21 via 192.178.0.13
192.178.4.0/22 via 192.178.0.13
192.178.12.0/22 via 192.178.0.13
192.178.16.0/22 via 192.178.0.13
192.178.2.0/23 via 192.178.0.13
192.178.0.128/25 via 192.178.0.13
192.178.0.32/28 via 192.178.0.13
192.178.0.0/30 via 192.178.0.13
192.178.0.4/30 via 192.178.0.13
192.178.0.8/30 via 192.178.0.13
192.178.0.16/30 via 192.178.0.13
192.178.0.20/30 via 192.178.0.13
192.178.8.0/22 via 192.178.1.3
```
- Alabasta
```
Interface
Fa0/0 (Ke Maingate dan Guanhao) :
IP : 192.178.2.3/23
Fa0/1 (Ke Jorge) :
IP : 192.178.0.33/28
```
```
Routing Network Address :
192.178.24.0/21 via 192.178.24.1
192.178.4.0/22 via 192.178.24.1
192.178.8.0/22 via 192.178.24.1
192.178.12.0/22 via 192.178.24.1
192.178.16.0/22 via 192.178.24.1
192.178.1.0/24 via 192.178.24.1
192.178.0.128/25 via 192.178.24.1
192.178.0.0/30 via 192.178.24.1
192.178.0.4/30 via 192.178.24.1
192.178.0.8/30 via 192.178.24.1
192.178.0.12/30 via 192.178.24.1
192.178.0.16/30 via 192.178.24.1
192.178.0.20/30 via 192.178.24.1
0.0.0.0/0 via 192.178.2.1
```
- Seastone
```
Interface
Fa0/0 (Ke EnniesLobby dan Oimo) :
IP : 192.178.1.3/24
Fa0/1 (Ke Elena) :
IP : 192.178.8.1/22
```
```
Routing Network Address :
0.0.0.0/0 via 192.178.1.1
192.178.24.0/21 via 192.178.1.1
192.178.4.0/22 via 192.178.1.1
192.178.12.0/22 via 192.178.1.1
192.178.16.0/22 via 192.178.1.1
192.178.2.0/23 via 192.178.1.1
192.178.0.128/25 via 192.178.1.1
192.178.0.32/28 via 192.178.1.1
192.178.0.0/30 via 192.178.1.1
192.178.0.4/30 via 192.178.1.1
192.178.0.8/30 via 192.178.1.1
192.178.0.12/30 via 192.178.1.1
192.178.0.16/30 via 192.178.1.1
192.178.0.20/30 via 192.178.1.1
```

## Server :
- Dorki

![image](https://user-images.githubusercontent.com/73766205/143477570-6d6d7009-af83-4e6f-b445-77c83e73ec0b.png)

- Fukurou

![image](https://user-images.githubusercontent.com/73766205/143477638-c6cac21a-33a5-4f98-9464-baded50eecd8.png)

## GNS3 - CIDR

### Topologi GNS3

![image](https://user-images.githubusercontent.com/16128257/143228495-efb1a8f5-4280-45ce-9193-097981f0ee8c.png)

### Subnetting Topologi

![image](https://user-images.githubusercontent.com/16128257/143228403-1487e2b8-8dff-4251-b564-0588c0c746fa.png)

![image](https://user-images.githubusercontent.com/16128257/143565385-8462ba46-07dd-461d-8fd9-9d7734175826.png)

![image](https://user-images.githubusercontent.com/16128257/143575404-4174c080-b73e-4385-a14b-1c662fc2d4b2.png)

![image](https://user-images.githubusercontent.com/16128257/143567785-20b000a6-d7ca-4c94-8562-bc0e75165cac.png)

![image](https://user-images.githubusercontent.com/16128257/143566404-5e3a058a-9c29-4a08-a8a5-50940c096bcc.png)

![image](https://user-images.githubusercontent.com/16128257/143568178-7bdf12e8-57ba-466e-8c34-a5bdf47e232f.png)

![image](https://user-images.githubusercontent.com/16128257/143568349-a4f22e65-ce88-4d61-883b-2084a26884f9.png)

![image](https://user-images.githubusercontent.com/16128257/143568504-ef67bd9d-6e87-43ee-ae42-c0202550b32b.png)

### Penghitungan CIDR dari Subnetting

![image](https://user-images.githubusercontent.com/16128257/143590216-512cf1d3-fba1-4eb6-8841-7d7bb95ac176.png)

### Hasil NID dan Netmask dari Penghitungan CIDR

```
A1: 192.178.32.0/22     # Water7, Cipher
A2: 192.178.128.0/22    # Foosha, BlueNo
A3: 192.178.0.0/25      # Pucci, Jipangu
A4: 192.178.16.0/30     # Water7, Pucci
A5: 192.178.64.0/30     # Foosha, Water7
A6: 192.179.128.0/30    # Foosha, Doriki
A7: 192.178.8.0/21      # Pucci, Calmbelt, Courtyard
A8: 192.179.4.0/22      # Guanhao, Jabra
A9: 192.179.64.0/30     # Foosha, Guanhao
A10: 192.179.48.0/30    # Guanhao, Oimo
A11: 192.179.0.0/23     # Guanhao, Alabasta, MainGate
A12: 192.179.2.0/28     # Alabasta, Jorge
A13: 192.179.32.0/24    # Oimo, Seastone, EnniesLobby
A14: 192.179.40.0/30    # Oimo, Fukurou
A15: 192.179.36.0/22    # Seastone, Elena
```

### Detail Konfigurasi Network Interface

Pada GNS3, klik kanan pada masing - masing node edit configuration network interface menjadi config masing - masing node berikut.

#### FOOSHA

```
auto eth0
iface eth0 inet dhcp

# A2
auto eth1
iface eth1 inet static
    address 192.178.128.1
    netmask 255.255.252.0

# A5
auto eth2
iface eth2 inet static
    address 192.178.64.1
    netmask 255.255.255.252

# A9
auto eth3
iface eth3 inet static
    address 192.179.64.1
    netmask 255.255.255.252

# A6
auto eth4
iface eth4 inet static
    address 192.179.128.1
    netmask 255.255.255.252
```

#### BLUENO

```
# A2
auto eth0
iface eth0 inet static
    address 192.178.128.2
    netmask 255.255.252.0
    gateway 192.178.128.1
    up echo nameserver 192.178.122.1 > /etc/resolv.conf
```

#### DORIKI

```
# A6
auto eth0
iface eth0 inet static
    address 192.179.128.2
    netmask 255.255.255.252
    gateway 192.179.128.1
    up echo nameserver 192.178.122.1 > /etc/resolv.conf
```

#### WATER7

```
# A5
auto eth0
iface eth0 inet static
    address 192.178.64.2
    netmask 255.255.255.252
    gateway 192.178.64.1
    up echo nameserver 192.178.122.1 > /etc/resolv.conf

# A4
auto eth1
iface eth1 inet static
    address 192.178.16.1
    netmask 255.255.255.252

# A1
auto eth2
iface eth2 inet static
    address 192.178.32.1
    netmask 255.255.255.0
```

#### CIPHER

```
# A1
auto eth0
iface eth0 inet static
    address 192.178.32.2
    netmask 255.255.252.0
    gateway 192.178.32.1
    up echo nameserver 192.178.122.1 > /etc/resolv.conf
```

#### PUCCI

```
# A4
auto eth0
iface eth0 inet static
    address 192.178.16.2
    netmask 255.255.255.252
    gateway 192.178.16.1
    up echo nameserver 192.178.122.1 > /etc/resolv.conf

# A3
auto eth1
iface eth1 inet static
    address 192.178.0.1
    netmask 255.255.255.128

# A7
auto eth2
iface eth2 inet static
    address 192.178.8.1
    netmask 255.255.248.0
```

#### JIPANGU

```
# A3
auto eth0
iface eth0 inet static
    address 192.178.0.2
    netmask 255.255.255.128
    gateway 192.178.0.1
    up echo nameserver 192.178.122.1 > /etc/resolv.conf
```

#### CAMBELT

```
# A7
auto eth0
iface eth0 inet static
    address 192.178.8.2
    netmask 255.255.248.0
    gateway 192.178.8.1
    up echo nameserver 192.178.122.1 > /etc/resolv.conf
```

#### COURTYARD

```
# A7
auto eth0
iface eth0 inet static
    address 192.178.8.3
    netmask 255.255.248.0
    gateway 192.178.8.1
    up echo nameserver 192.178.122.1 > /etc/resolv.conf
```

#### GUANHAO

```
# A9
auto eth0
iface eth0 inet static
     address 192.179.64.2
     netmask 255.255.255.252
     gateway 192.179.64.1
     up echo nameserver 192.178.122.1 > /etc/resolv.conf

# A8
auto eth1
iface eth1 inet static
    address 192.179.4.1
    netmask 255.255.252.0

# A10
auto eth2
iface eth2 inet static
    address 192.179.48.1
    netmask 255.255.255.252

# A11
auto eth3
iface eth3 inet static
     address 192.179.0.1
     netmask 255.255.254.0

```

#### JABRA

```
# A8
auto eth0
iface eth0 inet static
    address 192.179.4.2
    netmask 255.255.252.0
    gateway 192.179.4.1
    up echo nameserver 192.178.122.1 > /etc/resolv.conf
```

#### ALABASTA

```
# A11
auto eth0
iface eth0 inet static
    address 192.179.0.2
    netmask 255.255.254.0
    gateway 192.179.0.1
    up echo nameserver 192.178.122.1 > /etc/resolv.conf

# A12
auto eth1
iface eth1 inet static
    address 192.179.2.1
    netmask 255.255.255.240

```

#### MAINGATE

```
# A11
auto eth0
iface eth0 inet static
    address 192.179.0.3
    netmask 255.255.254.0
    gateway 192.179.0.1
    up echo nameserver 192.178.122.1 > /etc/resolv.conf

```

#### JORGE

```
# A12
auto eth0
iface eth0 inet static
    address 192.179.2.2
    netmask 255.255.255.240
    gateway 192.179.2.1
    up echo nameserver 192.178.122.1 > /etc/resolv.conf
```

#### OIMO

```
# A10
auto eth0
iface eth0 inet static
     address 192.179.48.2
     netmask 255.255.255.252
     gateway 192.179.48.1
     up echo nameserver 192.178.122.1 > /etc/resolv.conf

# A13
auto eth1
iface eth1 inet static
    address 192.179.32.1
    netmask 255.255.255.0

# A14
auto eth2
iface eth2 inet static
    address 192.179.40.1
    netmask 255.255.255.252
```

#### FUKUROU

```
# A14
auto eth0
iface eth0 inet static
    address 192.179.40.2
    netmask 255.255.255.252
    gateway 192.179.40.1
    up echo nameserver 192.178.122.1 > /etc/resolv.conf
```

#### ENNIESLOBBY

```
# A13
auto eth0
iface eth0 inet static
    address 192.179.32.3
    netmask 255.255.255.0
    gateway 192.179.32.1
    up echo nameserver 192.178.122.1 > /etc/resolv.conf
```

#### SEASTONE

```
# A13
auto eth0
iface eth0 inet static
    address 192.179.32.2
    netmask 255.255.255.0
    gateway 192.179.32.1
    up echo nameserver 192.178.122.1 > /etc/resolv.conf

# A15
auto eth1
iface eth1 inet static
    address 192.179.36.1
    netmask 255.255.252.0
```

#### ELENA

```
# A15
auto eth0
iface eth0 inet static
    address 192.179.36.2
    netmask 255.255.252.0
    gateway 192.179.36.1
    up echo nameserver 192.178.122.1 > /etc/resolv.conf
```

### Detail Konfigurasi Routing

Untuk setiap router (FOOSHA, PUCCI, dll), tambahkan command berikut pada `.bashrc`.

```
iptables -t nat -A POSTROUTING -o eth0 -j MASQUERADE -s 192.178.0.0/15
```

Untuk masing - masing router juga, tambahkan command - command dibawah berikut juga pada `.bashrc`.

Setelah command telah ditambahkan, kemudian save lalu run `source .bashrc` untuk melakukan run file `.bashrc`.

#### FOOSHA

```
route add -net 192.178.32.0 netmask 255.255.252.0 gw 192.178.64.2 #A5 - A1
route add -net 192.178.16.0 netmask 255.255.255.252 gw 192.178.64.2 #A5 - A4
route add -net 192.178.0.0 netmask 255.255.255.128 gw 192.178.64.2 #A5 - A3
route add -net 192.178.8.0 netmask 255.255.248.0 gw 192.178.64.2 #A5 - A7
route add -net 192.179.4.0 netmask 255.255.252.0 gw 192.179.64.2 #A9 - A8
route add -net 192.179.48.0 netmask 255.255.255.252 gw 192.179.64.2 #A9 - A10
route add -net 192.179.0.0 netmask 255.255.254.0 gw 192.179.64.2 #A9 - A11
route add -net 192.179.2.0 netmask 255.255.255.240 gw 192.179.64.2 #A9 - A12
route add -net 192.179.32.0 netmask 255.255.255.0 gw 192.179.64.2 #A9 - A13
route add -net 192.179.40.0 netmask 255.255.255.252 gw 192.179.64.2 #A9 - A14
route add -net 192.179.36.0 netmask 255.255.252.0 gw 192.179.64.2 #A9 - A15
```

#### WATER7

```
route add -net 0.0.0.0 netmask 0.0.0.0 gw 192.178.64.1 #A5 - Self
route add -net 192.178.0.0 netmask 255.255.255.128 gw 192.178.16.2 #A4 - A3
route add -net 192.178.8.0 netmask 255.255.248.0 gw 192.178.16.2 #A4 - A7
```

#### PUCCI

```
route add -net 0.0.0.0 netmask 0.0.0.0 gw 192.178.16.1 #A4 - Self
```

#### GUANHAO

```
route add -net 0.0.0.0 netmask 0.0.0.0 gw 192.179.64.1 #A9 - Self
route add -net 192.179.2.0 netmask 255.255.255.240 gw 192.179.0.2 #A11 - A12
route add -net 192.179.32.0 netmask 255.255.255.0 gw 192.179.48.2 #A10 - A13
route add -net 192.179.36.0 netmask 255.255.252.0 gw 192.179.48.2 #A10 - A15
route add -net 192.179.40.0 netmask 255.255.255.252 gw 192.179.48.2 #A10 - A14
```

#### ALABASTA

```
route add -net 0.0.0.0 netmask 0.0.0.0 gw 192.179.0.1 #A11 - Self
```

#### OIMO

```
route add -net 0.0.0.0 netmask 0.0.0.0 gw 192.179.48.1 #A10 - Self
route add -net 192.179.36.0 netmask 255.255.252.0 gw 192.179.32.2 #A13 - A15
```

#### SEASTONE

```
route add -net 0.0.0.0 netmask 0.0.0.0 gw 192.179.32.1 #A13 - Self
```
