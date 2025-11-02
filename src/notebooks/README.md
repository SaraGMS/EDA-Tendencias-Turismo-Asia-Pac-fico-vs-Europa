# 🌍 Análisis Exploratorio de Datos: Tendencias del Turismo Mundial

## 📌 Descripción del Proyecto

Este proyecto realiza un **Análisis Exploratorio de Datos (EDA)** completo sobre las tendencias del turismo mundial, con especial enfoque en la comparación entre **Europa** y **Asia-Pacífico** durante el período 1995-2024.

### 🎯 Hipótesis Principal
> **"Desde hace algunos años, se prefiere viajar al sudeste asiático que a Europa"**

Esta hipótesis surge de la observación de que viajar a países asiáticos se ha vuelto más popular debido a factores como:
- Cultura y naturaleza exóticas
- Mayor asequibilidad económica para estadías prolongadas
- Tendencias de trabajo remoto y estilo de vida freelance

---

## 📊 Datos y Fuente

### 🔗 Fuente de Datos
- **Organización:** UN Tourism (Organización Mundial del Turismo de las Naciones Unidas)
- **Dataset:** Inbound Tourism - Arrivals by Region (1995-2024)
- **URL:** [UN Tourism Statistics Database](https://www.untourism.int/tourism-statistics/tourism-data-inbound-tourism)
- **Última actualización:** 15 de octubre de 2025

### 📋 Variables del Dataset
- `reporter_area_label`: País/región reportante
- `partner_area_label`: Región de origen de los turistas
- `year`: Año del registro (1995-2024)
- `value`: Número de llegadas turísticas
- `indicator_label`: Descripción del indicador
- `flag`: Códigos de calidad de datos

---

## 🛠️ Tecnologías Utilizadas

### 📦 Librerías Python
```python
pandas                 # Manipulación y análisis de datos
numpy                  # Operaciones numéricas
matplotlib             # Visualización de datos
seaborn               # Visualización estadística avanzada
scipy                 # Análisis estadístico
```

### 🔧 Herramientas
- **Jupyter Notebook** - Desarrollo y análisis
- **Python 3.x** - Lenguaje de programación
- **Git** - Control de versiones

---

## 📁 Estructura del Proyecto

```
EDA_Sara_Gil/
├── README.md                     # Documentación del proyecto
├── src/
│   ├── memoria.ipynb            # Notebook principal con análisis EDA
│   ├── tourism_dashboard.py     #  # Datos procesados
│   ├── data/
│   │   └── UN_Tourism_inbound_arrivals_by_region_10_2025.csv
│   ├── notebooks/               # Notebooks adicionales
│   └── utils/                   # Funciones auxiliares
```

---

## 🔍 Análisis Realizados

### 1. 🧹 **Data Cleaning & Preprocessing**
- Eliminación de valores nulos y duplicados
- Corrección de clasificaciones regionales
- Normalización de datos temporales
- Validación de integridad de datos

### 2. 📈 **Análisis Descriptivo**
- **Estadísticas descriptivas completas**
  - Media, mediana, moda
  - Desviación estándar, asimetría, curtosis
  - Análisis de distribuciones por región

### 3. 🌍 **Análisis Regional Comparativo**

#### 🇪🇺 **Europa:**
- **34 países** analizados
- **24.4M llegadas totales** (2015-2024)
- **41.38%** del turismo mundial
- **Crecimiento promedio:** 4.84% anual (2015-2019)

#### 🌏 **Asia-Pacífico:**
- **16 países** analizados
- **10.8M llegadas totales** (2015-2024)
- **18.27%** del turismo mundial
- **Crecimiento promedio:** 6.14% anual (2015-2019)

### 4. 📊 **Análisis Temporal**
- **Evolución histórica 1995-2024**
- **Análisis pre-COVID (2015-2019)**
- **Impacto COVID-19 (2020-2021)**
- **Recuperación post-COVID (2022-2024)**

### 5. 🔬 **Análisis Estadístico Avanzado**

#### **Tests de Hipótesis:**
- **Test Chi-cuadrado:** Independencia región-período
  - χ² = 482,193.38
  - p-valor ≈ 0.00
  - **Resultado:** Dependencia significativa confirmada

- **Test t de Student:** Comparación de medias
  - p-valor = 0.1720
  - **Resultado:** No significativo estadísticamente

- **Test Mann-Whitney U:** Comparación no paramétrica
  - p-valor = 0.2429
  - **Resultado:** No significativo estadísticamente

---

## 🎨 Visualizaciones Creadas

### 📊 **Gráficos Principales**
1. **Evolución Temporal** - Líneas de tiempo por región
2. **Comparación de Totales** - Gráficos de barras
3. **Distribuciones** - Histogramas con KDE
4. **Variabilidad** - Box plots comparativos
5. **Intervalos de Confianza** - Análisis de incertidumbre
6. **Correlaciones** - Matrices de correlación
7. **Top Countries** - Rankings por región

### 🎯 **Dashboard Interactivo**
- **Streamlit App** con visualizaciones dinámicas
- Filtros por región, país y período temporal
- Métricas en tiempo real
- Gráficos interactivos

---

## 📋 Principales Hallazgos

### ✅ **Conclusiones Confirmadas**
1. **Asia-Pacífico muestra mayor crecimiento** (6.14% vs 4.84%)
2. **Europa mantiene mayor volumen absoluto** de turistas
3. **Diferencias significativas** en patrones de recuperación post-COVID
4. **Asia-Pacífico es más vulnerable** a crisis globales

### ❌ **Hipótesis No Confirmada Estadísticamente**
- Aunque Asia-Pacífico creció más rápido, **la diferencia no es estadísticamente significativa**
- Los intervalos de confianza se solapan
- p-valores > 0.05 en tests de medias

### 🦠 **Impacto COVID-19**
- **Europa:** -65.4% reducción (más resiliente)
- **Asia-Pacífico:** -92.1% reducción (mayor impacto)
- **Recuperación:** Europa más rápida, Asia-Pacífico aún rezagada

---

## 🚀 Cómo Ejecutar el Proyecto

### 📥 **Instalación**
```bash
# Clonar el repositorio
git clone [URL-del-repositorio]

# Navegar al directorio
cd "EDA Sara Gil"

# Instalar dependencias
pip install pandas numpy matplotlib seaborn scipy streamlit jupyter
```

### 🎮 **Ejecución**

#### **Notebook Jupyter:**
```bash
jupyter notebook src/memoria.ipynb
```

#### **Dashboard Streamlit:**
```bash
streamlit run src/tourism_dashboard.py
```

---

## 📖 Documentación Adicional

### 📚 **Recursos**
- [UN Tourism Statistics](https://www.untourism.int/tourism-statistics/)
- [Metodología EDA](https://www.kaggle.com/learn/data-visualization)
- [Documentación Pandas](https://pandas.pydata.org/docs/)

### 🤝 **Contacto**
- **Autora:** Sara Gil
- **Proyecto:** EDA Turismo Mundial 2025
- **Institución:** The Bridge - Bootcamp Data Science

---

## 📄 Licencia

Este proyecto está bajo la Licencia MIT. Los datos utilizados pertenecen a UN Tourism y se utilizan con fines educativos.

---

## 🔄 Actualizaciones

- **v1.0** (Nov 2025): Análisis inicial completo
- **v1.1** (Nov 2025): Dashboard Streamlit añadido
- **v1.2** (Nov 2025): Tests estadísticos avanzados

---

*Proyecto desarrollado como parte del Bootcamp de Data Science en The Bridge (2025)*