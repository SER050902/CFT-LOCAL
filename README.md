# CFT LOCAL

## Plataforma y Entorno

- Entorno virtualizado con **VirtualBox**
- Red configurada como **Adaptador de solo anfitrión**
- Máquina objetivo: **Ubuntu Server**

## Descripción de las pruebas

### Flag 1 - Imagen con información oculta

Se detecta un servicio HTTP en el puerto 8080. Navegando a la dirección indicada se encuentra una imagen (.jpeg) con datos ocultos. Se utiliza el comando `strings` para extraer la primera flag.

### Flag 2 - Acceso a contenedor Docker

A través del puerto 2375 (API de Docker sin autenticación), se conecta remotamente al daemon de Docker. Se accede a un contenedor Debian, donde se encuentra un archivo `flag.txt` con la segunda flag.

### Flag 3 - Acceso SSH

Dentro del contenedor Docker hay diccionarios de usuarios y contraseñas. Se utilizan junto con Hydra para realizar un ataque de fuerza bruta al servicio SSH. Tras obtener las credenciales válidas, se accede y se encuentra la tercera flag.

### Flag 4 - Encriptación César

Se accede a un archivo cifrado llamado `iodj.txt`, el cual está encriptado con un cifrado César (+3). Se descarga un script Python desde el servidor web y se modifica para usar desplazamiento -3, recuperando así la cuarta flag.

### Flag 5 (bonus) - Directorio cifrado con EncFS

Se encuentra un directorio llamado `secreto` cifrado con EncFS. Usando un archivo XML dentro del propio directorio cifrado como pista, se obtiene la contraseña de montaje. Dentro se encuentra un archivo `url.txt` con la quinta flag.
