# Proyectos del CFGS ASIR

Resumen de las **prácticas y proyectos** del Ciclo Superior de *Administración de Sistemas Informáticos en Red* (Liceo La Paz, A Coruña). Todo está montado en **máquinas virtuales** (VMware Workstation) y documentado paso a paso, con capturas y comprobaciones. Los apuntes completos están en mi web: [daniroca5.gamer.gd](https://daniroca5.gamer.gd/).

## 2.º curso

### Sistemas operativos: dominio Active Directory (ASO)

Un proyecto por fases sobre **Windows Server 2025**, con clientes **Windows 11**:

1. **Controlador de dominio**: AD DS, DNS integrado y un bosque nuevo `empresa.local`.
2. **Identidad**: unidades organizativas por sede y departamento, usuarios, grupos, unión de clientes al dominio y **perfiles móviles**. Diagnóstico de **Kerberos y LDAP**.
3. **Gobernanza con GPO**: herencia, **bloqueo de herencia frente a directiva forzada**, filtrado y resolución de incidencias (la impresión bloqueada por *PrintNightmare*).
4. **Acceso a recursos**: permisos de **recurso compartido + NTFS** (la «doble puerta»: gana el más restrictivo, y un *Deny* explícito manda sobre todo).

Además, **administración remota por SSH** y **RSAT** desde el cliente.

<p align="center">
<img src="img/aso-dominio-esquema.png" width="52%" alt="Esquema del dominio empresa.local">
<img src="img/aso-gpo-herencia.png" width="40%" alt="Bloqueo de herencia frente a directiva forzada">
</p>

### Servicios de red: DHCP y DNS (SRI)

- **DHCP en Windows Server y en Ubuntu Server** (`isc-dhcp-server`): ámbitos, exclusiones, **reservas por MAC** y red interna con `netplan`. Se comprueba desde un cliente Windows 7 con `ipconfig /all`.
- **DNS**: zonas de búsqueda **directa e inversa**, registros A, **CNAME** y **MX**, sufijos DNS y reenviadores.

<p align="center">
<img src="img/sri-netplan.png" width="49%" alt="Configuración de red con netplan">
<img src="img/sri-dns-zona.png" width="45%" alt="Zona DNS asir.cam">
</p>

### Aplicaciones web (IAW)

- **Servidor web** (LAMP y XAMPP), **FTP** y **correo**.
- **CMS**: instalación y configuración de **WordPress** y **Joomla**.
- **Seguridad de un blog**:
  - copias de la base de datos y de los ficheros;
  - borrar los ficheros que revelan la versión;
  - `.htaccess` sin listado de carpetas;
  - límite de intentos de acceso;
  - sacar `wp-config.php` de la raíz.
- **Publicación** del blog en un alojamiento gratuito: base de datos, cambio de URL y subida por FTP.

### Bases de datos (ASXBD)

**MySQL** en Linux y Windows:
- **copias y restauración** con `mysqldump` (bases, tablas, rutinas) y exportación con `SELECT … INTO OUTFILE`;
- **usuarios** con caducidad de contraseña y **privilegios**;
- **rutinas almacenadas**.

### Seguridad (SAD) y criptografía (ACP)

- **Fundamentos** (CIDAN, amenazas físicas y lógicas), **tipos de ataque y de malware**, análisis **forense**, planes y políticas de seguridad (ISO 27000).
- Correo cifrado y firmado con **OpenPGP** (Thunderbird) y **certificado electrónico**.

## 1.er curso

| Módulo | Proyectos |
|---|---|
| **ISO** | Bash y **tareas programadas con cron** ([automatizacion-bash](https://github.com/daniroca5/automatizacion-bash)), **PowerShell**, dominios y **Docker** |
| **PAR** | Redes en **Packet Tracer**: subredes, VLAN y **enrutamiento** estático y dinámico |
| **LM** | **XML** con DTD y XSD, **JSON y YAML**, y un portfolio en HTML y CSS ([FlexboxRocaDaniel](https://github.com/daniroca5/FlexboxRocaDaniel)) |
| **BDD** | Modelo **entidad-relación** y **SQL** |
| **FHW** | **Git**, Python e **IoT** |

<p align="center"><img src="img/aso-permisos-doble-puerta.png" width="360" alt="Permisos de compartido y NTFS"></p>

## Cómo trabajo

Cada práctica se documenta en Markdown: **objetivo, pasos, capturas y verificación**. De ahí salen la web de apuntes y los PDF de entrega. Los pasos llevan casillas para saber qué está hecho, y cada hito tiene una **prueba** que demuestra que funciona: un `gpresult`, un `nslookup`, un acceso denegado…

---

Daniel Roca Martínez · [Currículum](https://daniroca5.gamer.gd/cv/) · [LinkedIn](https://www.linkedin.com/in/daniel-r-m-02b369164/)
