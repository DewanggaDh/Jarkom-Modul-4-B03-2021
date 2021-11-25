# Jarkom-Modul-4-B03-2021

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

