# 🚀 PCB para Monitoreo de Señales Acelerométricas en Red de Control Sísmico  

## 📌 Introducción  
Este proyecto consiste en el diseño de una placa PCB (en su mayoría con componentes SMD) para la adquisición y transmisión de señales acelerométricas, destinada a redes de control sísmico. La placa integra un microcontrolador **ESP32** para procesamiento y comunicación inalámbrica, junto con componentes electrónicos y sensores optimizados para garantizar precisión en la medición de vibraciones. Los dispositivos utilizados usan comunicación SPI, I2C y UART. Estos tres protocolos son ampliamente utilizados en electrónica para la transferencia de datos entre dispositivos como microcontroladores, sensores, memorias, etc.

Las conexiones necesarias para la comunicación SPI (Serial Peripheral Interface) son: SCLK (Reloj), MOSI (Master Out Slave In), MISO (Master In Slave Out), SS/CS (Selección de esclavo).
Las conexiones necesarias para la comunicación I2C (Inter-Integrated Circuit) son: SCL (Reloj) y SDA (Datos).
Las conexiones necesarias para la comunicación UART (Universal Asynchronous Receiver-Transmitter) son: TX (Transmisión) y RX (Recepción).

En este proyecto el módulo GPS usa comunicación UART, el acelerómetro ADXL355Z usa comunicación SPI, el módulo RTC-DS3231 usa comunicación I2C, la tarjeta µSD usa comunicación SPI. La comunicación del ESP32-WROOM-32 con la entrada USB-C usa el protocolo UART. En cuanto a la alimentación del sistema, todos los dispositivos implementados se alimentan con un voltaje de +3.3V, este valor se consigue a partir de un Buck-Converter de +12V a +5V y un regulador de voltaje LD33V con salida de +3.3V.

