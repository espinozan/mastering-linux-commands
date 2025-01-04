# mastering-linux-commands
Unlock the power of Linux commands to enhance your productivity and master the terminal.




💻 Mastering Linux Commands: Todo lo que No Te Contaron en la Escuela 🔒

Dominar la terminal de Linux es una habilidad clave para cualquier profesional en el mundo de la tecnología. Ya seas Sysadmin, Developer, DevOps o trabajes en ciberseguridad, conocer a fondo los comandos de Linux es fundamental para avanzar en tu carrera. Los atajos y trucos avanzados de la terminal no solo transforman tu forma de trabajar, sino que mejoran significativamente la velocidad y eficiencia en las tareas cotidianas. Este curso te llevará más allá de lo básico, guiándote a través de comandos esenciales y secretos que potenciarán tu productividad y te brindarán una comprensión profunda del sistema. Sumérgete en el poder de la línea de comandos y prepárate para llevar tus habilidades en Linux al siguiente nivel.


🔧 Herramientas de Linux

1️⃣ rsync

Copia archivos y directorios localmente o remotamente, con opciones avanzadas como una barra de progreso.

Ejemplo:

$ rsync -vap --ignore-existing <source_file> <destination_file>

2️⃣ mkpasswd

Genera contraseñas complejas y aleatorias en segundos.

Ejemplo:

$ mkpasswd -l 8 
> iwF1g2Lo 

3️⃣ screen

Crea sesiones de terminal que siguen activas incluso si se pierde la conexión SSH.

Ejemplo:

$ screen 
$ screen -ls 
$ screen -r 

4️⃣ ldapsearch

Ideal para trabajar con bases de datos LDAP, te permite buscar, depurar y administrar entradas.

Ejemplo:

$ ldapsearch -x -W -D <username>

5️⃣ ncdu

Analiza rápidamente el uso de disco y descubre qué directorios ocupan más espacio.

Ejemplo:

$ ncdu 

6️⃣ lsof

Lista los archivos abiertos y qué procesos los están usando. Muy útil para solucionar problemas de montajes.

Ejemplo:

$ lsof 

📡 Herramientas de Red

1️⃣ Netcat (nc)

El “cuchillo suizo” para tareas de red: escaneo de puertos, creación de proxies, transferencia de archivos, y más.

Ejemplo:

$ nc -vz <host> <port> # Escanea puertos 
$ nc -l 8080 | nc <host> 80 # Crea un servidor proxy 

2️⃣ TCPDump

Captura y analiza tráfico de red para solucionar problemas o realizar auditorías de seguridad.

Ejemplo:

$ tcpdump -i <interface> <ipaddress or hostname> <port>

3️⃣ nslookup

Consulta servidores DNS para obtener información de red y depuración.

Ejemplo:

$ nslookup example.com

🛠️ Comandos Ad Hoc

1️⃣ Formatea JSON

Convierte respuestas JSON desordenadas en algo legible.

Ejemplo:

$ cat test.json | python -m json.tool 

2️⃣ Convierte Timestamps Unix a formato legible

Ejemplo:

$ date -d 1656685875 
Fri, 01 Jul 2022 14:31:15 +0000 

3️⃣ Diff de dos comandos

Compara la salida de dos comandos y resalta diferencias.

Ejemplo:

$ diff -u <(ls -l /dir1/) <(ls -l /dir2/) | colordiff 

4️⃣ Combina commits en Git

Ahorra espacio combinando commits anteriores.

Ejemplo:

$ git rebase -i HEAD~x 
$ git push --force-with-lease 

📢 Linux no solo es popular, sino que es imprescindible para gestionar servidores y aplicaciones modernas. Si dominas estas herramientas y comandos, tu eficiencia y habilidades avanzarán significativamente.

---

### 🔧 **Herramientas Avanzadas**  

**1️⃣ htop**  
Una alternativa interactiva a `top` para monitorear procesos y consumo de recursos.  

**Ejemplo:**  
```bash
$ htop
```  

**2️⃣ awk**  
Un poderoso procesador de texto para filtrar y transformar datos en archivos o salidas de comandos.  

**Ejemplo:**  
```bash
$ awk '/error/ {print $1, $2}' log.txt
```  

**3️⃣ xargs**  
Ejecuta comandos en paralelo, tomando entradas de otros comandos.  

**Ejemplo:**  
```bash
$ find . -name "*.log" | xargs rm
```  

---

### 📡 **Comandos de Red y Seguridad**  

**1️⃣ iperf3**  
Mide el rendimiento de red entre dos máquinas.  

**Ejemplo:**  
```bash
$ iperf3 -s # En el servidor
$ iperf3 -c <ip_del_servidor> # En el cliente
```  

**2️⃣ traceroute**  
Rastrea el camino que toma un paquete hasta un host.  

