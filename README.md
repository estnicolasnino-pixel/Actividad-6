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

1. **Clonar el repositorio:**
   ```bash
   git clone [https://github.com/TU_USUARIO/brazo-robotico-pybullet-esp32.git](https://github.com/TU_USUARIO/brazo-robotico-pybullet-esp32.git)
   cd brazo-robotico-pybullet-esp32
