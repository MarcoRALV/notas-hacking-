#### Description

Use `srch_strings` from the sleuthkit and some terminal-fu to find a flag in this disk image: [dds1-alpine.flag.img.gz](https://mercury.picoctf.net/static/4f3df7052b4121aff89af1a3f517afb1/dds1-alpine.flag.img.gz)


marcorojas@MarcoRojas:~$ wget https://mercury.picoctf.net/static/4f3df7052b4121aff89af1a3f517afb1/dds1-alpine.flag.img.gz
--2025-05-06 16:35:34--  https://mercury.picoctf.net/static/4f3df7052b4121aff89af1a3f517afb1/dds1-alpine.flag.img.gz
Resolving mercury.picoctf.net (mercury.picoctf.net)... 18.189.209.142
Connecting to mercury.picoctf.net (mercury.picoctf.net)|18.189.209.142|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 29768910 (28M) [application/octet-stream]
Saving to: ‘dds1-alpine.flag.img.gz’

dds1-alpine.flag.img.gz       100%[=================================================>]  28.39M  8.94MB/s    in 3.2s

2025-05-06 16:35:37 (8.94 MB/s) - ‘dds1-alpine.flag.img.gz’ saved [29768910/29768910]

marcorojas@MarcoRojas:~$ fls -o 2048 dds1-alpine.flag.img
Error stat(ing) image file (raw_open: image "dds1-alpine.flag.img" - No such file or directory)
marcorojas@MarcoRojas:~$ file dds1-alpine.flag.img  # Verificar tipo de archivo
dds1-alpine.flag.img: cannot open `dds1-alpine.flag.img' (No such file or directory)
marcorojas@MarcoRojas:~$ gunzip dds1-alpine.flag.img.gz
marcorojas@MarcoRojas:~$ file dds1-alpine.flag.img  # Verificar tipo de archivo
dds1-alpine.flag.img: DOS/MBR boot sector; partition 1 : ID=0x83, active, start-CHS (0x0,32,33), end-CHS (0x10,81,1), startsector 2048, 260096 sectors
marcorojas@MarcoRojas:~$ mmls dds1-alpine.flag.img  # Mostrar layout del disco
DOS Partition Table
Offset Sector: 0
Units are in 512-byte sectors

      Slot      Start        End          Length       Description
000:  Meta      0000000000   0000000000   0000000001   Primary Table (#0)
001:  -------   0000000000   0000002047   0000002048   Unallocated
002:  000:000   0000002048   0000262143   0000260096   Linux (0x83)
marcorojas@MarcoRojas:~$ fls -o [offset] dds1-alpine.flag.img  # Listar archivos
set se obtiene del comando mmls (generalmente 2048)Invalid image offset (tsk_parse: invalid image offset: [offset])
marcorojas@MarcoRojas:~$ # El offset se obtiene del comando mmls (generalmente 2048)
marcorojas@MarcoRojas:~$ strings dds1-alpine.flag.img | grep -i picoCTF



  SAY picoCTF{f0r3ns1c4t0r_n30phyt3_a011c142}
