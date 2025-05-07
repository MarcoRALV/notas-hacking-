

#### Description

Download this disk image and find the flag.Note: if you are using the webshell, download and extract the disk image into `/tmp` not your home directory.

- [Download compressed disk image](https://artifacts.picoctf.net/c/137/disk.flag.img.gz)
detalles: 
descargamos el reto 
marcorojas@MarcoRojas:~$ wget https://artifacts.picoctf.net/c/137/disk.flag.img.gz
--2025-05-07 12:57:17--  https://artifacts.picoctf.net/c/137/disk.flag.img.gz
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.161.55.61, 3.161.55.64, 3.161.55.26, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.161.55.61|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 47534568 (45M) [application/octet-stream]
Saving to: ‘disk.flag.img.gz’

disk.flag.img.gz              100%[=================================================>]  45.33M  10.5MB/s    in 4.3s

2025-05-07 12:57:23 (10.4 MB/s) - ‘disk.flag.img.gz’ saved [47534568/47534568]

marcorojas@MarcoRojas:~$ ls -lah disk.flag.img.gz
-rw-r--r-- 1 marcorojas marcorojas 46M Mar 15  2023 disk.flag.img.gz
marcorojas@MarcoRojas:~$ gzip -d disk.flag.img.gz
gzip: disk.flag.img already exists; do you wish to overwrite (y or n)? y
marcorojas@MarcoRojas:~$ ls -lah disk.flag.img
-rw-r--r-- 1 marcorojas marcorojas 300M Mar 15  2023 disk.flag.img
marcorojas@MarcoRojas:~$ mmls disk.flag.img
DOS Partition Table
Offset Sector: 0
Units are in 512-byte sectors

      Slot      Start        End          Length       Description
000:  Meta      0000000000   0000000000   0000000001   Primary Table (#0)
001:  -------   0000000000   0000002047   0000002048   Unallocated
002:  000:000   0000002048   0000206847   0000204800   Linux (0x83)
003:  000:001   0000206848   0000360447   0000153600   Linux Swap / Solaris x86 (0x82)
004:  000:002   0000360448   0000614399   0000253952   Linux (0x83)
marcorojas@MarcoRojas:~$ fls disk.flag.img -o 360448 -r

y pedimos la flag 
marcorojas@MarcoRojas:~$ icat disk.flag.img -o 360448 2371
picoCTF{by73_5urf3r_adac6cb4}
marcorojas@MarcoRojas:~$



picoCTF{by73_5urf3r_adac6cb4}