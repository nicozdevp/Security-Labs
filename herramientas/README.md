# Herramientas y Plataformas Utilizadas

Referencia de todas las herramientas, plataformas y entornos usados a lo largo del portafolio.

---

## Plataformas de Virtualización

### VMware Workstation
- **Uso:** Plataforma principal para correr las VMs de laboratorio (Kali Linux, CentOS 10, Windows 10)
- **Ventaja:** Soporte de múltiples interfaces de red simultáneas (NAT, Red NAT, Bridge, Host-only)
- **Labs:** Todos los módulos

### VirtualBox
- **Uso:** Correr OpenVAS/Greenbone para escaneos de vulnerabilidades
- **Labs:** [Lab OS/Redes - Ítem 7](../02-seguridad-so-redes/examen-final-techinnovate/informe.md#ítem-7)

### Cisco Packet Tracer
- **Uso:** Simulación de redes para configuración de IPv6 (Router, Switch, PC)
- **Labs:** [Examen SO/Redes - Ítem 2](../02-seguridad-so-redes/examen-final-techinnovate/informe.md#ítem-2)

---

## Sistemas Operativos

### Kali Linux
- **Rol:** Distribución de pentesting - plataforma de trabajo principal en todos los labs
- **Herramientas incluidas:** Wireshark, Nmap, fcrackzip, Metasploit, Nikto, netstat, arp-scan
- **Labs:** Todos los módulos

### CentOS 10 (Rocky Linux / AlmaLinux compatible)
- **Rol:** Servidor Linux - host del SIEM Wazuh y Suricata
- **Labs:** [Lab 03](../01-seguridad-defensiva/lab-03-wazuh-suricata-ids/), [Examen Final Defensiva](../01-seguridad-defensiva/examen-final-nicola-tesla/)

### Windows 10 / 11
- **Rol:** Endpoint monitoreado por el agente Wazuh
- **Labs:** [Lab 03](../01-seguridad-defensiva/lab-03-wazuh-suricata-ids/), [Examen Final Defensiva](../01-seguridad-defensiva/examen-final-nicola-tesla/)

### Metasploitable 2
- **Rol:** Máquina intencionalmente vulnerable usada como objetivo de escaneos y ataques
- **Labs:** [Examen SO/Redes - Ítem 7-8](../02-seguridad-so-redes/examen-final-techinnovate/), [Proyecto ETF](../03-seguridad-computacional/proyecto-etf/)

---

## SIEM / Monitoreo

### Wazuh
- **Tipo:** SIEM + XDR (Security Information & Event Management / Extended Detection and Response)
- **Componentes:** Manager · Indexer (OpenSearch) · Dashboard · Agentes
- **Capacidades usadas:**
  - Instalación en CentOS 10 con script oficial
  - Registro de agentes (Windows y Linux)
  - Correlación de eventos de seguridad
  - Detección de vulnerabilidades en endpoints
  - Integración con Suricata para eventos de red
- **Documentación:** https://documentation.wazuh.com
- **Labs:** [Lab 03](../01-seguridad-defensiva/lab-03-wazuh-suricata-ids/), [Examen Final Defensiva - Ítem 5](../01-seguridad-defensiva/examen-final-nicola-tesla/)

---

## IDS / IPS

### Suricata
- **Tipo:** NIDS/NIPS (Network Intrusion Detection/Prevention System)
- **Capacidades usadas:**
  - Configuración de interfaz de red (`ens160`)
  - Detección de tráfico malicioso en tiempo real
  - Logs en formato JSON (`/var/log/suricata/eve.json`)
  - Compatible con reglas Snort
- **Configuración clave:**
  ```bash
  # Reemplazar interfaz en config
  vim /etc/suricata/suricata.yaml
  :%s/eth0/ens160/g
  
  systemctl restart suricata
  ```
- **Labs:** [Lab 03](../01-seguridad-defensiva/lab-03-wazuh-suricata-ids/)

---

## Análisis de Tráfico de Red

### Wireshark
- **Tipo:** Analizador de protocolos de red (packet sniffer)
- **Capacidades usadas:**
  - Captura de tráfico HTTP vs HTTPS
  - Seguimiento de tramas (Follow TCP Stream)
  - Filtros por protocolo: `http`, `https`, `tcp`
  - Filtros por IP: `ip.src == x.x.x.x && ip.dst == y.y.y.y`
  - Análisis de capturas `.pcap` de malware
- **Labs:** [Lab 02](../01-seguridad-defensiva/lab-02-analisis-trafico-wireshark/)

---

## Análisis de Malware

### VirusTotal
- **Tipo:** Plataforma web de análisis estático de malware
- **URL:** https://www.virustotal.com
- **Capacidades usadas:**
  - Análisis de hashes (MD5, SHA1, SHA256)
  - Análisis de archivos ejecutables (WannaCry)
  - Análisis de reputación de IPs
  - Identificación de IOC (dropped files, dominios, URLs maliciosas)
- **Labs:** [Lab 02](../01-seguridad-defensiva/lab-02-analisis-trafico-wireshark/), [Examen Final Defensiva - Ítem 3-4](../01-seguridad-defensiva/examen-final-nicola-tesla/)

### ANY.RUN
- **Tipo:** Sandbox interactivo en línea para análisis dinámico de malware
- **URL:** https://app.any.run
- **Capacidades usadas:**
  - Ejecución controlada de WannaCry en Windows 10
  - Observación de comportamiento en tiempo real
  - Identificación de IOC dinámicos (procesos, archivos creados, tráfico de red)
  - Clasificación de peligrosidad (100/100 para WannaCry)
- **Labs:** [Examen Final Defensiva - Ítem 3](../01-seguridad-defensiva/examen-final-nicola-tesla/)

---

## Reconocimiento y Escaneo de Red

### Nmap
- **Tipo:** Escáner de red y puertos
- **Comandos usados:**
  ```bash
  nmap -sn 192.168.23.0/24          # Host discovery
  nmap -sV 192.168.23.0/24          # Detección de versiones de servicios
  nmap -O 192.168.23.0/24           # Detección de SO
  nmap -sn 192.168.23.0/24 > /escaneo_de_red.txt  # Guardar resultados
  ```
- **Labs:** [Examen SO/Redes - Ítem 5-6](../02-seguridad-so-redes/examen-final-techinnovate/)

### OpenVAS / Greenbone Vulnerability Manager
- **Tipo:** Escáner de vulnerabilidades de código abierto
- **Capacidades usadas:**
  - Escaneo completo de Metasploitable 2
  - Detección de más de 600 vulnerabilidades
  - Exportación de reportes a TXT para análisis con `grep`
- **Labs:** [Examen SO/Redes - Ítem 7-8](../02-seguridad-so-redes/examen-final-techinnovate/)

---

## Gestión de Tickets

### OTRS
- **Tipo:** Sistema de gestión de tickets adaptado para SOC
- **Uso:** Registro, asignación y seguimiento de incidentes de seguridad
- **Referenciado en:** [Examen Final Defensiva - Ítem 1](../01-seguridad-defensiva/examen-final-nicola-tesla/)

### RTIR (Request Tracker for Incident Response)
- **Tipo:** Extensión de ticket management para respuesta a incidentes de seguridad
- **Referenciado en:** [Examen Final Defensiva - Ítem 1](../01-seguridad-defensiva/examen-final-nicola-tesla/)

---

## Herramientas de Línea de Comandos (Linux)

| Comando | Uso en los labs |
|---------|----------------|
| `wireshark` | Análisis de tráfico de red |
| `nmap` | Reconocimiento y escaneo de puertos |
| `fcrackzip` | Cracking de contraseñas en archivos ZIP |
| `useradd / passwd` | Gestión de usuarios en Linux |
| `chmod / chown` | Gestión de permisos en Linux |
| `ps / top / kill` | Gestión de procesos en Linux |
| `grep / awk / sed` | Filtrado y análisis de logs |
| `tail -f` | Monitoreo de logs en tiempo real |
| `systemctl` | Gestión de servicios (wazuh, suricata) |
| `curl` | Generación de tráfico HTTP para tests |
| `ssh` | Conexión remota entre sistemas |
| `vim` | Edición de archivos de configuración y texto |
| `unzip` | Descompresión de archivos (incluidas muestras de malware) |
| `git clone` | Descarga de repositorios para labs |

---

## Logs Analizados

| Archivo de Log | Sistema | Contenido |
|----------------|---------|-----------|
| `/var/log/secure` | CentOS/RHEL | Autenticaciones SSH, creación de usuarios, accesos |
| `/var/log/messages` | CentOS/RHEL | Eventos generales del sistema, errores, arranque |
| `/var/log/suricata/eve.json` | Suricata | Alertas de red en formato JSON |
| `auth.log` | Debian/Ubuntu/Kali | Intentos de login SSH, sudo, autenticaciones |
