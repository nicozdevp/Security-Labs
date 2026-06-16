# Informe - Lab 01: Fundamentos de Redes

**Laboratorio 1**  
**Autor:** Nicolás Zamora  
**Fecha:** 08-09-2025

---

## Ejercicio 1 - Conversión Numérica: Decimal, Binario y Hexadecimal

| Decimal | Binario | Hexadecimal |
|---------|---------|-------------|
| 67 | 0100 0011 | 43 |
| 39 | 0010 0111 | 27 |
| 167 | 1011 0111 | B7 |
| 32 | 0010 0000 | 20 |
| 190 | 1011 1110 | BE |
| 8 | 0000 1000 | 08 |

---

## Ejercicio 2 - Función del Modelo OSI

El modelo OSI separa el funcionamiento de la red en 7 capas para estandarizar la comunicación, asignando a cada una sus propias funciones y protocolos, asegurando la seguridad y disponibilidad de los servicios.

| Capa | Nombre |
|------|--------|
| 7 | Aplicación |
| 6 | Presentación |
| 5 | Sesión |
| 4 | Transporte |
| 3 | Red |
| 2 | Enlace de datos |
| 1 | Física |

---

## Ejercicio 3 - Capa de Red del Modelo OSI

La capa de red determina la ruta física que deben tomar los datos y gestiona el enrutamiento de los paquetes entre redes.

**Protocolos:** IPv4, IPv6, ICMP  
**Dispositivos:** Routers y Switches de capa 3

---

## Ejercicio 4 - Protocolos Seguros

**HTTPS:** Protocolo web con cifrado TLS/SSL que protege los datos en tránsito entre cliente y servidor.

**SSH:** Permite conectarse de forma remota a un dispositivo usando criptografía para proteger la conexión.

**SFTP:** Protocolo de transferencia de archivos seguro que opera sobre SSH, manteniendo los datos cifrados durante la transmisión.

---

## Ejercicio 5 - Protocolos Inseguros

**Telnet:** Protocolo de acceso remoto que no cifra los datos, permitiendo que terceros puedan interceptarlos.

**HTTP:** Protocolo de transferencia de hipertexto en texto plano; no cifra los datos enviados en formularios o credenciales.

**FTP:** Transferencia de archivos entre dispositivos sin cifrado, vulnerable a interceptación.

---

## Ejercicio 6 - Topología en Cisco Packet Tracer

Se creó una red con 4 computadores conectados a un switch y un servidor.

**Topología:**
```
PC1 ─┐
PC2 ─┤
     Switch ─── Servidor
PC3 ─┤
PC4 ─┘
```

---

## Ejercicio 7 - Configuración IPv4 Estática

Se configuraron 2 PCs manualmente en la misma red:

| Campo | Valor |
|-------|-------|
| Red | 192.168.x.0 |
| Máscara | 255.255.255.0 |
| Gateway | 192.168.x.1 |
| DNS | 192.168.x.45 |

---

## Ejercicio 8 - Configuración de Servidor DHCP

Se configuró el servidor con IP `192.168.x.45` y se levantó el servicio DHCP para asignar IPs automáticamente a los 2 PCs restantes.

**Configuración DHCP:**

| Campo | Valor |
|-------|-------|
| Red | 192.168.x.0 |
| Rango de IPs | 192.168.x.50 - 192.168.x.70 (20 hosts) |
| Gateway | 192.168.x.1 |
| DNS | 192.168.x.45 |

Los 2 equipos sin IP estática recibieron dirección automáticamente desde el servidor DHCP.