**Ejemplo:**  
```bash
$ traceroute google.com
```  

**3️⃣ fail2ban-client**  
Administra `fail2ban` para proteger servidores contra ataques de fuerza bruta.  

**Ejemplo:**  
```bash
$ fail2ban-client status sshd
```  

---

### 🛠️ **Utilidades Útiles**  

**1️⃣ fzf**  
Un buscador de línea de comandos rápido y personalizable.  

**Ejemplo:**  
```bash
$ cat archivo.txt | fzf
```  

**2️⃣ bat**  
Una alternativa mejorada a `cat`, con resaltado de sintaxis y paginación.  

**Ejemplo:**  
```bash
$ bat archivo.txt
```  

**3️⃣ tldr**  
Muestra resúmenes claros y prácticos de los comandos más populares.  

**Ejemplo:**  
```bash
$ tldr tar
```  

---

### 🚀 **Optimización del Trabajo Diario**  

**1️⃣ rename**  
Renombra múltiples archivos con patrones flexibles.  

**Ejemplo:**  
```bash
$ rename 's/.txt$/.log/' *.txt
```  

**2️⃣ watch**  
Ejecuta un comando periódicamente y muestra el resultado en tiempo real.  

**Ejemplo:**  
```bash
$ watch -n 5 df -h
```  

**3️⃣ chage**  
Gestiona políticas de caducidad de contraseñas para usuarios.  

**Ejemplo:**  
```bash
$ chage -l <username>
```  

---

Estos comandos y herramientas no solo amplían tus capacidades técnicas, sino que también muestran versatilidad en el uso de Linux. 

---

### 🔧 **Herramientas Esenciales**

**1️⃣ `tmux`**  
Similar a `screen`, permite administrar múltiples sesiones de terminal en una sola ventana. Ofrece características avanzadas como dividir ventanas y compartir sesiones.

**Ejemplo:**  
```bash
$ tmux new -s my_session
$ tmux attach -t my_session
```  

**2️⃣ `du`**  
Muestra el uso de disco detallado, ideal para encontrar qué directorios ocupan más espacio.

**Ejemplo:**  
```bash
$ du -h --max-depth=1
```  

**3️⃣ `jq`**  
Un procesador JSON liviano y flexible, perfecto para manejar datos estructurados.

**Ejemplo:**  
```bash
$ cat data.json | jq '.key'
```  

---

### 📡 **Comandos de Red y Seguridad**

**1️⃣ `ss`**  
Una alternativa moderna y más eficiente a `netstat` para analizar sockets y conexiones de red.

**Ejemplo:**  
```bash
$ ss -tuln
```  

**2️⃣ `whois`**  
Obtiene información de registro de dominios y direcciones IP.

**Ejemplo:**  
```bash
$ whois example.com
```  

**3️⃣ `nmap`**  
Una poderosa herramienta para escaneo de puertos y auditorías de seguridad.

**Ejemplo:**  
```bash
$ nmap -A <target_ip>
```  

---

### 🛠️ **Utilidades de Sistema**

**1️⃣ `pv`**  
Muestra el progreso de datos que se transfieren a través de un pipe.

**Ejemplo:**  
```bash
$ pv largefile.tar.gz | tar xz
```  

**2️⃣ `df`**  
Monitorea el espacio libre en los sistemas de archivos montados.

**Ejemplo:**  
```bash
$ df -h
```  

**3️⃣ `uptime`**  
Consulta rápidamente cuánto tiempo lleva encendido el sistema y la carga del CPU.

**Ejemplo:**  
```bash
$ uptime
```  

---

### 🚀 **Optimización y Automatización**

**1️⃣ `cron`**  
Automatiza tareas periódicas.

**Ejemplo:**  
```bash
$ crontab -e
# Agrega: 0 3 * * * /path/to/script.sh
```  

**2️⃣ `sed`**  
Edita texto en streams o archivos directamente desde la terminal.

**Ejemplo:**  
```bash
$ sed 's/old/new/g' file.txt
```  

**3️⃣ `grep`**  
Busca patrones de texto dentro de archivos o salidas de comandos.

**Ejemplo:**  
```bash
$ grep -r 'error' /var/log
```  

---

Si dominas estos comandos adicionales, complementarás tu toolkit con herramientas aún más potentes.

---

### 🔧 **Herramientas Esenciales**

**1️⃣ `bmon`**  
Una herramienta interactiva para monitorear el uso de ancho de banda en tiempo real.  

**Ejemplo:**  
```bash
$ bmon
```  

**2️⃣ `asciinema`**  
Graba sesiones de terminal y compártelas como animaciones. Ideal para tutoriales o demostraciones.  

**Ejemplo:**  
```bash
$ asciinema rec
```  

**3️⃣ `uptimed`**  
Lleva un registro del tiempo de actividad del sistema y genera estadísticas históricas.  

