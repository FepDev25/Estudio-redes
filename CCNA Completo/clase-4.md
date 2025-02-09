# **Clase 4: Capa Física II**

## **1. Introducción a la Fibra Óptica**
La **fibra óptica** es un medio de transmisión que utiliza **pulsos de luz** para transportar datos a largas distancias con una **alta velocidad** y **baja pérdida de señal**.  
Se ha convertido en el estándar para **redes de alta velocidad y larga distancia**, reemplazando progresivamente al cableado de cobre en muchas aplicaciones.

### **Ventajas de la Fibra Óptica**
- **Mayor ancho de banda**: Soporta velocidades superiores a los cables de cobre.
- **Transmisión a largas distancias**: Puede alcanzar cientos de kilómetros sin repetidores.
- **Menor atenuación**: La señal pierde menos intensidad en comparación con otros medios.
- **Inmunidad a interferencias electromagnéticas (EMI)**: No se ve afectada por ondas de radio o ruido eléctrico.

---

## **2. Estructura de la Fibra Óptica**
Un cable de fibra óptica consta de varias capas que protegen y facilitan la transmisión de luz.

### **Componentes Principales:**
1. **Núcleo (Core)**
   - Es el **medio de transmisión** donde viajan los pulsos de luz.
   - Fabricado de **vidrio** o **plástico** de alta pureza.
   - Su tamaño afecta el tipo de fibra óptica y la velocidad de transmisión.

2. **Revestimiento (Cladding)**
   - Rodea el núcleo y tiene un **índice de refracción menor**.
   - Su función es **mantener la luz dentro del núcleo** mediante **reflexión interna total**.

3. **Cubierta Protectora (Buffer o Coating)**
   - Capa externa que protege la fibra contra daños físicos.

4. **Revestimiento Exterior (Jacket)**
   - Capa adicional de refuerzo, resistente a la humedad y químicos.

---

## **3. Tipos de Fibra Óptica**
Existen dos tipos principales de fibra óptica, diferenciados por el diámetro de su núcleo y su método de transmisión de luz.

### **3.1. Fibra Multimodo (MMF)**
- Permite que **múltiples rayos de luz** viajen simultáneamente en el núcleo.
- Se usa principalmente en **distancias cortas** (hasta 550 metros).
- Común en redes LAN y centros de datos.
- Se clasifica en:
  - **Índice Escalonado**: Densidad del núcleo constante.
  - **Índice Gradual**: Densidad del núcleo decrece desde el centro, reduciendo la dispersión.

#### **Categorías de Fibra Multimodo según TIA/EIA**
| Categoría | Diámetro del Núcleo | Aplicación | Emisor |
|-----------|--------------------|------------|--------|
| OM1 | 62.5 µm | Redes locales (LAN) | LED |
| OM2 | 50 µm | Redes locales (LAN) | LED |
| OM3 | 50 µm | Redes de alta velocidad (10G) | Láser VCSEL |
| OM4 | 50 µm | Redes de muy alta velocidad (40G/100G) | Láser VCSEL |

---

### **3.2. Fibra Monomodo (SMF)**
- Tiene un núcleo **mucho más delgado** (≈ 9 µm).
- Solo permite un **haz de luz altamente enfocado**.
- Se usa en **telecomunicaciones y redes de larga distancia** (hasta cientos de km).
- Transmite datos a **velocidades muy altas** con **baja dispersión**.

---

## **4. Conectores de Fibra Óptica**
Para conectar dispositivos a la fibra óptica, se utilizan distintos tipos de conectores.

| Conector | Descripción |
|----------|------------|
| **ST (Straight Tip)** | Conector de bayoneta, usado en redes antiguas. |
| **SC (Subscriber Connector)** | Conector cuadrado de empuje y tracción, muy común en telecomunicaciones. |
| **LC (Lucent Connector)** | Conector compacto de alta densidad, usado en centros de datos. |

---

## **5. Patch Cord de Fibra Óptica**
Un **patch cord** de fibra óptica es un **cable corto con conectores en ambos extremos**.  
Se usa para conectar dispositivos en redes de fibra, como switches y routers con puertos ópticos.

### **Tipos de Patch Cord según el Tipo de Fibra**
- **Monomodo (SMF)**: Cable amarillo con conectores azules.
- **Multimodo (MMF)**: Cable naranja o aqua con conectores beige o verdes.

---

## **6. Uso de Fibra Óptica en Switches Ethernet**
Los switches Ethernet pueden utilizar fibra óptica mediante **módulos de expansión**:

1. **SFP (Small Form-Factor Pluggable)**  
   - Permite conectar transceptores ópticos intercambiables en switches y routers.
   - Compatible con fibras multimodo y monomodo.

2. **SFP+ (Small Form-Factor Pluggable Plus)**  
   - Versión mejorada de **SFP** con soporte para **10G y más**.

3. **QSFP (Quad Small Form-Factor Pluggable)**  
   - Utilizado para conexiones de **40G y 100G** en redes de alto rendimiento.

---

### **Conclusión**
La fibra óptica es el medio de transmisión más avanzado, proporcionando **alta velocidad**, **larga distancia** y **baja interferencia** en redes modernas. Su implementación es clave en **redes empresariales, telecomunicaciones y centros de datos**.
