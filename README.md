# telecom-analysis

📋 Descripción del Proyecto ConnectaTel
🎯 Objetivo del Proyecto
Evaluar el comportamiento de los clientes de ConnectaTel, una empresa de telecomunicaciones en Latinoamérica, para:

Construir un perfil estadístico de los clientes
Detectar comportamientos atípicos y patrones de uso extremo
Crear segmentos de clientes estratégicos
Identificar oportunidades de mejora en planes y estrategias de retención
Sugerir mejoras en la oferta actual de servicios
📊 Datasets Utilizados
- El análisis trabajó con tres datasets principales con información registrada hasta 2024:

1. plans.csv - Información de planes actuales

Precio mensual, minutos incluidos, GB incluidos
Costos por excesos (mensajes, minutos, datos)
2. users_latam.csv - Información de clientes (4,000 registros)

Datos demográficos: edad, ciudad
Información contractual: fecha de registro, plan, churn
Problemas detectados: valores sentinel (-999 en edad, "?" en ciudad), fechas futuras
3. usage.csv - Detalle de uso real de servicios (40,000 registros)

Llamadas y mensajes por usuario
Duración de llamadas y longitud de mensajes
Datos MAR: nulos estructurales según tipo de comunicación
🔄 Etapas del Análisis Realizadas
Paso 1: Exploración Inicial

Carga y revisión de estructura de datasets
Identificación de tipos de datos y dimensiones
Paso 2: Identificación de Problemas de Calidad

Detección de valores nulos (11.7% en ciudad, 88.3% en churn_date)
Identificación de valores sentinel (-999, "?")
Análisis de fechas imposibles (40 registros en 2026)
Paso 3: Limpieza de Datos

Reemplazo de sentinels con valores apropiados
Corrección de fechas fuera de rango
Validación de nulos MAR en usage
Paso 4: Agregación por Usuario

Creación de métricas de uso: cantidad de mensajes, llamadas y minutos
Combinación con datos demográficos
Paso 5: Análisis de Distribuciones y Outliers

Visualización con histogramas y boxplots
Identificación de outliers usando método IQR
Decisión de mantener outliers (usuarios heavy users legítimos)
Paso 6: Segmentación de Clientes

Por Uso: Bajo Uso, Uso Medio, Alto Uso
Por Edad: Joven (<30), Adulto (30-59), Adulto Mayor (≥60)
Paso 7: Insights Ejecutivos

Análisis de oportunidades de upselling
Identificación de segmentos valiosos
Recomendaciones estratégicas
