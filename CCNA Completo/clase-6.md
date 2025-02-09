# **Clase 6: Switches de Capa 2**

## **1. Introducción a los Switches de Capa 2**
Los **switches de capa 2** operan en la **capa de enlace de datos** del modelo OSI y utilizan las **direcciones MAC** para tomar decisiones de reenvío de tramas dentro de una red local (LAN).

📌 **Características principales:**
- Operan en **capa 2 (Enlace de Datos)**.
- Usan **direcciones MAC** para tomar decisiones de transmisión.
- No analizan ni modifican el contenido de la **carga útil** de las tramas.
- Construyen y actualizan dinámicamente una **tabla de direcciones MAC**.

---

## **2. Tramas Ethernet (IEEE 802.3)**
Los **PDU (Protocol Data Units)** en la capa 2 se llaman **tramas**.

### **2.1. Estructura de una Trama Ethernet**
| Campo | Tamaño | Descripción |
|--------|--------|-------------|
| **Preambulo** | 7 bytes | Señal de sincronización antes del inicio de la trama. |
| **SFD (Start Frame Delimiter)** | 1 byte | Indica el inicio de la trama. |
| **MAC Destino** | 6 bytes | Dirección MAC del destinatario. |
| **MAC Origen** | 6 bytes | Dirección MAC del remitente. |
| **Tipo** | 2 bytes | Define el protocolo de la capa superior (Ej: IPv4, IPv6). |
| **Datos o Carga útil** | 46 - 1500 bytes | Contenido de la transmisión. |
| **CheckSum (FCS - Frame Check Sequence)** | 4 bytes | Detección de errores. |

📌 **Tamaño de una Trama Ethernet**  
- **Mínimo**: 64 bytes.  
- **Máximo**: 1518 bytes.  

---

## **3. Funcionamiento del Switch Ethernet de Capa 2**
Un switch Ethernet de capa 2 **no analiza el contenido de la carga útil de las tramas**, solo utiliza la **dirección MAC** para tomar decisiones de reenvío.

### **3.1. Tabla de Direcciones MAC**
El switch construye dinámicamente una **tabla de direcciones MAC**, que asocia direcciones MAC con puertos específicos.

🔹 **Proceso de aprendizaje de direcciones MAC:**
1. Examina la **dirección MAC de origen** de cada trama que ingresa por un puerto.
2. Si la dirección **no está en la tabla**, la agrega junto con el número de puerto.
3. Si la dirección **ya existe**, simplemente **actualiza el temporizador**.
4. Por defecto, la mayoría de los switches almacenan una entrada en la **tabla MAC por un máximo de 5 minutos**.

### **3.2. Tipos de Tráfico según la Dirección MAC**
#### **Unicast**
- La trama está destinada a un único dispositivo.
- Si la dirección MAC de destino está en la **tabla MAC**, el switch la envía solo por el puerto correspondiente.
- Si **no está en la tabla**, se produce un **unicast desconocido**, y el switch **inunda** la trama por todos los puertos excepto el de origen.

#### **Broadcast**
- Dirección MAC de destino: **FFFF:FFFF:FFFF**.
- La trama se envía a **todos los dispositivos** conectados al switch, excepto al puerto de origen.

📌 **El tráfico de broadcast debe minimizarse en redes grandes, ya que puede generar congestión.**

---

## **4. Configuración de Velocidad y Dúplex**
En los switches de capa 2, es crítico que **la velocidad y el modo dúplex sean los mismos** en ambos extremos de una conexión.

### **4.1. Autonegociación**
Permite que dos dispositivos conectados negocien automáticamente la mejor configuración de:
- **Velocidad** (10 Mbps, 100 Mbps, 1 Gbps, etc.).
- **Modo dúplex** (**Half-Duplex** o **Full-Duplex**).

### **4.2. Problema: Duplex Mismatch**
Ocurre cuando un dispositivo está configurado en **Full-Duplex** y el otro en **Half-Duplex**, lo que genera:
- **Pérdida de paquetes**.
- **Reducción del rendimiento**.
- **Colisiones** en la red.

🔹 **Solución:** Configurar manualmente la velocidad y el dúplex si la autonegociación no funciona correctamente.

---

## **5. Switches Cisco Catalyst**
Los switches Cisco Catalyst han sido una de las soluciones más utilizadas en redes empresariales.

📌 **Familias de switches:**
1. **Cisco Catalyst 2960X / 2960XR**  
   - Durante años fueron los switches de acceso estándar para conectar equipos terminales.
   - Compatibles con **VLANs, QoS, STP, y PoE**.

2. **Cisco Catalyst 9200 / 9200L** (Reemplazo actual)  
   - **Mayor rendimiento** y soporte para **redes SD-Access**.
   - **Mejor eficiencia energética** y **seguridad mejorada**.
   - **Compatible con Cisco DNA Center** para automatización y gestión centralizada.

---

## **6. Resumen General**
- Los **switches de capa 2** operan en la **capa de enlace de datos** y usan **direcciones MAC** para reenviar tramas.
- La **estructura de la trama Ethernet** incluye direcciones MAC, tipo de protocolo y detección de errores.
- Los switches aprenden direcciones MAC **de manera dinámica** y almacenan la información en una **tabla MAC**.
- La **autonegociación** evita errores de configuración, pero puede fallar si los dispositivos no la soportan bien.
- Cisco ha evolucionado sus switches desde la serie **2960X** a la más avanzada **9200/9200L**.

---