**Ejemplo:**  
```bash
$ uptimed
```  

---

### 📡 **Comandos de Red y Seguridad**

**1️⃣ `arp-scan`**  
Escanea la red local para identificar dispositivos conectados mediante ARP.  

**Ejemplo:**  
```bash
$ arp-scan --localnet
```  

**2️⃣ `openssl`**  
Una navaja suiza para gestionar certificados, cifrado, y conexiones SSL/TLS.  

**Ejemplo:**  
```bash
$ openssl s_client -connect example.com:443
```  

**3️⃣ `dig`**  
Una herramienta avanzada para consultas DNS, con más detalles que `nslookup`.  

**Ejemplo:**  
```bash
$ dig example.com
```  

---

### 🛠️ **Procesamiento de Datos**

**1️⃣ `sort`**  
Ordena líneas de texto en un archivo o salida de comandos.  

**Ejemplo:**  
```bash
$ sort -n archivo.txt
```  

**2️⃣ `uniq`**  
Elimina líneas duplicadas en un archivo, especialmente útil después de usar `sort`.  

**Ejemplo:**  
```bash
$ sort archivo.txt | uniq
```  

**3️⃣ `paste`**  
Une líneas de dos archivos en columnas paralelas.  

**Ejemplo:**  
```bash
$ paste file1.txt file2.txt
```  

---

### 🚀 **Optimización y Tareas Ad Hoc**

**1️⃣ `at`**  
Programa tareas únicas para ejecutarse en un momento específico.  

**Ejemplo:**  
```bash
$ echo "backup.sh" | at 02:00
```  

**2️⃣ `ncal`**  
Un calendario minimalista y visual para la terminal.  

**Ejemplo:**  
```bash
$ ncal -y
```  

**3️⃣ `yes`**  
Genera una línea de texto repetida, útil para pruebas automatizadas.  

**Ejemplo:**  
```bash
$ yes "Texto de prueba"
```  

---

### 💾 **Gestión de Archivos**

**1️⃣ `zip/unzip`**  
Comprime o descomprime archivos ZIP.  

**Ejemplo:**  
```bash
$ zip archivo.zip archivo1 archivo2
$ unzip archivo.zip
```  

**2️⃣ `tar`**  
Empaqueta y comprime con múltiples formatos.  

**Ejemplo:**  
```bash
$ tar -czvf archivo.tar.gz directorio/
```  

**3️⃣ `md5sum`**  
Genera y verifica checksums para validar integridad de archivos.  

**Ejemplo:**  
```bash
$ md5sum archivo.iso
```  

---

Con esta adición, tienes un **arsenal casi ilimitado para dominar Linux**.
Aquí tienes **más comandos avanzados y menos comunes**, que seguro agregarán aún más potencia a tu kit de herramientas de Linux:

---

### 🔧 **Herramientas Avanzadas**

**1️⃣ `fdupes`**  
Encuentra archivos duplicados en directorios específicos.  

**Ejemplo:**  
```bash
$ fdupes -r /ruta/del/directorio
```  

**2️⃣ `tree`**  
Muestra la estructura de directorios en un formato visual jerárquico.  

**Ejemplo:**  
```bash
$ tree -L 2
```  

**3️⃣ `ionice`**  
Establece la prioridad de entrada/salida para procesos, útil cuando manejas sistemas con discos ocupados.  

**Ejemplo:**  
```bash
$ ionice -c3 tar -czf backup.tar.gz /directorio
```  

---

### 📡 **Red y Análisis**

**1️⃣ `ethtool`**  
Gestiona y ajusta configuraciones avanzadas de interfaces de red.  

**Ejemplo:**  
```bash
$ ethtool eth0
```  

**2️⃣ `tcpflow`**  
Captura y analiza el contenido de las conexiones TCP.  

**Ejemplo:**  
```bash
$ tcpflow -i eth0 port 80
```  

**3️⃣ `mtr`**  
Combina las funcionalidades de `ping` y `traceroute` para diagnosticar redes.  

**Ejemplo:**  
```bash
$ mtr example.com
```  

---

### 🛠️ **Optimización del Sistema**

**1️⃣ `iotop`**  
Monitorea en tiempo real qué procesos consumen más I/O en disco.  

**Ejemplo:**  
```bash
$ iotop
```  

**2️⃣ `ps_mem`**  
Muestra el consumo de memoria por cada proceso, agrupado y resumido.  

**Ejemplo:**  
```bash
$ sudo ps_mem
```  

**3️⃣ `preload`**  
Una herramienta que precarga aplicaciones para acelerar su inicio.  

**Ejemplo:**  
```bash
$ sudo apt install preload
```  

---

### 💾 **Gestión de Archivos**

**1️⃣ `inotifywait`**  
Monitorea cambios en archivos o directorios en tiempo real.  

