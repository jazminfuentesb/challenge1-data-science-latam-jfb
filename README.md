# 📊 Análisis de Rendimiento Empresarial - AluraStore Challenge

## 🎯 Descripción del Proyecto

Proyecto de **Data Science** desarrollado como parte del Challenge Alura Latam, enfocado en el análisis exhaustivo de datos empresariales para la toma de decisiones estratégicas. Implementa técnicas de análisis exploratorio de datos (EDA) y visualización para evaluar el rendimiento de cuatro tiendas y determinar cuál presenta menor viabilidad comercial.

**Problema de Negocio:** Optimizar la cartera de tiendas identificando la unidad de negocio con menor rentabilidad para su potencial venta.

## 🔧 Tecnologías y Dependencias

### Entorno de Desarrollo
- **Python 3.8+**
- **Google Colab**

### Librerías Principales
```python
import pandas as pd                 # Manipulación y análisis de datos
import numpy as np                  # Operaciones numéricas
import matplotlib.pyplot as plt     # Visualización básica
import seaborn as sns              # Visualización avanzada estadística
```

### Dependencias Adicionales
```bash
# Si ejecutas localmente, instalar:
pip install pandas numpy matplotlib seaborn jupyter
```

## 📁 Estructura del Proyecto

```
challenge1-data-science-latam-jfb/
│
├── AluraStoreLatam.ipynb           # Notebook principal con análisis completo
├── README.md                       # Documentación técnica del proyecto
├── base-de-datos-challenge1-latam/ # Datos del proyecto (si aplicable)
│   ├── tienda1.csv               # Dataset Tienda 1
│   ├── tienda2.csv               # Dataset Tienda 2  
│   ├── tienda3.csv               # Dataset Tienda 3
│   └── tienda4.csv               # Dataset Tienda 4
```

## 🚀 Instalación y Ejecución

### Opción 1: Google Colab (Recomendado)
1. **Abrir directamente en Colab:**
   ```
   https://colab.research.google.com/github/jazminfuentesb/challenge1-data-science-latam-jfb/blob/main/AluraStoreLatam.ipynb
   ```

2. **Ejecutar todas las celdas:**
   - Runtime → Run all (Ctrl+F9)

### Opción 2: Entorno Local
1. **Clonar el repositorio:**
   ```bash
   git clone https://github.com/jazminfuentesb/challenge1-data-science-latam-jfb.git
   cd challenge1-data-science-latam-jfb
   ```

2. **Crear entorno virtual (opcional pero recomendado):**
   ```bash
   python -m venv venv
   source venv/bin/activate  # En Windows: venv\Scripts\activate
   ```

3. **Instalar dependencias:**
   ```bash
   pip install -r requirements.txt
   ```

4. **Ejecutar Jupyter Notebook:**
   ```bash
   jupyter notebook AluraStoreLatam.ipynb
   ```

## 📊 Metodología de Análisis

### Pipeline de Análisis Implementado

📊 Metodología de Análisis
Pipeline de Análisis Implementado

El proyecto sigue una metodología estructurada dividida en 6 etapas de análisis secuencial:

1. 📈 Análisis de Facturación

Objetivo: Determinar el rendimiento financiero por tienda
Métricas clave: Ingresos totales, comparativa entre tiendas
Resultado: Identificación de la tienda con menor facturación

2. 📦 Ventas por Categoría

Objetivo: Evaluar el comportamiento de ventas por categoría de productos
Métricas clave: Volumen de productos vendidos por categoría y tienda
Resultado: Identificación de categorías más y menos exitosas por tienda

3. ⭐ Calificación Promedio de la Tienda

Objetivo: Medir la satisfacción del cliente por tienda
Métricas clave: Rating promedio, comparativa de experiencia del cliente
Resultado: Evaluación de la calidad del servicio por tienda

4. 🏆 Productos Más y Menos Vendidos

Objetivo: Identificar el rendimiento de productos específicos
Métricas clave: Ranking de productos, análisis de demanda por tienda
Resultado: Catálogo de productos estrella y productos con menor rotación

5. 🚚 Envío Promedio por Tienda

Objetivo: Evaluar la eficiencia operativa y logística
Métricas clave: Costos de envío promedio, eficiencia operativa
Resultado: Identificación de ventajas competitivas en costos operativos

6. 📋 Informe Final: Recomendación de Tienda

Objetivo: Síntesis integral de todos los análisis realizados
Metodología: Análisis ponderado de factores múltiples
Resultado: Recomendación fundamentada para la decisión de venta

### Técnicas de Data Science Aplicadas

- **Análisis Exploratorio de Datos (EDA)**
- **Agregaciones y Groupby Operations**
- **Análisis Estadístico Descriptivo**
- **Visualización de Datos Multidimensional**
- **Análisis Comparativo de KPIs**

## 📈 Resultados Clave 

### Hallazgos Técnicos

