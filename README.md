# Energy Consumption Monitoring with PZEM-016 and ESP32

## Descripción (Spanish)

Este proyecto tiene como objetivo medir el consumo energético de un dispositivo conectado a través de un sensor **PZEM-016** y enviar los datos a **ThingSpeak** para su monitoreo. El código está diseñado para funcionar con un **ESP32** que se conecta a una red Wi-Fi y transmite los valores de voltaje y corriente del sensor a la plataforma ThingSpeak.

**Características del Proyecto:**

- **Medición de voltaje y corriente**: Utiliza el sensor PZEM-016 para medir el voltaje (V) y la corriente (A) de un dispositivo.
- **Conexión Wi-Fi**: El ESP32 se conecta a una red Wi-Fi utilizando las credenciales configuradas.
- **Envío de datos a ThingSpeak**: Los datos de consumo energético se suben a ThingSpeak cada 10 segundos para su visualización y análisis.

## Project Description (English)

This project aims to measure the energy consumption of a connected device using the **PZEM-016** sensor and send the data to **ThingSpeak** for monitoring. The code is designed to work with an **ESP32** that connects to a Wi-Fi network and transmits the voltage and current readings from the sensor to the ThingSpeak platform.

**Project Features:**

- **Voltage and Current Measurement**: Uses the PZEM-016 sensor to measure voltage (V) and current (A) of a device.
- **Wi-Fi Connectivity**: The ESP32 connects to a Wi-Fi network using the configured credentials.
- **Data Upload to ThingSpeak**: Energy consumption data is uploaded to ThingSpeak every 10 seconds for visualization and analysis.

## Funcionalidad del Código (Code Functionality)

### 1. Conexión Wi-Fi (Wi-Fi Connection)

- **Esp32**: El ESP32 se conecta a la red Wi-Fi utilizando las credenciales configuradas en el código (SSID y contraseña).
- **ThingSpeak**: Una vez conectado a la red, el ESP32 también se conecta a ThingSpeak para poder enviar los datos.

### 2. Lectura de Datos (Data Reading)

- El sensor **PZEM-016** mide dos parámetros: **voltaje (V)** y **corriente (A)**.
- Los datos se leen utilizando el protocolo de comunicación **Modbus RTU** a través de la interfaz **Serial2** del ESP32.
  
### 3. Envío de Datos (Data Upload)

- Los datos de voltaje y corriente se envían a **ThingSpeak** utilizando la API de ThingSpeak cada 10 segundos.
- Estos datos se almacenan en los campos 1 y 2 del canal de ThingSpeak, respectivamente.

### 4. Monitoreo Continuo (Continuous Monitoring)

- El sistema lee y envía los datos de forma continua cada 10 segundos, lo que permite el monitoreo en tiempo real del consumo energético.

## Instalación (Installation)

1. **Clonar el repositorio**:

   ```bash
   git clone https://github.com/Daviddaza2310/EnergyMonitoringProject.git
