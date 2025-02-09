# **Clase 1: Curso CCNA - Introducción a Redes**

## 1. Cisco: Empresa Líder en Equipos de Redes
Cisco es uno de los principales fabricantes de equipos de redes de datos. Su tecnología es ampliamente utilizada en infraestructuras de redes empresariales y de telecomunicaciones. Cisco proporciona una variedad de soluciones, desde equipos físicos hasta software de gestión de redes y seguridad.

## 2. CCNA: Certificación de Técnico en Redes
La certificación **Cisco Certified Network Associate (CCNA)** acredita conocimientos y habilidades en la configuración, operación y solución de problemas en redes de datos. Es una de las certificaciones más reconocidas en la industria de redes y es ideal para aquellos que buscan una carrera en redes, telecomunicaciones y seguridad.

---

## 3. Componentes de una Red

### 3.1. Host o Equipos Terminales
Son computadoras o dispositivos conectados a la red que participan en la comunicación. Se dividen en:

- **Clientes**: Ejecutan software que les permite solicitar y mostrar información de los servidores.  
  - Ejemplo: Computadoras de usuario, teléfonos inteligentes, laptops.
  
- **Servidores**: Ejecutan software que permite proveer información y servicios como correo electrónico, páginas web, archivos, entre otros.
  - Ejemplo: Servidores web, bases de datos, servidores de archivos.

### 3.2. Dispositivos Intermedios
Conectan dispositivos terminales a la red, proporcionando conectividad y garantizando que los datos viajen correctamente. Utilizan las direcciones de los dispositivos terminales para guiar el tráfico de la información.

Ejemplos de dispositivos intermedios:
- **Switch de Capa 2**: Funciona en la capa de enlace de datos, encaminando tramas dentro de una red local (LAN). No realiza enrutamiento entre redes, solo conecta dispositivos dentro de la misma red.
  
- **Switch Multicapa**: Opera en varias capas del modelo OSI, combinando funciones de switch y router. Puede realizar enrutamiento entre VLANs (Redes Locales Virtuales).
  
- **Router**: Dispositivo que enruta paquetes entre diferentes redes, dirigiendo el tráfico de datos desde la red de origen hasta la de destino.
  
- **Router Inalámbrico**: Similar a un router tradicional, pero permite la conectividad inalámbrica. Utiliza Wi-Fi para la transmisión de datos.

- **Firewall**: Dispositivo o software que controla el tráfico de entrada y salida de una red, filtrando paquetes para proteger la red de accesos no autorizados.

### 3.3. Medios de Transmisión
Es el canal por el cual los datos viajan desde el origen hasta el destino. Existen tres tipos principales:

- **Cableado de cobre**: Transmite datos mediante impulsos eléctricos. Son comunes los cables **UTP (Unshielded Twisted Pair)**, utilizados en redes Ethernet.
  - **Ventajas**: Costo bajo, fácil instalación.
  - **Desventajas**: Mayor interferencia, menor alcance y velocidad comparado con la fibra óptica.

- **Fibra óptica**: Utiliza pulsos de luz para la transmisión de datos, ofreciendo mayor velocidad y distancia. Existen dos tipos: **monomodo** (para largas distancias) y **multimodo** (para distancias más cortas).
  - **Ventajas**: Alta velocidad, menos interferencia, mayor alcance.
  - **Desventajas**: Costo elevado, más compleja de instalar.

- **Inalámbrico**: Transmite datos mediante la modulación de ondas electromagnéticas a través del espacio. Las tecnologías más comunes incluyen Wi-Fi, LTE, 5G.
  - **Ventajas**: Movilidad, fácil de implementar.
  - **Desventajas**: Menor seguridad, interferencia por obstáculos o distancias largas.

---

## 4. Diagramas de Topología
Son representaciones visuales de la red, mostrando la interconexión entre dispositivos.

- **Diagrama físico**: Representa la disposición real de los dispositivos y conexiones. Es útil para la instalación física y mantenimiento de la infraestructura.
  
- **Diagrama lógico**: Muestra la estructura de la red en términos de direccionamiento y comunicación, sin considerar el hardware físico. Este tipo de diagrama es importante para planificar cómo fluirán los datos a través de la red.

- **Topologías comunes**:
  - **Topología en estrella**: Todos los dispositivos están conectados a un dispositivo central (como un switch). Es la más común en redes LAN.
  - **Topología en anillo**: Los dispositivos están conectados en un círculo, y los datos viajan en una sola dirección.
  - **Topología en bus**: Todos los dispositivos están conectados a un cable central. Es menos común hoy en día.
  - **Topología malla**: Cada dispositivo está conectado a todos los demás dispositivos, proporcionando redundancia.

## 5. Métodos de Comunicación

### 5.1. Origen o Emisor
Es el dispositivo electrónico que necesita enviar un mensaje a otro. Puede ser cualquier equipo conectado a la red que requiere transmitir información, como una computadora, un teléfono móvil o una cámara IP.

### 5.2. Canal
El canal es el medio de transmisión que sirve de camino para que el mensaje viaje desde el origen hasta el destino. Dependiendo de la tecnología de la red, el canal puede ser cableado (fibra óptica, cable de cobre) o inalámbrico (Wi-Fi, 5G, Bluetooth).

### 5.3. Destino
Es el dispositivo electrónico que recibe el mensaje y lo interpreta. El destino puede ser cualquier dispositivo que esté esperando recibir y procesar los datos enviados, como otro servidor, cliente o dispositivo conectado a la red.

---

## 6. Protocolos

Los **protocolos** son un conjunto de reglas que permiten establecer la comunicación entre dispositivos en una red. Estos protocolos definen:

- Cómo se identifica el origen y el destino.
- Los detalles de la transmisión de los mensajes, como el formato de los datos, la dirección de origen y destino, y el proceso de error y corrección.

### 6.1. Funciones de los Protocolos
Los protocolos permiten que los dispositivos conectados a la red se comuniquen de manera efectiva y segura, incluso si tienen diferentes configuraciones de hardware o software.

---

## 7. Stack de Protocolos

Un **stack de protocolos** es un conjunto de protocolos que trabajan juntos para proveer servicios de comunicación sobre la red de datos. Estos protocolos pueden estar definidos por organizaciones, como la **ISO (International Organization for Standardization)** o los fabricantes de equipos.

### 7.1. Implementación de un Stack de Protocolos
El **stack de protocolos** muestra cómo los protocolos individuales son implementados e interactúan entre ellos, generalmente organizados en capas. Cada capa se encarga de un aspecto específico de la comunicación, y las capas superiores dependen de las funciones ofrecidas por las capas inferiores.

Un ejemplo común de un stack de protocolos es el **modelo OSI** (Open Systems Interconnection), que define siete capas:

1. **Capa de Aplicación**: Interacción con aplicaciones de software.
2. **Capa de Presentación**: Formato y codificación de los datos.
3. **Capa de Sesión**: Controla la comunicación entre dispositivos.
4. **Capa de Transporte**: Controla el flujo de datos y asegura la entrega correcta.
5. **Capa de Red**: Determina la ruta de los datos a través de la red.
6. **Capa de Enlace de Datos**: Establece la conexión física y organiza los datos en tramas.
7. **Capa Física**: Define la transmisión de señales a través del medio físico.
