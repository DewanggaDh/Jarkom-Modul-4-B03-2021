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

## GNS3 - VLSM

### Topologi GNS3

![image](https://user-images.githubusercontent.com/16128257/143228495-efb1a8f5-4280-45ce-9193-097981f0ee8c.png)

### Subnetting Topologi

![image](https://user-images.githubusercontent.com/16128257/143228403-1487e2b8-8dff-4251-b564-0588c0c746fa.png)

### Penghitungan VLSM dari Subnetting

![image](https://user-images.githubusercontent.com/16128257/143228561-ebd5519a-8355-4c59-ad90-48827d7d9451.png)

### Hasil NID dan Netmask dari Penghitungan VLSM

```
A1: 192.178.8.0/22
A2: 192.178.12.0/22
A3: 192.178.27.0/25
A4: 192.178.27.144/30
A5: 192.178.27.148/30
A6: 192.178.27.152/30
A7: 192.178.0.0/21
A8: 192.178.16.0/22
A9: 192.178.27.156/30
A10: 192.178.27.160/30
A11: 192.178.20.0/22
A12: 192.178.27.128/28
A13: 192.178.26.0/24
A14: 192.178.27.164/30
A15: 192.178.20.0/22
```

### Detail Konfigurasi Network Interface

#### FOOSHA

```
iface eth0 inet dhcp

auto eth1
iface eth1 inet static
    address 192.178.12.1
    netmask 255.255.252.0

auto eth2
iface eth2 inet static
    address 192.178.27.149
    netmask 255.255.255.252

auto eth3
iface eth3 inet static
    address 192.178.27.157
    netmask 255.255.255.252

auto eth4
iface eth4 inet static
    address 192.178.27.153
    netmask 255.255.255.252
```

![image](https://user-images.githubusercontent.com/16128257/143219674-2bfbcf19-8dca-4af9-8f45-5c2023ee04f0.png)

![image](https://user-images.githubusercontent.com/16128257/143229275-bf0a8215-0ba7-4d4b-9b02-90f9f66457c7.png)

#### DORIKI

```
auto eth0
iface eth0 inet static
    address 192.178.27.154
    netmask 255.255.255.252
    gateway 192.178.27.153
    up echo nameserver 192.178.122.1 > /etc/resolv.conf
```

![image](https://user-images.githubusercontent.com/16128257/143219994-235fa987-3f20-456c-bd23-aab35bcccd3e.png)

![image](https://user-images.githubusercontent.com/16128257/143229333-da6161c5-ff0d-408e-bc73-2b0c9ecd103d.png)

#### WATER7

```
auto eth0
iface eth0 inet static
    address 192.178.27.150
    netmask 255.255.255.252
    gateway 192.178.27.149
    up echo nameserver 192.178.122.1 > /etc/resolv.conf

auto eth1
iface eth1 inet static
    address 192.178.27.145
    netmask 255.255.255.252

auto eth2
iface eth2 inet static
    address 192.178.8.1
    netmask 255.255.255.0
```

![image](https://user-images.githubusercontent.com/16128257/143220228-0b5f25bb-b3a0-4180-95df-8a6024c56da4.png)

![image](https://user-images.githubusercontent.com/16128257/143229413-5644f7a0-8e18-4e9d-a904-540c8e33da9c.png)

#### BLUENO(1000Host)

```
auto eth0
iface eth0 inet static
    address 192.178.12.2
    netmask 255.255.252.0
    gateway 192.178.12.1
    up echo nameserver 192.178.122.1 > /etc/resolv.conf
```

![image](https://user-images.githubusercontent.com/16128257/143220492-063affa6-fa99-468e-8342-dbde1f67541c.png)

![image](https://user-images.githubusercontent.com/16128257/143229495-5d7cdbe4-99cc-4405-a470-92776ba99a12.png)

#### CIPHER(700Host)

```
auto eth0
iface eth0 inet static
    address 192.178.8.2
    netmask 255.255.252.0
    gateway 192.178.8.1
    up echo nameserver 192.178.122.1 > /etc/resolv.conf
```

![image](https://user-images.githubusercontent.com/16128257/143220715-1c8bf7ef-20d5-4ed6-95f4-3fba07da8d65.png)

![image](https://user-images.githubusercontent.com/16128257/143229589-4189abb2-ac96-4c0a-9d1b-61486b98b87d.png)

#### PUCCI

```
auto eth0
iface eth0 inet static
    address 192.178.27.146
    netmask 255.255.255.252
    gateway 192.178.27.145
    up echo nameserver 192.178.122.1 > /etc/resolv.conf

auto eth1
iface eth1 inet static
    address 192.178.27.1
    netmask 255.255.255.128

auto eth2
iface eth2 inet static
    address 192.178.0.1
    netmask 255.255.248.0
```

![image](https://user-images.githubusercontent.com/16128257/143222382-e8201ca2-8a6a-42d8-b025-b102a05430d0.png)

![image](https://user-images.githubusercontent.com/16128257/143229825-6279f5f5-088f-4267-a30e-e3e18d20927d.png)

#### JIPANGU(100Host)

```
auto eth0
iface eth0 inet static
    address 192.178.27.2
    netmask 255.255.255.128
    gateway 192.178.27.1
    up echo nameserver 192.178.122.1 > /etc/resolv.conf
```

![image](https://user-images.githubusercontent.com/16128257/143222532-6650471f-42b4-4780-9d23-fcd5fff1bfed.png)

![image](https://user-images.githubusercontent.com/16128257/143229898-5d12b5eb-b683-4fa1-b8fd-d5908e88f620.png)

#### COURTYARD(1020Host)

```
auto eth0
iface eth0 inet static
    address 192.178.4.0
    netmask 255.255.248.0
    gateway 192.178.0.1
    up echo nameserver 192.178.122.1 > /etc/resolv.conf
```

![image](https://user-images.githubusercontent.com/16128257/143222696-d891e9dc-58bf-47c5-bbed-f2f39fe0eda0.png)

![image](https://user-images.githubusercontent.com/16128257/143229962-f01f8ae0-de9d-47db-a8b1-4d61f17c368e.png)

#### CALMBELT(1000Host)

```
auto eth0
iface eth0 inet static
    address 192.178.0.2
    netmask 255.255.248.0
    gateway 192.178.0.1
    up echo nameserver 192.178.122.1 > /etc/resolv.conf
```

![image](https://user-images.githubusercontent.com/16128257/143222903-89588af3-0c35-4b4c-9485-cd3dcdb7d09c.png)

![image](https://user-images.githubusercontent.com/16128257/143230027-1374aadf-a3da-4efd-99dc-74bb010cbf3a.png)

#### GUANHAO

```
auto eth0
iface eth0 inet static
     address 192.178.27.158
     netmask 255.255.255.252
     gateway 192.178.27.157
     up echo nameserver 192.178.122.1 > /etc/resolv.conf

auto eth1
iface eth1 inet static
    address 192.178.16.1
    netmask 255.255.252.0

auto eth2
iface eth2 inet static
    address 192.178.27.161
    netmask 255.255.255.252

auto eth3
iface eth3 inet static
     address 192.178.24.1
     netmask 255.255.254.0
```

![image](https://user-images.githubusercontent.com/16128257/143223221-5e20a76b-9e03-4e9c-80e8-0bd425a10645.png)

![image](https://user-images.githubusercontent.com/16128257/143230097-d31ec1a9-fe8e-406c-918c-c2f04a31b9c0.png)

#### JABRA(520Host)

```
auto eth0
iface eth0 inet static
    address 192.178.16.2
    netmask 255.255.252.0
    gateway 192.178.16.1
    up echo nameserver 192.178.122.1 > /etc/resolv.conf
```

![image](https://user-images.githubusercontent.com/16128257/143223399-e782d288-7e78-4f4b-9b0d-02fa3125f00d.png)

![image](https://user-images.githubusercontent.com/16128257/143230185-a2ff0ed4-1ea0-4a53-9a20-9dceb8aeb93f.png)

#### MAINGATE(500Host)

```
auto eth0
iface eth0 inet static
    address 192.178.24.3
    netmask 255.255.254.0
    gateway 192.178.24.1
    up echo nameserver 192.178.122.1 > /etc/resolv.conf
```

![image](https://user-images.githubusercontent.com/16128257/143223563-8bcbbd82-ad32-48a5-8d32-504f158ca235.png)

![image](https://user-images.githubusercontent.com/16128257/143230275-18975504-b2a4-4210-805b-7b37ca54a347.png)

#### ALABASTA

```
auto eth0
iface eth0 inet static
    address 192.178.24.2
    netmask 255.255.254.0
    gateway 192.178.24.1
    up echo nameserver 192.178.122.1 > /etc/resolv.conf

auto eth1
iface eth1 inet static
    address 192.178.27.129
    netmask 255.255.255.240
```

![image](https://user-images.githubusercontent.com/16128257/143223760-f86055ca-d2c0-40ac-b5df-23f12532e744.png)

![image](https://user-images.githubusercontent.com/16128257/143230358-9da0c15e-cd9d-4a47-9856-260eb135e14c.png)

#### JORGE(12Host)

```
auto eth0
iface eth0 inet static
    address 192.178.27.130
    netmask 255.255.255.240
    gateway 192.178.27.129
    up echo nameserver 192.178.122.1 > /etc/resolv.conf
```

![image](https://user-images.githubusercontent.com/16128257/143223898-fc0fd0a8-c19c-40b5-8eec-88831fada97a.png)

![image](https://user-images.githubusercontent.com/16128257/143230437-207556d6-7343-4017-8ed7-19bd77e71c89.png)

#### OIMO

```
auto eth0
iface eth0 inet static
     address 192.178.27.162
     netmask 255.255.255.252
     gateway 192.178.27.161
     up echo nameserver 192.178.122.1 > /etc/resolv.conf

auto eth1
iface eth1 inet static
    address 192.178.26.1
    netmask 255.255.255.0

auto eth2
iface eth2 inet static
    address 192.178.27.165
    netmask 255.255.255.252
```

![image](https://user-images.githubusercontent.com/16128257/143227163-a2e94e0d-553b-4fde-a5d8-9951b3800edb.png)

![image](https://user-images.githubusercontent.com/16128257/143230528-de07a9ce-0005-4c0b-9e5f-525c073b7912.png)

#### FUKUROU

```
auto eth0
iface eth0 inet static
    address 192.178.27.166
    netmask 255.255.255.252
    gateway 192.178.27.165
    up echo nameserver 192.178.122.1 > /etc/resolv.conf
```

![image](https://user-images.githubusercontent.com/16128257/143227311-421ebace-cb65-42ec-98f2-c1c764b0d379.png)

![image](https://user-images.githubusercontent.com/16128257/143230607-72232935-c67b-4ed6-9bd0-1169e85ef8ba.png)

#### ENNIESLOBBY(250Host)

```
auto eth0
iface eth0 inet static
    address 192.178.26.3
    netmask 255.255.255.0
    gateway 192.178.26.1
    up echo nameserver 192.178.122.1 > /etc/resolv.conf
```

![image](https://user-images.githubusercontent.com/16128257/143227485-3a0653c4-5695-43f4-87b0-9d7c2a990efb.png)

![image](https://user-images.githubusercontent.com/16128257/143230674-ef77d74c-b91e-4f5a-9e7c-4055b5396113.png)

#### SEASTONE

```
auto eth0
iface eth0 inet static
    address 192.178.26.2
    netmask 255.255.255.0
    gateway 192.178.26.1
    up echo nameserver 192.178.122.1 > /etc/resolv.conf

auto eth1
iface eth1 inet static
    address 192.178.20.1
    netmask 255.255.252.0
```

![image](https://user-images.githubusercontent.com/16128257/143227680-6607da4d-6bd4-4aea-8c31-e4f9bc09c82d.png)

![image](https://user-images.githubusercontent.com/16128257/143230738-f8a51021-e0dc-4d0f-a357-e0f036ad8f79.png)

#### ELENA(720Host)

```
auto eth0
iface eth0 inet static
    address 192.178.20.2
    netmask 255.255.252.0
    gateway 192.178.20.1
    up echo nameserver 192.178.122.1 > /etc/resolv.conf
```

![image](https://user-images.githubusercontent.com/16128257/143227936-c915d730-9d51-4e33-9fa8-135b7ef211a1.png)

![image](https://user-images.githubusercontent.com/16128257/143230816-a6153bb0-7b28-4022-bdfb-f06f843f64bc.png)
