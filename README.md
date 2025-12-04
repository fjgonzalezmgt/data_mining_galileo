# Proyecto DATA MINING AND BIG DATA - Universidad Galileo

![R](https://img.shields.io/badge/R-276DC3?style=for-the-badge&logo=r&logoColor=white)
![Quarto](https://img.shields.io/badge/Quarto-75AADB?style=for-the-badge&logo=quarto&logoColor=white)
![Tidyverse](https://img.shields.io/badge/Tidyverse-1A162D?style=for-the-badge&logo=tidyverse&logoColor=white)
![Machine Learning](https://img.shields.io/badge/Machine_Learning-FF6F00?style=for-the-badge&logo=tensorflow&logoColor=white)
![License](https://img.shields.io/badge/License-CC0_1.0-lightgrey.svg?style=for-the-badge)

## 📋 Descripción

Proyecto de minería de datos desarrollado para la Universidad Galileo, enfocado en el análisis y clasificación de tumores mamarios utilizando técnicas de aprendizaje automático. El objetivo principal es predecir si un tumor es **Benigno (B)** o **Maligno (M)** basándose en características morfológicas de células tumorales.

**Autor:** Francisco Gonzalez  
**Carnet:** 24002914

## 🎯 Objetivo del Proyecto

Desarrollar y evaluar modelos de clasificación para predecir el diagnóstico de tumores mamarios mediante el análisis de características morfológicas de células tumorales extraídas de imágenes digitalizadas.

### Metas Específicas

1. **Identificación de Características Relevantes**: Determinar qué variables tienen mayor impacto en el diagnóstico
2. **Construcción de Modelos Predictivos**: Entrenar modelos como Logistic Regression, SVM, Random Forest y KNN
3. **Evaluación del Rendimiento**: Comparar modelos usando métricas como exactitud, sensibilidad, especificidad y precisión
4. **Optimización de la Clasificación**: Seleccionar el modelo más confiable para ayudar en el diagnóstico clínico

## 📊 Dataset

El dataset contiene variables relacionadas con las características morfológicas de células tumorales:

### Variables Principales

- **`diagnosis`**: Variable objetivo (B = Benigno, M = Maligno)
- **`radius_*`**: Radio de las células (tamaño del tumor)
- **`texture_*`**: Variación en la intensidad de la textura
- **`perimeter_*`**: Perímetro de las células
- **`area_*`**: Área de las células
- **`smoothness_*`**: Uniformidad del contorno celular
- **`compactness_*`**: Grado de compacidad celular
- **`concavity_*`**: Grado de concavidad en el contorno
- **`concave.points_*`**: Número de puntos cóncavos
- **`symmetry_*`**: Simetría de las células
- **`fractal_dimension_*`**: Dimensión fractal del contorno

Para cada característica se calculan tres tipos de mediciones: **Mean** (promedio), **SE** (error estándar), y **Worst** (valor más extremo).

## 🛠️ Tecnologías Utilizadas

### Lenguajes y Frameworks
- **R**: Lenguaje principal de programación
- **Quarto**: Sistema de publicación científica y técnica

### Librerías de R

#### Análisis y Visualización
- `tidyverse`: Conjunto de paquetes para ciencia de datos
- `ggplot2`: Gráficos avanzados y personalizables
- `summarytools`: Resúmenes descriptivos
- `kableExtra`: Creación de tablas atractivas
- `gt`: Generación de tablas bien diseñadas

#### Análisis de Correlación
- `corrplot`: Visualización de matrices de correlación
- `ggcorrplot`: Gráficos de correlación modernos

#### Machine Learning
- `caret`: Framework para aprendizaje automático
- `e1071`: Algoritmos SVM y funciones estadísticas
- `randomForest`: Implementación de Random Forest
- `class`: Métodos de clasificación como KNN

## 🚀 Uso

### Requisitos Previos

- R (versión 4.0 o superior)
- RStudio (recomendado)
- Quarto CLI

### Instalación de Dependencias

```r
# Instalar paquetes necesarios
install.packages(c(
  "tidyverse",
  "summarytools",
  "kableExtra",
  "gt",
  "corrplot",
  "ggcorrplot",
  "caret",
  "e1071",
  "randomForest",
  "class"
))
```

### Ejecución del Proyecto

1. Clonar el repositorio:
```bash
git clone https://github.com/fjgonzalezmgt/data_mining_galileo.git
cd data_mining_galileo
```

2. Asegurarse de que el archivo `data.csv` esté en el directorio raíz

3. Abrir el archivo `Proyecto.qmd` en RStudio

4. Renderizar el documento Quarto:
```r
# En R o RStudio
quarto::quarto_render("Proyecto.qmd")
```

O desde la línea de comandos:
```bash
quarto render Proyecto.qmd
```

## 📈 Análisis Realizados

1. **Análisis Exploratorio de Datos (EDA)**
   - Estadísticas descriptivas
   - Visualización de distribuciones
   - Análisis de correlaciones
   - Detección de valores atípicos

2. **Modelado Predictivo**
   - Regresión Logística
   - Support Vector Machines (SVM)
   - Random Forest
   - K-Nearest Neighbors (KNN)

3. **Evaluación de Modelos**
   - Matriz de confusión
   - Métricas de rendimiento (exactitud, sensibilidad, especificidad, precisión)
   - Validación cruzada

## 🏥 Aplicación Clínica

Este análisis tiene aplicaciones importantes en el diagnóstico clínico del cáncer de mama:

- Ayuda a médicos a clasificar tumores con mayor confianza
- Reduce la necesidad de pruebas invasivas adicionales
- Mejora la atención y los resultados para los pacientes
- Facilita el diagnóstico temprano del cáncer de mama

## 📄 Licencia

Este proyecto está bajo la licencia Creative Commons CC0 1.0 Universal. Ver el archivo [LICENSE.txt](LICENSE.txt) para más detalles.

## 🎓 Universidad Galileo

Proyecto desarrollado como parte del curso de **DATA MINING AND BIG DATA** en la Universidad Galileo, Guatemala.

---

**Desarrollado con ❤️ para avanzar en la investigación del cáncer de mama**
