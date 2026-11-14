# Sysadmin Infrastructure Lab

Dokumentasi praktik langsung tiga fondasi infrastruktur: **Networking**, **Docker**, dan **Windows Server & Active Directory**. Semua materi dikerjakan di lab sendiri (VirtualBox dan Cisco Packet Tracer), dengan penjelasan konsep, langkah praktik, dan catatan masalah nyata yang ditemui beserta cara memperbaikinya.

Bagian dari jalur belajar menuju **Cloud Engineer** lewat fondasi System Administrator. Repo pendamping: `ubuntu-server-sysadmin-roadmap` (12 langkah Ubuntu Server, tautkan ke URL GitHub-mu di sini).

## Progress

| # | Modul | Cakupan | Status |
|---|---|---|---|
| 01 | [Networking](01-networking/README.md) | VLAN, Subnetting, Routing (static, OSPF), Site-to-Site VPN (IPsec), Troubleshooting | ✅ |
| 02 | [Docker Basics](02-docker/README.md) | Perintah dasar, Dockerfile, Docker Compose | ✅ |
| 03 | [Windows Server & Active Directory](03-windows-server-ad/README.md) | Instalasi, AD DS, User/Group/GPO, DNS & DHCP, File Sharing & NTFS | ✅ |

## Contoh hal yang dibuktikan di dalamnya

- **Networking:** dua kantor dengan VLAN terpisah per departemen terhubung lewat tunnel IPsec yang berjalan, diverifikasi dengan `show crypto isakmp sa`.
- **Docker:** image Nginx sendiri dari Dockerfile yang dijalankan dan dikelola lewat Compose, termasuk alur edit lalu rebuild.
- **Windows Server & AD:** domain dibangun dari nol, user HR dan IT dibedakan lewat group, GPO hanya berlaku untuk OU HR, client mendapat IP dari DHCP lalu join domain, dan folder departemen saling tertutup lewat NTFS permission. Lab ini juga **diulang dari nol di domain kedua** tanpa melihat panduan untuk memverifikasi pemahaman.
- **Troubleshooting nyata:** record DNS ganda pada Domain Controller dengan dua adapter, *trust relationship failed* setelah *Reset Account*, port bentrok pada Docker, dan folder yang belum di-share.

## Environment

| Komponen | Detail |
|---|---|
| Host | Laptop 16 GB RAM, VirtualBox |
| Networking | Cisco Packet Tracer |
| Docker | Ubuntu Server (VM) dengan Docker Engine dan Compose v2 |
| Windows | Windows Server 2022 Standard Evaluation (Desktop Experience), Windows 11 Enterprise Evaluation sebagai client |

## Struktur repo

```
sysadmin-infrastructure-lab/
├── README.md
├── SCREENSHOTS.md              # daftar screenshot yang perlu ditambahkan
├── 01-networking/
│   ├── README.md
│   ├── cisco-ios-cheatsheet.md
│   └── screenshots/
├── 02-docker/
│   ├── README.md
│   ├── lab/                    # Dockerfile, index.html, docker-compose.yml
│   └── screenshots/
└── 03-windows-server-ad/
    ├── README.md
    └── screenshots/
```

## Batasan (yang belum tercakup)

Supaya jelas tingkat kemampuannya: ini level dasar yang dikerjakan langsung.
- Networking dilakukan di simulator, belum di perangkat fisik atau firewall sungguhan.
- Docker belum mencakup volume, network antar container, dan registry.
- Active Directory baru satu Domain Controller per domain, belum replikasi, backup, atau otomasi PowerShell.

## Catatan keamanan

Tidak ada password, kunci, atau token di repo ini. Password lab tidak didokumentasikan.
