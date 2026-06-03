# Fundamentos de Análisis en AWS - Parte 1

> **Estado:** 🔄 En progreso  
> **Duración total:** 2h  
> **Idioma del curso:** Español (LATAM)  
> **Completado el:** -  
> **Avance:** Lecciones 1-10 completadas

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

## Servicios de AWS por cada V

### Volumen — ¿Cómo almaceno grandes cantidades de datos?

**El desafío:** Los datos crecen de terabytes a petabytes. Los sistemas
tradicionales no escalan y el costo de ampliarlos es muy alto.

**Tipos de fuentes de datos:**

| Tipo | Ejemplos |
|------|---------|
| **Transaccionales** | Info de clientes, compras en línea, contratos |
| **Temporales** | Movimientos en videojuegos, caché del navegador |
| **Objetos** | Imágenes, videos, correos, contenido de redes sociales |

**Servicios AWS para Volumen:**
- **Amazon S3** → Almacenamiento de objetos escalable. Ideal para datos
  no estructurados (videos, imágenes, archivos).
- **Amazon RDS** → Base de datos relacional administrada en la nube.
- **Amazon Redshift** → Data warehouse para análisis a escala de petabytes.
- **Amazon DynamoDB** → Base de datos NoSQL rápida y altamente escalable.

---

### Variedad — ¿Cómo proceso datos de tipos tan distintos?

**El desafío:** Los datos vienen de múltiples fuentes con estructuras
muy diferentes. Integrarlos y administrarlos es complejo.

**Los 3 tipos de datos:**

| Tipo | Características | Ejemplos | Almacenamiento |
|------|----------------|---------|----------------|
| **Estructurados** | Esquema fijo, tablas con filas y columnas | Registros de suscriptores, transacciones | RDBMS (MySQL, PostgreSQL, Aurora) |
| **Semiestructurados** | Sin esquema estricto, flexible | JSON, XML, CSV, conversaciones de chat | NoSQL (DynamoDB, DocumentDB) |
| **No estructurados** | Sin estructura única, requieren etiquetado | Videos, fotos, PDFs, correos | Data lakes, S3 |

**OLTP vs OLAP — diferencia clave:**

| | OLTP | OLAP |
|--|------|------|
| **Para qué** | Almacenar y escribir datos rápido | Leer y analizar datos |
| **Optimizado para** | Operaciones de escritura | Operaciones de lectura |
| **Ejemplo** | App de compras registrando pedidos | Dashboard analizando ventas del mes |
| **Indexación** | Basada en filas | Basada en columnas |


**Servicios AWS para Variedad:**
- **Amazon Aurora** → RDBMS de alto rendimiento compatible con MySQL y PostgreSQL
- **Amazon RDS** → Bases de datos relacionales administradas
- **Amazon DynamoDB** → NoSQL clave-valor, muy flexible
- **Amazon DocumentDB** → Compatible con MongoDB (semiestructurado)
- **Amazon ElastiCache** → Caché en memoria para rendimiento en tiempo real
- **Amazon Redshift** → Almacenamiento columnar para análisis (OLAP)
- **AWS DMS** → Migración de bases de datos a AWS con mínimo tiempo de inactividad

---

### Velocidad — ¿Proceso en tiempo real o en lotes?

**El desafío:** Los datos se generan a una velocidad sin precedentes.
Los sistemas deben procesar millones de eventos simultáneos sin
degradar la experiencia del usuario.

**Los 2 tipos de procesamiento:**

| Tipo | Cuándo usarlo | Ejemplos |
|------|--------------|---------|
| **Por lotes (Batch)** | Grandes volúmenes a intervalos definidos | Registros de servidores, datos financieros, reportes |
| **Streaming** | Datos continuos que necesitan respuesta inmediata | Compras en e-commerce, sensores IoT, redes sociales |

**Las 4 velocidades de procesamiento:**

| Velocidad | Descripción |
|-----------|-------------|
| **Programado** | Se ejecuta en horarios fijos (ej: cada noche a las 2am) |
| **Periódico** | Se ejecuta cuando se acumula cierta cantidad de datos |
| **Casi en tiempo real** | Segundos o minutos de retraso |
| **En tiempo real** | Procesamiento instantáneo, milisegundos |

