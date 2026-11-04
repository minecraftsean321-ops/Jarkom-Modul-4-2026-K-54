# Jarkom-Modul-4-2026-K-54
In this project we will make subnetting for the topology that been given, and we will also configure each node in the topology so that it can connect with each other.

| Nama                 | NRP        |
|----------------------|------------|
| Viko Rizky Fauzan    | 5027251017 |
| Sean Arthur Tamajaya | 5027251050 |

## CPT - CIDR

### Topology 

<img width="950" height="auto" alt="image" src="https://github.com/user-attachments/assets/be0eed19-4720-4a23-a8eb-29c4def03d8a" />

## Tabel Penggabungan CIDR

### Cabang kiri

| Blok | Isi (anggota pohon) | Offset | Prefix | Supernet | Rentang awal | Rentang akhir |
|---|---|---|---|---|---|---|
| Schumann - Accela | | 584 | /30 | 192.238.2.72/30 | 192.238.2.72 | 192.238.2.75 |
| Switch 2 | | 576 | /29 | 192.238.2.64/29 | 192.238.2.64 | 192.238.2.71 |
| A1 | Schumann - Accela + Switch 2 | 576 | /28 | 192.238.2.64/28 | 192.238.2.64 | 192.238.2.79 |
| Akashic | | 592 | /29 | 192.238.2.80/29 | 192.238.2.80 | 192.238.2.87 |
| A2 | A1 + Akashic | 576 | /27 | 192.238.2.64/27 | 192.238.2.64 | 192.238.2.95 |
| Juri | | 512 | /26 | 192.238.2.0/26 | 192.238.2.0 | 192.238.2.63 |
| A3 | A2 + Juri | 512 | /25 | 192.238.2.0/25 | 192.238.2.0 | 192.238.2.127 |
| Copland | | 0 | /23 | 192.238.0.0/23 | 192.238.0.0 | 192.238.1.255 |
| B1 | A3 + Copland | 0 | /22 | 192.238.0.0/22 | 192.238.0.0 | 192.238.3.255 |
| Accela | | 1024 | /22 | 192.238.4.0/22 | 192.238.4.0 | 192.238.7.255 |
| B2 | B1 + Accela | 0 | /21 | 192.238.0.0/21 | 192.238.0.0 | 192.238.7.255 |
| Psyche | | 2048 | /22 | 192.238.8.0/22 | 192.238.8.0 | 192.238.11.255 |
| **Cabang kiri** | **B2 + Psyche** | **0** | **/20** | **192.238.0.0/20** | **192.238.0.0** | **192.238.15.255** |

### Cabang bawah

| Blok | Isi (anggota pohon) | Offset | Prefix | Supernet | Rentang awal | Rentang akhir |
|---|---|---|---|---|---|---|
| Phantoma - Shibuya | | 0 | /30 | 192.238.16.0/30 | 192.238.16.0 | 192.238.16.3 |
| Knights - Phantoma | | 4 | /30 | 192.238.16.4/30 | 192.238.16.4 | 192.238.16.7 |
| Protocol7 - Knights | | 8 | /30 | 192.238.16.8/30 | 192.238.16.8 | 192.238.16.11 |
| Deus - Protocol7 | | 12 | /30 | 192.238.16.12/30 | 192.238.16.12 | 192.238.16.15 |
| Tachibana - Deus | | 16 | /30 | 192.238.16.16/30 | 192.238.16.16 | 192.238.16.19 |
| Wired - Tachibana | | 20 | /30 | 192.238.16.20/30 | 192.238.16.20 | 192.238.16.23 |
| P2P bawah | Enam link /30 di atas | 0 | /27 | 192.238.16.0/27 | 192.238.16.0 | 192.238.16.31 |
| Knights | | 32 | /29 | 192.238.16.32/29 | 192.238.16.32 | 192.238.16.39 |
| D1 | Knights + P2P bawah | 0 | /26 | 192.238.16.0/26 | 192.238.16.0 | 192.238.16.63 |
| Phantoma | | 64 | /27 | 192.238.16.64/27 | 192.238.16.64 | 192.238.16.95 |
| D2 | D1 + Phantoma | 0 | /25 | 192.238.16.0/25 | 192.238.16.0 | 192.238.16.127 |
| Shibuya | | 128 | /26 | 192.238.16.128/26 | 192.238.16.128 | 192.238.16.191 |
| D3 | D2 + Shibuya | 0 | /24 | 192.238.16.0/24 | 192.238.16.0 | 192.238.16.255 |
| Protocol7 | | 256 | /26 | 192.238.17.0/26 | 192.238.17.0 | 192.238.17.63 |
| E1 | D3 + Protocol7 | 0 | /23 | 192.238.16.0/23 | 192.238.16.0 | 192.238.17.255 |
| Deus | | 512 | /25 | 192.238.18.0/25 | 192.238.18.0 | 192.238.18.127 |
| E2 | E1 + Deus | 0 | /22 | 192.238.16.0/22 | 192.238.16.0 | 192.238.19.255 |
| Tachibana | | 1024 | /23 | 192.238.20.0/23 | 192.238.20.0 | 192.238.21.255 |
| **Cabang bawah** | **E2 + Tachibana** | **0** | **/21** | **192.238.16.0/21** | **192.238.16.0** | **192.238.23.255** |

