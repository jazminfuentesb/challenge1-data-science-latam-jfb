# 📊 Análisis de Rendimiento Empresarial - AluraStore Challenge

## 🎯 Descripción del Proyecto

Proyecto de **Data Science** desarrollado como parte del Challenge Alura Latam, enfocado en el análisis exhaustivo de datos empresariales para la toma de decisiones estratégicas. Implementa técnicas de análisis exploratorio de datos (EDA) y visualización para evaluar el rendimiento de cuatro tiendas y determinar cuál presenta menor viabilidad comercial.

**Problema de Negocio:** Optimizar la cartera de tiendas identificando la unidad de negocio con menor rentabilidad para su potencial venta.

## 🔧 Tecnologías y Dependencias

### Entorno de Desarrollo
- **Python 3.8+**
- **Jupyter Notebook** / **Google Colab**

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
├── data/                          # Datos del proyecto (si aplicable)
│   ├── tienda1.csv               # Dataset Tienda 1
│   ├── tienda2.csv               # Dataset Tienda 2  
│   ├── tienda3.csv               # Dataset Tienda 3
│   └── tienda4.csv               # Dataset Tienda 4
└── images/                        # Visualizaciones generadas
    ├── ingresos_comparativa.png
    ├── ventas_categoria.png
    └── costos_envio.png
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

```python
# 1. Carga y Exploración de Datos
def load_and_explore_data():
    # Carga de datasets por tienda
    # Exploración inicial: shape, info(), describe()
    
# 2. Análisis de Facturación
def analyze_revenue():
    # Cálculo de ingresos totales por tienda
    # Identificación de outliers financieros
    
# 3. Análisis Categórico
def analyze_categories():
    # Distribución de ventas por categoría
    # Análisis comparativo entre tiendas
    
# 4. Análisis de Satisfacción
def analyze_customer_satisfaction():
    # Métricas de calificación promedio
    # Análisis de distribución de ratings
    
# 5. Análisis de Productos
def analyze_products():
    # Ranking de productos más/menos vendidos
    # Análisis de rendimiento por producto
    
# 6. Análisis de Costos Operativos
def analyze_operational_costs():
    # Evaluación de eficiencia logística
    # Comparativa de costos de envío
```

### Técnicas de Data Science Aplicadas

- **Análisis Exploratorio de Datos (EDA)**
- **Agregaciones y Groupby Operations**
- **Análisis Estadístico Descriptivo**
- **Visualización de Datos Multidimensional**
- **Análisis Comparativo de KPIs**

## 📈 Resultados Clave y KPIs

### Métricas Principales Evaluadas

| KPI | Descripción | Método de Cálculo |
|-----|-------------|-------------------|
| **Revenue Total** | Ingresos por tienda | `df['Precio'].sum()` |
| **Avg. Customer Rating** | Satisfacción promedio | `df['Calificación'].mean()` |
| **Shipping Cost Efficiency** | Costo logístico promedio | `df['Costo de envío'].mean()` |
| **Product Performance** | Ranking de productos | `df['Producto'].value_counts()` |
| **Category Distribution** | Distribución por categoría | `df.groupby('Categoría').size()` |

### Hallazgos Técnicos

```python
# Resultado del análisis financiero
revenue_results = {
    'Tienda 1': 1150880400.00,  # Líder en facturación
    'Tienda 2': 1116343500.00,  # 2º lugar (-3.0%)
    'Tienda 3': 1098019600.00,  # 3º lugar (-4.6%)
    'Tienda 4': 1038375700.00   # Menor rendimiento (-9.8%)
}

# Eficiencia operativa detectada
shipping_efficiency = {
    'Tienda 4': 23459.46,  # Más eficiente
    'Tienda 3': 24805.68,  # 2º lugar
    'Tienda 2': 25216.24,  # 3º lugar  
    'Tienda 1': 26018.61   # Menos eficiente
}
```

## 🔍 Análisis Técnico de la Decisión

### Algoritmo de Recomendación Implementado

```python
def business_recommendation_algorithm(revenue_data, satisfaction_data, 
                                    cost_data, weights={'revenue': 0.7, 
                                                       'satisfaction': 0.2, 
                                                       'efficiency': 0.1}):
    """
    Algoritmo ponderado para recomendación de tienda a vender
    Prioriza métricas financieras sobre operativas
    """
    scores = {}
    for store in revenue_data.keys():
        weighted_score = (
            revenue_data[store] * weights['revenue'] +
            satisfaction_data[store] * weights['satisfaction'] +
            (1/cost_data[store]) * weights['efficiency']  # Inversión para costos
        )
        scores[store] = weighted_score
    
    return min(scores, key=scores.get)  # Tienda con menor score ponderado
```

### Conclusión Técnica

**Output del Análisis:** `Tienda 4` identificada como candidata óptima para venta.

**Justificación Algorítmica:**
- **Revenue Gap:** -9.8% vs líder (factor determinante)
- **Operational Efficiency:** +10.9% vs promedio (no compensa gap financiero)
- **Customer Satisfaction:** 4.00/5 (dentro del rango aceptable)

## 🛠️ Posibles Mejoras y Extensiones

### Análisis Adicionales Sugeridos
- **Análisis Temporal:** Tendencias de ventas por período
- **Segmentación de Clientes:** Clustering por comportamiento
- **Análisis Predictivo:** Forecasting de ingresos futuros
- **Análisis de Correlación:** Relación entre variables
- **A/B Testing:** Comparación estadística entre tiendas

### Optimizaciones Técnicas
```python
# Implementaciones futuras sugeridas
def advanced_analytics():
    # Time series analysis
    # Customer segmentation (K-means)
    # Revenue forecasting (ARIMA/Prophet)
    # Statistical significance testing
```

## 🚨 Limitaciones y Consideraciones

### Limitaciones del Dataset
- **Datos transversales:** Sin componente temporal
- **Variables limitadas:** Ausencia de costos operativos detallados
- **Métricas faltantes:** ROI, margen de ganancia, costos fijos

### Supuestos del Análisis
- Datos representativos del período analizado
- Homogeneidad en estructura de costos entre tiendas
- Estabilidad de patrones de consumo

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
