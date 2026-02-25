# Prevención de Fuga de Talento: Análisis Predictivo de Rotación de Empleados

Este proyecto de **People Analytics** aborda una de las problemáticas más costosas para las organizaciones: la alta rotación de personal. A través de un análisis exhaustivo y modelos de **Machine Learning**, el objetivo es identificar qué empleados tienen mayor probabilidad de abandonar la empresa y por qué.

## Antecedentes del Proyecto
En el contexto actual, la rotación de empleados genera altos costos de reclutamiento, capacitación y pérdida de conocimiento. Como analista de datos, este proyecto busca transformar datos de Recursos Humanos en estrategias de retención accionables.

Se proporcionan insights y recomendaciones en las siguientes áreas clave:
* **Perfil del Abandono:** Características demográficas y laborales comunes en empleados que renuncian.
* **Impacto Económico:** Estimación del costo de la rotación para la empresa.
* **Factores Críticos:** Identificación de variables como salario, antigüedad y satisfacción.
* **Modelo Predictivo:** Clasificación de empleados con riesgo de salida.

> **Recursos del Proyecto:**
> * [Notebook: Análisis Exploratorio y Dashboard (EDA Y BI.ipynb)]
> * [Notebook: Desarrollo del Modelo de Machine Learning (MODELO ML.ipynb)]

---

## Estructura de Datos y Validaciones Iniciales
La base de datos analizada contiene información detallada sobre el ciclo de vida del empleado, incluyendo:
* **Datos Demográficos:** Edad, estado civil, distancia al hogar.
* **Datos Laborales:** Departamento, rol, nivel educativo, sueldo mensual, horas extra.
* **Historial y Satisfacción:** Años en la empresa, años con el actual jefe, niveles de satisfacción en el trabajo y equilibrio vida-carrera.

Se realizaron validaciones de nulos, eliminación de columnas irrelevantes (como el ID del empleado) y transformaciones para convertir variables categóricas en numéricas aptas para el modelo.

---

## Resumen Ejecutivo
### Resumen de Hallazgos
El análisis revela que la rotación no es aleatoria: variables como las **horas extra**, el **sueldo mensual** y la **antigüedad en el puesto actual** son los principales detonantes. Un empleado que trabaja horas extra y percibe un salario por debajo del promedio de su nivel tiene una probabilidad significativamente más alta de abandonar la compañía. El modelo predictivo permite identificar estos perfiles con antelación para que el equipo de HR pueda intervenir.

---

## Análisis Detallado de Insights

### 1. Factores Económicos y de Carga Laboral
* **Sueldo Mensual:** Se observa que los empleados que abandonan suelen tener un sueldo medio notablemente inferior a los que permanecen.
* **Horas Extra:** El trabajo fuera de jornada es un predictor crítico; la tasa de rotación es drásticamente mayor en quienes reportan horas extra frecuentes.

### 2. Factores de Permanencia y Liderazgo
* **Años con el jefe actual:** Existe una correlación entre el tiempo de relación con el líder directo y la estabilidad del empleado. Los primeros dos años son críticos para la retención.
* **Relación Vida-Carrera:** Bajos niveles de satisfacción en este indicador coinciden con los picos de salida de personal joven.

### 3. Modelo de Machine Learning
* **Objetivo:** Detectar empleado a empleado la probabilidad de abandono.
* **Algoritmo:** Se implementó un modelo de clasificación que prioriza la sensibilidad (Recall) para asegurar que se identifique a la mayor cantidad posible de empleados en riesgo.

---

## Recomendaciones
Con base en los hallazgos del proyecto, se recomienda al equipo de **Gestión Humana**:
1.  **Revisión Salarial Focalizada:** Revisar las bandas salariales de los roles con mayor rotación para asegurar competitividad.
2.  **Gestión de Horas Extra:** Monitorear la carga laboral y compensar el tiempo extra para evitar el agotamiento (burnout).
3.  **Programas de Liderazgo:** Fortalecer la relación jefe-empleado durante los primeros 24 meses, identificados como el periodo de mayor riesgo.
4.  **Entrevistas de Retención:** Utilizar la lista de empleados con "Alta Probabilidad de Salida" generada por el modelo para realizar entrevistas preventivas.

---

## Supuestos y Consideraciones
* **Costo de Rotación:** Se asumió un costo estimado por empleado para cuantificar el impacto económico del problema.
* **Datos de Satisfacción:** Se asume que las encuestas de satisfacción son honestas y reflejan el sentir real del colaborador.
* **Estacionariedad:** Los patrones de abandono identificados se consideran constantes durante el periodo del análisis.
