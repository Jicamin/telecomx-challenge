# Proyecto Telecom X - Parte 2: Predicción de Cancelación (Churn)

## Propósito del Análisis

Este proyecto tiene como objetivo principal desarrollar modelos predictivos para anticipar la cancelación (churn) de clientes en Telecom X. A partir de variables relevantes que describen el comportamiento y características de los clientes, buscamos identificar patrones que permitan predecir qué usuarios tienen mayor probabilidad de cancelar sus servicios. Esto ayudará a la empresa a implementar estrategias de retención efectivas.

---

## Estructura del Proyecto

- `telecomx_parte2_notebook.ipynb`: Cuaderno principal donde se realiza el análisis exploratorio, la preparación de datos, el modelado y la evaluación.
- `telecomx_parte1_tratados.csv`: Archivo CSV con los datos tratados y limpios provenientes de la Parte 1.
- `README.md`: Este archivo con la documentación del proyecto.
- Carpeta `visualizaciones/` (opcional): Contiene gráficos e imágenes generados durante el análisis.

---

## Preparación de Datos

1. **Clasificación de variables**  
   - Variables numéricas: facturación mensual, cuentas diarias, etc.  
   - Variables categóricas: categoría de facturación, estado de pago a tiempo, etc.

2. **Preprocesamiento**  
   - Se aplicó codificación one-hot para variables categóricas para convertirlas a formato numérico.  
   - Se realizó normalización (estandarización) para variables numéricas en modelos que la requieren, como Regresión Logística.

3. **División de datos**  
   - Los datos se dividieron en conjuntos de entrenamiento (70%) y prueba (30%) para evaluar el rendimiento de los modelos.

4. **Manejo de desbalanceo**  
   - Se exploraron técnicas de balanceo de clases, como undersampling, para mejorar la calidad del modelo ante la posible desproporción entre clientes activos y cancelados.

---

## Modelización y Justificación

- **Modelos usados:**  
  - *Regresión Logística*: sensible a la escala, por lo que se usó normalización.  
  - *Árbol de Decisión*: no requiere normalización.

- **Justificación:**  
  - Se eligieron modelos con diferentes sensibilidades a la escala para comparar resultados y entender el impacto del preprocesamiento.  
  - La normalización asegura que modelos basados en distancia o coeficientes no se sesguen por la magnitud de las variables.

---

## Insights y Gráficos

Durante el análisis exploratorio se observaron patrones como:

- Los clientes con facturación mensual baja y con retrasos en pago tienen mayor riesgo de cancelar.  
- La cantidad de cuentas diarias es un indicador relevante para la retención.

Se incluyen gráficos de barras que muestran la importancia de variables según los modelos entrenados y boxplots para visualizar la relación entre variables clave y la cancelación.

---

## Instrucciones para Ejecutar el Cuaderno

1. Clona o descarga el repositorio.  
2. Asegúrate de tener instalado Python 3 y las siguientes librerías:  