**Ejemplo:**  
```bash
$ inotifywait -m /ruta/a/observar
```  

**2️⃣ `file`**  
Determina el tipo de archivo basándose en su contenido.  

**Ejemplo:**  
```bash
$ file archivo.iso
```  

**3️⃣ `shred`**  
Sobrescribe archivos con datos aleatorios para garantizar su eliminación segura.  

**Ejemplo:**  
```bash
$ shred -u archivo.txt
```  

---

### 🚀 **Automatización y Scripts**

**1️⃣ `atop`**  
Una herramienta avanzada para monitorear el rendimiento del sistema, con la capacidad de almacenar históricos.  

**Ejemplo:**  
```bash
$ atop
```  

**2️⃣ `gpg`**  
Cifra y firma datos y comunicaciones con el estándar OpenPGP.  

**Ejemplo:**  
```bash
$ gpg -c archivo.txt
```  

**3️⃣ `bc`**  
Una calculadora de línea de comandos, compatible con cálculos avanzados.  

**Ejemplo:**  
```bash
$ echo "scale=2; 5/3" | bc
```  

---

### 🧠 **Trucos y Atajos**

**1️⃣ Crear alias personalizados**  
Agiliza tareas con alias en tu `~/.bashrc`.  

**Ejemplo:**  
```bash
$ echo "alias ll='ls -la'" >> ~/.bashrc && source ~/.bashrc
```  

**2️⃣ Ejecutar múltiples comandos en paralelo**  
Usa `&` o `&&` según tus necesidades.  

**Ejemplo:**  
```bash
$ comando1 & comando2
```  

**3️⃣ Correr un comando sin que quede en el historial**  
Usa un espacio antes del comando (requiere que `HISTCONTROL=ignorespace` esté activo).  

**Ejemplo:**  
```bash
$  comando_secreto
```  

---

### ¿Necesitas Más?

Estos comandos son ideales para sistemas de desarrollo, administración de servidores, análisis de redes y seguridad.

Aquí tienes **aún más comandos y herramientas avanzadas** que probablemente no conocías y que son muy útiles para tareas especializadas en Linux:

---

### 🔧 **Gestión del Sistema**

**1️⃣ `nmon`**  
Monitorea el rendimiento del sistema (CPU, memoria, red, disco, etc.) en tiempo real.  

**Ejemplo:**  
```bash
$ nmon
```  

**2️⃣ `uname`**  
Muestra información detallada sobre el sistema operativo.  

**Ejemplo:**  
```bash
$ uname -a
```  

**3️⃣ `uptimed`**  
Registra el tiempo de actividad del sistema y genera estadísticas históricas.  

**Ejemplo:**  
```bash
$ uptimed
```  

---

### 📡 **Herramientas de Red**

**1️⃣ `arp`**  
Muestra y manipula la tabla ARP para ver dispositivos en la red local.  

**Ejemplo:**  
```bash
$ arp -a
```  

**2️⃣ `curl`**  
Una herramienta extremadamente versátil para hacer solicitudes HTTP y FTP desde la terminal.  

**Ejemplo:**  
```bash
$ curl -I https://example.com
```  

**3️⃣ `vnstat`**  
Monitorea el uso de la red a largo plazo.  

**Ejemplo:**  
```bash
$ vnstat
```  

---

### 🛠️ **Gestión de Archivos y Directorios**

**1️⃣ `stat`**  
Obtén información detallada sobre un archivo (permisos, tamaño, última modificación, etc.).  

**Ejemplo:**  
```bash
$ stat archivo.txt
```  

**2️⃣ `find`**  
Busca archivos en una jerarquía de directorios con filtros avanzados.  

**Ejemplo:**  
```bash
$ find /ruta -type f -size +10M
```  

**3️⃣ `duf`**  
Una versión moderna de `df`, con una interfaz más legible para monitorear el uso del disco.  

**Ejemplo:**  
```bash
$ duf
```  

---

### 🚀 **Procesamiento de Datos**

**1️⃣ `cut`**  
Extrae columnas específicas de un archivo o flujo de texto.  

**Ejemplo:**  
```bash
$ cut -d',' -f1,3 archivo.csv
```  

**2️⃣ `sort`**  
Ordena líneas en un archivo o salida.  

**Ejemplo:**  
```bash
$ sort -k2 -n archivo.txt
```  

**3️⃣ `split`**  
Divide un archivo grande en partes más pequeñas.  

**Ejemplo:**  
```bash
$ split -b 50M archivo_grande.tar.gz parte_
```  

---

### 💻 **Automatización y Programación**

**1️⃣ `watch`**  
Ejecuta comandos periódicamente y muestra la salida en tiempo real.  

**Ejemplo:**  
```bash
$ watch -n 1 free -h
```  

