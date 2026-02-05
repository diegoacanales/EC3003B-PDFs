---
layout: default
title: "E4: Tabulador Salarial"
---

# E4: Tabulador Salarial + Métricas

<div class="meta">
    <span class="meta-item"><strong>Peso:</strong> 15%</span>
    <span class="meta-item"><strong>Tipo:</strong> Equipo</span>
    <span class="meta-item"><strong>Fecha límite:</strong> Mié 25 feb, 11:59pm</span>
    <span class="meta-item"><strong>Módulos:</strong> M10, M11</span>
</div>

## Objetivo de Aprendizaje

Construir un tabulador salarial con bandas que integre la jerarquía interna (evaluación por puntos) con datos de mercado, calculando métricas estándar de compensación.

## Contexto

El tabulador salarial es la herramienta central para la administración de compensaciones. Traduce el valor interno de los puestos a rangos salariales competitivos con el mercado.

## Instrucciones

### 1. Agrupación en Grados Salariales

Usando los puntajes de E3:
- Definir **5-7 grados salariales**
- Establecer rangos de puntos por grado
- Asignar cada puesto a su grado correspondiente

### 2. Datos de Mercado

Incorporar información de benchmarking:
- Usar datos proporcionados de encuestas salariales
- Identificar puestos de referencia (benchmark jobs)
- Calcular percentiles de mercado (P25, P50, P75)

### 3. Construcción de Bandas Salariales

Para cada grado, definir:

| Elemento | Fórmula/Criterio |
|----------|------------------|
| Mínimo | Típicamente 80-85% del punto medio |
| Punto medio | Basado en P50 de mercado |
| Máximo | Típicamente 115-120% del punto medio |
| Range spread | (Máx - Mín) / Mín × 100 |

### 4. Cálculo de Métricas

Para cada empleado/puesto, calcular:

#### Compa-Ratio
$$CR = \frac{\text{Salario actual}}{\text{Punto medio del grado}} \times 100$$

Interpretación:
- CR < 80%: Por debajo del rango
- 80-90%: Zona de desarrollo
- 90-110%: En rango competitivo
- 110-120%: Zona de alto desempeño
- CR > 120%: Por encima del rango (red circle)

#### Range Penetration
$$RP = \frac{\text{Salario actual} - \text{Mínimo}}{\text{Máximo} - \text{Mínimo}} \times 100$$

#### Midpoint Progression
$$MP = \frac{\text{Punto medio grado N+1}}{\text{Punto medio grado N}} - 1$$

### 5. Diagnóstico de Equidad

Analizar:
- Distribución de compa-ratios por nivel/área/género
- Identificar green circles (CR < 80%) y red circles (CR > 120%)
- Calcular costo de ajuste para alcanzar equidad

## Entregables

1. **Tabulador salarial**
   - Tabla con grados, rangos de puntos, bandas salariales
   - Visualización gráfica del tabulador

2. **Base de datos con métricas**
   - Archivo Excel/CSV con todos los empleados
   - Compa-ratio, range penetration por empleado
   - Resumen estadístico por área/nivel

3. **Análisis de equidad**
   - Identificación de outliers (green/red circles)
   - Cálculo de costo de ajuste
   - Recomendaciones prioritarias

4. **Reflexión** (máx 400 palabras):
   - ¿Qué patrones de inequidad encontraron?
   - ¿Qué factores podrían explicarlos?

## Rúbrica de Evaluación

| Criterio | Excelente (15) | Bueno (12) | Suficiente (9) | Insuficiente (0-6) |
|----------|----------------|------------|----------------|-------------------|
| Diseño del tabulador | Bandas bien calibradas, progresión lógica | Diseño coherente con ajustes menores | Diseño funcional pero inconsistente | Diseño incorrecto |
| Cálculo de métricas | Métricas correctas para todos los empleados | Cálculos correctos con errores menores | Métricas incompletas | Cálculos incorrectos |
| Análisis de equidad | Análisis profundo con recomendaciones accionables | Análisis adecuado | Análisis superficial | Sin análisis |
| Visualización | Gráficas claras y profesionales | Visualización adecuada | Visualización básica | Sin visualización |

<div class="alert alert-info">
    <strong>Datos disponibles:</strong>
    <ul>
        <li>Salarios actuales de Geotest (anonimizados)</li>
        <li>Datos de encuesta salarial del sector</li>
        <li>Template de tabulador en Excel</li>
    </ul>
</div>

---

<a href="{{ '/actividades' | relative_url }}" class="btn btn-secondary">← Volver a Actividades</a>
