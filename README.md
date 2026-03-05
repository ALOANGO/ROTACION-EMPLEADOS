# Prevención de Fuga de Talento: Análisis Predictivo de Rotación de Empleados


## 1- Ojetivo y Antecedentes del Proyecto
Este proyecto aborda una de las problemáticas más costosas para las organizaciones: la alta rotación de personal. A través de un análisis exhaustivo y modelos de **Machine Learning**, el objetivo es identificar por qué los empleados estàn abandonando la empresa y que perfil de empleados tienen mayor probabilidad de abandonar la empresa.

En el contexto actual, la rotación de empleados genera altos costos de reclutamiento, capacitación y pérdida de conocimiento. Como analista de datos, este proyecto busca transformar datos de Recursos Humanos en estrategias de retención accionables.


> **Recursos del Proyecto:**
> * [Notebook: Análisis Exploratorio y Dashboard (EDA Y BI.ipynb)]


---

## 2- Anàlisis exploratorio de datos
La base de datos analizada corresponden a 1.470 empleados y contiene información detallada sobre el ciclo de vida de cada empleado, incluyendo:
* Datos Demográficos:** Edad, estado civil, distancia al hogar.
* Datos Laborales:** Departamento, rol, nivel educativo, sueldo mensual, horas extra.
* Historial y Satisfacción:** Años en la empresa, años con el actual jefe, niveles de satisfacción en el trabajo y equilibrio vida-carrera.

<img width="544" height="455" alt="image" src="https://github.com/user-attachments/assets/8b64f2d9-ff25-4f04-bd0f-a2559d663911" />


Se realizaron validaciones de nulos, eliminación de columnas irrelevantes (como el ID del empleado) y transformaciones para convertir variables categóricas en numéricas aptas para el modelo.

---

## 3- Anàlisis diagnostico (Resumen Ejecutivo de hallazgos)

### a. Cuantificacion del problema 

El 16% de los empleados abandonan la empresa. El análisis revela que la rotación no es aleatoria: variables como las **horas extra**, el **sueldo mensual**, **estado civil** y **percibir un salario por debajo del promedio de su nivel**, son los principales detonantes para una probabilidad significativamente más alta de abandonar la compañía. 

<img width="648" height="286" alt="image" src="https://github.com/user-attachments/assets/77abf406-77b6-4751-be24-ca6417f3a98d" />
<img width="651" height="533" alt="image" src="https://github.com/user-attachments/assets/7b18734b-ef9e-458a-95a0-1de30820c9c3" />



### b. Estimacion del impacto economico

Según el estudio "Cost of Turnover" del Center for American Progress:

* El coste de la fuga de los empleados que ganan menos de 30000 es del 16,1% de su salario.
* El coste de la fuga de los empleados que ganan entre 30000-50000 es del 19,7% de su salario.
* El coste de la fuga de los empleados que ganan entre 50000-75000 es del 20,4% de su salario.
* El coste de la fuga de los empleados que ganan más de 75000 es del 21% de su salario.

Este problema nos ha costado en el ultimo año USD 2.719.005

### c. Escenarios de ahorro

¿Cuánto dinero podríamos ahorrar fidelizando mejor a nuestros empleados?

* Reducir un 10% la fuga de empleados nos ahorraría USD 271.900 cada año.
* Reducir un 20% la fuga de empleados nos ahorraría USD 543.801 cada año.
* Reducir un 30% la fuga de empleados nos ahorraría USD 815.701 cada año.

> **Recursos del Proyecto:**
> * [Notebook: Análisis Exploratorio y Dashboard (EDA Y BI.ipynb)]
  
---

## 4- Modelo de Machine Learning

Se elabora un modelo de ml que prediga la probabilidad de abandono de un empleado, implementando un DecisionTree Classifier con una presicion del 70%.

<img width="330" height="121" alt="image" src="https://github.com/user-attachments/assets/44b6a448-7ee8-495a-ad2f-75870f914610" />
<img width="985" height="528" alt="image" src="https://github.com/user-attachments/assets/99a6420b-cae7-4bbe-b9cf-153b3e190545" />



  
Importancia de las variables del modelo de ML nos dà la respuesta del por que estan abandonando los empleados
<img width="985" height="528" alt="image" src="https://github.com/user-attachments/assets/5bb02c14-7fc1-4aa6-876b-6bf6d9dc56b5" />


> **Recursos del Proyecto:**
> * [Notebook: Desarrollo del Modelo de Machine Learning (MODELO ML.ipynb)]
---

## 5- Recomendaciones

Se proporcionan insights y recomendaciones en las siguientes áreas clave:
* **Perfil del Abandono:** Características demográficas y laborales comunes en empleados que renuncian.
* **Impacto Económico:** Estimación del costo de la rotación para la empresa.
* **Factores Críticos:** Identificación de variables como salario, antigüedad y satisfacción.
* **Modelo Predictivo:** Clasificación de empleados con riesgo de salida.
  
Con base en los hallazgos del proyecto, se recomienda al equipo de **Gestión Humana**:
1.  **Revisión Salarial Focalizada:** Revisar las bandas salariales de los roles con mayor rotación para asegurar competitividad.
2.  **Gestión de Horas Extra:** Monitorear la carga laboral y compensar el tiempo extra para evitar el agotamiento (burnout).
3.  **Programas de Liderazgo:** Fortalecer la relación jefe-empleado durante los primeros 24 meses, identificados como el periodo de mayor riesgo.
4.  **Entrevistas de Retención:** Utilizar la lista de empleados con "Alta Probabilidad de Salida" generada por el modelo para realizar entrevistas preventivas.

¿Cuanto dinero podríamos ahorrar fidelizando mejor a nuestros empleados?
Habíamos visto que los representantes de ventas son el puesto que más se van. ¿Tendría sentido hacer un plan específico para ellos? ¿Cual sería el coste ahorrado si disminuimos la fuga un 30%?

El modelo predictivo permitirà identificar estos perfiles con antelación para que el equipo de HR pueda intervenir.
---

## Supuestos y Consideraciones
* **Costo de Rotación:** Se asumió un costo estimado por empleado para cuantificar el impacto económico del problema.
* **Datos de Satisfacción:** Se asume que las encuestas de satisfacción son honestas y reflejan el sentir real del colaborador.
* **Estacionariedad:** Los patrones de abandono identificados se consideran constantes durante el periodo del análisis.
