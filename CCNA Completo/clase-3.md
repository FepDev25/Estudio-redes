# **Clase 3: Capa Física**

## 1. Función de la Capa Física
La **capa física** se encarga del **transporte de bits** a través del medio de transmisión. Recibe **tramas completas** desde la capa de **Enlace de Datos**, las **codifica como señales eléctricas, ópticas o de radio**, y las transmite.

- **Codificación de las tramas:** Convierte los bits en señales eléctricas, ópticas o de radiofrecuencia.
- **Generación de señales:** Las señales generadas deben ser enviadas por el medio de transmisión adecuado.

---

## 2. Estándares de la Capa Física
Existen diversas organizaciones que regulan los estándares de la capa física:

- **ISO** (International Organization for Standardization)
- **TIA/EIA** (Telecommunications Industry Association / Electronic Industries Alliance)
- **ITU** (International Telecommunication Union)
- **ANSI** (American National Standards Institute)
- **IEEE** (Institute of Electrical and Electronics Engineers)
- **Autoridades reguladoras nacionales:** FCC (EE.UU.) y ETSI (Europa)

---

## 3. Ancho de Banda
El **ancho de banda** es la capacidad de un medio de transmisión para transportar datos. En el ámbito digital, se mide en **bits por segundo (bps)** e indica la cantidad de datos que pueden fluir de un origen a un destino en un tiempo determinado.

**Tabla de unidades de medición del ancho de banda:**
| Unidad  | Abreviación | Equivalencia |
|---------|------------|-------------|
| Kilobits por segundo  | Kbps  | 1,000 bps |
| Megabits por segundo  | Mbps  | 1,000,000 bps |
| Gigabits por segundo  | Gbps  | 1,000,000,000 bps |

---

## 4. Cableado de Cobre
El **cableado de cobre** es el más común en redes hoy en día. En este tipo de cableado, los datos se transmiten como **impulsos eléctricos** a través de los alambres de cobre.

### 4.1. Cable UTP (Unshielded Twisted Pair)
El cable **UTP** es un tipo de cableado de cobre que consta de **4 pares de alambres trenzados y codificados por colores**. Cada par incluye:
- **Un conductor de color sólido.**
- **Un segundo conductor blanco con rayas del mismo color.**

**Colores de los pares en un cable UTP:**
- **Par 1:** Azul
- **Par 2:** Naranja
- **Par 3:** Verde
- **Par 4:** Marrón (Café)

Cuando los cables UTP se terminan con conectores **RJ45**, permiten conectar hosts a dispositivos intermedios como **switches**.

**Beneficio del trenzado:**  
El **trenzado de los alambres** protege contra la interferencia electromagnética y la **diafonía** (crosstalk).

---

## 5. Ruido e Interferencia en la Transmisión
El **ruido o interferencia** es cualquier señal eléctrica que **no sea la señal de datos** y que pueda afectar la integridad de la información.

### 5.1. Fuentes de ruido
- **Internas:** Generadas dentro del cableado.
- **Externas:** Generadas por dispositivos electrónicos cercanos.

### 5.2. Tipos de interferencia
- **EMI (Electromagnetic Interference):** Interferencia electromagnética generada por motores, líneas eléctricas, etc.
- **RFI (Radio Frequency Interference):** Interferencia por señales de radiofrecuencia, como transmisores de radio y microondas.
- **Diafonía (Crosstalk):** Interferencia entre cables adyacentes debido a la inducción electromagnética.

---

## 6. Clasificación de Cables UTP por IEEE
La **IEEE** clasifica los cables UTP según su rendimiento, es decir, su capacidad de transmitir diferentes anchos de banda.

**Tabla de clasificación de cables UTP:**
| Categoría | Ancho de Banda | Distancia Máxima |
|-----------|--------------|-----------------|
| Cat 5e   | 1Gbps      | 100 metros |
| Cat 6    | 1Gbps      | 100 metros |
| Cat 6A   | 10Gbps      | 100 metros |

---

## 7. Tipos de Cables de Red

### 7.1. Cable **Straight-Through** (Directo)
Los **hosts** (PCs, impresoras, etc.) **transmiten** datos a través de los **pines 1 y 2** y esperan **recibir datos** en los **pines 3 y 6**.  
Los **switches** de **capa 2** hacen lo opuesto.

En un **cable directo**, el **pin 1 de un extremo se conecta con el pin 1 del otro extremo**, el **pin 2 con el pin 2**, y así sucesivamente.

🔹 **Se usa para conectar:**  
- Un **host** a un **switch** o **router**.
- Un **switch** a un **router**.

---

### 7.2. Cable **Cross-Over** (Cruzado)
Los cables cruzados se usan para conectar **dos dispositivos similares**, como:
- **Switch de Capa 2 ↔ Switch de Capa 2**
- **Router ↔ Router**
- **PC ↔ PC**

Sin embargo, hoy en día estos cables **se están volviendo obsoletos** debido a la tecnología **Auto-MDIX**, que detecta automáticamente la conexión correcta.

---

## 8. Auto-MDIX
**Auto-MDIX** (Automatic Medium-Dependent Interface Crossover) es una función que permite que los dispositivos de red **detecten automáticamente** si necesitan usar un cable **directo o cruzado** y ajusten la conexión internamente.

🔹 **Ventaja:**  
Elimina la necesidad de elegir entre un **cable Straight-Through o Cross-Over**, facilitando la instalación y reduciendo errores de conexión.

---

## 📌 Resumen Rápido:
✅ La **capa física** se encarga de la transmisión de bits a través de señales eléctricas, ópticas o de radio.  
✅ Los **cables de cobre** más comunes son **UTP**, que contienen 4 pares de alambres trenzados para reducir la interferencia.  
✅ **Tipos de interferencia:** EMI, RFI y diafonía.  
✅ **Clasificación de cables:** IEEE define categorías como **Cat 5e, Cat 6 y Cat 6A** según el ancho de banda.  
✅ **Cables de red:**  
   - **Straight-Through** → Para conectar host a switch o router.  
   - **Cross-Over** → Para conectar dispositivos similares.  
✅ **Auto-MDIX** hace que los dispositivos ajusten automáticamente el tipo de conexión.  
