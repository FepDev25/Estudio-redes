# **Clase 5: Capa de Enlace de Datos**

## 1. Función de la Capa de Enlace de Datos
La **capa de enlace de datos** prepara los datos para ser transportados por el medio físico y es responsable de la **comunicación de equipo a equipo** en una red.

### Funciones principales:
- Aceptar paquetes de la **capa 3 (Red)** y **encapsularlos** en tramas de la **capa 2**.
- Controlar cómo los datos son **colocados y recibidos** en el medio de transmisión.
- Intercambiar **tramas** entre equipos terminales.
- **Detectar errores** y rechazar tramas dañadas.

---

## 2. Estándares de la Capa 2
Los estándares que regulan la capa de enlace de datos son:

- **ITU** (Unión Internacional de Telecomunicaciones)
- **ANSI** (Instituto Nacional Estadounidense de Estándares)
- **ISO** (Organización Internacional de Normalización)
- **IEEE** (Instituto de Ingenieros Eléctricos y Electrónicos)

---

## 3. Tipos de Redes

Las redes pueden clasificarse según diferentes criterios, como el **tamaño y cobertura geográfica**.

### 3.1. LAN (Red de Área Local)
- Red que cubre un **espacio geográfico limitado**.
- Los equipos y medios de transmisión **son de propiedad privada**.
- Conecta los **hosts** de una misma empresa u organización.
- Puede abarcar una **oficina, un edificio o varios edificios en un campus**.

### 3.2. WAN (Red de Área Extensa)
- Red con un **mayor alcance geográfico**, pudiendo cubrir **ciudades o países**.
- Creada y mantenida por **empresas de telecomunicaciones**, que alquilan estos servicios a otras empresas.

---

## 4. Estándares IEEE en la Capa 2

En **1985**, **IEEE inició el proyecto 802** con el objetivo de generar **estándares** que permitieran la comunicación entre equipos de diferentes fabricantes.

- **Ethernet**: Familia de tecnologías de redes definida en los estándares **802.2 y 802.3**.
- Los estándares abarcan **la capa física y la capa de enlace de datos** en el **modelo híbrido** de redes.

---

## 5. Acceso al Medio

### 5.1. Acceso al Medio Legacy (Antiguo)
- Las primeras generaciones de **Ethernet** usaban una **tecnología de bus** o un concentrador llamado **hub**.
- Ofrecía un medio de transmisión **compartido** y operaba en **modo half-duplex**.

#### **Half-Duplex**
- Solo un dispositivo podía **enviar o recibir** información a la vez.
- Se requería un método de **contención** para evitar colisiones.

#### **CSMA/CD (Carrier Sense Multiple Access with Collision Detection)**
- Método de contención que permitía que **múltiples dispositivos** compartieran el medio de transmisión **half-duplex**.
- **Detectaba colisiones** y definía un algoritmo para la retransmisión.

---

### 5.2. Acceso al Medio en Redes Actuales
- Utilizan **switches de capa 2**, lo que permite operar en **modo full-duplex**.

#### **Full-Duplex**
- Múltiples dispositivos pueden **transmitir y recibir** simultáneamente en un medio de transmisión **dedicado**.
- **CSMA/CD ya no es necesario** en redes con switches de capa 2.

---

## 6. Direcciones MAC

Las **direcciones MAC** identifican el **origen y destino físico** en un **segmento local de red**.

### Características:
- Se usan en la **capa de enlace de datos** del modelo OSI (**capa 2** del modelo híbrido).
- Son **únicas para cada dispositivo** en una red.
- Consisten en **48 bits binarios**.
- Se representan en **hexadecimal** (cada dígito hexadecimal representa **4 bits binarios**).

### **Formatos de Direcciones MAC**:
Ejemplos de representación:

- **AAAA:BBBB:CCCC**
- **AAAA.BBBB.CCCC**
- **AA:AA:BB:BB:CC:CC**

