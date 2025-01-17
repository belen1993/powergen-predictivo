### Reto: **"Construyendo las bases del mantenimiento predictivo"**

#### **Objetivo General**  
En esta etapa se quiere crear una solución en Azure ML Studio para cargar y procesar datos de mantenimiento de equipos y registros de operación. El objetivo es extraer métricas iniciales, como frecuencia de mantenimiento y duración promedio de vida útil de los equipos, para comenzar a entender los datos. Asimismo, generar nuevos datos derivados de los existentes para enriquecerlos.

Para ello, PowerGen nos ha provisto de 3 fuentes de datos para obtener la información que necesitamos: *Historicos de Ordenes de Trabajo*, *Caracteristicas de los Equipos*, y *Registros de Condiciones*.

Nuestra misión es trabajar en equipo para generar un conjunto de datos enriquecido, listo para la siguiente fase.


#### **Tareas del Reto:**
1. **Carga de datos:**
   - Importar los datasets `Historicos_Ordenes.csv`, `Caracteristicas_Equipos.csv`, y `Registros_Condiciones.csv` usando Python (en memoria).
   - Crear nueva base de datos "data_powergen":
      - Crear tabla de base de datos para datos de mantenimiento (Historicos_Ordenes). Cargar los datos Historicos_Ordenes en la tabla correspondiente.
      - Crear tabla de base de datos para generar información combinada (Resultados_join).

2. **Filtrado y agrupamiento:**
   - Contar el número total de órdenes de mantenimiento realizadas para cada equipo (`ID_Equipo`).
   - Calcular la duración promedio de vida útil de los equipos en el dataset `Caracteristicas_Equipos.csv`.
   - Filtrar las órdenes de trabajo para identificar las de tipo "Correctivo" y calcular el costo promedio de estas.

3. **Resúmenes básicos:**
   - Encontrar el equipo con el mayor número de fallos (mantenimiento correctivo).
   - Generar un resumen básico de las temperaturas promedio y máximas registradas para cada equipo.

4. **Consultas básicas:**
   - Listar todas las órdenes de mantenimiento correctivo para un equipo específico, junto con sus costos y tiempos de reparación.
   - Extraer los registros operativos para los días en los que la vibración superó los 3.0 mm/s y la temperatura fue mayor a 60 °C.

5. **Agregaciones y métricas:**
   - Calcular el tiempo promedio entre mantenimientos para cada equipo.
   - Determinar la suma total de horas acumuladas (`Horas_Acumuladas`) por equipo.

6. **Datos derivados:**
   - Crear una tabla combinada que una los datos de `Historicos_Ordenes` y `Registros_Condiciones` mediante el campo `ID_Equipo` en la tabla `Resultados_join`. Esta tabla debe incluir:
     - Número total de órdenes de mantenimiento por equipo.
     - Promedio de condiciones operativas (temperatura, vibración, presión) de cada equipo.


**NOTAS:** 
- Todas las soluciones en Python deben implementarse mediante funciones. Las funciones deben invocarse al final para ejecutar el proceso deseado.
- Usar el kernel: **Python 3.8 - AzureML (Python 3.10.11)**

#### **Estructura de carpetas:**
- Carpeta **src** para los `jupyter notebooks` y `archivos` de trabajo  
- Carpeta **dist** para *exportar los jupyter notebooks a módulos*. (Opcional).
- Los **data** para almacenar archivos *csv*
- Ejemplo: 

```
.
└── reposiutorio/
    ├── data/
    │   └── [archivos csv]
    ├── dist/
    │   └── [módulos python]
    └── src/
        └── [archivos jupyter y python]
```


#### **Trabajo en equipo:**  
   - Usar un repositorio común:
      - Un integrante del equipo crea un repositorio e invita a los demás a su repositorio.
      - El resto de integrantes clona el repositorio compartido.
      - Todos trabajan contra el repositorio compartido.
      - Nota: invitar también al formador
   - Trabajo por pares:
      - Recomendable abordar las tareas por pares.
   - Dividir las tareas (ejemplo):
      - Tareas relacionadas con los `Historicos_Ordenes.csv`.
      - `Registros_Condiciones.csv` y `Caracteristicas_Equipos.csv`.
      - Consultas básicas y de agregación.
      - Generación de tablas derivadas.
   - Recomendaciones:
      - Evitar trabajar en el mismo archivo a la vez. Especialmente los jupyter notebooks.
      - No es necesario trabajar por ramas.
      - Comunicarse cuando haya commits y pushes para realizar pulls. Evitar en lo posible conflictos.


#### **Entregables:**
- URL del repositorio con los módulos de Python.
- Se debe añadir a la tarea del campus (1 por equipo)


### **Duración y Evaluación**
1. **Duración:**  
   - 3 horas aprox.
   - Los descansos están a criterio de cada equipo.


3. **Criterios de Evaluación:**  
   - **Funcionalidad:** Código y consultas sin errores.  
   - **Resultados:** Respuestas correctas a las preguntas planteadas.  
   - **Colaboración:** División clara del trabajo y buena integración de los resultados.


### **Resultados Esperados**
Al finalizar el reto, los participantes habrán logrado:
1. Identificar patrones básicos de mantenimiento y condiciones operativas.
2. Construir un conjunto de datos combinado con métricas clave sobre los equipos.
3. Estar listos para pasar a una etapa más avanzada de modelado y análisis predictivo.