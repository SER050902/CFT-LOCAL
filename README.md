# CFT LOCAL

## Preparación del entorno

1. Instalar VirtualBox y crear dos máquinas virtuales:
   - Ubuntu Server (objetivo)
   - Kali Linux o similar (atacante)

2. Configurar ambas máquinas en red con **Adaptador de solo anfitrión** y asegurarse de que estén en la misma subred (por ejemplo, 192.168.56.0/24).

3. Asegúrar de tener herramientas `nmap`, `hydra`, `docker`, `python3`, y `encfs` instaladas según se necesiten.

---

## Retos incluidos

### Flag 1 - Esteganografía web

Exploración de un servicio HTTP en busca de archivos con contenido oculto.

### Flag 2 - Exposición de servicios Docker

Identificación y explotación de una API expuesta sin autenticación para interactuar con contenedores.

### Flag 3 - Acceso remoto por SSH

Uso de diccionarios para realizar un ataque de fuerza bruta contra el servicio SSH y obtener acceso.

### Flag 4 - Cifrado clásico

Desencriptación de un archivo protegido mediante cifrado César en entorno Linux.

### Flag 5 (Bonus) - Acceso a volúmenes cifrados

Montaje de un sistema de archivos cifrado localmente mediante herramientas estándar para descubrir información adicional.

---
