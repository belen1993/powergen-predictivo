### DATOS CSV

#### **1. Históricos de Órdenes de Trabajo (`Historicos_Ordenes.csv`)**
Este archivo contiene los registros históricos de mantenimiento de los equipos en la planta.

- **ID_Orden:** Identificador único para cada orden de trabajo. Ejemplo: OT000001.
- **ID_Equipo:** Identificador único del equipo asociado a la orden. Ejemplo: E001.
- **Fecha:** Fecha en que se realizó la orden de trabajo.
- **Tipo_Mantenimiento:** Tipo de mantenimiento realizado, que puede ser:
  - **Correctivo:** Reparación de un fallo inesperado.
  - **Preventivo:** Mantenimiento programado para prevenir fallos.
- **Tiempo_Reparacion_Horas:** Tiempo, en horas, dedicado a completar la orden de trabajo.
- **Costo_Mantenimiento:** Costo en moneda local asociado al mantenimiento realizado.
- **Ubicacion:** Planta energética donde se realizó el mantenimiento. Posibles valores:
  - Planta Norte
  - Planta Sur
  - Planta Este
  - Planta Oeste

#### **2. Características de los Equipos (`Caracteristicas_Equipos.csv`)**
Este archivo describe las especificaciones técnicas de cada equipo en la planta.

- **ID_Equipo:** Identificador único del equipo. Ejemplo: E001.
- **Tipo_Equipo:** Categoría del equipo, como:
  - Turbina
  - Generador
  - Bomba
  - Transformador
- **Fabricante:** Nombre del fabricante del equipo. Ejemplo: Fabricante A.
- **Fecha_Instalacion:** Fecha en que el equipo fue instalado en la planta.
- **Vida_Util_Anios:** Vida útil esperada del equipo en años.
- **Potencia_kW:** Potencia nominal del equipo en kilovatios.

#### **3. Registros de Condiciones Operativas (`Registros_Condiciones.csv`)**
Este archivo registra las condiciones operativas de los equipos en intervalos de tiempo.

- **ID_Equipo:** Identificador único del equipo. Ejemplo: E001.
- **Fecha:** Fecha de registro de las condiciones operativas.
- **Horas_Operativas:** Número de horas que el equipo operó en el día del registro.
- **Temperatura_C:** Temperatura operativa del equipo, medida en grados Celsius.
- **Vibracion_mm_s:** Nivel de vibración del equipo, medido en milímetros por segundo.
- **Presion_Bar:** Presión operativa del equipo, medida en bares.
- **Horas_Acumuladas:** Total acumulado de horas operativas para el equipo desde su instalación, calculado como la suma acumulativa de las horas operativas registradas.

