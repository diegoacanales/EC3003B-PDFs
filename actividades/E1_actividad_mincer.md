---
layout: default
title: "E1: Actividad Mincer"
---

# E1: Actividad Mincer

<div class="meta">
    <span class="meta-item"><strong>Peso:</strong> 10%</span>
    <span class="meta-item"><strong>Tipo:</strong> Individual</span>
    <span class="meta-item"><strong>Fecha límite:</strong> Jue 12 feb, 11:59pm</span>
    <span class="meta-item"><strong>Módulos:</strong> M01, M02, M03</span>
</div>

## Objetivo de Aprendizaje

Aplicar la ecuación de Mincer para estimar los retornos a la educación y experiencia en el mercado laboral mexicano, interpretando los coeficientes en el contexto de decisiones de compensación.

## Contexto

Antes de diseñar un sistema de compensaciones para la empresa, necesitamos entender cómo el mercado laboral mexicano valora diferentes características del capital humano. La ecuación de Mincer es el punto de partida para cuantificar estos retornos.

<div class="alert alert-info">
    <strong>Novedad:</strong> Cada estudiante analizará una región diferente de México. Esto permite comparaciones entre regiones y evita duplicación de trabajo.
</div>

## Asignación de Regiones

Cada estudiante tiene asignada una región según los últimos 4 dígitos de su matrícula. Configura tu matrícula en el archivo `.do` y el código filtrará automáticamente tu región.

| Matrícula | Región | Estados (códigos INEGI) | Nombre |
|-----------|--------|-------------------------|--------|
| 6662 | R1 | 02, 03 | Baja California |
| 6925 | R2 | 26, 25, 18 | Pacífico Norte |
| 4381 | R3 | 08, 10, 32 | Sierra Norte |
| 7384, 2288 | R4 | 05, 19, 28 | Noreste |
| 7844 | R5 | 14, 06, 01 | Occidente |
| 3259 | R6 | 11, 22, 24 | Bajío |
| 6762, 6450 | R7 | 09, 15 | Megalópolis |
| 7782 | R8 | 16, 12 | Sur-Pacífico |
| 7325 | R9 | 21, 29, 17 | Centro |
| 6971 | R10 | 30, 13, 27 | Golfo |
| 1076 | R11 | 20, 07 | Sur |
| 6323 | R12 | 31, 23, 04 | Peninsular |

**Nota:** Las regiones R4 (Noreste) y R7 (Megalópolis) tienen 2 estudiantes cada una para comparación entre pares.

## Instrucciones

### Parte 1: Análisis Nacional (25 puntos)

#### 1. Preparación de datos - Muestra Nacional (10 pts)

- Filtra la muestra **nacional** a trabajadores asalariados de 18-65 años
- Construye las variables: log(ingreso por hora), años de educación, experiencia potencial, experiencia²
- Reporta estadísticas descriptivas de la muestra nacional
- **Esperado:** ~50,000-80,000 observaciones

#### 2. Estimación básica - Muestra Nacional (15 pts)

$$\ln(w) = \beta_0 + \beta_1 \cdot Educ + \beta_2 \cdot Exp + \beta_3 \cdot Exp^2 + \varepsilon$$

- Presenta la tabla de regresión con errores estándar robustos
- Interpreta cada coeficiente en términos porcentuales
- Guarda estos resultados para comparación posterior

### Parte 2: Análisis Regional (45 puntos)

#### 3. Extensiones - Tu Región (15 pts)

- Filtra a **tu región asignada** usando los códigos de estado
- Agrega variables de control: género, sector formal/informal
- Compara los coeficientes con y sin controles
- Discute el sesgo por variables omitidas en tu región

#### 4. Análisis por sector - Tu Región (15 pts)

- Filtra la muestra regional al sector construcción/ingeniería (códigos SCIAN relevantes)
- Estima la ecuación de Mincer para este subsector
- Compara los retornos con la muestra regional general
- ¿Qué implica esto para Geotest en tu región?

#### 5. Aplicación al proyecto - Tu Región (15 pts)

- Estima un modelo con dummies de nivel educativo (secundaria, preparatoria, licenciatura, posgrado)
- Calcula el "premio salarial" de cada nivel respecto a secundaria
- ¿Cómo se comparan estos premios regionales con la estructura de la empresa?

### Parte 3: Comparaciones (20 puntos)

#### 6A. Comparación Regional vs Nacional (10 pts)

- Compara los retornos de tu región con los nacionales
- Proporciona hipótesis sobre las diferencias observadas

