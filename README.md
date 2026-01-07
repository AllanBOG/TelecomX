# Telecom X - Análisis de Evasión de Clientes (Churn)

## Objetivo del Proyecto
Análisis completo de la tasa de evasión de clientes (churn) para Telecom X, identificando factores clave y proporcionando recomendaciones estratégicas para reducir la pérdida de clientes.

## Dataset
- **Fuente**: [TelecomX_Data.json](https://github.com/ingridcristh/challenge2-data-science-LATAM/blob/main/TelecomX_Data.json)
- **Registros**: 7,267 clientes iniciales → 7,032 después de limpieza
- **Período**: Clientes con antigüedad de 1 a 72 meses
- **Variables**: 21 características demográficas, de servicio y financieras

## Características Principales

### 1. ETL Completo
- Extracción directa desde API JSON
- Transformación de datos anidados a formato tabular
- Limpieza automática de valores inconsistentes
- Estandarización de variables categóricas y numéricas

### 2. Análisis Exploratorio (EDA)
- Distribución de churn por variables demográficas
- Análisis de impacto por tipo de contrato y servicio
- Identificación de segmentos de alto riesgo
- Visualizaciones comparativas churn vs no churn

### 3. Visualizaciones Integradas
- 8 gráficos organizados en dashboard unificado
- Análisis de variables categóricas y numéricas
- Segmentación por perfiles de cliente
- Resumen ejecutivo con hallazgos clave

## Estructura del Proyecto
telecom-churn-analysis/
├── telecom_analysis.ipynb # Notebook principal con análisis completo
├── telecom_data_transformed.csv # Dataset limpio y transformado
├── requirements.txt # Dependencias del proyecto
└── README.md # Este archivo


## Requisitos Técnicos
### Dependencias Principales

pandas>=1.5.0
numpy>=1.23.0
matplotlib>=3.6.0
seaborn>=0.12.0
jupyter>=1.0.0


### Instalación
```bash
# Clonar el repositorio
git clone https://github.com/tu-usuario/telecom-churn-analysis.git
cd telecom-churn-analysis

# Instalar dependencias
pip install -r requirements.txt

# Ejecutar Jupyter Notebook
jupyter notebook telecom_analysis.ipynb

**## Uso del Proyecto**
1. Ejecución Completa
El notebook está diseñado para ejecutarse secuencialmente:

python
# Ejecutar todas las celdas en orden
# El análisis se realiza automáticamente
2. Secciones Principales
Extracción de Datos: Carga desde API JSON

Limpieza y Transformación: ETL completo

Análisis Descriptivo: Estadísticas básicas

Análisis Visual: 8 gráficos integrados

Segmentación: Identificación de grupos de riesgo

Conclusiones: Hallazgos y recomendaciones

3. Personalización
python
# Para analizar variables específicas
variables_interes = ['tipo_contrato', 'cargos_mensuales', 'antiguedad_meses']
df_analisis = df_clean[variables_interes + ['Churn']]
Hallazgos Clave
Factores Críticos Identificados
Tipo de Contrato: Contratos mensuales tienen 42.7% churn vs 2.8% en contratos de 2 años

Antigüedad: 38.6% de abandonos ocurren en los primeros 12 meses

Precio: Clientes con cargos altos tienen 34% más probabilidad de irse

Servicios: Seguridad online reduce churn de 41.7% a 16.0%

Segmentos de Alto Riesgo
Segmento	Clientes	Tasa Churn	Riesgo
Nuevos con contrato mensual	2,134	47.8%	Muy Alto
Fibra óptica sin soporte	874	55.3%	Muy Alto
Cargos altos + factura digital	1,058	41.2%	Alto
Recomendaciones Implementadas
Técnicas Aplicadas
Normalización de datos JSON anidados

Codificación de variables categóricas

Análisis de distribución y correlaciones

Visualizaciones comparativas por segmento

Identificación automática de outliers

Métricas Calculadas
Tasa global de churn: 26.6%

Diferencia promedio antigüedad: 19.8 meses

Impacto de contratos: 39.9 puntos porcentuales

Efecto servicios agregados: -25.7 puntos

Resultados y Outputs
Archivos Generados
telecom_data_transformed.csv: Dataset limpio listo para modelado

8 visualizaciones integradas en dashboard único

Tablas de análisis con métricas comparativas

Segmentación automática de grupos de riesgo

Insights Accionables
Oportunidad principal: Conversión de contratos mensuales a anuales

Momento crítico: Intervención en primeros 12 meses

Servicio clave: Inclusión de seguridad online en planes básicos

Segmento prioritario: Clientes nuevos con fibra óptica

Visualizaciones Incluidas
Dashboard Completo (8 gráficos)
Distribución general de churn

Churn por género

Impacto del tipo de contrato

Influencia del método de pago

Efecto del servicio de internet

Distribución de antigüedad

Análisis de cargos mensuales

Comparativa cargos totales

Formatos de Visualización
Gráficos de torta para distribución

Barras comparativas por categoría

Histogramas para variables numéricas

Texto formateado con hallazgos clave

Cómo Extender el Proyecto
1. Modelado Predictivo
python
# Ejemplo: Implementar modelo de clasificación
from sklearn.ensemble import RandomForestClassifier

model = RandomForestClassifier()
model.fit(X_train, y_train)
predictions = model.predict(X_test)
2. Análisis Temporal
python
# Análisis por cohortes mensuales
df_clean['cohorte'] = df_clean['fecha_ingreso'].dt.to_period('M')
analisis_cohortes = df_clean.groupby('cohorte')['Churn'].mean()
3. Sistema de Alertas
python
# Identificar clientes en riesgo
clientes_riesgo = df_clean[
    (df_clean['tipo_contrato'] == 'Month-to-month') &
    (df_clean['antiguedad_meses'] < 6) &
    (df_clean['cargos_mensuales'] > df_clean['cargos_mensuales'].median())
]
Checklist de Implementación
Completado
Extracción de datos desde API

Limpieza y transformación ETL

Análisis exploratorio completo

Visualizaciones integradas

Identificación de segmentos

Recomendaciones estratégicas

Exportación de datos limpios

Próximas Mejoras
Implementación de modelo predictivo

Dashboard interactivo con Plotly

Análisis de cohortes temporales

Sistema de scoring de riesgo

API para consultas en tiempo real

Contribución
Reportar Problemas
Revisar issues existentes

Crear nuevo issue con:

Descripción del problema

Pasos para reproducir

Comportamiento esperado vs actual

Sugerir Mejoras
Fork del repositorio

Crear branch de feature

Commit de cambios

Pull request descriptivo

Licencia
Este proyecto está bajo licencia MIT. Ver archivo LICENSE para más detalles.

Autores
Análisis y Desarrollo: [Tu Nombre]

Dataset Original: challenge2-data-science-LATAM

Metodología: Proceso CRISP-DM adaptado

Contacto
Proyecto: Telecom X Churn Analysis

Repositorio: github.com/tu-usuario/telecom-churn-analysis

Temas relacionados: Data Science, Análisis de Churn, Telecomunicaciones, Python

