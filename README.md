# Portafolio de Ciberseguridad - Nicolás Zamora

> Estudiante de Ciberseguridad en Duoc UC · Santiago, Chile
> Correo: nic.zamora@duocuc.cl

Repositorio con evidencia práctica de los laboratorios y evaluaciones desarrollados durante mi formación en ciberseguridad. Cada carpeta corresponde a una asignatura o módulo, con informes en Markdown, capturas de pantalla reales y los comandos usados.

---

## Módulos

| # | Módulo | Temas principales | Herramientas |
|---|--------|-------------------|--------------|
| [01](01-seguridad-defensiva/) | **Ciberseguridad Defensiva** | SOC, SIEM, gestión de alertas, análisis de malware, Wazuh, Suricata | Wazuh, Suricata, Wireshark, VirusTotal, fcrackzip, Kali Linux, CentOS 10 |
| [02](02-seguridad-so-redes/) | **Seguridad en S.O. y Redes** | OSI, protocolos, IPv4/IPv6, usuarios Linux, firewall, escaneo de vulnerabilidades, normativas | Nmap, OpenVAS, Nikto, Wireshark, firewalld, Cisco Packet Tracer, Kali Linux, CentOS 10 |
| [03](03-seguridad-computacional/) | **Seguridad en Sistemas Computacionales** | Ethical hacking, políticas de seguridad, plan de mitigación | Kali Linux, Metasploitable 2 |

---

## Habilidades Demostradas

### Seguridad Defensiva (Blue Team)
- Configuración e implementación de SIEM con **Wazuh** (servidor, indexador, dashboard)
- Despliegue de agentes Wazuh en **Windows** y **Linux (Kali)**
- Configuración de **Suricata** como NIDS/NIPS con reglas de detección
- Gestión del ciclo de vida de alertas en un SOC (10 etapas: recepción - lecciones aprendidas)
- Análisis de logs del sistema (`/var/log/secure`, `/var/log/suricata/eve.json`)

### Análisis de Tráfico y Malware
- Captura y análisis de tráfico con **Wireshark** (HTTP vs HTTPS, filtros avanzados)
- Análisis de malware real (**WannaCry**) en **VirusTotal** y **ANY.RUN** (sandboxing)
- Identificación de **IOC** (hashes SHA256, IPs, dominios, dropped files)
- Ataque de diccionario con **fcrackzip** y wordlist rockyou

### Redes y Sistemas Operativos
- Modelo OSI: 7 capas, protocolos seguros (HTTPS, SSH, SFTP) e inseguros (Telnet, HTTP, FTP)
- Direccionamiento **IPv4** (clases, subred, gateway) e **IPv6** (unicast global, link-local)
- Diseño de topologías con **Cisco Packet Tracer** (switch, servidor, DHCP)
- Administración de usuarios, grupos y permisos en Linux (`useradd`, `chmod 754`, `chown`)
- Configuración de firewall con **firewalld** (puertos TCP 80, 443, 20, 21)
- Reconocimiento de red con **Nmap** (`-sn`, `-sV`, `-O`, identificación de CVEs)
- Escaneo de vulnerabilidades web con **Nikto**
- Escaneo de vulnerabilidades con **OpenVAS/Greenbone** sobre Metasploitable 2

### Normativas y Documentación
- Conocimiento de **PCI DSS** y su aplicación en protección de datos financieros
- Conocimiento de la **Ley 21.459** sobre delitos informáticos en Chile
- Creación de matrices de riesgo (impacto × probabilidad)
- Redacción de políticas de seguridad (objetivo, alcance, responsables, sanciones)
- Desarrollo de playbooks para DDoS y troyanos
- Clasificación de riesgos según triada CIA

---

## Entorno de Trabajo

| Componente | Detalle |
|------------|---------|
| Plataforma de virtualización | VMware Workstation |
| Distribución atacante | Kali Linux |
| Servidor Linux | CentOS 10 |
| Endpoint Windows | Windows 10 |
| Máquina vulnerable | Metasploitable 2 |
| Simulación de red | Cisco Packet Tracer |
| SIEM/XDR | Wazuh (servidor + agentes) |
| IDS/IPS | Suricata |
| Análisis de tráfico | Wireshark |
| Escaneo de vulnerabilidades | OpenVAS / Greenbone |
| Análisis web | Nikto |
| Escaneo de red | Nmap |
| Análisis de malware | VirusTotal · ANY.RUN |
| Firewall Linux | firewalld |

---

## Estructura del Repositorio

```
portafolio-ciberseguridad/
├── 01-seguridad-defensiva/
│   ├── lab-01-fundamentos-soc/               # Laboratorio 1 - SOC, SIEM, políticas, playbooks
│   ├── lab-02-analisis-trafico-wireshark/    # Laboratorio 2 - Wireshark, WannaCry, fcrackzip
│   ├── lab-03-wazuh-suricata-ids/            # Laboratorio 3 - Wazuh + Suricata en producción
│   └── examen-final-nicola-tesla/            # Examen Final - caso completo SOC
├── 02-seguridad-so-redes/
│   ├── lab-01-fundamentos-redes/             # Laboratorio 1 - OSI, protocolos, Packet Tracer, DHCP
│   ├── lab-02-administracion-linux/          # Laboratorio 2 - usuarios, permisos, firewalld, Wireshark
│   ├── lab-03-vulnerabilidades-y-normativas/ # Laboratorio 3 - OpenVAS, Nmap, Nikto, CIA, PCI DSS
│   └── examen-final-techinnovate/            # Examen Final - IPv4/IPv6, Nmap, OpenVAS
├── 03-seguridad-computacional/
│   └── proyecto-etf/                         # ETF - Ethical hacking, política, mitigación
└── herramientas/                             # Referencia de todas las herramientas usadas
```

---
