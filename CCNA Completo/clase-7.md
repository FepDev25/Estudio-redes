# **Clase 7: Capa de Red**

## **1. Introducción a la Capa de Red**
En una red **LAN con switches de capa 2**, los dispositivos solo pueden **transportar tramas** dentro del mismo segmento de red. La **capa de red (capa 3)** permite la comunicación entre dispositivos que **no están localmente conectados**, facilitando la transferencia de datos entre **múltiples redes**.

📌 **Funciones clave de la capa de red:**
- Permite el **intercambio de datos** entre redes diferentes.
- Usa **protocolos de enrutamiento** para encontrar la mejor ruta.
- **Encapsula y des-encapsula paquetes** para su transmisión.

---

## **2. Routers: Dispositivos de Capa 3**
Los **routers** son dispositivos de **capa 3** que **interconectan diferentes redes** y permiten la comunicación entre ellas.

### **Funciones de un Router**
Para lograr la comunicación **extremo a extremo** entre diferentes redes, los protocolos de la capa de red realizan tres funciones principales:

1. **Encapsulación**  
   - Reciben la **PDU de la capa 4 (Transporte)** y la encapsulan en **paquetes de capa 3**.  
   - Agregan un **encabezado** con información como la **dirección IP de origen y destino**.  
   - Luego, el paquete es **entregado a la capa 2** para su transmisión.

2. **Enrutamiento**  
   - Determina la **mejor ruta** para enviar los paquetes desde el **origen hasta el destino** en otra red.  
   - Los routers usan **tablas de enrutamiento** para elegir el mejor camino.  

3. **Des-encapsulación**  
   - Cuando el **paquete llega al host destino**, el **encabezado de capa 3 es removido**.  
   - El **PDU resultante** se entrega a la **capa 4 (Transporte)**.  

---

## **3. Protocolo IP**
El **Protocolo de Internet (IP)** es el principal protocolo de la **capa de red** y se encarga de:
- **Definir el formato de los paquetes IP**.
- **Estructurar y gestionar direcciones IP**.
- **Realizar el enrutamiento** desde el origen al destino a través de múltiples redes.

📌 Actualmente, utilizamos **IPv4** de manera predominante, mientras que **IPv6** se usa en redes de **proveedores de servicios** y en infraestructuras modernas.

---

## **4. Protocolos Auxiliares en la Capa de Red**
Además del protocolo IP, existen otros **protocolos auxiliares** que facilitan el funcionamiento de la capa de red:

| Protocolo | Función |
|-----------|---------|
| **ICMP (Internet Control Message Protocol)** | Diagnostica problemas en el enrutamiento. Se usa en herramientas como `ping` y `traceroute`. |
| **DHCP (Dynamic Host Configuration Protocol)** | Asigna direcciones IP automáticamente a los dispositivos en una red. |
| **ARP (Address Resolution Protocol)** | Descubre las direcciones de capa 2 (MAC) de los dispositivos de la red. Permite que un host encuentre la dirección MAC de otro dispositivo en la misma LAN. |

---

## **5. Paquetes IPv4**
Los **paquetes IPv4** consisten en **dos partes**:
1. **Encabezado**: Contiene información sobre el paquete y su enrutamiento.
2. **Carga útil (Payload)**: Contiene los datos transmitidos.

### **Estructura del Encabezado IPv4**
El encabezado de un paquete IPv4 incluye varios **campos clave**:

| Campo | Tamaño | Función |
|--------|--------|---------|
| **Versión** | 4 bits | Especifica la versión del protocolo (IPv4 o IPv6). |
| **Longitud del encabezado (IHL)** | 4 bits | Indica el tamaño del encabezado. |
| **Tipo de Servicio (ToS)** | 8 bits | Prioridad del paquete (QoS). |
| **Longitud Total** | 16 bits | Tamaño total del paquete (encabezado + datos). |
| **Identificación** | 16 bits | Identifica fragmentos de un paquete. |
| **Flags** | 3 bits | Indican si el paquete puede ser fragmentado. |
| **Tiempo de Vida (TTL)** | 8 bits | Número de saltos permitidos antes de ser descartado. |
| **Protocolo** | 8 bits | Especifica el protocolo de la capa de transporte (TCP, UDP, etc.). |
| **Checksum del encabezado** | 16 bits | Verifica la integridad del encabezado. |
| **Dirección IP de Origen** | 32 bits | Dirección del dispositivo que envía el paquete. |
| **Dirección IP de Destino** | 32 bits | Dirección del dispositivo que recibe el paquete. |

---

## **6. Direccionamiento IPv4**
Las **direcciones IPv4** se utilizan para identificar dispositivos en una red. Están formadas por **32 bits binarios**.

📌 **Ejemplo de dirección IPv4 en binario y decimal:**
```plaintext
11000000 10101000 00001010 00000001  →  192.168.10.1
```

