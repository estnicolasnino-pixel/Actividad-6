# Actividad primera parte-6
# Sistema de Dibujo 3D con Brazo Robótico (ESP32 + PyBullet)

Este proyecto implementa un sistema de control para un brazo robótico simulado en 3D dentro del entorno **PyBullet**, controlado mediante comandos enviados vía comunicación serial UART desde una placa **ESP32** conectada a un **teclado matricial 4x4** y una **pantalla LCD I2C**.

## Requisitos del Hardware
- ESP32 NodeMCU
- Teclado matricial 4x4 (Pines Filas: 32, 33, 25, 26 | Pines Columnas: 27, 14, 12, 13)
- Pantalla LCD 16x2 I2C (SDA: GPIO 21, SCL: GPIO 22)
- Cable USB a Micro-USB/USB-C para comunicación Serial

## Requisitos del Software
- Python 3.8+
- Arduino IDE (con soporte para ESP32)
- Librerías de Python: `pybullet`, `pyserial`

##  Instalación y Uso

### 1. Configuración de Archivos y Carpetas
1. Crea una carpeta principal en tu equipo con el nombre `brazo-robotico-pybullet-esp32`.
2. Dentro de esa carpeta, asegúrate de tener colocados juntos los siguientes archivos del proyecto:
   - `control_dibujo.py` (Script principal de Python)
   - `brazo.urdf` (Modelo 3D del brazo robótico)
   - `firmware_teclado_lcd.ino` (Código fuente para la ESP32)

## 2. Instalación de Dependencias de Python
Abre la terminal o consola de comandos en la carpeta de tu proyecto y ejecuta el siguiente comando para instalar las librerías necesarias:

```bash
pip install pybullet pyserial
# Sistema Distribución de Visión Artificial y Renderizado en ESP32 + OLED


##Actividad segunda  parte-6
Este proyecto implementa un sistema distribuido de procesamiento de imágenes y transmisión de mapas de bits en tiempo real desde una PC hacia un nodo esclavo microcontrolado.

## Arquitectura del Sistema
* **Nodo A (Maestro Virtual - PC):** Captura el flujo de video vía OpenCV, aplica binarización y empaqueta la matriz de bits mediante un protocolo de trama `[0xAA, BitmapData, 0xFF]`.
* **Nodo B (Esclavo Físico - ESP32):** Recibe la trama por el puerto serie UART (115200 baudios), parsea la cabecera/pie de control y renderiza la imagen en una pantalla OLED de 0.96" (SSD1306) vía I2C.

##  Requisitos e Instalación

### 1. Python (Nodo A)
Instalar las dependencias requeridas:
```bash
pip install -r requirements.txt
```

### 2. ESP32 (Nodo B)
Librerías requeridas en Arduino IDE:
* `Adafruit SSD1306`
* `Adafruit GFX Library`

##  Ejecución

1. Cargar el firmware `firmware/esp32_esclavo/esp32_esclavo.ino` en la ESP32.
2. Ajustar el puerto COM en el script de Python.
3. Ejecutar la transmisión de dibujos:
   ```bash
   python python/transmitir_dibujo.py
   ```
4. Presionar `ESPACIO` frente a la cámara para transmitir el marco binarizado a la OLED.
