# Informe - Lab 02: Administración Linux, Permisos y Firewall

**Laboratorio 2**  
**Autor:** Nicolás Zamora  
**Fecha:** 15-10-2025

---

## Ejercicio 1 - Creación de Usuarios en Linux

Se crearon 3 usuarios en CentOS 10 con contraseña `hello.136`:

```bash
useradd usuario1
passwd usuario1

useradd usuario2
passwd usuario2

useradd usuario3
passwd usuario3
```

![Usuarios creados en CentOS 10](imagenes/image1.png)

---

## Ejercicio 2 - Creación de Grupo

```bash
groupadd prueba2-nz
```

![Grupo creado](imagenes/image2.png)

---

## Ejercicio 3 - Creación de Directorio y Archivo

```bash
mkdir -p /unidad2/prueba2/nz/
touch /unidad2/prueba2/nz/nz.txt
```

![Directorio y archivo creados](imagenes/image3.png)

---

## Ejercicio 4 - Permisos del Archivo

Permisos asignados: **usuario: rwx | grupo: r-x | otros: r--** (chmod 754)

```bash
# Asignar permisos
chmod 754 /unidad2/prueba2/nz/nz.txt

# Asignar propietario y grupo dueño
chown usuario1:prueba2-nz /unidad2/prueba2/nz/nz.txt

# Verificar
ls -lah /unidad2/prueba2/nz/nz.txt
# Salida esperada: -rwxr-xr-- 1 usuario1 prueba2-nz ... nz.txt
```

| Entidad | Permisos | Valor |
|---------|----------|-------|
| Usuario (dueño) | rwx - lectura + escritura + ejecución | 7 |
| Grupo | r-x - lectura + ejecución | 5 |
| Otros | r-- - solo lectura | 4 |

![Permisos asignados al archivo](imagenes/image4.png)

---

## Ejercicio 5 - Procesos con Mayor Uso de Recursos

```bash
top
```

El comando `top` muestra en tiempo real los procesos ordenados por consumo de CPU y memoria, permitiendo identificar cuáles están utilizando más recursos del sistema.

![Salida del comando top](imagenes/image5.png)

---

## Ejercicio 6 - Configuración de Firewalld (HTTP/HTTPS)

Se configuraron de forma permanente los puertos 80 (HTTP) y 443 (HTTPS) por TCP:

```bash
# Agregar puertos de forma permanente
firewall-cmd --permanent --add-port=80/tcp
firewall-cmd --permanent --add-port=443/tcp

# Aplicar cambios
firewall-cmd --reload

# Verificar estado
firewall-cmd --list-ports
```

![Estado de firewalld con puertos 80 y 443](imagenes/image6.png)
![Verificación de puertos activos](imagenes/image7.png)

---

## Ejercicio 7 - Configuración de Firewalld (FTP)

Se agregaron los puertos 20 y 21 (FTP) por TCP:

```bash
# Agregar puertos FTP de forma permanente
firewall-cmd --permanent --add-port=20/tcp
firewall-cmd --permanent --add-port=21/tcp

# Aplicar cambios
firewall-cmd --reload

# Verificar estado
firewall-cmd --list-ports
```

**Resultado:** firewalld quedó configurado únicamente con los puertos 80, 443, 20 y 21 por TCP.

![Firewalld con puertos FTP agregados](imagenes/image8.png)
![Estado final del firewall](imagenes/image9.png)

---

## Ejercicio 8 - Captura de Tráfico con Wireshark

Se navegó por un sitio web desde Kali Linux y se capturó el tráfico para identificar una trama específica.

```
Filtro aplicado:
frame contains "palabra_buscada"
```

**Pasos realizados:**
1. Abrir Wireshark en Kali Linux e iniciar captura en la interfaz activa
2. Navegar al sitio web seleccionado
3. Aplicar el filtro `frame contains` con la palabra del sitio
4. Identificar y seguir la trama HTTP capturada

![Página web seleccionada para la captura](imagenes/image10.png)
![Wireshark capturando tráfico](imagenes/image11.png)
![Filtro frame contains aplicado con la trama encontrada](imagenes/image12.png)
