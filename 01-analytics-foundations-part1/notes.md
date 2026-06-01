# Fundamentos de Análisis en AWS - Parte 1

> **Estado:** 🔄 En progreso  
> **Duración total:** 2h  
> **Idioma del curso:** Español (LATAM)  
> **Completado el:** -  
> **Avance:** Lecciones 1-5 completadas

---

## Qué aprendí hoy

El curso introduce los conceptos base del análisis de datos y cómo AWS los aborda. Aprendí que el análisis no es solo "revisar datos", sino un proceso con tipos bien definidos según el objetivo. También entendí la diferencia entre análisis, ML e IA generativa, y por qué los macrodatos presentan desafíos que las bases de datos tradicionales no pueden resolver.

---

## Conceptos clave

### ¿Qué es el análisis?

- **Análisis:** proceso de usar herramientas y técnicas especializadas para encontrar nuevo valor a partir de datos sin procesar.
- **Análisis de datos:** práctica de interpretar datos que lleva a decisiones significativas.
- Sin análisis, las empresas toman decisiones basadas en intuición y suerte. Con análisis, las decisiones se basan en evidencia.

---

### Los 4 tipos de análisis

| Tipo | Pregunta que responde | Técnicas principales |
|------|----------------------|---------------------|
| **Descriptivo** | ¿Qué ocurrió? | Gráficos, tablas, narrativas generadas |
| **Diagnóstico** | ¿Por qué ocurrió? | Minería de datos, correlaciones, análisis detallado |
| **Predictivo** | ¿Qué podría suceder? | ML, previsión, modelado predictivo |
| **Prescriptivo** | ¿Qué debería hacer? | Simulación, redes neuronales, motores de recomendación |

---

### Machine Learning (ML)

- **ML** es un subconjunto de la IA.
- Los modelos de ML aprenden de datos y mejoran su precisión a través del **entrenamiento** (procesar datos múltiples veces).
- Se vuelven más precisos con más datos y más iteraciones.
- Ejemplo real: Amazon.com recomienda productos según historial de compras → eso es ML en producción.

#### Los 3 niveles de ML en AWS

| Nivel | Para quién | Qué ofrece |
|-------|-----------|------------|
| **Servicios de IA** | Desarrolladores sin experiencia en ML | APIs listas para usar, sin conocimiento de ML requerido |
| **Servicios de ML** | Desarrolladores que quieren personalizar | Herramientas optimizadas para ML personalizado |
| **Marcos e infraestructura** | Profesionales de ML | Control total para crear, entrenar y desplegar modelos propios |

---

### IA Generativa en AWS

- **IA Generativa:** tipo de ML que crea contenido nuevo (texto, imágenes, video, música) a partir de instrucciones del usuario.
- Usa **aprendizaje profundo** y **redes neuronales artificiales** que imitan la estructura del cerebro humano.
- Se basa en **modelos fundacionales**: modelos grandes preentrenados con cantidades masivas de datos.
- Diferencia clave con ML tradicional: el ML predice, la IA gen **crea contenido original**.

---

### Amazon Q Developer

- Servicio de generación de código que analiza tu código mientras escribes.
- Usa **procesamiento de lenguaje natural** para entender comentarios en inglés y generar funciones completas.
- Incluye **escaneo de seguridad** que detecta vulnerabilidades en el código generado y el escrito por el desarrollador.
- Compatible con VS Code y JetBrains (mis IDEs actuales ✅).
- Soporta más de 15 lenguajes de programación, incluyendo Java y Python.

---

### Las 5 V de los Macrodatos (Big Data)

- **Macrodatos:** datos que se almacenan rápidamente de varias fuentes, tienen tamaño enorme, y son complicados de proteger, analizar y extraer valor.
- Los sistemas tradicionales de bases de datos NO pueden resolver estos desafíos. Se necesitan soluciones especializadas.

| V | Desafío | Pregunta clave |
|---|---------|----------------|
| **Volumen** | Cantidad masiva de datos | ¿Cómo almaceno todo esto? |
| **Variedad** | Múltiples tipos y formatos de datos | ¿Cómo proceso datos tan distintos? |
| **Velocidad** | Rapidez de generación y procesamiento | ¿Proceso en tiempo real o en lotes? |
| **Veracidad** | Calidad y confiabilidad de los datos | ¿Mis datos son confiables? |
| **Valor** | Información útil extraída de los datos | ¿Qué decisión tomo con esto? |

---

## Conexión con mis proyectos

- **RAG Chatbot:** Procesa consultas de usuarios en tiempo real → desafío de **Velocidad**. La calidad de los documentos que usa el chatbot es un desafío de **Veracidad**.


---
## Progreso de lecciones

- [x] Lección 1: Introducción y conceptos generales
- [x] Lección 2: Análisis (tipos y técnicas)
- [x] Lección 3: Machine Learning
- [x] Lección 4: IA Generativa y Amazon Q Developer
- [x] Lección 5: Las 5 V de los macrodatos
- [ ] Lección 6: Volumen y servicios AWS
- [ ] Lección 7: Variedad y servicios AWS
- [ ] Lección 8: Velocidad y servicios AWS
- [ ] Lección 9: Veracidad y servicios AWS
- [ ] Lección 10: Valor y servicios AWS
- [ ] Conclusión y cuestionario final