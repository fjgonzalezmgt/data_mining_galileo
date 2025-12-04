# Contribuyendo al Proyecto

¡Gracias por tu interés en contribuir a este proyecto de análisis de datos sobre tumores mamarios! 🎉

## Cómo Contribuir

### Reportar Problemas

Si encuentras un bug o tienes una sugerencia para mejorar el proyecto:

1. Verifica que el problema no haya sido reportado previamente en [Issues](https://github.com/fjgonzalezmgt/data_mining_galileo/issues)
2. Abre un nuevo issue describiendo claramente:
   - El problema o sugerencia
   - Pasos para reproducir (si es un bug)
   - El comportamiento esperado
   - Capturas de pantalla (si aplica)

### Proponer Cambios

Para contribuir con código o análisis:

1. **Fork** el repositorio
2. Crea una rama para tu contribución (`git checkout -b feature/nueva-caracteristica`)
3. Realiza tus cambios siguiendo las guías de estilo
4. Asegúrate de que el código funcione correctamente
5. Commit tus cambios con mensajes descriptivos (`git commit -m 'Añadir nueva visualización de correlaciones'`)
6. Push a tu rama (`git push origin feature/nueva-caracteristica`)
7. Abre un **Pull Request**

## Guías de Estilo

### Código R

- Usa nombres de variables descriptivos en español o inglés (consistente)
- Comenta las secciones complejas del código
- Sigue las convenciones de [tidyverse style guide](https://style.tidyverse.org/)
- Usa indentación de 2 espacios

### Quarto/Markdown

- Usa encabezados jerárquicos apropiados (H1, H2, H3, etc.)
- Incluye descripciones claras para gráficos y tablas
- Asegúrate de que el documento se renderice correctamente antes de hacer commit

### Commits

- Usa mensajes de commit claros y descriptivos en español
- Usa tiempo presente ("Añadir característica" no "Añadida característica")
- Referencia issues relevantes cuando aplique (#123)

## Configuración del Entorno de Desarrollo

### Requisitos Previos

- R (versión 4.0 o superior)
- RStudio (recomendado)
- Quarto CLI

### Instalación de Dependencias

```r
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

### Obtener el Dataset

El archivo `data.csv` debe obtenerse del [Wisconsin Breast Cancer Dataset](https://archive.ics.uci.edu/ml/datasets/Breast+Cancer+Wisconsin+(Diagnostic)) o de la fuente original utilizada en el proyecto. Colócalo en el directorio raíz del proyecto.

### Ejecutar el Proyecto

```bash
quarto render Proyecto.qmd
```

## Tipos de Contribuciones Bienvenidas

- 🐛 Corrección de bugs
- 📊 Nuevas visualizaciones de datos
- 🤖 Mejoras en modelos de machine learning
- 📝 Mejoras en documentación
- ✅ Adición de tests
- 🌐 Traducciones
- 💡 Nuevas ideas y características

## Proceso de Revisión

- Todas las contribuciones serán revisadas por el mantenedor del proyecto
- Se puede solicitar cambios o aclaraciones
- Una vez aprobado, tu contribución será fusionada

## Preguntas

Si tienes preguntas sobre cómo contribuir, no dudes en abrir un issue o contactar al mantenedor del proyecto.

## Código de Conducta

Este proyecto sigue un Código de Conducta. Al participar, se espera que mantengas un ambiente respetuoso y colaborativo. Por favor, consulta [CODE_OF_CONDUCT.md](CODE_OF_CONDUCT.md) para más detalles.

---

**¡Gracias por contribuir al avance de la investigación del cáncer de mama! ❤️**
