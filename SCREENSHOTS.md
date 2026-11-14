# Daftar Screenshot yang Perlu Ditambahkan

Screenshot adalah bukti bahwa praktik benar-benar dikerjakan. Simpan di folder `screenshots/` pada modul masing-masing dengan nama file di bawah, lalu hapus tanda komentar (`<!--` dan `-->`) pada bagian **Bukti Praktik** di README modul.

Sebelum mengunggah, periksa tiap gambar: **jangan sertakan password, kunci, atau token**. Kaburkan jika terlihat.

## 01-networking
| File | Isi |
|---|---|
| `vlan-brief.png` | `show vlan brief` dan `show interfaces trunk` |
| `ospf-routes.png` | `show ip route` dengan rute OSPF/statis |
| `ipsec-sa.png` | `show crypto isakmp sa` dan `show crypto ipsec sa` |
| `ping-antar-kantor.png` | Ping berhasil lintas kantor lewat tunnel |

## 02-docker
| File | Isi |
|---|---|
| `docker-images-ps.png` | `docker images` dan `docker ps` |
| `docker-curl-custom.png` | Hasil `curl http://localhost:8889` dari image sendiri |
| `docker-compose-up.png` | `docker compose up -d` dan `docker compose ps` |
| `docker-rebuild.png` | Halaman sebelum dan sesudah `--build` |

## 03-windows-server-ad
| File | Isi |
|---|---|
| `ad-dcdiag.png` | Hasil `dcdiag` |
| `ad-ou-users-groups.png` | Struktur OU beserta user dan group |
| `gpo-linked-hr.png` | GPO tertaut di OU HR (Group Policy Management) |
| `gpo-controlpanel-blocked.png` | Pesan Control Panel terblokir di client |
| `gpo-gpresult-client.png` | `gpresult /r` sebagai user HR |
| `dhcp-ipconfig-client.png` | `ipconfig /all` di client (pilih yang tanggal lease-nya wajar) |
| `dhcp-address-leases.png` | Address Leases di server |
| `ad-computer-joined.png` | Komputer client di folder Computers |
| `share-access-denied.png` | Pesan akses ditolak (user HR ke folder IT) |
| `ntfs-effective-access.png` | Tab Effective Access, user HR vs IT di folder yang sama |
