# posologia_ddd_ia
Uso de Azure OpenAI con modelos LLM para evaluar posologías farmacéuticas y transformarlas a DDD (Dosis Diaria Definida) mediante razonamiento automatizado.
Uso de Azure OpenAI con modelos LLM que actúan como juez para evaluar posologías farmacéuticas y calcular su DDD (Dosis Diaria Definida). El LLM no determina la veracidad de los datos, sino que evalúa la concordancia entre la posología y la referencia DDD, gestionando diferencias de formato, unidades y tolerancias, y generando automáticamente una justificación razonada mediante prompt junto con una puntuación asociada. La solución se ejecuta sobre SAS Viya, permitiendo escalabilidad para grandes volúmenes de datos.
El sistema genera automáticamente:
- Resultados normalizados en tres formatos: DDD_azure (ej. 30 mg), DDD_azure_numero (ej. 30) y DDD_azure_unidad (ej. mg)
- Justificación detallada de la evaluación frente al valor esperado
- Puntuación multicriterio del 1 al 10 basada en corrección factual
- Estado final: correcto o incorrecto
