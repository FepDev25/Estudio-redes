# **Clase 8: Configuración de IPv4 en Windows**

## **1. Configuración de IPv4 en Windows**
En Windows, la configuración de **IPv4** se puede realizar de dos maneras:

### **1.1. Configuración Manual**
El usuario debe ingresar manualmente la información de la dirección IP y otros parámetros de red.

📌 **Parámetros necesarios:**
- **Dirección IP**: Identificación única del host en la red.
- **Máscara de subred**: Determina qué parte de la IP corresponde a la red y cuál al host.
- **Puerta de enlace predeterminada (Gateway)**: Dirección IP del router que conecta a otras redes.
- **Servidor DNS**: Direcciones IP de los servidores que resuelven nombres de dominio.

📌 **Pasos para configurar IPv4 manualmente en Windows:**
1. Abrir el **Panel de Control** → **Centro de redes y recursos compartidos**.
2. Hacer clic en **Cambiar configuración del adaptador**.
3. Seleccionar el adaptador de red y abrir **Propiedades**.
4. Seleccionar **Protocolo de Internet versión 4 (TCP/IPv4)** → **Propiedades**.
5. Ingresar manualmente la dirección IP, máscara de subred, gateway y servidores DNS.
6. Guardar los cambios y cerrar.

---

### **1.2. Configuración Automática mediante DHCP**
En lugar de asignar manualmente la dirección IP, se puede configurar el dispositivo para que obtenga automáticamente una dirección de un **servidor DHCP (Dynamic Host Configuration Protocol)**.

📌 **Ventajas del DHCP:**
- **Evita conflictos de direcciones IP** dentro de la red.
- **Asigna automáticamente** direcciones a los dispositivos sin intervención manual.
- Permite una **gestión centralizada** de direcciones en redes grandes.

📌 **Pasos para configurar DHCP en Windows:**
1. Seguir los **pasos 1-4** de la configuración manual.
2. Seleccionar **Obtener una dirección IP automáticamente**.
3. Seleccionar **Obtener la dirección del servidor DNS automáticamente**.
4. Guardar los cambios y cerrar.

---

## **2. Verificación de la Configuración de IPv4 en Windows**
Windows proporciona herramientas para verificar la configuración de IPv4.

### **2.1. Comando `ipconfig`**
El comando **ipconfig** muestra la configuración de red del sistema.

📌 **Ejemplo de uso en la terminal (CMD):**
```bash
ipconfig

Adaptador de Ethernet:

   Dirección IPv4. . . . . . . . . . . . . . . . . . : 192.168.1.10
   Máscara de subred . . . . . . . . . . . . . . . . : 255.255.255.0
   Puerta de enlace predeterminada . . . . . . . . . : 192.168.1.1
```


### **2.2. Información adicional con ipconfig /all**
El comando ipconfig /all muestra información detallada sobre la configuración de red.
```bash
ipconfig /all
```

📌 **Información adicional que proporciona:**
- Dirección MAC del adaptador de red.
- Estado del DHCP (activado o desactivado).
- Servidores DNS configurados.
- Duración de la concesión de la IP si se usa DHCP.

---

## **3. Prueba de Conectividad IPv4**
Para comprobar si un host tiene conectividad con otro dispositivo en la red o en Internet, se usa el comando **ping**.

### **3.1. Comando `ping`**
El comando **ping** envía paquetes de **echo ICMP** a un dispositivo remoto y espera una respuesta.

📌 **Ejemplo de uso:**
```bash
ping 192.168.1.1

Haciendo ping a 192.168.1.1 con 32 bytes de datos:
Respuesta desde 192.168.1.1: bytes=32 tiempo<1ms TTL=64
```
📌 **Salida si no hay conexión:**
```bash
ping 192.168.1.1

Haciendo ping a 192.168.1.1 con 32 bytes de datos:
Tiempo de espera agotado para esta solicitud.
```
Si el ping falla, puede deberse a:
- Problemas de conectividad en la red.
- El dispositivo de destino está apagado o con firewall bloqueando ICMP.
- Errores en la configuración de IP o gateway.

## **4. ARP: Resolución de Direcciones MAC**
En redes **Ethernet**, para que un paquete **unicast** pueda ser transmitido, debe contener una **dirección IPv4 de destino** en su encabezado. Sin embargo, la trama Ethernet que lo transporta **requiere una dirección MAC de destino**.

📌 **¿Cómo se obtiene la dirección MAC de destino?**  
Se usa el protocolo **ARP (Address Resolution Protocol)** para descubrir la dirección MAC asociada a una dirección IP.

### **4.1. Tabla ARP (Cache ARP)**
Cada host mantiene una **tabla ARP** donde almacena las **direcciones IP y MAC** de los dispositivos con los que ha interactuado recientemente.

📌 **Para ver la caché ARP en Windows:**
```bash
arp -a
Interfaz: 192.168.1.10 --- 0x3
  Dirección IP         Dirección MAC          Tipo
  192.168.1.1         00-1a-2b-3c-4d-5e       dinámica
  192.168.1.20        00-1b-2c-3d-4e-5f       dinámica
```
📌 **Tipos de entradas en la tabla ARP:**
- Estática: Configurada manualmente y no cambia hasta que se elimina.
- Dinámica: Aprendida automáticamente y expira después de un tiempo si no se usa.

## **5. Resumen General**
- **IPv4 en Windows** se puede configurar **manualmente** o **automáticamente mediante DHCP**.
- Se puede **verificar la configuración** con `ipconfig` y obtener información detallada con `ipconfig /all`.
- La **conectividad se prueba con `ping`**, que envía paquetes ICMP al destino.
- **ARP** permite obtener la **dirección MAC** de un dispositivo a partir de su **dirección IP**.
- La **tabla ARP (`arp -a`)** almacena direcciones **IP y MAC** de dispositivos conocidos.
