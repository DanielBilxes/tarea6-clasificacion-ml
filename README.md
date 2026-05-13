Tarea 6: Clasificación - Teaching Assistant Evaluation

Este repositorio contiene el código y análisis para la Tarea 6 del curso, enfocada en resolver un problema de clasificación multiclase utilizando algoritmos de Machine Learning. 

Integrantes:
* Ignacio Essus
* Adolfo Gayoso
* Marcelo Rebolledo
* Daniel Sepúlveda

Definición del Problema:
El objetivo principal de este proyecto es predecir la evaluación final (Baja, Media o Alta que recibirá un ayudante de cátedra (Teaching Assistant) por parte de sus alumnos. Para lograrlo, utilizamos características demográficas y contextuales de la clase asignada.

Se abordó como un problema de Clasificación Multiclase (3 categorías) utilizando aprendizaje supervisado.

Sobre el Dataset:
Se utilizó el conjunto de datos Teaching Assistant Evaluation proveniente del UCI Machine Learning Repository. 
* Instancias: 151 filas.
* Atributos (Features): 5 (Hablante nativo de inglés, Instructor del curso, Curso específico, Semestre, Tamaño de la clase).
* Variable Objetivo (Target): Evaluation_Score (1 = Bajo, 2 = Medio, 3 = Alto).

Debido a su naturaleza mayoritariamente categórica y tamaño reducido, representa un desafío clásico en la predicción de Machine Learning.

Metodología y Flujo de Trabajo:

El experimento se desarrolló en un Google Colab Notebook siguiendo estas etapas:

1. Análisis Exploratorio de Datos (EDA): 
   * Verificación de datos nulos y tipos de variables.
   * Análisis visual de la distribución de las clases (balanceadas) e impacto del idioma nativo en la evaluación mediante gráficos con Seaborn.
2. Preprocesamiento:*
   * Separación de características y variable objetivo (X e y).
   * Aplicación de One-Hot Encoding para las variables categóricas nominales (Instructor, Curso, etc.).
   * División de datos usando Hold-out estratificado (80% Train, 20% Test) y escalado numérico con StandardScaler.
3. Entrenamiento y Evaluación: 
   * Se entrenaron y evaluaron tres modelos de clasificación:
     * Decision Tree (Árbol de Decisión)
     * Random Forest
     * K-Nearest Neighbors (KNN)
   * Métricas: Accuracy, Precision (macro), Recall (macro), F1-Score (macro) y Matrices de Confusión.

Resultados Principales:

Tras la ejecución del experimento en el conjunto de prueba, se obtuvieron los siguientes hallazgos:

* Mejor Modelo: El Random Forest demostró ser el algoritmo más robusto, alcanzando el F1-Score más alto y un Accuracy de ~64.5%. Logró predecir con gran eficacia las clases extremas (evaluaciones Bajas y Altas).
* Modelos Deficientes El modelo *KNN* tuvo el peor desempeño, demostrando que un enfoque basado en distancias geométricas no es adecuado para este dataset altamente categórico (se confundió fuertemente al intentar predecir la clase Alta).
* Conclusión General: El rendimiento máximo esperado en este dataset es moderado (60-70%) debido a su baja dimensionalidad de registros frente a una alta cantidad de categorías (IDs de cursos y profesores).
