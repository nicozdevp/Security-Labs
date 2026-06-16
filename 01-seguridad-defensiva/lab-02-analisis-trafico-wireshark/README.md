# Lab 02 — Análisis de Tráfico con Wireshark, IOC y Cracking de Contraseñas

**Asignatura:** Ciberseguridad Defensiva  
**Fecha:** 15-10-2025  
**Nota:** 7.0 / 7.0 (21/21 puntos)  
**Equipo:** Eva Gonzalez · Diego Reyes · Alvaro Diaz · Nicolás Zamora

---

## Objetivos

- Capturar y analizar tráfico de red HTTP vs HTTPS con Wireshark
- Identificar paquetes sin cifrar vs cifrados
- Analizar malware real (WannaCry) e identificar sus IOC
- Aplicar filtros avanzados en Wireshark por IP origen/destino
- Ejecutar ataque de diccionario sobre archivo ZIP comprimido con fcrackzip
- Establecer conexión SSH entre sistemas y gestionar procesos
- Analizar logs del sistema con comandos de terminal

---

## Herramientas Utilizadas

| Herramienta | Propósito |
|-------------|-----------|
| **Wireshark** | Captura y análisis de tráfico de red |
| **Kali Linux** | Plataforma de trabajo principal |
| **CentOS 10** | Servidor de destino SSH |
| **Windows** | Cliente SSH origen |
| **VirusTotal** | Análisis estático de malware |
| **fcrackzip** | Cracking de contraseñas en archivos ZIP |
| **rockyou.txt** | Diccionario de contraseñas |
| **SSH** | Conexión remota entre sistemas |

---

## Contenido

Ver [informe.md](informe.md) para la evidencia completa con capturas.

---

## Conceptos Clave Aprendidos

- **HTTP vs HTTPS:** El tráfico HTTP viaja sin cifrar (se pueden leer credenciales); HTTPS cifra todo el contenido del paquete.
- **IOC (Indicadores de Compromiso):** Artefactos que evidencian que un sistema fue comprometido (hashes, IPs maliciosas, dominios, archivos dropped).
- **Filtros Wireshark:** `ip.src == X.X.X.X && ip.dst == Y.Y.Y.Y` permite filtrar tráfico específico.
- **fcrackzip:** Herramienta de fuerza bruta / diccionario para archivos ZIP protegidos con contraseña.
- **tail -n 30 /var/log/messages:** Muestra las últimas 30 líneas del log general del sistema (alertas, errores, eventos de arranque).
