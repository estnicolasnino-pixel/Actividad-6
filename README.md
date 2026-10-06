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

### 2. Instalación de Dependencias de Python
Abre la terminal o consola de comandos en la carpeta de tu proyecto y ejecuta el siguiente comando para instalar las librerías necesarias:

```bash
pip install pybullet pyserial