**2️⃣ `taskset`**  
Establece la afinidad de CPU para un proceso.  

**Ejemplo:**  
```bash
$ taskset -c 0,2,4 comando
```  

**3️⃣ `nohup`**  
Ejecuta un comando para que continúe funcionando incluso si cierras la terminal.  

**Ejemplo:**  
```bash
$ nohup comando &
```  

---

### 🔒 **Seguridad**

**1️⃣ `gpg`**  
Cifra archivos con claves públicas/privadas.  

**Ejemplo:**  
```bash
$ gpg -c archivo_secreto.txt
```  

**2️⃣ `iptables`**  
Gestiona reglas de firewall para proteger servidores.  

**Ejemplo:**  
```bash
$ iptables -A INPUT -p tcp --dport 22 -j ACCEPT
```  

**3️⃣ `auditd`**  
Monitorea eventos de seguridad y cambios en el sistema.  

**Ejemplo:**  
```bash
$ ausearch -m avc -ts recent
```  

---

### 🧠 **Tips y Trucos**

**1️⃣ Historial sin duplicados**  
Evita registrar comandos duplicados en tu historial.  

```bash
$ export HISTCONTROL=ignoredups
```  

**2️⃣ Limita el tamaño del historial**  

```bash
$ export HISTSIZE=5000
$ export HISTFILESIZE=10000
```  

**3️⃣ Reutiliza el último argumento del comando anterior**  

```bash
$ echo "Hola Mundo"
$ cat !$  # Expande al último argumento ("Hola Mundo")
```  

---

### 🔧 Herramientas Adicionales y Avanzadas para Linux

**1️⃣ `cut`**  
Extrae columnas específicas de un archivo o flujo de texto.  

**Ejemplo:**  
```bash
$ cut -d',' -f1,3 archivo.csv
```  

**2️⃣ `split`**  
Divide archivos grandes en partes más pequeñas para facilitar su manejo.  

**Ejemplo:**  
```bash
$ split -b 100M archivo_grande.bin parte_
```  

**3️⃣ `diff`**  
Compara archivos línea por línea y resalta las diferencias.  

**Ejemplo:**  
```bash
$ diff archivo1.txt archivo2.txt
```  

---

### 🧠 Trucos Avanzados

**1️⃣ Redirigir errores y salidas a archivos diferentes**  
Guarda la salida estándar y los errores en diferentes archivos.  

**Ejemplo:**  
```bash
$ comando > salida.log 2> error.log
```  

**2️⃣ Procesar grandes cantidades de datos con `parallel`**  
Ejecuta comandos en paralelo para acelerar procesos.  

**Ejemplo:**  
```bash
$ find . -name '*.jpg' | parallel convert {} {.}.png
```  

**3️⃣ Comprimir salidas en tiempo real**  
Usa `gzip` para reducir el tamaño de datos mientras se transfieren o procesan.  

**Ejemplo:**  
```bash
$ comando | gzip > salida.gz
```  

---

Estas herramientas y comandos amplían tu control sobre Linux, permitiéndote manejar desde flujos de trabajo básicos hasta optimización avanzada en servidores y redes.🚀

Aquí tienes **más comandos y herramientas avanzadas de Linux**, útiles para diversas tareas y menos conocidos por usuarios promedio:

---

### 🔧 **Herramientas Esenciales**

**1️⃣ `nc (Netcat)`**  
Realiza transferencias de archivos, escaneo de puertos y conexiones simples.  

**Ejemplo:**  
```bash
$ nc -l -p 1234 > archivo_recibido
$ cat archivo_a_enviar | nc <ip_destino> 1234
```  

**2️⃣ `htpasswd`**  
Crea y administra archivos de contraseñas encriptadas para autenticación en servidores web como Apache o NGINX.  

**Ejemplo:**  
```bash
$ htpasswd -c .htpasswd usuario
```  

**3️⃣ `watch`**  
Ejecuta un comando en intervalos regulares y muestra su salida en tiempo real.  

**Ejemplo:**  
```bash
$ watch -n 5 'ls -lh /var/log'
```  

---

### 📡 **Comandos de Red**

**1️⃣ `iftop`**  
Supervisa el tráfico de red en tiempo real, clasificando por conexiones activas.  

**Ejemplo:**  
```bash
$ iftop -i eth0
```  

**2️⃣ `ncat`**  
Una mejora de Netcat, compatible con protocolos avanzados como SSL/TLS.  

**Ejemplo:**  
```bash
$ ncat -l --ssl --ssl-cert cert.pem --ssl-key key.pem 1234
```  

**3️⃣ `tshark`**  
Una versión de línea de comandos de Wireshark para capturar y analizar paquetes.  

**Ejemplo:**  
```bash
$ tshark -i eth0 -f "port 80"
```  

---