#### 6B. Comparación Temporal 2022 vs 2024 (10 pts)

- Compara tus resultados nacionales con los obtenidos en clase (ENIGH 2022)
- ¿Han cambiado los retornos? ¿Por qué podría ser?

### Parte 4: Visualización (10 puntos)

#### 7. Gráficas de tu región (10 pts)

- Histograma de log salarios
- Scatter plot: Educación vs Log Salario
- Perfil edad-ingresos por nivel educativo
- **Importante:** Todos los gráficos deben indicar tu región en el título

## Entregables

1. **Archivo Stata (.do)** con tu matrícula configurada y todo el código comentado
2. **Documento PDF** con tablas de regresión, gráficas y respuestas a todas las preguntas de reflexión
3. **Carpeta de resultados** con tablas y gráficas exportadas (nombradas con tu código de región)

## Preguntas de Reflexión

Tu PDF debe responder las siguientes preguntas:

- **1.1:** Tamaño de muestra nacional vs ENIGH 2022
- **2.1:** Interpretación del coeficiente de escolaridad
- **4.1:** Sesgo por variables omitidas en tu región
- **5.1:** Retornos sectoriales en tu región
- **6A:** Comparación tu región vs nacional
- **6B:** Comparación temporal 2022 vs 2024
- **7.1:** Premios educativos y estructura de la empresa
- **9.1:** Reflexión final (máx 500 palabras)

## Rúbrica de Evaluación

### Análisis Técnico (40 puntos)

| Criterio | Excelente (10) | Bueno (8) | Suficiente (6) | Insuficiente (0-4) |
|----------|----------------|-----------|----------------|-------------------|
| Preparación de datos | Muestra correctamente filtrada (nacional y regional) | Muestra correcta con errores menores | Errores significativos | Datos mal preparados |
| Estimación OLS | Modelo correcto, errores robustos, interpretación precisa | Modelo correcto con errores menores | Errores en especificación | Modelo incorrecto |
| Extensiones regionales | Controles relevantes, comparación regional rigurosa | Controles correctos, comparación superficial | Controles incompletos | No incluye |
| Análisis sectorial | Filtro correcto, comparación informativa | Análisis correcto con conexión débil | Análisis incompleto | No incluye |

### Aplicación al Proyecto (30 puntos)

| Criterio | Excelente (15) | Bueno (12) | Suficiente (9) | Insuficiente (0-6) |
|----------|----------------|------------|----------------|-------------------|
| Premios educativos | Cálculo correcto, conexión explícita con datos regionales | Cálculo correcto, conexión implícita | Errores menores | Cálculo incorrecto |
| Comparaciones | Comparación regional/nacional y temporal bien fundamentadas | Comparaciones adecuadas | Comparaciones superficiales | No incluye |

### Presentación y Código (30 puntos)

| Criterio | Excelente (10) | Bueno (8) | Suficiente (6) | Insuficiente (0-4) |
|----------|----------------|-----------|----------------|-------------------|
| Código Stata | Matrícula configurada, bien organizado, reproducible | Funcional con comentarios básicos | Funcional pero desorganizado | No funciona |
| Tablas y gráficas | Formato publicación, etiquetas claras incluyendo región | Formato adecuado con errores menores | Formato básico | Ilegibles |
| Documento | Bien estructurado, redacción clara, todas las reflexiones | Estructura clara con errores menores | Estructura confusa | Incompleto |

## Recursos

<div class="alert alert-info">
    <strong>Recursos disponibles:</strong>
    <ul>
        <li>Datos ENIGH 2024 (Canvas)</li>
        <li>Template de código: <code>actividades/M01_actividad_estudiante.do</code></li>
        <li>Tabla de códigos de estado INEGI</li>
    </ul>
</div>

<div class="alert alert-warning">
    <strong>Notas importantes:</strong>
    <ul>
        <li><strong>Matrícula:</strong> Asegúrate de configurar tu matrícula correctamente en el archivo .do (línea 45)</li>
        <li><strong>Plagio:</strong> El código y análisis deben ser propios. Estudiantes con la misma región pueden discutir, pero deben entregar trabajos independientes.</li>
        <li><strong>IA:</strong> Pueden usar Claude/ChatGPT para debugging, pero deben entender todo su código.</li>
        <li><strong>Formato de tablas:</strong> Usar esttab o outreg2 para exportar tablas profesionales.</li>
    </ul>
</div>

---

<a href="{{ '/actividades' | relative_url }}" class="btn btn-secondary">← Volver a Actividades</a>
