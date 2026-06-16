# Portafolio de Ciberseguridad — Nicolás Zamora

> Estudiante de Ciberseguridad en Duoc UC · Santiago, Chile
> Correo: nic.zamora@duocuc.cl

Repositorio con evidencia práctica de los laboratorios y evaluaciones desarrollados durante mi formación en ciberseguridad. Cada carpeta corresponde a una asignatura o módulo, con informes en Markdown, capturas de pantalla reales y los comandos usados.

---

## Módulos

| # | Módulo | Temas principales | Herramientas |
|---|--------|-------------------|--------------|
| [01](01-seguridad-defensiva/) | **Ciberseguridad Defensiva** | SOC, SIEM, gestión de alertas, análisis de malware, Wazuh, Suricata | Wazuh, Suricata, Wireshark, VirusTotal, fcrackzip, Kali Linux, CentOS 10 |
| [02](02-seguridad-so-redes/) | **Seguridad en S.O. y Redes** | IPv4/IPv6, procesos Linux, permisos, reconocimiento de red, escaneo de vulnerabilidades | Nmap, OpenVAS/Greenbone, Kali Linux, CentOS 10, Cisco Packet Tracer |
| [03](03-seguridad-computacional/) | **Seguridad en Sistemas Computacionales** | Ethical hacking, políticas de seguridad, plan de mitigación | Kali Linux, Metasploitable 2 |

---

## Habilidades Demostradas

### Seguridad Defensiva (Blue Team)
- Configuración e implementación de SIEM con **Wazuh** (servidor, indexador, dashboard)
- Despliegue de agentes Wazuh en **Windows** y **Linux (Kali)**
- Configuración de **Suricata** como NIDS/NIPS con reglas de detección
- Gestión del ciclo de vida de alertas en un SOC (10 etapas: recepción → lecciones aprendidas)
- Análisis de logs del sistema (`/var/log/secure`, `/var/log/suricata/eve.json`)

### Análisis de Tráfico y Malware
- Captura y análisis de tráfico con **Wireshark** (HTTP vs HTTPS)
- Análisis de malware real (**WannaCry**) en **VirusTotal** y **ANY.RUN** (sandboxing)
- Identificación de **IOC** (hashes SHA256, IPs, dominios, dropped files)
- Ataque de diccionario con **fcrackzip** y wordlist rockyou

### Redes y Sistemas Operativos
- Direccionamiento **IPv4** (clases, subred, gateway) e **IPv6** (unicast global, link-local)
- Administración de procesos en Linux (`ps`, `top`, `kill`)
- Gestión de permisos (`chmod 754`, grupos, usuarios)
- Reconocimiento de red con **Nmap** (`-sn`, `-sV`, `-O`)
- Escaneo de vulnerabilidades con **OpenVAS/Greenbone** sobre Metasploitable 2

### Análisis y Documentación
- Creación de matrices de riesgo (impacto × probabilidad)
- Redacción de políticas de seguridad (objetivo, alcance, responsables, sanciones)
- Desarrollo de playbooks para DDoS y troyanos
- Clasificación de riesgos según CIA (Confidencialidad, Integridad, Disponibilidad)

---

## Entorno de Trabajo

| Componente | Detalle |
|------------|---------|
| Plataforma de virtualización | VMware Workstation |
| Distribución atacante | Kali Linux |
| Servidor Linux | CentOS 10 |
| Endpoint Windows | Windows 10 |
| Simulación de red | Cisco Packet Tracer |
| SIEM/XDR | Wazuh (servidor + agentes) |
| IDS/IPS | Suricata |
| Análisis de tráfico | Wireshark |
| Análisis de malware | VirusTotal · ANY.RUN |

---

## Estructura del Repositorio

```
portafolio-ciberseguridad/
├── 01-seguridad-defensiva/
│   ├── lab-01-fundamentos-soc/          # Prueba 1 — SOC, SIEM, políticas, playbooks
│   ├── lab-02-analisis-trafico-wireshark/  # Prueba N-2 — Wireshark, WannaCry, fcrackzip
│   ├── lab-03-wazuh-suricata-ids/       # Prueba N-3 — Wazuh + Suricata en producción
│   └── examen-final-nicola-tesla/       # Examen Final — caso completo SOC
├── 02-seguridad-so-redes/
│   └── examen-final-techinnovate/       # Examen Final — IPv4/IPv6, Nmap, OpenVAS
├── 03-seguridad-computacional/
│   └── proyecto-etf/                    # ETF — Ethical hacking, política, mitigación
└── herramientas/                        # Referencia de todas las herramientas usadas
```

---