### 🛠️ **Procesamiento de Datos y Textos**

**1️⃣ `sort`**  
Ordena datos en archivos o entradas estándar.  

**Ejemplo:**  
```bash
$ sort -k2,2 archivo.csv
```  

**2️⃣ `split`**  
Divide un archivo grande en partes más pequeñas.  

**Ejemplo:**  
```bash
$ split -b 10M archivo_grande.txt parte_
```  

**3️⃣ `comm`**  
Compara dos archivos línea por línea, mostrando las diferencias.  

**Ejemplo:**  
```bash
$ comm archivo1.txt archivo2.txt
```  

---

### 🚀 **Automatización y Optimización**

**1️⃣ `alias`**  
Crea atajos para comandos repetitivos.  

**Ejemplo:**  
```bash
$ alias actualizar='sudo apt update && sudo apt upgrade -y'
```  

**2️⃣ `nohup`**  
Ejecuta comandos que continuarán corriendo incluso después de cerrar la sesión.  

**Ejemplo:**  
```bash
$ nohup script_largo.sh &
```  

**3️⃣ `fg` y `bg`**  
Mueve procesos entre primer plano y segundo plano.  

**Ejemplo:**  
```bash
$ bg %1
$ fg %1
```  

---

### 🔒 **Seguridad y Auditorías**

**1️⃣ `auditd`**  
Supervisa y registra eventos en el sistema para auditorías de seguridad.  

**Ejemplo:**  
```bash
$ sudo auditctl -w /ruta/a/monitorear -p warx
```  

**2️⃣ `passwd`**  
Administra contraseñas de usuarios en el sistema.  

**Ejemplo:**  
```bash
$ passwd <usuario>
```  

**3️⃣ `chattr`**  
Evita que archivos sean modificados, incluso por el usuario root.  

**Ejemplo:**  
```bash
$ sudo chattr +i archivo_critico.txt
```  

---

### 💾 **Gestión de Almacenamiento**

**1️⃣ `blkid`**  
Muestra identificadores únicos de particiones (UUIDs).  

**Ejemplo:**  
```bash
$ blkid
```  

**2️⃣ `lsblk`**  
Lista todos los dispositivos de bloque, incluidos discos y particiones.  

**Ejemplo:**  
```bash
$ lsblk -f
```  

**3️⃣ `resize2fs`**  
Expande o reduce el tamaño de un sistema de archivos ext4.  

**Ejemplo:**  
```bash
$ resize2fs /dev/sda1
```  

---

### 💡 **Tips Extra**

- **Corregir errores de sintaxis fácilmente:**  
  Usa `Ctrl + x, e` para abrir la línea de comandos en un editor si el comando es muy largo.  

- **Repetir comandos recientes:**  
  Usa `!número` para ejecutar un comando por su número en el historial (`history`).  

- **Buscar en historial:**  
  Usa `Ctrl + r` seguido de palabras clave para buscar comandos ejecutados anteriormente.  

---

Aquí tienes más **tips extra para usar Linux** como un experto:  

---

### 💡 **Optimización del Uso de la Terminal**

1️⃣ **Edición rápida de comandos:**  
- Usa `Ctrl + a` para mover el cursor al inicio de la línea.  
- Usa `Ctrl + e` para moverlo al final.  
- Usa `Alt + f` y `Alt + b` para moverte palabra por palabra.  
- Usa `Ctrl + k` para borrar desde el cursor hasta el final de la línea.  

---

2️⃣ **Corrección de errores comunes en comandos:**  
- Si olvidas usar `sudo` y obtienes un error de permisos, escribe:  
  ```bash
  $ sudo !!
  ```  
  Esto ejecuta el último comando con `sudo`.

---

3️⃣ **Reutilizar argumentos anteriores:**  
- Usa `Alt + .` para insertar el último argumento del comando previo.  

**Ejemplo:**  
```bash
$ tar -czf archivo.tar.gz directorio/
$ mv archivo.tar.gz /ruta/destino/Alt+.
```

---

4️⃣ **Ejecutar varios comandos en una línea:**  
- Usa `;` para ejecutar comandos consecutivos:  
  ```bash
  $ comando1; comando2; comando3
  ```  
- Usa `&&` para que el siguiente comando solo se ejecute si el anterior tuvo éxito:  
  ```bash
  $ comando1 && comando2
  ```  
- Usa `||` para ejecutar el siguiente comando solo si el anterior falla:  
  ```bash
  $ comando1 || comando2
  ```

---

### 🔍 **Historial y Comandos Anteriores**

5️⃣ **Buscar rápidamente en el historial:**  
- Usa `history | grep <palabra>` para buscar comandos pasados.  
- Para ejecutar directamente, combina con `!`:  
  ```bash
  $ !<número_comando>
  ```  

---

