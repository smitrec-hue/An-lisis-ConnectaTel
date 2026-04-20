# Análisis-ConnectaTel
Evaluación del comportamiento de los clientes de una empresa de telecomunicaciones en Latinoamérica, ConnectaTel. 
# 📊 Análisis de Comportamiento y Segmentación de Clientes: ConnectaTel

![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)
![Pandas](https://img.shields.io/badge/Pandas-2.0+-orange.svg)
![Matplotlib](https://img.shields.io/badge/Matplotlib-3.5+-green.svg)
![Seaborn](https://img.shields.io/badge/Seaborn-0.12+-blue.svg)

## 📋 Descripción del Proyecto
Este proyecto simula el rol de un **Analista de Datos** para **ConnectaTel**, una empresa de telecomunicaciones en Latinoamérica. El objetivo principal es evaluar el comportamiento de los clientes durante el año 2024, identificando patrones de consumo, detectando anomalías (outliers) y creando segmentaciones estratégicas para mejorar la retención y la oferta comercial.

## 🛠️ Tecnologías Utilizadas
- **Python**: Lenguaje principal de análisis.
- **Pandas**: Manipulación y limpieza de estructuras de datos.
- **NumPy**: Operaciones lógicas y manejo de valores nulos/centinela.
- **Matplotlib & Seaborn**: Visualización de datos y análisis exploratorio (EDA).

## 🗂️ Estructura de los Datos
El análisis integra tres fuentes de datos principales:
- `plans.csv`: Detalles de precios y límites de los planes (Básico y Premium).
- `users.csv`: Información demográfica y registro de clientes.
- `usage.csv`: Registro detallado de consumo real (llamadas, mensajes y minutos).

## 🚀 Fases del Análisis

### 1. Limpieza y Preparación de Datos
- **Corrección de Valores Centinela**: Identificación de edades erróneas (ej. `-999`) e imputación mediante la **mediana** para preservar la integridad estadística.
- **Estandarización**: Conversión de caracteres de "desconocido" (como `'?'`) en valores nulos oficiales (`pd.NA`) en variables categóricas.
- **Integración**: Consolidación de datasets para generar un perfil de usuario único (`user_profile`).

### 2. Análisis de Límites y Outliers
- **Método IQR**: Implementación del Rango Intercuartílico para detectar consumos extremos.
- **Decisión Estratégica**: Se analizó la plausibilidad de los valores máximos (ej. 155 minutos vs límite de 61) decidiendo **mantener los outliers**, ya que representan el segmento de mayor valor comercial (Heavy Users) y no errores de medición.

### 3. Segmentación de Clientes
Se crearon dimensiones de análisis personalizadas:
- **Grupo de Edad**: Clasificación en `Joven`, `Adulto` y `Adulto Mayor`.
- **Nivel de Uso**: Clasificación basada en actividad real en `Bajo uso`, `Uso medio` y `Alto uso`.

## 📈 Hallazgos Clave (Insights)
- **Perfil Demográfico**: El **50% de la base (2,008 usuarios)** son Adultos, siendo el segmento más rentable y estable.
- **Concentración de Uso**: El **73% de los usuarios** se clasifica en "Uso Medio", definiendo la carga operativa estándar de la red.
- **Identificación de Power Users**: Se detectó un segmento crítico de **278 usuarios de "Alto Uso"**. Estos representan una oportunidad inmediata de *Up-selling* hacia planes superiores.

## 💡 Recomendaciones de Negocio
1. **Migración Proactiva**: Ofrecer el plan Premium a los usuarios identificados como outliers en el plan Básico para evitar su fuga por facturación excedente.
2. **Optimización de Oferta**: Diseñar un plan intermedio (80-90 min) para capturar el valor de los usuarios que superan el plan Básico pero no requieren el Premium.
3. **Fidelización por Edad**: Crear programas de lealtad específicos para el grupo de **Adultos Mayores (29% de la base)**, quienes mantienen un consumo de voz constante.

## 💻 Instalación y Uso
1. Clonar el repositorio.
2. Instalar las dependencias necesarias:
   ```bash
   pip install pandas numpy matplotlib seaborn
3.	Ejecutar el notebook S7 Version-Estudiante-Project-ConnectaTel.ipynb en cualquier entorno de Jupyter o Google Colab.
________________________________________
-	Autor: Salvador Mitre Carlos
-	LinkedIn: [Enlace a tu perfil]
-	Proyecto finalizado en marzo de 2026.
