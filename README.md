# 📞 Análisis de Rendimiento — Call Center Arcoiris

<p align="center">
  <img src="https://img.shields.io/badge/Google%20Sheets-34A853?style=for-the-badge&logo=google-sheets&logoColor=white" />
</p>

## 📋 Descripción

Proyecto de análisis de datos para el departamento de call center de la empresa **Arcoiris**. A partir de datos extraídos del software de gestión de llamadas, se realizó un análisis exhaustivo del rendimiento diario de los agentes con el objetivo de identificar áreas de mejora, optimizar la calidad del servicio y aumentar la eficacia en ventas y gestión de reclamaciones.

> **Contexto real**: La empresa es una PYME que utiliza Google Sheets como herramienta de análisis. Este proyecto sirve como prueba de concepto para evaluar si migrar a herramientas más avanzadas.

> **Datos**: Los datos en bruto utilizados en este proyecto fueron proporcionados por [Unicorn Academy](https://unicornacademy.es/) en el marco del Bootcamp de Data Analyst, con fines de aprendizaje y práctica profesional.

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
- **** — Para filtrar, ordenar y agregar datos dinámicamente según los filtros de los dashboards (rango de fechas, tipo de agente, orden ascendente/descendente)

### Funciones de Agregación
- **** — Suma de minutos de llamada, pausa y gestión por agente
- **** — Conteo de llamadas, ventas y reclamaciones por agente
- **** — Cálculo de tiempos medios (llamada: 15 min | pausa: 3 min | gestión: 11 min) y calificación media por agente

### Funciones Lógicas y de Clasificación
- **** — Clasificación automática de agentes en escala de calificación:
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
| uid=501(cris) gid=20(staff) groups=20(staff),12(everyone),61(localaccounts),79(_appserverusr),80(admin),81(_appserveradm),33(_appstore),98(_lpadmin),100(_lpoperator),204(_developer),250(_analyticsusers),395(com.apple.access_ftp),398(com.apple.access_screensharing),399(com.apple.access_ssh),400(com.apple.access_remote_ae),701(com.apple.sharepoint.group.1) | INT | Identificador único del registro diario por agente |
|  | INT | Identificador del agente |
|  | TEXT | Nombre completo del agente |
|  | DATE | Día de registro |
|  | INT | Minutos totales en llamadas |
|  | INT | Minutos totales en pausa |
|  | INT | Minutos totales en gestión |
|  | INT | Cantidad total de llamadas |
|  | INT | Ventas realizadas |
|  | INT | Reclamaciones gestionadas |
|  | FLOAT | Calificación de calidad del día |
|  | INT | Llamadas no atendidas |

---

## 💡 Principales Hallazgos

- Tasa de conversión promedio del equipo: **84,44%**, con variaciones individuales entre 77% y 100%
- Los agentes con mejor calificación de servicio no siempre son los de mayor volumen de llamadas
- Se detectaron agentes con alta conversión pero también alto volumen de reclamaciones — posible trade-off calidad/velocidad
- La distribución del tiempo entre llamadas, gestión y pausas muestra oportunidades de redistribución de carga

---

## 📊 Dashboard Interactivo

👉 **[Ver Dashboard en Google Sheets](https://docs.google.com/spreadsheets/d/e/2PACX-1vQTfcWu-J-t3tg2P17yhNmMuVX2gwuwTXH8Dkg4hBLqdEyEB2TbwF2wlmO4aBTIad2lMqfiFImOswO_/pubhtml)**

🌐 **[Ver GitHub Pages](https://crism31.github.io/call-center-arcoiris/)**

---

## 🛠️ Herramientas

![Google Sheets](https://img.shields.io/badge/Google%20Sheets-34A853?style=for-the-badge&logo=google-sheets&logoColor=white)

---

## 📫 Contacto

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com/in/cristobalmoyacantillana/)
