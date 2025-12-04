# Instrucciones para Obtener el Dataset

Este proyecto requiere el archivo `data.csv` para funcionar correctamente. El archivo no está incluido en el repositorio por razones de tamaño y distribución.

## Cómo obtener el dataset

### Opción 1: Descarga desde UCI Machine Learning Repository

1. Visita: https://archive.ics.uci.edu/ml/datasets/Breast+Cancer+Wisconsin+(Diagnostic)
2. Descarga el archivo `wdbc.data`
3. Renombra el archivo como `data.csv`
4. Coloca el archivo en el directorio raíz del proyecto (mismo nivel que este archivo)

### Opción 2: Descarga automática con R

Ejecuta este código en R desde el directorio del proyecto:

```r
# Descargar el dataset
url <- "https://archive.ics.uci.edu/ml/machine-learning-databases/breast-cancer-wisconsin/wdbc.data"
download.file(url, "data.csv")

# Verificar que el archivo se descargó correctamente
if (file.exists("data.csv")) {
  cat("¡Dataset descargado exitosamente!\n")
  cat("Tamaño del archivo:", file.size("data.csv"), "bytes\n")
} else {
  cat("Error al descargar el dataset\n")
}
```

### Opción 3: Usar dataset de ejemplo desde el paquete mlbench

Si prefieres usar un dataset ya incluido en paquetes de R:

```r
# Instalar el paquete si no lo tienes
if (!require("mlbench")) install.packages("mlbench")

# Cargar el dataset
library(mlbench)
data(BreastCancer)

# Guardar como CSV
write.csv(BreastCancer, "data.csv", row.names = FALSE)
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
