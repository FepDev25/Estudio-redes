# **Clase 2: Stack TCP/IP y Modelo OSI**

## **1. Introducción al Stack TCP/IP**
El **stack TCP/IP** es el conjunto de protocolos más utilizado en las redes de datos modernas, siendo la base del funcionamiento de Internet. Fue desarrollado por el **Departamento de Defensa de los EE.UU.** y es mantenido por la **IETF (Internet Engineering Task Force)**.  

Se basa en **4 capas**, cada una con funciones específicas en la transmisión de datos:

### **Capas del Modelo TCP/IP**
1. **Aplicación**  
   - Define protocolos de comunicación entre aplicaciones.  
   - Ejemplos: HTTP, FTP, DNS, SMTP.  

2. **Transporte**  
   - Controla el flujo de datos entre dispositivos y garantiza la integridad de la comunicación.  
   - Protocolos: TCP (confiable, orientado a conexión), UDP (rápido, sin conexión).  

3. **Internet**  
   - Se encarga del **enrutamiento** y la **identificación de dispositivos** en la red.  
   - Protocolos: IP (direccionamiento), ICMP (diagnóstico de red), ARP (resolución de direcciones).  

4. **Acceso a la Red**  
   - Define la forma en que los datos se envían físicamente en la red.  
   - Protocolos: Ethernet, Wi-Fi, PPP.  

---

## **2. Modelo de Referencia**
El **modelo de referencia** es una abstracción que describe cómo los datos viajan a través de la red, permitiendo estandarizar la comunicación entre diferentes dispositivos y fabricantes.

### **2.1. Modelo de Referencia OSI**
El **modelo OSI (Open Systems Interconnection)** fue desarrollado por la **ISO** como una guía teórica que divide la comunicación en **7 capas**:

| Capa | Función |
|------|---------|
| **7. Aplicación** | Interacción con las aplicaciones y el usuario final. |
| **6. Presentación** | Formatea y cifra los datos para garantizar compatibilidad. |
| **5. Sesión** | Administra las conexiones entre aplicaciones. |
| **4. Transporte** | Controla el flujo de datos y la confiabilidad. |
| **3. Red** | Enrutamiento de datos entre diferentes redes. |
| **2. Enlace de Datos** | Transmite tramas entre dispositivos en la misma red. |
| **1. Física** | Envía bits a través del medio de transmisión. |

---

### **2.2. Comparación entre TCP/IP y OSI**
El **modelo TCP/IP** es una implementación práctica del modelo OSI, pero con solo **4 capas** en lugar de 7. Se agrupan algunas funciones:

| Modelo OSI | Modelo TCP/IP |
|------------|--------------|
| Aplicación, Presentación y Sesión | Aplicación |
| Transporte | Transporte |
| Red | Internet |
| Enlace de Datos y Física | Acceso a la Red |

📌 **Diferencias clave:**  
- **El modelo OSI es teórico**, mientras que **TCP/IP se usa en redes reales**.  
- **TCP/IP combina capas**, mientras que OSI las separa en más detalles.  

---

## **3. Modelo Híbrido de 5 Capas**
Para facilitar el aprendizaje y aplicar modelos en redes reales, se utiliza un **modelo híbrido de 5 capas**, basado en TCP/IP pero con una división más clara:

1. **Aplicación** → Protocolos que permiten la comunicación entre aplicaciones.  
2. **Transporte** → Segmentación, control de flujo y fiabilidad de la transmisión.  
3. **Red** → Enrutamiento y direccionamiento de datos a través de múltiples redes.  
4. **Enlace de Datos** → Control de acceso al medio y transmisión de tramas.  
5. **Física** → Transmisión de bits a través de cables o señales inalámbricas.  

Este modelo se usa comúnmente en la **enseñanza y certificaciones como CCNA**.

---

## **4. Segmentación y Encapsulación**
### **4.1. ¿Qué es la Segmentación?**
La **segmentación** es el proceso de dividir los datos en **unidades más pequeñas**, llamadas **PDU (Protocol Data Unit)**, para su transmisión eficiente a través de la red.  

Esto permite que los datos se transporten de manera segura y lleguen en el orden correcto.

### **4.2. Proceso de Encapsulación**
Cada capa del modelo añade su propio encabezado a los datos antes de enviarlos a la siguiente capa. Este proceso se llama **encapsulación**:

| Capa | PDU (Unidad de Datos) | Función |
|------|----------------|----------|
| **Aplicación** | Datos | Información generada por el usuario. |
| **Transporte** | Segmento (TCP) / Datagrama (UDP) | Control del flujo de datos. |
| **Red** | Paquete | Dirección lógica de origen y destino. |
| **Enlace de Datos** | Trama | Dirección física (MAC) y control de errores. |
| **Física** | Bits | Transmisión eléctrica u óptica. |

Ejemplo:  
🔹 Un correo electrónico enviado por una aplicación pasa por **todas las capas**, agregando información en cada una antes de ser transmitido por la red.

---

## **5. Des-encapsulación**
Cuando los datos llegan al destino, cada capa **remueve su encabezado** antes de entregarlos a la siguiente capa superior. Este proceso se llama **des-encapsulación**.

📌 **Ejemplo:**  
- Un **router** usa la capa de **Red** para leer direcciones IP y decidir el siguiente salto.  
- Un **switch** usa la capa de **Enlace de Datos** para leer direcciones MAC y reenviar tramas dentro de una red local.  
- Un **dispositivo final (PC, servidor, móvil)** recibe los datos y los interpreta en la **capa de Aplicación**.  

---

## **6. Resumen General**
- **El modelo TCP/IP** es el más utilizado y consta de **4 capas**.  
- **El modelo OSI** es una referencia teórica con **7 capas** para entender el funcionamiento de las redes.  
- **El modelo híbrido de 5 capas** se usa para simplificar el aprendizaje.  
- **La segmentación y encapsulación** permiten la transmisión eficiente de datos en una red.  
- **La des-encapsulación** permite que los datos sean interpretados correctamente en el destino.  
