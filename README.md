# 🚀 PCB para Monitoreo de Señales Acelerométricas en Red de Control Sísmico  

## 📌 Introducción  
Este proyecto consiste en el diseño de una placa PCB (en su mayoría con componentes SMD) para la adquisición y transmisión de señales acelerométricas en tiempo real, destinada a redes de control sísmico. La placa integra un microcontrolador **ESP32** para procesamiento y comunicación inalámbrica, junto con componentes electrónicos y sensores optimizados para garantizar precisión en la medición de vibraciones.  

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
- `R1`: 8.2kΩ (Tipo: `SMD`, Componente: `2512`).
- `R2`: 100kΩ (Tipo: `SMD`, Componente: `2512`).
- `R3`: 8.2kΩ (Tipo: `SMD`, Componente: `2512`).
- `R4`: 220kΩ (Tipo: `Potenciómetro Modular`, Componente: `PV36P`).
- `R5`: 3.3kΩ (Tipo: `SMD`, Componente: `1206`).
- `R6`: 3.3kΩ (Tipo: `SMD`, Componente: `1206`).
- `R7`: 3.3kΩ (Tipo: `SMD`, Componente: `1206`).
- `R8`: 3.3kΩ (Tipo: `SMD`, Componente: `1206`).
- `R9`: 4.7kΩ (Tipo: `SMD`, Componente: `1206`).
- `R10`: 4.7kΩ (Tipo: `SMD`, Componente: `1206`).
- `R11`: 4.7kΩ (Tipo: `SMD`, Componente: `1206`).
- `R12`: 4.7kΩ (Tipo: `SMD`, Componente: `1206`).
- `R13`: 200Ω (Tipo: `SMD`, Componente: `1206`).
- `R14`: 5.11kΩ (Tipo: `SMD`, Componente: `1206`).
- `R15`: 5.11kΩ (Tipo: `SMD`, Componente: `1206`).
- `R16`: 4.7kΩ (Tipo: `SMD`, Componente: `1206`).
- `R17`: 4.7kΩ (Tipo: `SMD`, Componente: `2512`).
- `R18`: 10kΩ (Tipo: `SMD`, Componente: `1206`).
- `R19`: 10kΩ (Tipo: `SMD`, Componente: `1206`).

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
- `C13`: 100nF (Tipo: `SMD`, Componente: `0603`, Código: `104`).
- `C14`: 1µF (Tipo: `SMD`, Componente: `0603`, Código: `105`).
- `C15`: 100nF (Tipo: `SMD`, Componente: `0603`, Código: `104`).
- `C16`: 100nF (Tipo: `SMD`, Componente: `0603`, Código: `104`).
- `C17`: 10µF (Tipo: `SMD`, Componente: `1206`, Código: `106`).
- `C18`: 100nF (Tipo: `SMD`, Componente: `0603`, Código: `104`).
- `C19`: 100nF (Tipo: `SMD`, Componente: `0603`, Código: `104`).

#### Inductores  
- `L1`: 2uH (Tipo: `SMD`, Componente: `0805`).

#### Diodos  
- `D1`: Diodo Schottky `1N5819` (Código: `SS1H10-E3/61T`).  
- `D2`: Diodo LED `1N5819` (Código: `SS1H10-E3/61T`).  
- `D3`: Diodo Schottky `1N5819` (Código: `SS1H10-E3/61T`).  
- `D4`: Diodo Schottky `1N5819` (Código: `SS1H10-E3/61T`).  
- `D5`: Diodo Schottky `1N5819` (Código: `SS1H10-E3/61T`).  
- `D6`: Diodo Schottky `1N5819` (Código: `SS1H10-E3/61T`).  
- `D7`: Diodo LED `1N5819` (Código: `SS1H10-E3/61T`).  

### 🔋 Conector de Fuente de Alimentación (+12V)  
- Conector XH 2 posiciones.  

### 📊 Test Points para Depuración  
- Pin Header 1x1:
  
- Pin Header 1x2:
  
- Pin Header 1x3:
  
- Pin Header 1x4:

---

## 🖼️ Imágenes del Diseño  
### Vista 3D de la PCB  
![Vista 3D de la PCB](/images/pcb_3d_view.png)  

### Esquemático  
![Esquemático](/images/schematic_diagram.png)  

---

## 📥 Descarga de Archivos Gerber  
Los archivos Gerber para fabricación están disponibles en la carpeta [`/gerber_files`](/gerber_files) de este repositorio. Incluyen:  
- `PCB_TOP.gbr` (Capa superior).  
- `PCB_BOTTOM.gbr` (Capa inferior).  
- `PCB_DRILL.txt` (Archivo de taladros).  

---

## 🛠️ Características y Sustento del Diseño  
### ✔️ Características Clave  
- **Bajo ruido**: Diseño optimizado para minimizar interferencias en señales analógicas.  
- **Comunicación inalámbrica**: Integración de Wi-Fi/Bluetooth mediante ESP32.  
- **Robustez**: Protección contra sobretensiones y filtrado de señales.  

### 📐 Criterios de Diseño  
- **Layout**: Separación de señales analógicas/digitales para reducir acoplamiento.  
- **Material**: PCB de 2 capas con FR4 de 1.6mm.  
- **Conectores**: Headers estándar para facilitar prototipado.  

---

## 🎯 Conclusiones y Recomendaciones  
### ✅ Conclusiones  
- La placa cumple con los requisitos de precisión y escalabilidad para redes sísmicas.  
- El uso del ESP32 reduce costos y simplifica la integración con sistemas IoT.  

### ⚠️ Precauciones  
- **Montaje**: Verificar polaridad de componentes sensibles (ej. capacitores electrolíticos).  
- **Fabricación**: Asegurar que el fabricante cumpla con tolerancias de impedancia si se requiere.  

### 🔮 Recomendaciones  
- Realizar pruebas de vibración mecánica en el prototipo.  
- Considerar encapsulado para ambientes hostiles.  

---

## 📜 Licencia  
Este proyecto está bajo licencia **MIT**. Para más detalles, consulta el archivo [LICENSE](/LICENSE).  
