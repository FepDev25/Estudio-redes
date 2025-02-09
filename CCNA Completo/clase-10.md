# **Clase 10: Configuración Básica de un Switch I**

## **1. Sistemas Operativos en Dispositivos de Red**
Los **dispositivos terminales** (PCs, servidores) y los **dispositivos intermedios** (switches, routers) deben tener un **sistema operativo** para funcionar correctamente.

### **1.1. Componentes del Sistema Operativo**
- **Kernel**: Es la parte del sistema operativo que interactúa directamente con el **hardware**.
- **Shell**: Es la interfaz del sistema operativo que permite al usuario **interactuar con el sistema**.
  - Puede ser mediante **CLI (Command Line Interface)**.
  - O mediante **GUI (Graphical User Interface)**.

---

## **2. Sistemas Operativos de Cisco**
Cisco utiliza diferentes versiones de **sistemas operativos** para sus dispositivos de red:

| Sistema Operativo | Descripción |
|------------------|-------------|
| **IOS** | Ha sido utilizado durante muchos años en routers y switches de Cisco. |
| **IOS-XE** | Versión moderna que ha reemplazado al IOS tradicional. |
| **IOS-XR** | Diseñado para **proveedores de servicios** y redes de alto rendimiento. |
| **NX-OS** | Optimizado para **equipos de Data Center**. |

---

## **3. Acceso a la CLI de un Switch**
El usuario interactúa con el sistema operativo del switch a través de la **CLI (Command Line Interface)**, digitando comandos en una terminal.

### **3.1. Métodos de Acceso a la CLI**
📌 **Localmente a través del puerto de consola.**  
📌 **Remotamente mediante protocolos como Telnet o SSH.**  

---

## **4. Puerto de Consola en un Switch**
El **puerto de consola** fue diseñado específicamente para permitir el acceso al **CLI** de un switch o router sin depender de la red.

### **4.1. Métodos de Conexión al Puerto de Consola**
| Método | Conexión entre PC y Switch |
|--------|-----------------------------|
| **Clásico** | PC con puerto **DB-9**, Switch con **RJ-45** para consola. |
| **Moderno** | PC con **USB**, Switch con **USB** para consola. |
| **Híbrido** | PC con **USB**, Switch con **RJ-45** para consola. |

---

## **5. Explicación del Puerto COM y Herramientas para la CLI**
### **5.1. ¿Qué es un Puerto COM?**
- Los **puertos COM** (o **puertos seriales**) se usan para acceder al CLI de switches y routers.
- Antes se usaban **adaptadores DB-9 a RJ-45**, ahora se usan **USB a RJ-45**.

### **5.2. Herramientas para Acceder a la CLI**
Para conectarse al puerto de consola, se necesitan programas de emulación de terminal como:

| Herramienta | Descripción |
|------------|-------------|
| **PuTTY** | Software gratuito para SSH, Telnet y conexión serial. |
| **Tera Term** | Alternativa a PuTTY con más opciones gráficas. |
| **SecureCRT** | Software profesional con soporte para múltiples sesiones. |

📌 **Ejemplo de conexión con PuTTY:**
1. Conectar el cable **USB-RJ45** o **DB9-RJ45** entre la PC y el switch.
2. Abrir **PuTTY** y seleccionar **Serial** como método de conexión.
3. Ingresar el **Puerto COM** detectado (Ej: `COM3` o `COM4`).
4. Configurar la velocidad en **9600 baudios**.
5. Hacer clic en **Open** para acceder a la CLI del switch.

---

## **6. Resumen**
- Todos los **dispositivos de red** tienen un **sistema operativo** (IOS, IOS-XE, NX-OS, etc.).
- Se puede acceder a la **CLI** de un switch **localmente** (puerto de consola) o **remotamente** (Telnet/SSH).
- Existen **diferentes métodos de conexión** al puerto de consola (clásico, moderno e híbrido).
- Se utilizan **puertos COM** y herramientas como **PuTTY** para la configuración inicial.

---