```python
# Resultados del análisis financiero más significativos

Ingreso total por tienda:

Tienda 1: $1,150,880,400.00
Tienda 2: $1,116,343,500.00
Tienda 3: $1,098,019,600.00
Tienda 4: $1,038,375,700.00

La tienda que más vende es: Tienda 1 con un ingreso total de $1,150,880,400.00

La tienda que menos vende es: Tienda 4 con un ingreso total de $1,038,375,700.00

---------------------------------------------------------------------------------

Costo de envío promedio por tienda:
Tienda 1: 26018.61
Tienda 2: 25216.24
Tienda 3: 24805.68
Tienda 4: 23459.46

La tienda con el menor costo de envío es la Tienda 1 con un promedio de 26018.61

La tienda con el menor costo de envío es la Tienda 4 con un promedio de 23459.46

```

### Conclusión Técnica

**Output del Análisis:** `Tienda 4` identificada como candidata óptima para venta.


 **Justificación para Vender la Tienda 4**:
 
1. **Menor Ingreso Total**: La Tienda 4 registró consistentemente el menor ingreso total de las cuatro tiendas. Este es el indicador más directo de su baja rentabilidad y menor generación de valor.

2. **Menor Volumen de Ventas General**: Más allá del ingreso, la Tienda 4 también mostró, en general, un menor volumen de productos vendidos a través de las categorías en comparación con las otras tiendas, lo que indica una actividad comercial más débil.

3. **A pesar del Costo de Envío Bajo**: Aunque la Tienda 4 tuvo el costo de envío promedio más bajo, esta ventaja en la reducción de gastos no es suficiente para compensar su bajo desempeño en ventas y facturación. Un costo de envío eficiente pierde relevancia si el volumen de negocio que lo acompaña es mínimo.

4. **Calificación de Cliente**: Si bien su calificación promedio es intermedia, no es lo suficientemente alta como para compensar su debilidad en ingresos y volumen.

## 🛠️ Posibles Mejoras y Extensiones

### Análisis Adicionales Sugeridos
- **Análisis Temporal:** Tendencias de ventas por período
- **Segmentación de Clientes:** Clustering por comportamiento
- **Análisis Predictivo:** Forecasting de ingresos futuros
- **Análisis de Correlación:** Relación entre variables
- **A/B Testing:** Comparación estadística entre tiendas


## 🚨 Limitaciones y Consideraciones

### Variables Disponibles en el Dataset
El dataset contiene **13 columnas** con información detallada:
- **Producto, Categoría del Producto, Precio** (métricas de producto)
- **Costo de envío, Fecha de Compra** (métricas operativas)
- **Vendedor, Lugar de Compra** (información geográfica)
- **Calificación** (satisfacción del cliente)
- **Método de pago, Cantidad de cuotas** (información financiera)
- **lat, lon** (coordenadas geográficas)
- **Tienda** (identificador de tienda)

### Limitaciones del Análisis Actual
- **Análisis temporal limitado:** No se exploró la evolución temporal de ventas por fechas
- **Información geográfica no utilizada:** Coordenadas lat/lon disponibles pero no analizadas
- **Segmentación de vendedores:** No se analizó el rendimiento por vendedor individual
- **Análisis de métodos de pago:** Patrones de pago no explorados
- **Métricas financieras faltantes:** ROI, margen de ganancia neta, costos operativos totales

### Oportunidades de Análisis Futuro
- **Análisis geoespacial:** Utilizar coordenadas para mapeo de ventas
- **Análisis temporal:** Tendencias estacionales y patrones de crecimiento
- **Segmentación de clientes:** Análisis por método de pago y ubicación
- **Performance de vendedores:** Evaluación individual de equipo de ventas
- **Análisis de cuotas:** Impacto del financiamiento en las ventas

### Supuestos del Análisis
- Datos representativos del período 2020-2023 (basado en fechas observadas)
- Homogeneidad en estructura de costos operativos entre tiendas
- Calificaciones reflejan satisfacción real del cliente
- Precios incluyen todos los costos para el cliente final


## 👨‍💻 Información del Desarrollador

**Jazmín Fuentes**
- **GitHub:** [@jazminfuentesb](https://github.com/jazminfuentesb)
- **LinkedIn:** [https://www.linkedin.com/in/jazmin-fuentes/]
- **Email:** [jazminfuentes.1213@gmail.com]

### Competencias Técnicas Demostradas
- **Python Programming:** Pandas, NumPy, Matplotlib
- **Data Analysis:** EDA, Statistical Analysis, KPI Development
- **Business Intelligence:** Strategic Decision Making, ROI Analysis
- **Visualization:** Data Storytelling, Dashboard Creation
- **Problem Solving:** Business Problem Translation to Technical Solution

---

**🎯 Challenge Status:** ✅ Completado  
**📊 Analysis Type:** Exploratory Data Analysis (EDA)  
**🏆 Business Impact:** Strategic Decision Support System  

---
*Desarrollado como parte del programa Alura Latam - Challenge Data Science*