### Navi (Cabang kanan)

| Blok | Isi (anggota pohon) | Offset | Prefix | Supernet | Rentang awal | Rentang akhir |
|---|---|---|---|---|---|---|
| Wired - Navi | | 320 | /30 | 192.238.25.64/30 | 192.238.25.64 | 192.238.25.67 |
| Switch 7 | | 256 | /26 | 192.238.25.0/26 | 192.238.25.0 | 192.238.25.63 |
| C1 | Wired - Navi + Switch 7 | 256 | /25 | 192.238.25.0/25 | 192.238.25.0 | 192.238.25.127 |
| Switch 8 | | 0 | /24 | 192.238.24.0/24 | 192.238.24.0 | 192.238.24.255 |
| C2 | C1 + Switch 8 | 0 | /23 | 192.238.24.0/23 | 192.238.24.0 | 192.238.25.255 |
| Switch 6 | | 512 | /24 | 192.238.26.0/24 | 192.238.26.0 | 192.238.26.255 |
| **Navi (Cabang kanan)** | **C2 + Switch 6** | **0** | **/22** | **192.238.24.0/22** | **192.238.24.0** | **192.238.27.255** |

### Cabang atas

| Blok | Isi (anggota pohon) | Offset | Prefix | Supernet | Rentang awal | Rentang akhir |
|---|---|---|---|---|---|---|
| Cyberia - Wired | | 128 | /30 | 192.238.28.128/30 | 192.238.28.128 | 192.238.28.131 |
| Cyberia | | 0 | /25 | 192.238.28.0/25 | 192.238.28.0 | 192.238.28.127 |
| **Cabang atas** | **Cyberia + Cyberia - Wired** | **0** | **/24** | **192.238.28.0/24** | **192.238.28.0** | **192.238.28.255** |

### Hasil akhir (tabel CIDR)

| Subnet | Prefix | Ukuran blok | Offset | Network | Mask | Range host | Gateway | Broadcast |
|---|---|---|---|---|---|---|---|---|
| Cabang kiri | /20 | 4096 | 0 | 192.238.0.0 | 255.255.240.0 | 192.238.0.1 - 192.238.15.254 | 192.238.0.1 | 192.238.15.255 |
| Cabang bawah | /21 | 2048 | 4096 | 192.238.16.0 | 255.255.248.0 | 192.238.16.1 - 192.238.23.254 | 192.238.16.1 | 192.238.23.255 |
| Navi (Cabang kanan) | /22 | 1024 | 6144 | 192.238.24.0 | 255.255.252.0 | 192.238.24.1 - 192.238.27.254 | 192.238.24.1 | 192.238.27.255 |
| Cabang atas | /24 | 256 | 7168 | 192.238.28.0 | 255.255.255.0 | 192.238.28.1 - 192.238.28.254 | 192.238.28.1 | 192.238.28.255 |
| Seluruh jaringan | /19 | 8192 | 0 | 192.238.0.0 | 255.255.224.0 | 192.238.0.1 - 192.238.31.254 | 192.238.0.1 | 192.238.31.255 |

## Scripth Konfigurasi Setiap Node

### ROUTER Cyberia
```
enable
configure terminal
hostname Cyberia
no ip domain-lookup
!
interface FastEthernet0/0
 description Ke Cloud0 (NAT, outside)
 ip address dhcp
 ip nat outside
 no shutdown
!
interface FastEthernet0/1
 description LAN Switch1 (JJ, MyuMyu)
 ip address 192.238.28.1 255.255.255.128
 ip nat inside
 no shutdown
!
interface FastEthernet1/0
 description Link ke Wired
 ip address 192.238.28.129 255.255.255.252
 ip nat inside
 no shutdown
!
access-list 1 permit 192.238.0.0 0.0.31.255
ip nat inside source list 1 interface FastEthernet0/0 overload
!
ip route 192.238.0.0 255.255.224.0 192.238.28.130
!
end
write memory
```