6️⃣ **Repetir comandos con reemplazos rápidos:**  
- Usa `^palabra_original^nueva_palabra` para corregir errores.  

**Ejemplo:**  
```bash
$ mv archivo.tx /carpeta
$ ^tx^txt
```

---

### 🚀 **Atajos para Procesos y Trabajos**

7️⃣ **Controlar procesos en segundo plano:**  
- Usa `&` para enviar un proceso al fondo al iniciar:  
  ```bash
  $ comando_largo &
  ```  
- Detén un proceso con `Ctrl + z` y envíalo al fondo con `bg`.  
- Trae un proceso al primer plano con `fg`.  

---

8️⃣ **Controlar recursos del sistema:**  
- Limita el uso de CPU de un proceso con `cpulimit`:  
  ```bash
  $ cpulimit -l 50 -p <PID>
  ```  
- Limita el uso de RAM con `cgroups` o `systemd` (más avanzado).  

---

### ⚙️ **Scripting y Automatización**

9️⃣ **Ejecución de scripts sin permisos root:**  
- Haz que un archivo sea ejecutable:  
  ```bash
  $ chmod +x script.sh
  ```  
- Usa `./` para ejecutarlo.  

---

🔟 **Programar tareas con `cron`:**  
- Edita el cron con:  
  ```bash
  $ crontab -e
  ```  
  **Ejemplo:** Ejecutar un script todos los días a las 3 am:  
  ```bash
  0 3 * * * /ruta/a/script.sh
  ```  

---

### 🛠️ **Gestión de Archivos y Directorios**

1️⃣1️⃣ **Expandir comodines para trabajar con muchos archivos:**  
- Usa `*` para todos los archivos:  
  ```bash
  $ rm *.txt
  ```  
- Usa `{}` para listas específicas:  
  ```bash
  $ mv archivo{1,2,3}.txt /destino
  ```  
- Usa `?` para un único carácter variable:  
  ```bash
  $ cp archivo?.txt /destino
  ```

---

1️⃣2️⃣ **Encontrar archivos rápidamente:**  
- Usa `find` para buscar en el sistema de archivos:  
  ```bash
  $ find /ruta -name "archivo*.txt"
  ```  
- Usa `locate` (requiere instalación):  
  ```bash
  $ locate archivo.txt
  ```

---

1️⃣3️⃣ **Borrar archivos grandes de forma eficiente:**  
Si un archivo bloquea espacio, incluso después de eliminarlo:  
  ```bash
  $ lsof +L1
  $ truncate -s 0 /ruta/del/archivo
  ```  

---

### 🔒 **Seguridad y Encriptación**

1️⃣4️⃣ **Crear archivos protegidos con contraseña:**  
- Usa `zip` con protección:  
  ```bash
  $ zip -e archivo.zip archivo.txt
  ```  
- Usa `openssl` para cifrado simple:  
  ```bash
  $ openssl enc -aes-256-cbc -salt -in archivo.txt -out archivo.enc
  ```

---

### 🧪 **Tips Curiosos y Divertidos**

1️⃣5️⃣ **Convertir comandos en memes:**  
- Usa `cowsay` para agregar humor:  
  ```bash
  $ cowsay "Hola, soy Linux"
  ```  
- Usa `fortune` para frases aleatorias combinadas:  
  ```bash
  $ fortune | cowsay
  ```  

1️⃣6️⃣ **Animaciones ASCII en la terminal:**  
- Instala `sl` para ver un tren en ASCII al escribir mal `ls`:  
  ```bash
  $ sl
  ```  
- Usa `cmatrix` para un efecto Matrix:  
  ```bash
  $ cmatrix
  ```

---

Aquí tienes **tips avanzados para la gestión de redes en Linux** que pueden ser muy útiles:  

---

### 🌐 **Diagnóstico y Monitoreo de Redes**

1️⃣ **Verificar conectividad básica:**  
- Usa `ping` para comprobar si un host está accesible:  
  ```bash
  $ ping -c 4 ejemplo.com
  ```  
  - **Tip Extra:** Usa `ping -i 0.2` para reducir el intervalo entre pings y obtener más respuestas rápidamente.  

---

2️⃣ **Resolver problemas de DNS:**  
- Usa `nslookup` para buscar registros DNS:  
  ```bash
  $ nslookup ejemplo.com
  ```  
- Usa `dig` para obtener más detalles:  
  ```bash
  $ dig ejemplo.com
  ```  
  **Extra:** Agrega la opción `+short` para simplificar la salida:  
  ```bash
  $ dig ejemplo.com +short
  ```  

---

3️⃣ **Ver rutas hacia un servidor (traceroute):**  
- Usa `traceroute` para diagnosticar rutas y latencia:  
  ```bash
  $ traceroute ejemplo.com
  ```  
  Si no tienes `traceroute`, usa `mtr` para un análisis en tiempo real:  
  ```bash
  $ mtr ejemplo.com
  ```  

