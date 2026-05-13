1. ¿Cuál es nuestro problema?
Desde la perspectiva del Machine Learning, nos enfrentamos a un problema de Clasificación Multiclase.

Es de Clasificación: Porque no estamos intentando adivinar un valor numérico continuo e infinito (como intentar predecir el sueldo exacto de una persona), sino que queremos asignar una "etiqueta" o categoría a cada caso.

Es Multiclase: Porque tenemos más de dos opciones posibles para el resultado. Si fuera un problema binario, las opciones serían solo "Buen ayudante" o "Mal ayudante". Aquí tenemos tres categorías.

2. ¿Qué queremos predecir exactamente?
El objetivo principal es predecir la calificación o nivel de desempeño que recibirá un ayudante de cátedra (TA) por parte de sus estudiantes al finalizar el curso.

En este dataset, esa predicción (tu variable Target o variable objetivo, llamada Evaluation_Score) se divide en tres niveles:

Clase 1: Desempeño Bajo.

Clase 2: Desempeño Medio.

Clase 3: Desempeño Alto.

¿Qué pistas (variables) usamos para adivinar el futuro?
Para que nuestros algoritmos (el Árbol de Decisión, el Random Forest y el KNN) aprendan a predecir si el ayudante será de nivel 1, 2 o 3, los alimentamos con 5 características clave (los features):

Idioma: Si el ayudante es hablante nativo de inglés o no.

Instructor: Quién es el profesor principal a cargo de esa asignatura.

Curso: Qué materia específica se está enseñando.

Semestre: Si la clase se está dictando en un semestre regular o en verano.

Tamaño de la clase: Cuántos alumnos asisten a esa sección.
