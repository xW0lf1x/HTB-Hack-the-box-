# Linux Labs

Máquinas y prácticas de ciberseguridad en sistemas Linux.

- MEOW:
1. Reconocimiento

nmap -sC -sV TARGET_IP
Servicio detectado:
23/tcp — Telnet

2. Enumeración del servicio

telnet TARGET_IP
Servicio Telnet accesible desde la máquina objetivo.

3. Acceso al sistema

Credenciales utilizadas:
Usuario: root
Contraseña: vacía
Acceso obtenido con privilegios de administrador.

5. Exploración

Comandos utilizados:

whoami
hostname
id
pwd
ls -la
cat /etc/os-release

Información identificada:

Usuario actual: root.
Directorio: /root.
Sistema operativo: Ubuntu 20.04.2.
Archivo flag.txt (no publicada).

5. Hallazgos

Servicio Telnet expuesto.
Acceso remoto como root sin contraseña.
Ausencia de autenticación segura.
Posibilidad de obtener control total del sistema.

6. Mitigaciones

Deshabilitar Telnet y utilizar SSH.
Exigir contraseñas robustas y autenticación segura.
Evitar accesos remotos directos como root.
Restringir el acceso a servicios administrativos.

- FAWN:

1. Reconocimiento

nmap -sC -sV TARGET_IP
Servicio detectado:
21/tcp — FTP (vsftpd 3.0.3).
Resultado relevante:
Acceso FTP anónimo permitido.
Archivo flag.txt visible en el servidor.

2. Enumeración FTP

ftp TARGET_IP
Credenciales utilizadas:
Usuario: anonymous
Contraseña: vacía.
Acceso al servicio FTP sin credenciales personales.

4. Exploración del servidor

Comandos FTP
ls
Archivos identificados:
flag.txt (32 bytes).
4. Descarga del archivo

get flag.txt
Salir del servicio FTP:
exit
Consultar el archivo descargado:
cat flag.txt

5. Hallazgos

Servicio FTP accesible.
Inicio de sesión anónimo permitido.
Archivos accesibles sin autenticación personal.
Posible exposición de información.

6. Mitigaciones

Deshabilitar el acceso FTP anónimo.
Exigir autenticación para acceder a los archivos.
Restringir permisos de lectura y descarga.
Evitar almacenar información sensible en directorios públicos.
Utilizar SFTP o FTPS para transferencias seguras.
