# Analisis-de-datos-de-una-tienda-online

##Introducción al Analisis

El objetivo de este proyecto es identificar estrategias para aumentar los ingresos de una tienda online mediante dos enfoques complementarios: la priorización de hipótesis y el análisis de una prueba A/B.

En la Parte 1, se trabaja con el archivo hypotheses_us.csv, que contiene nueve hipótesis sobre posibles mejoras. Cada hipótesis incluye estimaciones de Reach (alcance), Impact (impacto), Confidence (confianza) y Effort (esfuerzo). Para priorizarlas, se aplican dos frameworks ampliamente utilizados en la toma de decisiones:

* ICE (Impact, Confidence, Effort): ayuda a identificar iniciativas de alto impacto y alta probabilidad de éxito en relación con el esfuerzo requerido.

* RICE (Reach, Impact, Confidence, Effort): incorpora además el alcance, permitiendo valorar qué tantas personas se verían beneficiadas por cada hipótesis.

Se ordenan las hipótesis según ambos métodos y se comparan los resultados, analizando cómo la introducción del alcance (RICE) modifica la priorización respecto al enfoque ICE.

En la Parte 2, se analiza un experimento A/B con datos de los archivos orders_us.csv y visits_us.csv. El propósito es evaluar si una nueva versión del sitio (grupo B) supera a la actual (grupo A). Para ello se realizan:

* Visualizaciones de ingresos, tamaño de pedido promedio y tasas de conversión.

* Identificación y tratamiento de anomalías mediante percentiles.

* Pruebas de significancia estadística para evaluar las diferencias entre grupos, tanto en datos brutos como filtrados.

El análisis permite extraer conclusiones sobre el desempeño de cada grupo y tomar una decisión fundamentada sobre el futuro de la nueva versión del sitio.

## Conclusiones y conjeturas sobre la significancia estadística de la diferencia en el tamaño promedio de pedido entre los grupos utilizando los datos filtrados.
### Grupo A: 118.2

### Grupo B: 145.13

p-value: 0.7057 (> 0.05)

### Conjeturas principales:

Aunque el grupo B muestra un promedio de pedido mayor (≈ 145 vs 118 en A), la diferencia no es estadísticamente significativa. Esto significa que la variación podría deberse al azar y no a un efecto real del experimento.

Los resultados sugieren que la prueba no aporta evidencia sólida de que el experimento impacte en el tamaño promedio de pedido.

El hecho de que el grupo B tenga un valor mayor podría indicar una tendencia interesante, pero debido al alto p-value (>0.70), no podemos confiar en que se mantenga si se repite la prueba.

Esto contrasta con los resultados de la tasa de conversión, donde sí hubo una diferencia significativa a favor del grupo B.

El experimento probablemente no influye en el valor de cada pedido, pero sí logra incrementar la frecuencia de conversión de usuarios. En otras palabras, los clientes del grupo B compran más seguido, pero no necesariamente gastan más en cada pedido individual.

### Con base en los resultados de la prueba:
* Conversión: el grupo B tiene una tasa de conversión significativamente mayor que el grupo A (p-value < 0.05).

* Tamaño promedio de pedido: no hay diferencia significativa entre los grupos (p-value ≈ 0.70).

* Ingresos totales: dado que la conversión aumenta en B y el ticket promedio no cambia significativamente, es muy probable que los ingresos generales crezcan en B.

### Decisión:

Parar la prueba y considerar al grupo B como líder.

### Justificación:
* Ya existe evidencia estadística suficiente de que el grupo B convierte mejor.

* El valor promedio del pedido no muestra diferencias, lo que significa que el impacto positivo de B se da únicamente en la frecuencia de conversión, lo cual sigue siendo un beneficio real para el negocio.

* Continuar la prueba no aportaría nueva información relevante, y mantenerla implica un costo de oportunidad.


