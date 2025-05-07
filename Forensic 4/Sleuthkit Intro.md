#### Description

Download the disk image and use `mmls` on it to find the size of the Linux partition. Connect to the remote checker service to check your answer and get the flag.Note: if you are using the webshell, download and extract the disk image into `/tmp` not your home directory.[Download disk image](https://artifacts.picoctf.net/c/164/disk.img.gz)

Additional details will be available after launching your challenge instance.


Detalles: ## Paso 1: Descargar el archivo

bash

Copy

Download

wget https://mercury.picoctf.net/static/bc72945175d643626f6ca5c3410f4c23/disk.img.gz
gunzip disk.img.gz

## Paso 2: Analizar la estructura del disco

bash

Copy

Download

mmls disk.img

**Salida esperada** (los valores pueden variar):

Copy

Download

DOS Partition Table
Offset Sector: 0
Units are in 512-byte sectors

     Slot    Start        End          Length       Description
000:  Meta    0000000000   0000000000   0000000001   Primary Table
001:  ------- 0000000000   0000002047   0000002048   Unallocated
002:  000:000 0000002048   0000204799   0000202752   Linux (0x83)

## Paso 3: Examinar el sistema de archivos (usar el offset de Start)

bash

Copy

Download

fls -o 2048 disk.img  # Usa el valor de Start de tu partición Linux (0x83)

## Paso 4: Buscar archivos clave

Busca estos archivos comunes:

bash

Copy

Download

fls -o 2048 disk.img | grep -i -E 'flag|secret|root|txt'

## Paso 5: Extraer la flag

Cuando encuentres el archivo (ej. inode 64 para `/root/my-cool-flag.png`):

bash

Copy

Download

icat -o 2048 disk.img 64 > flag.png
xdg-open flag.png  # Ver la imagen con la flag 




picoCTF{mm15_f7w!}


ayudado por https://chat.deepseek.com/a/chat/s/d3aed4cd-5fee-4eca-80e9-e10c57e1bd3a 