### ROUTER Wired
```
enable
configure terminal
hostname Wired
no ip domain-lookup
!
interface FastEthernet0/0
 description Link ke Cyberia
 ip address 192.238.28.130 255.255.255.252
 no shutdown
!
interface FastEthernet0/1
 description Link ke Navi
 ip address 192.238.25.65 255.255.255.252
 no shutdown
!
interface FastEthernet1/0
 description Segmen Switch2 (Psyche, Copland, Schumann)
 ip address 192.238.2.65 255.255.255.248
 no shutdown
!
interface FastEthernet1/1
 description Link ke Tachibana
 ip address 192.238.16.21 255.255.255.252
 no shutdown
!
ip route 0.0.0.0 0.0.0.0 192.238.28.129
ip route 192.238.16.0 255.255.248.0 192.238.16.22
ip route 192.238.24.0 255.255.252.0 192.238.25.66
ip route 192.238.0.0 255.255.252.0 192.238.2.67
ip route 192.238.2.64 255.255.255.224 192.238.2.68
ip route 192.238.4.0 255.255.252.0 192.238.2.68
ip route 192.238.8.0 255.255.252.0 192.238.2.66
!
end
write memory
```

### ROUTER Navi
```
enable
configure terminal
hostname Navi
no ip domain-lookup
!
interface FastEthernet0/0
 description Link ke Wired
 ip address 192.238.25.66 255.255.255.252
 no shutdown
!
interface FastEthernet0/1
 description LAN Switch6 (Alice, Reika)
 ip address 192.238.26.1 255.255.255.0
 no shutdown
!
interface FastEthernet1/0
 description LAN Switch7 (Taro)
 ip address 192.238.25.1 255.255.255.192
 no shutdown
!
interface FastEthernet1/1
 description LAN Switch8 (Yasuo, Miho, Kuma)
 ip address 192.238.24.1 255.255.255.0
 no shutdown
!
ip route 0.0.0.0 0.0.0.0 192.238.25.65
!
end
write memory
```

### ROUTER Psyche
```
enable
configure terminal
hostname Psyche
no ip domain-lookup
!
interface FastEthernet0/0
 description Segmen Switch2
 ip address 192.238.2.66 255.255.255.248
 no shutdown
!
interface FastEthernet0/1
 description LAN Switch3 (Karl, Lin)
 ip address 192.238.8.1 255.255.252.0
 no shutdown
!
ip route 0.0.0.0 0.0.0.0 192.238.2.65
!
end
write memory
```

### ROUTER Copland
```
enable
configure terminal
hostname Copland
no ip domain-lookup
!
interface FastEthernet0/0
 description Segmen Switch2
 ip address 192.238.2.67 255.255.255.248
 no shutdown
!
interface FastEthernet0/1
 description LAN Juri (langsung)
 ip address 192.238.2.1 255.255.255.192
 no shutdown
!
interface FastEthernet1/0
 description LAN Switch4 (Masayuki)
 ip address 192.238.0.1 255.255.254.0
 no shutdown
!
ip route 0.0.0.0 0.0.0.0 192.238.2.65
!
end
write memory
```

### ROUTER Schumann
```
enable
configure terminal
hostname Schumann
no ip domain-lookup
!
interface FastEthernet0/0
 description Segmen Switch2
 ip address 192.238.2.68 255.255.255.248
 no shutdown
!
interface FastEthernet0/1
 description LAN Akashic (langsung)
 ip address 192.238.2.81 255.255.255.248
 no shutdown
!
interface FastEthernet1/0
 description Link ke Accela
 ip address 192.238.2.73 255.255.255.252
 no shutdown
!
ip route 0.0.0.0 0.0.0.0 192.238.2.65
ip route 192.238.4.0 255.255.252.0 192.238.2.74
!
end
write memory
```

### ROUTER Accela
```
enable
configure terminal
hostname Accela
no ip domain-lookup
!
interface FastEthernet0/0
 description Link ke Schumann
 ip address 192.238.2.74 255.255.255.252
 no shutdown
!
interface FastEthernet0/1
 description LAN Switch5 (Omnipresence, Denpa)
 ip address 192.238.4.1 255.255.252.0
 no shutdown
!
ip route 0.0.0.0 0.0.0.0 192.238.2.73
!
end
write memory
```

### ROUTER Tachibana
```
enable
configure terminal
hostname Tachibana
no ip domain-lookup
!
interface FastEthernet0/0
 description Link ke Wired
 ip address 192.238.16.22 255.255.255.252
 no shutdown
!
interface FastEthernet0/1
 description LAN Switch9 (Collective, Ghost)
 ip address 192.238.20.1 255.255.254.0
 no shutdown
!
interface FastEthernet1/0
 description Link ke Deus
 ip address 192.238.16.17 255.255.255.252
 no shutdown
!
ip route 0.0.0.0 0.0.0.0 192.238.16.21
ip route 192.238.16.0 255.255.252.0 192.238.16.18
!
end
write memory
```