---

4️⃣ **Medir velocidad de transferencia:**  
- Usa `iperf` para probar ancho de banda entre dos nodos (uno como servidor y otro como cliente):  
  **Servidor:**  
  ```bash
  $ iperf3 -s
  ```  
  **Cliente:**  
  ```bash
  $ iperf3 -c <IP_del_servidor>
  ```  

---

### 🛠️ **Configuración de Redes**

5️⃣ **Mostrar interfaces de red y direcciones IP:**  
- Usa `ip a` para obtener detalles de todas las interfaces:  
  ```bash
  $ ip a
  ```  
  **Tip Extra:** Filtra información específica, como IPv4:  
  ```bash
  $ ip -4 a
  ```  

---

6️⃣ **Configurar IP estática temporalmente:**  
- Asigna una IP a una interfaz (temporal hasta reiniciar):  
  ```bash
  $ sudo ip addr add 192.168.1.100/24 dev eth0
  ```  
- Cambia la puerta de enlace predeterminada:  
  ```bash
  $ sudo ip route add default via 192.168.1.1
  ```  

---

7️⃣ **Restablecer interfaces de red:**  
- Usa `ifdown` y `ifup` para reiniciar una interfaz:  
  ```bash
  $ sudo ifdown eth0 && sudo ifup eth0
  ```  
  Si usas `NetworkManager`, puedes hacerlo con:  
  ```bash
  $ nmcli device reapply eth0
  ```  

---

### 🔍 **Escaneo y Análisis de Redes**

8️⃣ **Escaneo básico con Nmap:**  
- Detecta hosts activos en tu red:  
  ```bash
  $ nmap -sn 192.168.1.0/24
  ```  
- Escanea puertos abiertos en un host:  
  ```bash
  $ nmap -p 1-65535 ejemplo.com
  ```  
  **Extra:** Usa `-A` para habilitar detección avanzada (SO, servicios, etc.):  
  ```bash
  $ nmap -A ejemplo.com
  ```  

---

9️⃣ **Capturar tráfico de red:**  
- Usa `tcpdump` para analizar paquetes:  
  ```bash
  $ sudo tcpdump -i eth0
  ```  
  Filtra por puerto:  
  ```bash
  $ sudo tcpdump -i eth0 port 80
  ```  
  Guarda el tráfico en un archivo para analizarlo después:  
  ```bash
  $ sudo tcpdump -w captura.pcap
  ```  
  **Tip Extra:** Abre el archivo `.pcap` en Wireshark para un análisis visual detallado.  

---

10️⃣ **Escaneo de redes Wi-Fi:**  
- Usa `iwlist` para ver redes cercanas:  
  ```bash
  $ sudo iwlist wlan0 scan
  ```  
  Si prefieres algo más visual, usa `nmcli`:  
  ```bash
  $ nmcli dev wifi list
  ```  

---

### 🔒 **Seguridad en Redes**

1️⃣1️⃣ **Bloquear conexiones sospechosas con UFW:**  
- Permitir solo conexiones SSH:  
  ```bash
  $ sudo ufw allow ssh
  ```  
- Bloquear IP específica:  
  ```bash
  $ sudo ufw deny from 192.168.1.50
  ```  

---

1️⃣2️⃣ **Limitar conexiones por puerto con `iptables`:**  
- Permitir solo 10 conexiones por minuto en el puerto 22:  
  ```bash
  $ sudo iptables -A INPUT -p tcp --dport 22 -m limit --limit 10/min -j ACCEPT
  ```  

---

### 📡 **Redes Avanzadas**

1️⃣3️⃣ **Compartir Internet desde Linux (NAT):**  
- Habilita IP forwarding:  
  ```bash
  $ sudo sysctl -w net.ipv4.ip_forward=1
  ```  
- Configura NAT con `iptables`:  
  ```bash
  $ sudo iptables -t nat -A POSTROUTING -o eth0 -j MASQUERADE
  ```  

---

1️⃣4️⃣ **Configurar un servidor DHCP con `dnsmasq`:**  
- Instala y edita la configuración básica en `/etc/dnsmasq.conf`:  
  ```bash
  interface=eth0
  dhcp-range=192.168.1.100,192.168.1.200,12h
  ```  
  Reinicia el servicio:  
  ```bash
  $ sudo systemctl restart dnsmasq
  ```

---

1️⃣5️⃣ **Crear túneles SSH para saltar restricciones:**  
- Redirige un puerto local a un servidor remoto:  
  ```bash
  $ ssh -L 8080:localhost:80 usuario@servidor
  ```  
  Ahora puedes acceder a `localhost:8080` para conectarte al puerto 80 del servidor.  

---

mastering-linux-commands
			created by 
				  espinozan 😊
