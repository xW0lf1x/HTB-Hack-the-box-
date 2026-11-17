# Windows Labs

Máquinas y prácticas de ciberseguridad en sistemas Windows.

- Dancing:

1. Reconocimiento
nmap -sC -sV TARGET_IP

2. Enumeración SMB
smbclient -L //TARGET_IP/

3. Acceso al recurso compartido
smbclient //TARGET_IP/WorkShares

4. Exploración
- Amy.J
- James.P
- worknotes.txt
- flag.txt
5. Hallazgos
- Acceso al recurso compartido sin credenciales personales.
- Exposición de documentos.
- Permisos de acceso demasiado amplios.
6. Mitigaciones
- Restringir permisos SMB.
- Exigir autenticación.
- Aplicar mínimo privilegio.

- Explosion: 
