# Examen Final — Caso TechInnovate: Infraestructura de Red Segura

**Asignatura:** Ciberseguridad en Sistemas Operativos y Redes  
**Sigla:** CIBERSEGURIDAD SISTEMA OPERATIVO Y REDES_001D  
**Fecha de entrega:** 03-12-2025  
**Alumno:** Nicolás Zamora · nic.zamora@duocuc.cl  
**Profesor:** Claudio Rojas

---

## Contexto del Caso

> *"TechInnovate es una empresa tecnológica que está configurando su nueva infraestructura de red y sistemas operativos en un entorno controlado. La empresa necesita asegurar que sus sistemas sean robustos y seguros."*

---

## Ítems Evaluados

| # | Ítem | Herramienta |
|---|------|-------------|
| 1 | [Direccionamiento IPv4](informe.md#ítem-1--direccionamiento-ipv4) | Kali Linux, CentOS 10, `ifconfig`/`ip addr` |
| 2 | [Direccionamiento IPv6](informe.md#ítem-2--direccionamiento-ipv6) | Cisco Packet Tracer |
| 3 | [Procesos en Linux](informe.md#ítem-3--administración-de-procesos-en-linux) | `ps`, `top`, `kill` |
| 4 | [Permisos en Linux](informe.md#ítem-4--gestión-de-permisos-en-linux) | `chmod`, `chown`, `groupadd`, `useradd` |
| 5 | [Reconocimiento de red](informe.md#ítem-5--herramientas-de-reconocimiento-de-red) | Nmap, `netstat`, `arp-scan` |
| 6 | [Análisis de resultados Nmap](informe.md#ítem-6--análisis-de-resultados-del-reconocimiento) | Nmap output analysis |
| 7 | [Escaneo de vulnerabilidades](informe.md#ítem-7--escaneo-de-vulnerabilidades) | OpenVAS / Greenbone |
| 8 | [Análisis de vulnerabilidades](informe.md#ítem-8--análisis-de-vulnerabilidades) | OpenVAS reports |

---

## Entorno de Laboratorio

```
Plataforma:     VMware Workstation
Máquina 1:      Kali Linux  (192.168.23.133 — Clase C)
Máquina 2:      CentOS 10
Máquina 3:      Metasploitable 2 (objetivo de vulnerabilidades)
Simulador red:  Cisco Packet Tracer (IPv6)
Red:            192.168.23.0/24
```

---

## Informe Completo

Ver [informe.md](informe.md) para evidencia completa con 28 capturas de pantalla.
