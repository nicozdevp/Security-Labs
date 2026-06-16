# Lab 03 - Implementación de Wazuh SIEM + Suricata IDS

**Asignatura:** Ciberseguridad Defensiva  
**Fecha:** 19-11-2025  
**Autor:** Nicolás Zamora

---

## Objetivos

- Instalar Wazuh en CentOS 10 y verificar interfaz web
- Agregar agentes Wazuh en Windows y Kali Linux
- Configurar Suricata IDS con interfaz de red correcta
- Generar tráfico malicioso y verificar detección en logs de Suricata
- Gestionar usuarios y auditar accesos con logs del sistema
- Definir conceptos clave: IOC, HIDS, gestión de alertas

---

## Arquitectura del Laboratorio

```
┌─────────────────────────────────────────────────────┐
│                    Red Virtual (VMware)              │
│                                                     │
│  ┌──────────────┐    ┌──────────────┐    ┌────────┐ │
│  │  CentOS 10   │    │  Kali Linux  │    │Windows │ │
│  │  Wazuh SIEM  │◄───│  Agente      │    │Agente  │ │
│  │  Suricata    │◄───│  Wazuh       │    │Wazuh   │ │
│  │  IDS/NIDS    │    │              │    │        │ │
│  └──────────────┘    └──────────────┘    └────────┘ │
└─────────────────────────────────────────────────────┘
```

---

## Herramientas Utilizadas

| Herramienta | Versión/Detalle | Rol |
|-------------|-----------------|-----|
| **Wazuh** | Servidor + Indexador + Dashboard | SIEM/XDR central |
| **Suricata** | IDS/NIPS multiproceso | Detección de tráfico malicioso |
| **CentOS 10** | Servidor Linux | Host del SIEM |
| **Kali Linux** | Distribución de pentesting | Agente + generador de tráfico |
| **Windows 10** | Endpoint | Agente monitoreado |

---

## Conceptos Definidos

### IOC (Indicators of Compromise)
Pistas o artefactos que sugieren que una red o sistema ha sido comprometido por una amenaza cibernética. Pueden incluir: tráfico de red anómalo, inicios de sesión desde ubicaciones extrañas, presencia de archivos y procesos sospechosos.

### HIDS (Host-based Intrusion Detection System)
Solución de ciberseguridad instalada en un sistema individual (servidor o estación de trabajo) para monitorear su actividad y detectar signos de actividad sospechosa. Analiza archivos de registro, procesos y actividades del sistema.

### Proceso de Gestión de Alertas
Proceso que implica recibir, evaluar, priorizar, responder y supervisar las notificaciones generadas por sistemas de seguridad. Su objetivo es mitigar amenazas y resolver incidentes de manera eficiente.

---

## Informe Completo

Ver [informe.md](informe.md) para la evidencia con capturas de pantalla.