### ROUTER Deus
```
enable
configure terminal
hostname Deus
no ip domain-lookup
!
interface FastEthernet0/0
 description LAN Switch10 (Lilith, Specter)
 ip address 192.238.18.1 255.255.255.128
 no shutdown
!
interface FastEthernet0/1
 description Link ke Tachibana
 ip address 192.238.16.18 255.255.255.252
 no shutdown
!
interface FastEthernet1/0
 description Link ke Protocol7
 ip address 192.238.16.13 255.255.255.252
 no shutdown
!
ip route 0.0.0.0 0.0.0.0 192.238.16.17
ip route 192.238.16.0 255.255.254.0 192.238.16.14
ip route 192.238.16.20 255.255.255.252 192.238.16.17
!
end
write memory
```

### ROUTER Protocol7
```
enable
configure terminal
hostname Protocol7
no ip domain-lookup
!
interface FastEthernet0/0
 description Link ke Deus
 ip address 192.238.16.14 255.255.255.252
 no shutdown
!
interface FastEthernet0/1
 description LAN Switch11 (Chisa, Hodgeson)
 ip address 192.238.17.1 255.255.255.192
 no shutdown
!
interface FastEthernet1/0
 description Link ke Knights
 ip address 192.238.16.9 255.255.255.252
 no shutdown
!
ip route 0.0.0.0 0.0.0.0 192.238.16.13
ip route 192.238.16.0 255.255.255.0 192.238.16.10
ip route 192.238.16.16 255.255.255.248 192.238.16.13
!
end
write memory
```

### ROUTER Knights
```
enable
configure terminal
hostname Knights
no ip domain-lookup
!
interface FastEthernet0/0
 description Link ke Protocol7
 ip address 192.238.16.10 255.255.255.252
 no shutdown
!
interface FastEthernet0/1
 description LAN Eiri (langsung)
 ip address 192.238.16.33 255.255.255.248
 no shutdown
!
interface FastEthernet1/0
 description Link ke Phantoma
 ip address 192.238.16.5 255.255.255.252
 no shutdown
!
ip route 0.0.0.0 0.0.0.0 192.238.16.9
ip route 192.238.16.0 255.255.255.252 192.238.16.6
ip route 192.238.16.64 255.255.255.224 192.238.16.6
ip route 192.238.16.128 255.255.255.192 192.238.16.6
!
end
write memory
```

### ROUTER Phantoma
```
enable
configure terminal
hostname Phantoma
no ip domain-lookup
!
interface FastEthernet0/0
 description Link ke Knights
 ip address 192.238.16.6 255.255.255.252
 no shutdown
!
interface FastEthernet0/1
 description Link ke Shibuya
 ip address 192.238.16.1 255.255.255.252
 no shutdown
!
interface FastEthernet1/0
 description LAN Switch12 (Semi)
 ip address 192.238.16.65 255.255.255.224
 no shutdown
!
ip route 0.0.0.0 0.0.0.0 192.238.16.5
ip route 192.238.16.128 255.255.255.192 192.238.16.2
!
end
write memory
```

### ROUTER Shibuya

```
enable
configure terminal
hostname Shibuya
no ip domain-lookup
!
interface FastEthernet0/0
 description Link ke Phantoma
 ip address 192.238.16.2 255.255.255.252
 no shutdown
!
interface FastEthernet0/1
 description LAN Switch13 (Lain, Mika)
 ip address 192.238.16.129 255.255.255.192
 no shutdown
!
ip route 0.0.0.0 0.0.0.0 192.238.16.1
!
end
write memory
```

## Tahap Pengujian 

### Cek tiap router 

```
show ip interface brief
show ip route
```

- Wired
<img width="912" height="161" alt="image" src="https://github.com/user-attachments/assets/8607faa7-1c82-4259-8f97-aef4ca20e131" />  
<img width="923" height="296" alt="image" src="https://github.com/user-attachments/assets/d6463bef-35b4-4eaf-b2be-a56505b94236" />

- Pysche
<img width="909" height="99" alt="image" src="https://github.com/user-attachments/assets/afabedfb-be0a-47a5-a739-397073d1cbdd" />  
<img width="911" height="136" alt="image" src="https://github.com/user-attachments/assets/60e495c6-1e79-4442-9e41-e5fa6af58bb7" />

- Navi
<img width="913" height="141" alt="image" src="https://github.com/user-attachments/assets/46fb274c-48f4-4e95-8171-f22f6fc0b1a8" />  
<img width="911" height="174" alt="image" src="https://github.com/user-attachments/assets/6b52cad0-b529-44c1-885a-b2a7ab220099" />

- Tachibana
<img width="916" height="137" alt="image" src="https://github.com/user-attachments/assets/c9a7e668-dcad-4dae-816b-63f1b2fe94f8" />  
<img width="907" height="168" alt="image" src="https://github.com/user-attachments/assets/8e509529-f066-4f7f-b67e-92037dad5aa8" />


