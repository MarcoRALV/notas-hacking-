
#### Description

[🥛](http://mercury.picoctf.net:48380/)


Detelles: ### Paso 1: Inspeccionar el código fuente

1. Haz clic derecho → "Ver código fuente"
    
2. Busca archivos JavaScript vinculados (generalmente `script.js` o similar)
    

### Paso 2: Analizar el JavaScript

Busca funciones que manejen los clics:

javascript

Copy

Download

function handleClick(position) {
  // Código que procesa los clics
  if (position === 3) {
    // Aquí podría estar la lógica sensible
  }
}

### Paso 3: Solución común

1. **Método 1**: Haz clic en todas las áreas de la imagen secuencialmente
    
2. **Método 2**: Envía directamente la posición correcta via URL:
    
    Copy
    
    Download
    
    http://saturn.picoctf.net:64710/?pos=3
    

### Paso 4: Usar curl para automatizar

bash

Copy

Download

curl "http://saturn.picoctf.net:64710/?pos=3" | grep -o "picoCTF{.*}"

picoCTF{imag3_m4n1pul4t10n_sl4p5}


ayudado por https://chat.deepseek.com/a/chat/s/d3aed4cd-5fee-4eca-80e9-e10c57e1bd3a 