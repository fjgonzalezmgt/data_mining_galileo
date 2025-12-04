# Instrucciones para Obtener el Dataset

Este proyecto requiere el archivo `data.csv` para funcionar correctamente. El archivo no está incluido en el repositorio por razones de tamaño y distribución.

## Cómo obtener el dataset

### Opción 1: Descarga desde UCI Machine Learning Repository (Recomendada)

1. Visita: https://archive.ics.uci.edu/ml/datasets/Breast+Cancer+Wisconsin+(Diagnostic)
2. Descarga el archivo `wdbc.data`
3. **Importante**: El archivo `wdbc.data` no tiene encabezados de columna. Necesitarás agregárselos o usar la Opción 2 que lo hace automáticamente.
4. Renombra el archivo como `data.csv`
5. Coloca el archivo en el directorio raíz del proyecto (mismo nivel que este archivo)

### Opción 2: Descarga automática con R (Recomendada)

Ejecuta este código en R desde el directorio del proyecto. Esta opción descarga el dataset y agrega los encabezados de columna correctos:

```r
# Descargar el dataset
url <- "https://archive.ics.uci.edu/ml/machine-learning-databases/breast-cancer-wisconsin/wdbc.data"
download.file(url, "wdbc.data")

# Leer el archivo sin encabezados
data <- read.csv("wdbc.data", header = FALSE)

# Agregar nombres de columnas según la documentación del dataset
colnames(data) <- c("id", "diagnosis", 
                    "radius_mean", "texture_mean", "perimeter_mean", "area_mean", 
                    "smoothness_mean", "compactness_mean", "concavity_mean", 
                    "concave.points_mean", "symmetry_mean", "fractal_dimension_mean",
                    "radius_se", "texture_se", "perimeter_se", "area_se", 
                    "smoothness_se", "compactness_se", "concavity_se", 
                    "concave.points_se", "symmetry_se", "fractal_dimension_se",
                    "radius_worst", "texture_worst", "perimeter_worst", "area_worst", 
                    "smoothness_worst", "compactness_worst", "concavity_worst", 
                    "concave.points_worst", "symmetry_worst", "fractal_dimension_worst")

# Guardar con encabezados correctos
write.csv(data, "data.csv", row.names = FALSE)

# Limpiar archivo temporal
file.remove("wdbc.data")

# Verificar
if (file.exists("data.csv")) {
  cat("¡Dataset descargado exitosamente con encabezados correctos!\n")
  cat("Tamaño del archivo:", file.size("data.csv"), "bytes\n")
  cat("Número de filas:", nrow(data), "\n")
} else {
  cat("Error al crear el dataset\n")
}
```

### Opción 3: Usar dataset desde mlbench (Solo para pruebas)

⚠️ **Advertencia**: El dataset BreastCancer de mlbench tiene una estructura diferente y columnas distintas. Esto causará errores con el código existente en `Proyecto.qmd`. Use esta opción solo para pruebas y tenga en cuenta que necesitará modificar el código del proyecto.

```r
# NOTA: Esta opción no es compatible sin modificar Proyecto.qmd
# Instalar el paquete si no lo tienes
if (!require("mlbench")) install.packages("mlbench")

# Cargar el dataset
library(mlbench)
data(BreastCancer)

# Guardar como CSV
write.csv(BreastCancer, "data_mlbench.csv", row.names = FALSE)

cat("Dataset de mlbench guardado como data_mlbench.csv\n")
cat("ADVERTENCIA: Este dataset tiene estructura diferente al esperado.\n")
cat("Se recomienda usar la Opción 2 para compatibilidad completa.\n")
```

## Verificación

Una vez que hayas obtenido el archivo `data.csv`, deberías poder ver:

- Un archivo llamado `data.csv` en el directorio raíz
- El archivo debe contener datos sobre características de tumores mamarios
- Aproximadamente 569 filas de datos

## Estructura Esperada del Dataset

El dataset debe contener las siguientes columnas:

- `id`: Identificador único
- `diagnosis`: Diagnóstico (M = Maligno, B = Benigno)
- Variables de características morfológicas (radius, texture, perimeter, area, smoothness, compactness, concavity, concave.points, symmetry, fractal_dimension)
- Cada característica tiene tres variantes: mean, se (error estándar), y worst

## Problemas Comunes

- **Error: "No such file or directory"**: Asegúrate de que `data.csv` está en el directorio raíz del proyecto
- **Error al leer el archivo**: Verifica que el archivo esté en formato CSV válido
- **Datos faltantes**: Algunos datasets pueden requerir limpieza adicional

## Referencias

- Wisconsin Breast Cancer Dataset: https://archive.ics.uci.edu/ml/datasets/Breast+Cancer+Wisconsin+(Diagnostic)
- Documentación del dataset: https://archive.ics.uci.edu/ml/machine-learning-databases/breast-cancer-wisconsin/wdbc.names

---

**Nota**: Si continúas teniendo problemas para obtener el dataset, abre un issue en el repositorio.
