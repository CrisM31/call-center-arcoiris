# 📞 Análisis de Rendimiento — Call Center Arcoiris

<p align="center">
  <img src="https://img.shields.io/badge/Google%20Sheets-34A853?style=for-the-badge&logo=google-sheets&logoColor=white" />
</p>

## 📋 Descripción

Proyecto de análisis de datos para el departamento de call center de la empresa **Arcoiris**. A partir de datos extraídos del software de gestión de llamadas, se realizó un análisis exhaustivo del rendimiento diario de los agentes con el objetivo de identificar áreas de mejora, optimizar la calidad del servicio y aumentar la eficacia en ventas y gestión de reclamaciones.

> **Contexto real**: La empresa es una PYME que utiliza Google Sheets como herramienta de análisis. Este proyecto sirve como prueba de concepto para evaluar si migrar a herramientas más avanzadas.

> **Datos**: Los datos en bruto utilizados en este proyecto fueron proporcionados por [Unicorn Academy](https://unicornacademy.es/) en el marco del Bootcamp de Data Analyst, para el desarrollo de pensamiento y habilidades analíticas.

---

## 📊 Dashboard

👉 **[Ver Dashboard en Google Sheets](https://docs.google.com/spreadsheets/d/e/2PACX-1vQTfcWu-J-t3tg2P17yhNmMuVX2gwuwTXH8Dkg4hBLqdEyEB2TbwF2wlmO4aBTIad2lMqfiFImOswO_/pubhtml)** 👈

---

## 🎯 Objetivos del Análisis

| Objetivo | Indicadores clave |
|---|---|
| **Eficiencia en llamadas** | Minutos totales, cantidad de llamadas y llamadas perdidas por agente |
| **Gestión del tiempo** | Minutos en gestión y pausa por agente |
| **Ventas y reclamaciones** | Volumen y tasa de conversión / reclamaciones por agente |
| **Calidad de servicio** | Calificación diaria individual y comparativa |
| **Evaluación individual** | Ranking y análisis por agente |
| **Seguimiento temporal** | Tendencias de rendimiento en el período analizado |

---

## 📊 Dashboards

El proyecto está compuesto por **4 hojas** en Google Sheets:

### 1. 🏆 Desempeño y Calidad
- Top 5 agentes con **menor % de reclamaciones**
- Top 5 agentes con **mayor % de conversión en ventas**
- Top 5 agentes con **mejor calificación de servicio**
- Filtros interactivos por **rango de fechas** y por tipo de agentes (Mejores / Peores)

### 2. ⚡ Rendimiento / Productividad
- **Tiempo medio** de llamada, pausa y gestión del equipo
- Top 5 agentes por **cantidad de llamadas** con minutos y media
- Gráfico de evolución de **llamadas en el tiempo**

### 3. 📋 Tabla de Agentes
- Resumen consolidado de todos los agentes con métricas acumuladas del período
- Columna de **escala de calificación** (Excelente / Muy Buena / Buena / Mala / Muy Mala)

### 4. 🗃️ Datos en Bruto
- Tabla original con registros diarios por agente (fuente de todas las métricas)

---

## 🛠️ Técnicas y Fórmulas Aplicadas

### Funciones de Consulta y Filtrado
- **`QUERY`** — Para filtrar, ordenar y agregar datos dinámicamente según los filtros de los dashboards (rango de fechas, tipo de agente, orden ascendente/descendente)

### Funciones de Agregación
- **`SUMIF`** — Suma de minutos de llamada, pausa y gestión por agente
- **`COUNTIF`** — Conteo de llamadas, ventas y reclamaciones por agente
- **`AVERAGEIF`** — Cálculo de tiempos medios (llamada: 15 min | pausa: 3 min | gestión: 11 min) y calificación media por agente

### Funciones Lógicas y de Clasificación
- **`IFS`** — Clasificación automática de agentes en escala de calificación:
  - ⭐ Excelente (5-6) | Muy Buena (4-5) | Buena (3-5) | Mala (2-3) | Muy Mala (1-2)

### Funciones de Porcentaje y Métricas Derivadas
- Cálculo de **% de conversión** (ventas / llamadas)
- Cálculo de **% de reclamaciones** (reclamaciones / llamadas)
- Media de minutos por llamada por agente

### Visualización
- **Gráficos de barras y líneas** — Evolución de llamadas en el tiempo y comparativa entre agentes
- **Formato condicional** — Resaltado visual por rangos de rendimiento

### Interactividad
- **Validación de datos (dropdowns)** — Filtros de selección para tipo de agente (Mejores/Peores) y orden (asc/desc)
- **Filtros de fecha** — Segmentación del análisis por rango temporal

---

## 🗃️ Dataset

Datos descargados del software de gestión del call center. Período analizado: **13 al 25 de noviembre de 2023** | **50 agentes** | **650 registros diarios**.

| Campo | Tipo | Descripción |
|---|---|---|
| `id` | INT | Identificador único del registro diario por agente |
| `agente_id` | INT | Identificador del agente |
| `agente_nombre` | TEXT | Nombre completo del agente |
| `fecha` | DATE | Día de registro |
| `min_llamada` | INT | Minutos totales en llamadas |
| `min_pausa` | INT | Minutos totales en pausa |
| `min_gestion` | INT | Minutos totales en gestión |
| `llamadas` | INT | Cantidad total de llamadas |
| `ventas` | INT | Ventas realizadas |
| `reclamaciones` | INT | Reclamaciones gestionadas |
| `calificacion` | FLOAT | Calificación de calidad del día |
| `llamadas_perdidas` | INT | Llamadas no atendidas |

---

## 💡 Principales Hallazgos

- Tasa de conversión promedio del equipo: **84,44%**, con variaciones individuales entre 77% y 100%
- Los agentes con mejor calificación de servicio no siempre son los de mayor volumen de llamadas
- Se detectaron agentes con alta conversión pero también alto volumen de reclamaciones — posible trade-off calidad/velocidad
- La distribución del tiempo entre llamadas, gestión y pausas muestra oportunidades de redistribución de carga

---

## 🧹 Limpieza de Datos y Proceso Analítico

Antes de construir cualquier análisis, los datos en bruto presentaban inconsistencias que habrían comprometido la calidad de los resultados. Trabajar con datos sucios es la realidad de un analista en su día a día, por lo que esta iteración ayuda mucho a tener claro que problemas nos podríamos encontrar en una base de datos. 

### Problemas encontrados en los datos en bruto

- **Fechas con formato incorrecto** - Las fechas no seguían un formato homogéneo, lo que impedía realizar filtros temporales confiables. Se normalizaron a `DD/MM/YYYY` para garantizar que los filtros por rango de fecha en los dashboards funcionaran correctamente.

- **Registros duplicados** - El dataset original contenía filas duplicadas que habrían inflado métricas como el total de llamadas o ventas, generando conclusiones incorrectas. Se identificaron y eliminaron aplicando criterios de unicidad por combinación de agente y fecha.

- **Errores de formato numérico** - Varios valores numéricos usaban punto como separador decimal en lugar de coma (estándar en español), por lo que Google Sheets los interpretaba como texto y no como números. Esto impedía que funciones como `SUM`, `AVERAGE` o `QUERY` pudieran operar con ellos. Se corrigieron todos antes de comenzar el análisis.

Solo una vez validada y limpia la base de datos se procedió a trabajar con los datos. Ese orden no es arbitrario: **un análisis construido sobre datos sucios produce insights incorrectos**, sin importar qué tan bien estén diseñados los dashboards.

### Flujo de construcción del proyecto

El análisis siguió una secuencia lógica y progresiva:

1. **Datos en bruto → Limpieza y validación** - Corrección de formatos, eliminación de duplicados y verificación de consistencia del dataset completo.
2. **Hoja "Tabla Agentes" → Primeras agregaciones** - Consolidación del rendimiento por agente usando `SUMIF`, `COUNTIF` y `AVERAGEIF`. Se aplicaron formatos condicionales para identificar visualmente rangos de rendimiento, y se implementó la escala de calificación con `IFS`.
3. **Dashboard "Rendimiento" → Análisis de productividad** - Tiempos medios del equipo, rankings dinámicos de agentes por volumen de llamadas y evolución temporal con gráficos.
4. **Dashboard "Desempeño y Calidad" → Análisis comparativo** - Top agentes en ventas, reclamaciones y calidad de servicio, con filtros interactivos por fecha y tipo de agente construidos con `QUERY`.

Este flujo del dato crudo al insight visual— refleja cómo trabaja un analista en un entorno real: primero confiar en los datos, luego transformarlos, y finalmente comunicarlos de forma clara a quienes toman decisiones.

---

## 🛠️ Herramientas

![Google Sheets](https://img.shields.io/badge/Google%20Sheets-34A853?style=for-the-badge&logo=google-sheets&logoColor=white)

---

## 📫 Contacto

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com/in/cristobalmoyacantillana/)

