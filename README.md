# 🧪 Análisis de Comportamiento de Usuario mediante Embudo de Conversión y Test A/A/B para aplicación de productos alimenticios
## 🎯 Objetivo
Investigar el comportamiento de los usuarios dentro de la aplicación de una empresa emergente de productos alimenticios, con dos propósitos principales:
- Analizar el embudo de conversión para identificar puntos críticos de abandono.
- Evaluar el impacto de un cambio tipográfico mediante un test A/A/B, determinando si el nuevo diseño afecta la experiencia del usuario.

## ⚙️ Metodología
- Se utilizó un archivo que contiene registros de eventos de usuario con información sobre acciones, timestamp y grupo experimental.
- Se renombraron las columnas para facilitar el análisis. 
- Se eliminaron registros duplicados, asegurando que cada fila represente un evento único.
- Se transformó el tipo de datos. 
- Se excluyeron eventos debido a inconsistencias en los datos. Esto permitió trabajar con un periodo confiable.
- Se analizaron los eventos más frecuentes y se construyó el embudo de conversión.
- Se realizaron pruebas estadísticas para comparar los grupos experimentales, tanto de forma individual como combinada.

## 📊 Resultados
### Embudo de conversión
| Evento                   | Usuarios únicos | Proporción sobre total |
|--------------------------|------------------|-------------------------|
| MainScreenAppear         | 7,429            | 98.5%                   |
| CartScreenAppear         | 3,742            | 49.6%                   |
| PaymentScreenSuccessful  | 3,542            | 46.9%                   |

- MainScreen → CartScreen: 49% de conversión  
- CartScreen → Pago: 95% de conversión  
- Usuarios que completan todo el recorrido: 3,446 (46.39%)
📌 La mayor pérdida ocurre en la transición de pantalla principal al carrito.

### Test A/A/B
- Los grupos de control (246 y 247) mostraron diferencias iniciales significativas (t = -10.28, p = 0.0000), lo que sugiere posibles sesgos de muestreo.
- Sin embargo, en los eventos clave, los grupos se comportaron de forma uniforme.
- El grupo experimental (248) mostró diferencias frente a los controles individuales, pero no frente a los controles combinados (p = 1.0000 en todos los eventos).
- Las proporciones de participación en eventos fueron muy similares entre todos los grupos.

## 🧾 Conclusiones
- La exclusión de registros inconsistentes fortaleció la confiabilidad del análisis.
- El embudo revela que el principal desafío está en la etapa inicial (MainScreen → CartScreen), donde se pierde el 51% de los usuarios.
- El proceso de pago es eficiente, con una tasa de conversión del 95% desde el carrito.
- Aunque hubo diferencias iniciales entre los grupos de control, el comportamiento frente a los eventos fue uniforme, validando la segmentación experimental.
- Las fuentes alteradas no generaron diferencias significativas frente a los controles combinados, lo que indica que el rediseño tipográfico no afecta negativamente la experiencia del usuario.

## ✅ Recomendaciones
1. Optimizar la pantalla principal para mejorar la transición hacia el carrito, mediante mejoras en diseño, navegación y personalización.
2. Implementar el nuevo diseño tipográfico, ya que no genera fricción ni pérdida de usuarios.
3. Mantener el nivel de significancia en 0.05 y aplicar correcciones por múltiples pruebas en futuros experimentos.
4. Continuar con pruebas iterativas, enfocadas en retención, navegación y conversión.

## 🌟 Aclaraciones
Incluye observaciones de revisión realizadas durante el bootcamp. Refleja tanto el enfoque técnico como la evolución del análisis con base en feedback experto.
