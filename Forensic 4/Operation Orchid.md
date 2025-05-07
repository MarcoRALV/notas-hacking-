#### Description

Download this disk image and find the flag.Note: if you are using the webshell, download and extract the disk image into `/tmp` not your home directory.

- [Download compressed disk image](https://artifacts.picoctf.net/c/212/disk.flag.img.gz)
Detalles: marcorojas@MarcoRojas:~$ wget https://artifacts.picoctf.net/c/212/disk.flag.img.gz
--2025-05-07 13:06:38--  https://artifacts.picoctf.net/c/212/disk.flag.img.gz
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.161.55.26, 3.161.55.100, 3.161.55.64, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.161.55.26|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 44360923 (42M) [application/octet-stream]
Saving to: ‘disk.flag.img.gz’

disk.flag.img.gz                   100%[================================================================>]  42.31M  12.0MB/s    in 4.2s

2025-05-07 13:06:44 (9.98 MB/s) - ‘disk.flag.img.gz’ saved [44360923/44360923]

marcorojas@MarcoRojas:~$ ls -lah disk.flag.img.gz
-rw-r--r-- 1 marcorojas marcorojas 43M Mar 15  2023 disk.flag.img.gz
marcorojas@MarcoRojas:~$ gzip -d disk.flag.img.gz
gzip: disk.flag.img already exists; do you wish to overwrite (y or n)? y
marcorojas@MarcoRojas:~$ ls -lah disk.flag.img
-rw-r--r-- 1 marcorojas marcorojas 400M Mar 15  2023 disk.flag.img
marcorojas@MarcoRojas:~$ mmls disk.flag.img
DOS Partition Table
Offset Sector: 0
Units are in 512-byte sectors

      Slot      Start        End          Length       Description
000:  Meta      0000000000   0000000000   0000000001   Primary Table (#0)
001:  -------   0000000000   0000002047   0000002048   Unallocated
002:  000:000   0000002048   0000206847   0000204800   Linux (0x83)
003:  000:001   0000206848   0000411647   0000204800   Linux Swap / Solaris x86 (0x82)
004:  000:002   0000411648   0000819199   0000407552   Linux (0x83)
marcorojas@MarcoRojas:~$ fls disk.flag.img -o 411648
d/d 11: lost+found
d/d 12: boot
d/d 13: etc
d/d 81: proc
d/d 82: dev
d/d 83: tmp
d/d 84: lib
d/d 87: var
d/d 96: usr
d/d 106:        bin
d/d 120:        sbin
d/d 460:        home
d/d 466:        media
d/d 470:        mnt
d/d 471:        opt
d/d 472:        root
d/d 473:        run
d/d 475:        srv
d/d 476:        sys
d/d 2041:       swap
V/V 51001:      $OrphanFiles
marcorojas@MarcoRojas:~$ fls disk.flag.img -o 411648 472
r/r 1875:       .ash_history
r/r * 1876(realloc):    flag.txt
r/r 1782:       flag.txt.enc
marcorojas@MarcoRojas:~$ icat disk.flag.img -o 411648 472
�
 .
  ..S$
      .ash_historyflag.txt��
                            flag.txt.enc
                                        �,洞marcorojas@MarcoRojas:~$ icat disk.flag.img -o 411648 472 > flag.txt.enc
marcorojas@MarcoRojas:~$ file flag.txt.enc
flag.txt.enc: data
marcorojas@MarcoRojas:~$ icat disk.flag.img -o 411648 1875
touch flag.txt
nano flag.txt
apk get nano
apk --help
apk add nano
nano flag.txt
openssl
openssl aes256 -salt -in flag.txt -out flag.txt.enc -k unbreakablepassword1234567
shred -u flag.txt
ls -al
halt
marcorojas@MarcoRojas:~$ openssl aes256 -salt -d -in flag.txt.enc -out flag.txt -k unbreakablepassword1234567
bad magic number
marcorojas@MarcoRojas:~$ ls
'Forensics is fun.pptm'     buildings.png    cookies                   disk.flag.img        flag.txt           hash           retos
'Forensics is fun.pptm.1'   capture.pcap     dds1-alpine.flag.img      disk.flag.img.gz.1   flag.txt.enc       heapdump       server.py
'Forensics is fun.pptm.2'   capture.pcap.1   dds1-alpine.flag.img.gz   disk.flag.img.gz.2   fundamentosciber   picopico.key   shell.php
marcorojas@MarcoRojas:~$ cat flag.txt
marcorojas@MarcoRojas:~$ cat flag.txt.enc
�
 .
  ..S$
      .ash_historyflag.txt��
                            flag.txt.enc
                                        �,洞marcorojas@MarcoRojas:~$ openssl aes256 -salt -d -in flag.txt.enc -out flag.txt -k unbreakablepassword1234567
marcorojas@MarcoRojas:~$ cat flag.txt.enc
�
 .
  ..S$
      .ash_historyflag.txt��
                            flag.txt.enc
                                        �,洞marcorojas@MarcoRojas:~$ cat flag.txt
marcorojas@MarcoRojas:~$ openssl aes256 -salt -d -in flag.txt.enc -out flag.txt -k unbreakablepassword1234567
bad magic number
marcorojas@MarcoRojas:~$ cat flag.txt
marcorojas@MarcoRojas:~$ icat disk.flag.img -o 411648 1875
touch flag.txt
nano flag.txt
apk get nano
apk --help
apk add nano
nano flag.txt
openssl
openssl aes256 -salt -in flag.txt -out flag.txt.enc -k unbreakablepassword1234567
shred -u flag.txt
ls -al
halt
marcorojas@MarcoRojas:~$ icat disk.flag.img -o 411648 1782
Salted__0��!�-6V����0�U��l��&�:�pj_1�0�|�h
                         icat disk.flag.img -o 411648 1875  t disk.flag.img -o 411648 1875
touch flag.txt
nano flag.txt
apk get nano
apk --help
apk add nano
nano flag.txt
openssl
openssl aes256 -salt -in flag.txt -out flag.txt.enc -k unbreakablepassword1234567
shred -u flag.txt
ls -al
halt
marcorojas@MarcoRojas:~$ openssl aes256 -salt -d -in flag.txt.enc -out flag.txt -k unbreakablepassword1234567
bad magic number
marcorojas@MarcoRojas:~$ cat flag.txt.enc
�
 .
  ..S$
      .ash_historyflag.txt��
                            flag.txt.enc
                                        �,洞marcorojas@MarcoRojas:~$ openssl aes256 -salt -d -in flag.txt.enc -out flag.txt -k unbreakablepassword1234567
marcorojas@MarcoRojas:~$ icat disk.flag.img -o 411648 1875
touch flag.txt
nano flag.txt
apk get nano
apk --help
apk add nano
nano flag.txt
openssl
openssl aes256 -salt -in flag.txt -out flag.txt.enc -k unbreakablepassword1234567
shred -u flag.txt
ls -al
halt
marcorojas@MarcoRojas:~$ icat disk.flag.img -o 411648 1782
Salted__0��!�-6V����0�U��l��&�:�pj_1�0�|�h
                         openssl aes256 -salt -d -in flag.txt.enc -out flag.txt -k unbreakablepassword1234567
bad magic number
marcorojas@MarcoRojas:~$ cat flag.txt
marcorojas@MarcoRojas:~$ cat flag.txt.enc
�
 .
  ..S$
      .ash_historyflag.txt��
                            flag.txt.enc
                                        �,洞marcorojas@MarcoRojas:~$ openssl aes256 -salt -d -in flag.txt.enc -out flag.txt -k unbreakablepassword1234567
marcorojas@MarcoRojas:~$ icat disk.flag.img -o 411648 1782  > flag2.txt.enc
marcorojas@MarcoRojas:~$ openssl aes256 -salt -d -in flag2.txt.enc -out flag.txt -k unbreakablepassword1234567
*** WARNING : deprecated key derivation used.
Using -iter or -pbkdf2 would be better.
bad decrypt
140039219615040:error:06065064:digital envelope routines:EVP_DecryptFinal_ex:bad decrypt:../crypto/evp/evp_enc.c:610:
marcorojas@MarcoRojas:~$ cat flag.txt
picoCTF{h4un71ng_p457_0a710765}marcorojas@MarcoRojas:~$ 