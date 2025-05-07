#### Descripción

Descargue esta imagen de disco, busque la clave e inicie sesión en la máquina remota.Nota: si está usando el shell web, descargue y extraiga la imagen del disco en un `/tmp`directorio que no sea su directorio de inicio.

Habrá detalles adicionales disponibles después de lanzar su instancia de desafío.

marcorojas@MarcoRojas:~$ wget https://artifacts.picoctf.net/c/71/disk.img.gz
--2025-05-07 13:24:44--  https://artifacts.picoctf.net/c/71/disk.img.gz
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.161.55.61, 3.161.55.100, 3.161.55.26, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.161.55.61|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 48132743 (46M) [application/octet-stream]
Saving to: ‘disk.img.gz’

disk.img.gz                   100%[=================================================>]  45.90M  11.1MB/s    in 5.5s

2025-05-07 13:24:50 (8.38 MB/s) - ‘disk.img.gz’ saved [48132743/48132743]

marcorojas@MarcoRojas:~$ gzip -d disk.img.gz
marcorojas@MarcoRojas:~$ ls -lah disk.img
-rw-r--r-- 1 marcorojas marcorojas 230M Aug  4  2023 disk.img
marcorojas@MarcoRojas:~$ mmls disk.img
DOS Partition Table
Offset Sector: 0
Units are in 512-byte sectors

      Slot      Start        End          Length       Description
000:  Meta      0000000000   0000000000   0000000001   Primary Table (#0)
001:  -------   0000000000   0000002047   0000002048   Unallocated
002:  000:000   0000002048   0000206847   0000204800   Linux (0x83)
003:  000:001   0000206848   0000471039   0000264192   Linux (0x83)
marcorojas@MarcoRojas:~$ fls disk.img -o 206848
d/d 11: lost+found
d/d 12: boot
d/d 13: etc
d/d 79: proc
d/d 80: dev
d/d 81: tmp
d/d 82: lib
d/d 85: var
d/d 94: usr
d/d 104:        bin
d/d 118:        sbin
d/d 458:        home
d/d 464:        media
d/d 468:        mnt
d/d 469:        opt
d/d 470:        root
d/d 471:        run
d/d 473:        srv
d/d 474:        sys
V/V 33049:      $OrphanFiles
marcorojas@MarcoRojas:~$ fls disk.img -o 206848 470
r/r 2344:       .ash_history
d/d 3916:       .ssh
marcorojas@MarcoRojas:~$ fls disk.img -o 206848 3916
r/r 2345:       id_ed25519
r/r 2346:       id_ed25519.pub
marcorojas@MarcoRojas:~$ icat disk.img 206848 2345 > key file
Invalid inode address: file
usage: icat [-hrRsvV] [-f fstype] [-i imgtype] [-b dev_sector_size] [-o imgoffset] image [images] inum[-typ[-id]]
        -h: Do not display holes in sparse files
        -r: Recover deleted file
        -R: Recover deleted file and suppress recovery errors
        -s: Display slack space at end of file
        -i imgtype: The format of the image file (use '-i list' for supported types)
        -b dev_sector_size: The size (in bytes) of the device sectors
        -f fstype: File system type (use '-f list' for supported types)
        -o imgoffset: The offset of the file system in the image (in sectors)
        -v: verbose to stderr
        -V: Print version
marcorojas@MarcoRojas:~$ icat disk.img -o 206848 2345 > key file
Invalid inode address: file
usage: icat [-hrRsvV] [-f fstype] [-i imgtype] [-b dev_sector_size] [-o imgoffset] image [images] inum[-typ[-id]]
        -h: Do not display holes in sparse files
        -r: Recover deleted file
        -R: Recover deleted file and suppress recovery errors
        -s: Display slack space at end of file
        -i imgtype: The format of the image file (use '-i list' for supported types)
        -b dev_sector_size: The size (in bytes) of the device sectors
        -f fstype: File system type (use '-f list' for supported types)
        -o imgoffset: The offset of the file system in the image (in sectors)
        -v: verbose to stderr
        -V: Print version
marcorojas@MarcoRojas:~$ icat disk.img -o 206848 2345 > key_file
marcorojas@MarcoRojas:~$ chmod 600 key_file
marcorojas@MarcoRojas:~$ ssh -i key_file -p 63034 ctf-player@saturn.picoctf.net
The authenticity of host '[saturn.picoctf.net]:63034 ([13.59.203.175]:63034)' can't be established.
ECDSA key fingerprint is SHA256:bAr5vzQiLGB7zQsjXlfTNpzZw4qLsrE39u6WXjqMjWA.
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Warning: Permanently added '[saturn.picoctf.net]:63034,[13.59.203.175]:63034' (ECDSA) to the list of known hosts.
Welcome to Ubuntu 20.04.5 LTS (GNU/Linux 6.5.0-1023-aws x86_64)

 * Documentation:  https://help.ubuntu.com
 * Management:     https://landscape.canonical.com
 * Support:        https://ubuntu.com/advantage

This system has been minimized by removing packages and content that are
not required on a system that users do not log into.

To restore this content, you can run the 'unminimize' command.

The programs included with the Ubuntu system are free software;
the exact distribution terms for each program are described in the
individual files in /usr/share/doc/*/copyright.

Ubuntu comes with ABSOLUTELY NO WARRANTY, to the extent permitted by
applicable law.

ctf-player@challenge:~$ ls
flag.txt
ctf-player@challenge:~$ cat flag.txt
picoCTF{k3y_5l3u7h_af277f77}ctf-player@challenge:~$


picoCTF{k3y_5l3u7h_af277f77} 