**Servicios AWS para Velocidad:**
- **Amazon Kinesis Data Streams** → Streaming de datos en tiempo real
- **Amazon Kinesis Data Firehose** → Carga de streaming a S3, Redshift, etc.
- **AWS Lambda** → Procesamiento serverless de eventos en tiempo real
- **Amazon MSK (Managed Kafka)** → Streaming a escala empresarial

---

### Veracidad — ¿Mis datos son confiables?

**El desafío:** Los datos cambian al transferirse entre sistemas y
procesos, afectando su integridad y confiabilidad.

**ETL vs ELT — los dos enfoques de transformación:**

| | ETL | ELT |
|--|-----|-----|
| **Orden** | Extraer → Transformar → Cargar | Extraer → Cargar → Transformar |
| **Cuándo transformar** | Antes de cargar | Después de cargar |
| **Usado con** | Bases de datos heredadas | Bases de datos modernas en la nube |
| **Ventaja** | Datos limpios desde el inicio | Flexibilidad para transformar cuando se necesite |

**Propósito del ETL/ELT:**
- Garantizar exactitud, precisión y profundidad de los datos
- Reunir datos de diferentes fuentes en una imagen completa
- Crear datasets personalizados para responder preguntas de negocio

**Servicios AWS para Veracidad:**
- **AWS Glue** → ETL serverless: extrae, transforma y carga datos
- **AWS Glue DataBrew** → Limpieza y preparación visual de datos
- **AWS Lambda** → Transformaciones ligeras en tiempo real

---

### Valor — ¿Qué decisión tomo con estos datos?

**El desafío:** Tener datos no es suficiente. Hay que extraer
información útil que permita tomar decisiones estratégicas.

**El proceso para generar valor:**
1. Recopilar datos, hechos y conclusiones
2. Identificar la audiencia y sus expectativas
3. Elegir el estilo de visualización adecuado
4. Crear informes y dashboards

**Los 3 tipos de informes visuales:**

| Tipo | Descripción | Ejemplo |
|------|-------------|---------|
| **Estáticos** | No cambian, son una "foto" del momento | PDF con resultados del mes |
| **Interactivos** | El usuario puede explorar y filtrar | Reporte web con filtros |
| **Dashboards** | Vista en tiempo real con múltiples métricas | Panel de ventas en vivo |


**Servicios AWS para Valor:**
- **Amazon QuickSight** → BI y dashboards interactivos
- **Amazon Athena** → Consultas SQL directamente sobre datos en S3
- **Amazon SageMaker** → ML para generar predicciones y análisis avanzado
- **Amazon Q (QuickSight)** → Generar dashboards con lenguaje natural

---

## 🗺️ Mapa completo: Las 5 V y sus servicios AWS

| V | Servicio principal | Para qué |
|---|-------------------|---------|
| **Volumen** | Amazon S3 | Almacenar cualquier cantidad de datos |
| **Volumen** | Amazon Redshift | Data warehouse a escala masiva |
| **Variedad** | AWS Glue | ETL para cualquier tipo de dato |
| **Variedad** | Amazon DynamoDB | NoSQL flexible |
| **Velocidad** | Amazon Kinesis | Streaming en tiempo real |
| **Velocidad** | AWS Lambda | Procesamiento serverless |
| **Veracidad** | AWS Glue DataBrew | Limpieza y transformación |
| **Valor** | Amazon QuickSight | Visualización y BI |
| **Valor** | Amazon Athena | Consultas SQL sobre S3 |

---
## Progreso de lecciones

- [x] Lección 1: Introducción y conceptos generales
- [x] Lección 2: Análisis (tipos y técnicas)
- [x] Lección 3: Machine Learning
- [x] Lección 4: IA Generativa y Amazon Q Developer
- [x] Lección 5: Las 5 V de los macrodatos
- [x] Lección 6: Volumen y servicios AWS
- [x] Lección 7: Variedad y servicios AWS
- [x] Lección 8: Velocidad y servicios AWS
- [x] Lección 9: Veracidad y servicios AWS
- [x] Lección 10: Valor y servicios AWS
- [ ] Lección 11: Servicios de AWS para el volumen
- [ ] Lección 12: Servicios de AWS para la variedad
- [ ] Lección 13: Servicios de AWS para la velocidad
- [ ] Lección 14: Servicios de AWS para la veracidad
- [ ] Lección 15: Servicios de AWS para el valor
- [ ] Conclusión y cuestionario final