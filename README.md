# Musiclib
Aplikasi bank lirik lagu berbasis laravel yang menggunakan RDBMS MySQL Cluster sebagai database utama dan Redis Cluster sebagai data cache.

## Arsitektur
### 1. MySQL Cluster
Cluster yang akan digunakan pada kali ini ada 7 buah server dengan spesifikasi seperti berikut

id | Hostname | IP Adrress | Deskripsi
--- | --- | --- | ---
1 | manager | 192.168.100.100 | Sebagai cluster manager
2 | data1 | 192.168.100.2 | Sebagai data node
3 | data1 | 192.168.100.3 | Sebagai data node
4 | data1 | 192.168.100.4 | Sebagai data node
11 | service1 | 192.168.100.11 | Sebagai service node (API)
12 | service1 | 192.168.100.12 | Sebagai service node (API)
|-| proxy | 192.168.100.21 | Sebagai proxySQL (Load Balancer)

### 2. Redis Cluster
Redis cluster akan menggunakan 3 node, 1 node master dan 2 node slave. Spesifikasinya adalah sebagai berikut :   

| No | Hostname | IP Address | Peran |
| --- | --- | --- | --- |
| 1 | rmaster | 192.168.200.100 | master |
| 2 | rslave1 | 192.168.200.101 | slave |
| 3 | rslave2 | 192.168.200.102 | slave |   

## Instalasi Basis Data
Semua tahapan instalasi basis data baik MySQL Cluster dan Redis Cluster sudah dilakukan dan terdokumentasi pada :
1. [Dokumentasi Implementasi MySQL Cluster](https://github.com/tamtama17/Implementasi-MySQL-Cluster)   
2. [Dokumentasi Implementasi Redis](https://github.com/tamtama17/Impelemtasi-Redis)   

## Konfigurasi
## Penjelasan Aplikasi
## Tes Failover