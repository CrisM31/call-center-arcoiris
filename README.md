# 📞 Análisis de Rendimiento — Call Center Arcoiris

<p align="center">
  <img src="https://img.shields.io/badge/Google%20Sheets-34A853?style=for-the-badge&logo=google-sheets&logoColor=white" />
  <img src="https://img.shields.io/badge/Estado-Completado-success?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Bootcamp-Unicorn%20Data%20Analyst-blueviolet?style=for-the-badge" />
</p>

## 📋 Descripción

Proyecto de análisis de datos para el departamento de call center de la empresa **Arcoiris** (Ficticio). Se realizó un análisis exhaustivo del rendimiento diario de los agentes con el objetivo de identificar áreas de mejora, optimizar la calidad del servicio y aumentar la eficacia en ventas y gestión de reclamaciones.

> **Contexto**: La empresa es una PYME que utiliza Google Sheets como herramienta de análisis. Este proyecto sirve como prueba de concepto para evaluar si migrar a herramientas más avanzadas.

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

## 📊 Dashboard Interactivo

👉 **[Ver Dashboard en Google Sheets](https://docs.google.com/spreadsheets/d/e/2PACX-1vQTfcWu-J-t3tg2P17yhNmMuVX2gwuwTXH8Dkg4hBLqdEyEB2TbwF2wlmO4aBTIad2lMqfiFImOswO_/pubhtml)**

El dashboard está dividido en 3 vistas:

- **Desempeño y Calidad** — Top agentes en ventas, reclamaciones y calificación de servicio con filtros interactivos
- **Rendimiento / Productividad** — Tiempo medio de llamadas, pausas y gestión; ranking por cantidad de llamadas
- **Tabla de Agentes** — Resumen consolidado del rendimiento de todos los agentes con escala de calificación

---

## 🗃️ Dataset

Datos descargados del software de gestión del call center. Período analizado: **noviembre 2023**.

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

## 🛠️ Herramientas

![Google Sheets](https://img.shields.io/badge/Google%20Sheets-34A853?style=for-the-badge&logo=google-sheets&logoColor=white)

---

## 📫 Contacto

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com/in/cristobalmoyacantillana/)
