# Política de Seguridad

## Versiones Soportadas

Este proyecto es un proyecto académico y de investigación. Actualmente estamos trabajando con:

| Versión | Soportada          |
| ------- | ------------------ |
| main    | :white_check_mark: |
| otras   | :x:                |

## Reportar una Vulnerabilidad

La seguridad es importante para nosotros. Si descubres una vulnerabilidad de seguridad en este proyecto, por favor ayúdanos reportándola de manera responsable.

### Cómo Reportar

Para reportar una vulnerabilidad de seguridad:

1. **NO** abras un issue público
2. Envía un correo electrónico al mantenedor del proyecto describiendo la vulnerabilidad
3. Incluye la siguiente información:
   - Tipo de vulnerabilidad
   - Pasos para reproducir el problema
   - Versiones afectadas
   - Impacto potencial
   - Cualquier solución o mitigación sugerida

### Qué Esperar

- **Confirmación**: Confirmaremos la recepción de tu reporte dentro de 48 horas
- **Evaluación**: Evaluaremos la vulnerabilidad y su impacto
- **Actualización**: Te mantendremos informado sobre el progreso
- **Resolución**: Trabajaremos en una solución y la publicaremos

### Prácticas de Seguridad

Para mantener este proyecto seguro:

- ✅ NO cometas datos sensibles (credenciales, tokens, etc.)
- ✅ Usa `.gitignore` para excluir archivos sensibles
- ✅ Mantén las dependencias actualizadas
- ✅ Revisa el código antes de hacer commit
- ✅ Usa variables de entorno para información sensible

### Datos Sensibles

Este proyecto trabaja con datos médicos públicos. Recuerda:

- El dataset de Wisconsin Breast Cancer es público y anónimo
- NO uses datos médicos reales de pacientes sin autorización
- Respeta la privacidad y confidencialidad de los datos médicos
- Cumple con regulaciones como HIPAA si trabajas con datos reales

## Dependencias de Seguridad

Este proyecto usa paquetes de R. Para mantener la seguridad:

1. Mantén R actualizado a la última versión estable
2. Actualiza regularmente los paquetes:
   ```r
   update.packages(ask = FALSE)
   ```
3. Verifica las fuentes de los paquetes que instalas

## Recursos Adicionales

- [Guía de Seguridad de GitHub](https://docs.github.com/en/code-security)
- [OWASP Top 10](https://owasp.org/www-project-top-ten/)
- [Seguridad en Ciencia de Datos](https://www.datasciencelearner.com/data-security-in-data-science/)

---

**Gracias por ayudarnos a mantener este proyecto seguro.**
