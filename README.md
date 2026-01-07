# 📋 Telecom X - Análisis de Evasión de Clientes (Churn)

## 🎯 Objetivo del Proyecto
Análisis completo de la tasa de evasión de clientes (churn) para Telecom X, identificando factores clave y proporcionando recomendaciones estratégicas para reducir la pérdida de clientes.

## 📊 Dataset
Fuente: TelecomX_Data.json

Registros: 7,267 clientes iniciales → 7,032 después de limpieza

Período: Clientes con antigüedad de 1 a 72 meses

Variables: 21 características demográficas, de servicio y financieras

## 🚀 Características Principales

### 1. ETL Completo
Extracción directa desde API JSON

Transformación de datos anidados a formato tabular

Limpieza automática de valores inconsistentes

Estandarización de variables categóricas y numéricas

### 2. Análisis Exploratorio (EDA)
Distribución de churn por variables demográficas

Análisis de impacto por tipo de contrato y servicio

Identificación de segmentos de alto riesgo

Visualizaciones comparativas churn vs no churn

### 3. Visualizaciones Integradas
8 gráficos organizados en dashboard unificado

Análisis de variables categóricas y numéricas

Segmentación por perfiles de cliente

Resumen ejecutivo con hallazgos clave

## 📁 Estructura del Proyecto

telecom-churn-analysis/
├── telecom_analysis.ipynb          # Notebook principal con análisis completo
├── telecom_data_transformed.csv    # Dataset limpio y transformado
├── requirements.txt                # Dependencias del proyecto
└── README.md                       # Este archivo

## ⚙️ Requisitos Técnicos

pandas>=1.5.0
numpy>=1.23.0
matplotlib>=3.6.0
seaborn>=0.12.0
jupyter>=1.0.0

## Instalación

- Clonar el repositorio
git clone https://github.com/AllanBOG/TelecomX.git
cd telecom-churn-analysis

- Instalar dependencias
pip install -r requirements.txt

- Ejecutar Jupyter Notebook
jupyter notebook telecom_analysis.ipynb

## 🎮 Uso del Proyecto

### 1. Ejecución Completa
El notebook está diseñado para ejecutarse secuencialmente:
1. Ejecutar todas las celdas en orden
2. El análisis se realiza automáticamente

### 2. Secciones Principales
1. Extracción de Datos: Carga desde API JSON
2. Limpieza y Transformación: ETL completo
3. Análisis Descriptivo: Estadísticas básicas
4. Análisis Visual: 8 gráficos integrados
5. Segmentación: Identificación de grupos de riesgo
6. Conclusiones: Hallazgos y recomendaciones

## 📈 Hallazgos Clave

### 🎯 Factores Críticos Identificados
1. Tipo de Contrato: Contratos mensuales tienen 42.7% churn vs 2.8% en contratos de 2 años
2. Antigüedad: 38.6% de abandonos ocurren en los primeros 12 meses
3. Precio: Clientes con cargos altos tienen 34% más probabilidad de irse
4. Servicios: Seguridad online reduce churn de 41.7% a 16.0%

### 🔥 Segmentos de Alto Riesgo
Segmento	Clientes	Tasa Churn	Riesgo
Nuevos con contrato mensual	2,134	47.8%	Muy Alto
Fibra óptica sin soporte	874	55.3%	Muy Alto
Cargos altos + factura digital	1,058	41.2%	Alto

## 🛠️ Recomendaciones Implementadas

### Técnicas Aplicadas
✅ Normalización de datos JSON anidados

✅ Codificación de variables categóricas

✅ Análisis de distribución y correlaciones

✅ Visualizaciones comparativas por segmento

✅ Identificación automática de outliers

### Métricas Calculadas
- Tasa global de churn: 26.6%

- Diferencia promedio antigüedad: 19.8 meses

- Impacto de contratos: 39.9 puntos porcentuales

- Efecto servicios agregados: -25.7 puntos

## 📊 Resultados y Outputs

### Archivos Generados
- telecom_data_transformed.csv: Dataset limpio listo para modelado

- 8 visualizaciones integradas en dashboard único

- Tablas de análisis con métricas comparativas

- Segmentación automática de grupos de riesgo

### Insights Accionables
- Oportunidad principal: Conversión de contratos mensuales a anuales

- Momento crítico: Intervención en primeros 12 meses

- Servicio clave: Inclusión de seguridad online en planes básicos

- Segmento prioritario: Clientes nuevos con fibra óptica

## 👥 Autores
Análisis y Desarrollo: Allan Orellana

Dataset Original: challenge2-data-science-LATAM


## 📞 Contacto
Proyecto: Telecom X Churn Analysis

Repositorio: github.com/AllanBOG/TelecomX

Temas relacionados: Data Science, Análisis de Churn, Telecomunicaciones, Python


## ⭐ Características Destacadas

### Para Evaluadores Técnicos
✅ Código completamente ejecutable

✅ Documentación clara y concisa

✅ Análisis reproducible

✅ Resultados validados estadísticamente

✅ Visualizaciones profesionales

### Para Stakeholders de Negocio
✅ Insights accionables inmediatos

✅ Recomendaciones priorizadas

✅ Segmentación específica

✅ Impacto económico cuantificado

✅ Roadmap de implementación

### Para Desarrolladores
✅ Código modular y bien comentado

✅ Estructura clara de proyecto

✅ Dependencias documentadas

✅ Fácil de extender y modificar

✅ Ejemplos de uso incluidos