Este proyecto se basa en la electrónica (Hardware) necesaria para que el sistema de monitoreo sísmico funcione, todo el software que usa este proyecto se encuentra en el repositorio [RSA Sensor](https://github.com/JorgeZh-hub/RSA_sensor)

---

## 🔍 Componentes Utilizados  
A continuación se detallan los componentes clave del diseño:  

### 🎛️ Microcontrolador  
- **ESP32-WROOM-32** (Modelo: `ESP32-WROOM-32E`, Tipo: `SMD`).  

### 📊 Sensores, Módulos y Reloj
- **Acelerómetro** (Modelo: `ADXL355Z` o equivalente, Tipo: `Modular`).
- **GPS** (Modelo: `GPS-FPGMMOPA6H` o equivalente, Tipo: `Modular`).
- **RTC** (Modelo: `DS3231` o equivalente, Tipo: `SMD SOIC-16`).  

### 🔧 Circuitos Integrados (ICs)  
- **MP2307** (Tipo: `SMD SOIC8N (EXPOSED PAD)` o equivalente). 
- **LD33V** (Tipo: `SMD SOT-223` o equivalente). 
- **CH340G** (Tipo: `SMD SOP-16` o equivalente). 
- **74LVC125A** (Tipo: `SMD TSSOP−14` o equivalente). 

### 🔌 Componentes Pasivos  
#### Resistencias  
- `R1`: 8.2kΩ (Tipo: `SMD`, Componente SMD: `2512`).
- `R2`: 100kΩ (Tipo: `SMD`, Componente SMD: `2512`).
- `R3`: 8.2kΩ (Tipo: `SMD`, Componente SMD: `2512`).
- `R4`: 220kΩ (Tipo: `Potenciómetro Modular`, Componente: `PV36P`).
- `R5`: 3.3kΩ (Tipo: `SMD`, Componente SMD: `1206`).
- `R6`: 3.3kΩ (Tipo: `SMD`, Componente SMD: `1206`).
- `R7`: 3.3kΩ (Tipo: `SMD`, Componente SMD: `1206`).
- `R8`: 3.3kΩ (Tipo: `SMD`, Componente SMD: `1206`).
- `R9`: 4.7kΩ (Tipo: `SMD`, Componente SMD: `1206`).
- `R10`: 4.7kΩ (Tipo: `SMD`, Componente SMD: `1206`).
- `R11`: 4.7kΩ (Tipo: `SMD`, Componente SMD: `1206`).
- `R12`: 4.7kΩ (Tipo: `SMD`, Componente SMD: `1206`).
- `R13`: 200Ω (Tipo: `SMD`, Componente SMD: `1206`).
- `R14`: 5.11kΩ (Tipo: `SMD`, Componente SMD: `1206`).
- `R15`: 5.11kΩ (Tipo: `SMD`, Componente SMD: `1206`).
- `R16`: 4.7kΩ (Tipo: `SMD`, Componente SMD: `1206`).
- `R17`: 4.7kΩ (Tipo: `SMD`, Componente SMD: `2512`).
- `R18`: 10kΩ (Tipo: `SMD`, Componente SMD: `1206`).
- `R19`: 10kΩ (Tipo: `SMD`, Componente SMD: `1206`).

#### Capacitores  
- `C1`: 100nF (Tipo: `Cerámico Modular 2.54mm`, Código: `104`).
- `C2`: 10µF (Tipo: `Electrolítico Modular 5mm`).
- `C3`: 10µF (Tipo: `Electrolítico Modular 5mm`).
- `C4`: 200nF (Tipo: `Cerámico Modular 2.54mm`, Código: `204`).
- `C5`: 100µF (Tipo: `Electrolítico Modular 5mm`).
- `C6`: 100µF (Tipo: `Electrolítico Modular 5mm`).
- `C7`: 100nF (Tipo: `Cerámico Modular 2.54mm`, Código: `104`).
- `C8`: 12µF (Tipo: `Electrolítico Modular 5mm`).
- `C9`: 100nF (Tipo: `Cerámico Modular 2.54mm`, Código: `104`).
- `C10`: 4.7nF (Tipo: `Cerámico Modular 2.54mm`, Código: `402`).
- `C11`: 10nF (Tipo: `Cerámico Modular 2.54mm`, Código: `103`).
- `C12`: 12µF (Tipo: `Electrolítico Modular 5mm`).
- `C13`: 100nF (Tipo: `SMD`, Componente SMD: `0603`, Código: `104`).
- `C14`: 1µF (Tipo: `SMD`, Componente SMD: `0603`, Código: `105`).
- `C15`: 100nF (Tipo: `SMD`, Componente SMD: `0603`, Código: `104`).
- `C16`: 100nF (Tipo: `SMD`, Componente SMD: `0603`, Código: `104`).
- `C17`: 10µF (Tipo: `SMD`, Componente SMD: `1206`, Código: `106`).
- `C18`: 100nF (Tipo: `SMD`, Componente SMD: `0603`, Código: `104`).
- `C19`: 100nF (Tipo: `SMD`, Componente SMD: `0603`, Código: `104`).

#### Inductores  
- `L1`: 2uH (Tipo: `SMD`, Componente: `0805`).

#### Diodos  
- `D1`: Diodo `1N4148` (Encapsulado: `SMA/DO-214AC`, Código SMD: `US1M`).  
- `D2`: Diodo LED (Código SMD: `1206`).  
- `D3`: Diodo `1N4148` (Encapsulado: `SMA/DO-214AC`, Código SMD: `US1M`).  
- `D4`: Diodo `1N4148` (Encapsulado: `SMA/DO-214AC`, Código SMD: `US1M`).  
- `D5`: Diodo `1N4001` (Encapsulado: `SMA/DO-214AC`, Código SMD: `S1M`).  
- `D6`: Diodo `1N4001` (Encapsulado: `SMA/DO-214AC`, Código SMD: `S1M`).  
- `D7`: Diodo LED (Código SMD: `1206`).  

### 🔋 Conector de Fuente de Alimentación (+12V)  
- Conector XH 2 posiciones.  

### 📊 Test Points para Depuración  
- Pin Header 1x4 (Conectado al ADXL355Z): `IO15/IO13/IO12/IO14`
- Pin Header 1x5 (Conectado a 74LVC125A(Tarjeta SD), DS3231, CH340G(USB C), CH340G, DS3231): `MOSI/SCL/TXD0/RXD0/SDA`
- Pin Header 1x5 (Conectado a 74LVC125A(Tarjeta SD), 74LVC125A, 74LVC125A, GPS, GPS): `MISO/SCK/CS/RXGPS/TXGPS`

---

## 🖼️ Imágenes del Diseño  

### Esquemático  
![Esquemático](/images_schematic)  

### Circuito Impreso  
![PCB](/images_pcb_layers)  

### Vista 3D de la PCB  
![Vista 3D de la PCB](/images_pcb_3d_view)  

---

## 📥 Descarga de Archivos Gerber, ODB, Drill y BOM
Los archivos para fabricación están disponibles en la carpeta [`/PCB_SMD`](/PCB_SMD) de este repositorio. Los archivos Gerber se pueden visualizar en el archivo PDF ![Gerber images](/Gerber_images.pdf).

---

## 🛠️ Características y Sustento del Diseño 
Este proyecto se ha realizado con el objetivo de optimizar el prototipo modular expuesto en el repositorio [Modular-PCB-Design-for-Seismic-Monitoring](https://github.com/Christian-Loja/Modular-PCB-Design-for-Seismic-Monitoring) del sistema de monitoreo sísmico, para esto se han utilizado componentes de montaje superficial para mejorar la eficiencia y reducir tamaño. Adicionalmente, se han implementado zonas de cobre y planos de masa para minimizar el ruido e interferencias y mejorar la disipación térmica. Se han colocado varios puntos de prueba (test points) para depuración a partir de peinetas (Pin Headers macho) en donde se pueden conectar jumpers o sondas de osciloscopio para observar las señales provenientes del módulo GPS, módulo RTC, acelerómetro, tarjeta micro SD y puerto USB C que se dirigen al ESP32.
En la etapa de alimentación (Buck-Converter) se han colocado resistores con código SMD `2512` (mayor tamaño) para segurar que soporten valores de potencia de hasta `0.5 watts`, así mismo, los capacitores utilizados son electrolíticos y cerámicos modulares para mejorar la disipación de potencia y también debido a que los valores de capacitancia y voltaje requeridos son dificiles de conseguir en una versión SMD (capacitores de tantalio). El inductor utilizado también se ha dimensionado para asegurar una operación en un rango seguro, por esa razón su encapsulado `0805` es ligeramente más grande que los demás componentes SMD. Los demás componentes pasivos, es decir los que operan con la alimentación de 3.3V, son de dimensiones más pequeñas (codigos SMD `0603` y `1206`) debido a que manejan corrientes y voltajes más pequeños. 

### ✔️ Características Clave  
- **Reducción de tamaño**: Optimización del espacio en la placa al reemplazar los módulos ESP32DEV-KIT, Buck-Converter MH-Mini360, Lector µSD y RTC-DS3231 por una versión SMD dieñada para cada módulo. Para lograr estos reemplazos fue necesario aplicar ingeniería inversa a los modulos. La implementación de las versiones SMD también proporciona mayor resistencia al movimiento y vibraciones a comparación con sus versiones modulares. 
- **Bajo ruido**: Para minimizar interferencias en las señales se ha colocado un plano de tierra en ambas caras del diseño, de modo que se cortocircuite cualquier señal no deseada que incida sobre la placa. Estos planos de tierra también mejoran la disipación térmica de los componentes, por ende, se reduce el ruido térmico.  
- **Comunicación inalámbrica**: Para mantener las funciones de conectividad Wifi del ESP32 se implementó el modelo ESP32-WROOM-32E cuyo encapsulado cuenta con una antena externa para la comunicación.  
- **Robustez y eficiencia energética**: Para asegurar la integridad de los componentes presentes en la placa se ha configurado una serie de diodos rectificadores que dirigen el flujo de corriente de cualquiera de las fuentes (+12V o USB-C) hacia un regulador de voltaje que proporcionará los 3.3V necesarios en el proyecto. La fuente de alimentación principal se ha implementado mediante un Buck-Converter debido a que permite manejar corrientes considerables manteniendo una generación de calor baja y, principalemte, debido a la alta eficiencia energética que este tipo de fuentes proporciona (aprox 85%).

### 📐 Criterios de Diseño  
- **Grosor de líneas de alimentación**: Para una corriente de `1A` se recomienda `1mm` de ancho de pista, por lo tanto, dependiendo de la ubicación de la pista se usarán grosores dentro del rango `0.5–1mm` ya que las corrientes que circulan por la placa están por debajo de 1A.  
- **Grosor de líneas de transmisión**: Para comunicación SPI se recomiendan grosores de pista dentro del rango `0.2–0.3mm`. Para comunicación I2C se recomienda el rango `0.15–0.25mm`. Para comunicación UART se recomienda el rango `0.15–0.25mm`. Para mantener lineas de un solo grosor se usará `0.2032mm` para SPI, I2C y UART.
- **Diseño de doble cara**: Para facilitar la alimentación y conexión entre componentes se ha diseñado una placa de doble cara. La cara superior contiene todos los componentes y la mayoria de conexiones entre ellos, la cara inferior se usa para transportar señales de comunicación SPI, I2C o UART que no puedan enrutarse en la capa superior. El diseño de doble cara permite tener un plano de tierra que cubra gran parte de ambas caras con esto se logra reducir significativamente las interferencias.
- **Separación entre líneas de transmisión**: Para evitar acoplamientos e interferencias en las señales de SPI y UART se recomienda una distancia entre pistas de almenos 3 veces el ancho de la pista. De forma similar para las señales de I2C se recomienda una separación de almenos 2 veces el ancho de pista. Estos parámetros fueron tomados en cuenta en todos los enrutamientos de la placa.

---

## 🎯 Conclusiones y Recomendaciones  
### ✅ Verificación de errores eléctricos (ERC) y Verificación de reglas de diseño (DRC).
- La validación de reglas de diseño y de errores eléctricos realizada por el software Fusion 360 se muestra en una tabla que lista los errores encontrados. En este caso la validación de ERC y DRC muestran cero errores, estos resultados se muestran en las carpetas ![Esquemático](/images_schematic) y ![PCB](/images_pcb_layers) respectivamente.

### 🔍 Conclusiones  
- La placa ha sido diseñada en el Software Fusion 360 de AutoDesk. Esta plataforma facilita el desarrollo y diseño de circuitos gracias a la gran variedad de componentes recopilados en sus librerías. Sin embargo, durante la realización de este proyecto no se encontraron librerías que contengan sensores como el acelerómetro ADXL355Z, el módulo GPS-FPGMMOPA6H, ESP32-WROOM-32, IC MP2307, IC LD33V, IC CH340G, Micro-SD Holder, IC 74LVC125A y el IC DS3231. Por lo tanto, estos componentes tuvieron que ser diseñados por completo (esquemático, footprint y modelo 3D) en la misma plataforma Fusion 360. Varios paquetes de software de AutoDesk (incluido Fusion 360) son dirigidos hacia la comunidad científica y de investigación, por ende cuentan con licencias sin costo para estudiantes o miembros de universidades. Estas son opciones excelentes y completas para diseño electrónico, PCB, radiofrecuencia, mecánica y muchas otras áreas de ingeniería.
- Para facilitar el ensamblaje del diseño se utilizaron componentes comunes en el mercado. Para los capacitores del circuito de alimentación se implementaron versiones modulares debido a que su disipación de potencia es mayor que en el resto del circuito, además, algunos de sus valores de capacitancia (10µF, 100µF) pueden ser dificiles de encontrar en versiones SMD.
- Los planos de tierra son una parte muy importante para mejorar la disipación térmica y reducir las interferencias, por esta razón ambas caras del PCB están cubiertas casi en su totalidad por este plano. Si bien los planos de cobre (zonas de cobre aisladas de cualquier señal y diferentes al plano de tierra) también ayudan a la disipación térmica, en este caso no se han implementado debido a que podrían ser fuente de interferencia para las señales I2C, SPI y UART. Los planos de tierra cubren casi por completo los puntos vacios del PCB por lo que la implementación de planos de cobre no es necesaria.
- Este diseño cuenta con una entrada USB-C que permite alimentar el circuito entero y programar el ESP32. Se ha escogido esta versión de USB para mantener un proyecto moderno con conexiones estandarizadas ampliamente utlizadas.

### ⚠️ Precauciones  
- **Montaje**: Verificar polaridad de componentes sensibles (ej. entrada de 12 voltios y capacitores electrolíticos), se recomienda observar los modelos 3D y footprints durante el ensamblaje del circuito para mayor seguridad.  
- **Adquisición de componentes**: Asegurar que los componentes por comprar tengan un codigo SMD correspondiente a cada elemento listado en este repositorio, caso contrario, no será posible soldarlos en la placa por la diferencia de dimensiones.  

### 🔮 Recomendaciones  
- Añadir una etapa de protección de sobretensiones y picos de corriente para evitar daños en el hardware y pérdidas de información.  
- Considerar encapsulado/blindaje para ambientes hostiles.
- Añadir un circuito para alimentación de respaldo para todo el sistema. Actualmente solo el RTC DS3231 cuenta con una bateria que mantiene activo el reloj durante periodos de desconexión eléctrica.

---

## 📜 Licencia  
Este proyecto está bajo licencia **MIT**. Para más detalles, consulta el archivo [LICENSE](/LICENSE).  
