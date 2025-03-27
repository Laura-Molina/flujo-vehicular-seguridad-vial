#  Análisis de Flujo Vehicular y Seguridad Vial en Autopistas AUSA

## 📌 Descripción

Este proyecto analiza datos de siniestralidad y flujo vehicular en las autopistas de la Ciudad Autónoma de Buenos Aires (AUSA), con el objetivo de entender si existe relación entre el tráfico vehicular, las condiciones climáticas y los accidentes de tránsito. 

Los datos provienen de la plataforma oficial [Buenos Aires Data](https://data.buenosaires.gob.ar/), específicamente de los conjuntos:
- **Seguridad Vial Autopistas AUSA**
- **Flujo vehicular por radares AUSA**

---

## ❓ Preguntas de análisis

- ¿Están relacionadas las tasas de siniestralidad con el flujo vehicular?
- ¿Influye el estado meteorológico en la ocurrencia de siniestros?
- ¿Qué autopistas presentan mayor cantidad de accidentes?
- ¿En qué momentos del día hay mayor flujo vehicular?
- ¿Existen períodos con más siniestros registrados?

---

##  Proceso del proyecto

### 1. Extracción y descarga de datos
- **Seguridad Vial Autopista AUSA:**  
  - Siniestros 2022, 2023, 2024 (archivos CSV)
- **Flujo Vehicular por Radares AUSA:**  
  - Flujo vehicular 2022, 2023, 2024 (archivos CSV)

### 2. Carga de datos en SQL Server
- Se encontraron errores de codificación al cargar algunos archivos.
- Se modificaron tipos de datos (fechas como `DATETIME`, valores como `INT`) para normalizar.
- Se identificaron filas en blanco y valores inconsistentes (especialmente en Flujo Vehicular 2024).

### 3. Creación de vistas en SQL
- `VistaSiniestros22_23_24`
- `Vista_FlujoVehícular2022`
- `Vista_FlujoVehícular2023`
- `Vista_FlujoVehícular2024`

### 4. Transformaciones en Power BI (Power Query)
- Limpieza de filas en blanco.
- Renombrado de columnas para uniformidad.
- Anexado de datos por año.

### 5. Modelado y visualización en Power BI
- Análisis por autopista, hora del día, tipo de vehículo, día de la semana y condiciones meteorológicas.
- Debido a que no hay coincidencia exacta entre siniestros y flujo por autopista y fecha, los datos fueron analizados **por separado** (sin cruce directo).

---

## 📊 Principales hallazgos

- 📈 **La mayoría de los siniestros están relacionados con el aumento del flujo vehicular.**
- 🌤️ **Las condiciones meteorológicas no parecen influir: la mayor siniestralidad ocurre con clima bueno.**
- 🚗 **Autos y camiones presentan más siniestros entre las 12 y 16 h (cuando hay mayor tráfico).**
- 🚌 **Los buses presentan siniestros entre las 4 y 8 h, en el inicio del incremento del flujo.**
- 🚧 **Las colisiones con obstáculos fijos ocurren mayormente los domingos entre las 4 y 8 h.**

---

## 📂 Estructura del proyecto
flujo-vehicular-seguridad-vial/ │ ├── README.md ├── dashboard/ │ └── flujo_vehicular_seguridad_vial.pbix └── sql/ └── vistas_sql_proyecto.sql


---

## 👩‍💻 Autora

**Laura Viviana Molina**  
Analista de Datos | Power BI | SQL | Python  
[LinkedIn](https://www.linkedin.com/in/tu-perfil)  
[Correo de contacto]




