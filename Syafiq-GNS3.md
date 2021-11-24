## GNS3 - VLSM

### FOOSHA

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

### DORIKI

```
auto eth0
iface eth0 inet static
    address 192.178.27.154
    netmask 255.255.255.252
    gateway 192.178.27.153
    up echo nameserver 192.178.122.1 > /etc/resolv.conf
```

![image](https://user-images.githubusercontent.com/16128257/143219994-235fa987-3f20-456c-bd23-aab35bcccd3e.png)


### WATER7

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

### BLUENO(1000Host)

```
auto eth0
iface eth0 inet static
    address 192.178.12.2
    netmask 255.255.252.0
    gateway 192.178.12.1
    up echo nameserver 192.178.122.1 > /etc/resolv.conf
```

![image](https://user-images.githubusercontent.com/16128257/143220492-063affa6-fa99-468e-8342-dbde1f67541c.png)

### CIPHER(700Host)

```
auto eth0
iface eth0 inet static
    address 192.178.8.2
    netmask 255.255.252.0
    gateway 192.178.8.1
    up echo nameserver 192.178.122.1 > /etc/resolv.conf
```

![image](https://user-images.githubusercontent.com/16128257/143220715-1c8bf7ef-20d5-4ed6-95f4-3fba07da8d65.png)

### PUCCI

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

### JIPANGU(100Host)

```
auto eth0
iface eth0 inet static
    address 192.178.27.2
    netmask 255.255.255.128
    gateway 192.178.27.1
    up echo nameserver 192.178.122.1 > /etc/resolv.conf
```

![image](https://user-images.githubusercontent.com/16128257/143222532-6650471f-42b4-4780-9d23-fcd5fff1bfed.png)

### COURTYARD(1020Host)

```
auto eth0
iface eth0 inet static
    address 192.178.4.0
    netmask 255.255.248.0
    gateway 192.178.0.1
    up echo nameserver 192.178.122.1 > /etc/resolv.conf
```

![image](https://user-images.githubusercontent.com/16128257/143222696-d891e9dc-58bf-47c5-bbed-f2f39fe0eda0.png)

### CALMBELT(1000Host)

```
auto eth0
iface eth0 inet static
    address 192.178.0.2
    netmask 255.255.248.0
    gateway 192.178.0.1
    up echo nameserver 192.178.122.1 > /etc/resolv.conf
```

![image](https://user-images.githubusercontent.com/16128257/143222903-89588af3-0c35-4b4c-9485-cd3dcdb7d09c.png)

### GUANHAO

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

### JABRA(520Host)

```
auto eth0
iface eth0 inet static
    address 192.178.16.2
    netmask 255.255.252.0
    gateway 192.178.16.1
    up echo nameserver 192.178.122.1 > /etc/resolv.conf
```

![image](https://user-images.githubusercontent.com/16128257/143223399-e782d288-7e78-4f4b-9b0d-02fa3125f00d.png)

### MAINGATE(500Host)

```
auto eth0
iface eth0 inet static
    address 192.178.24.3
    netmask 255.255.254.0
    gateway 192.178.24.1
    up echo nameserver 192.178.122.1 > /etc/resolv.conf
```

![image](https://user-images.githubusercontent.com/16128257/143223563-8bcbbd82-ad32-48a5-8d32-504f158ca235.png)

### ALABASTA

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

### JOGRE(12Host)

```
auto eth0
iface eth0 inet static
    address 192.178.27.130
    netmask 255.255.255.240
    gateway 192.178.27.129
    up echo nameserver 192.178.122.1 > /etc/resolv.conf
```

![image](https://user-images.githubusercontent.com/16128257/143223898-fc0fd0a8-c19c-40b5-8eec-88831fada97a.png)
