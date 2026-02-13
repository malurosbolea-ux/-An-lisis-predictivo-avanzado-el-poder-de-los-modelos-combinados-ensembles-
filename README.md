# Análisis predictivo avanzado: el poder de los modelos combinados (ensembles)

¡Hola! Soy María Luisa Ros Bolea. En este repositorio presento una investigación técnica y estratégica centrada en resolver una de las grandes preguntas del Machine Learning: ¿funcionan mejor los algoritmos cuando trabajan en equipo que cuando lo hacen en solitario?

A menudo, en los proyectos de datos, buscamos "el algoritmo perfecto" para predecir el comportamiento de un cliente o una tendencia de mercado. A través de este proyecto, demuestro con datos reales cómo la combinación inteligente de distintos modelos predictivos (lo que llamamos *ensembles*) puede compensar las debilidades individuales de cada uno y generar predicciones mucho más robustas y precisas. Todo ello, por supuesto, acompañado de visualizaciones analíticas diseñadas con una paleta de colores personalizada (¡el rosa nunca puede faltar en mis dashboards!).

## Archivos del proyecto

He condensado toda la investigación, el código y las reflexiones estratégicas en un único archivo interactivo para que no pierdas detalle de mi proceso mental y técnico:

* **[Notebook de la investigación (Jupyter)](./ensembles_exercise_1_FINAL.ipynb)**: En este documento ejecuto todo el flujo de trabajo. Desde la automatización de la carga masiva de 13 conjuntos de datos diferentes, hasta el entrenamiento y evaluación cruzada de múltiples algoritmos. Contiene explicaciones paso a paso, por lo que es muy fácil de seguir.

## Mi metodología paso a paso

Me gusta hacer las cosas con orden y sentido, no tirar código por tirar. Por eso, estructuré este análisis de forma evolutiva, explicándolo todo poco a poco para que se entienda la lógica de negocio detrás de cada línea de código:

### 1. Los cimientos: modelos individuales
Primero, entrené cuatro algoritmos base muy diferentes entre sí: Regresión Logística, K-Nearest Neighbors (KNN), Árboles de Decisión (Decision Trees) y Máquinas de Vectores de Soporte (SVM). 
¿La conclusión? El Teorema de *No Free Lunch* es real: no hay un modelo que gane siempre. Dependiendo de los datos, uno es mejor que otro. Necesitábamos algo mejor.


### 2. Creando equipos de algoritmos (Ensembles)
Para mejorar los resultados, apliqué diferentes estrategias de "trabajo en equipo":
* **Bagging (Bootstrap Aggregating):** Consiste en entrenar muchas copias de un mismo modelo con pequeñas variaciones en los datos. Demostré que esto es oro puro para modelos inestables como los Árboles de Decisión, logrando mejorar su precisión media en un 3.6%. Sin embargo, aplicarlo a modelos estables (como la Regresión Logística) es malgastar recursos.
* **Boosting (AdaBoost):** Aquí los modelos aprenden de forma secuencial, donde cada nuevo modelo intenta corregir los errores del anterior (como un profesor particular que insiste en lo que peor llevas). Descubrí que es ideal para modelos sencillos, pero que si se lo aplicas a un modelo complejo y fuerte (como un SVM), el rendimiento cae en picado.
* **Voting y Stacking:** Puse a votar a todos los algoritmos juntos. Comprobé empíricamente que la diversidad es clave: los modelos que más discrepan entre sí son los que más se benefician de trabajar juntos en un *Stacking*.

### 3. La traca final: mi propio "súper-ensemble"
No me conformé con lo estándar. Para rematar el proyecto, construí un meta-modelo de *Stacking* de alto nivel que combinaba en su interior otros ensembles (un *Bagging* de árboles, un *Boosting* de modelos simples y un *Voting* heterogéneo). Logré un algoritmo tremendamente competitivo y consistente frente a los 13 escenarios de datos evaluados.

## Sobre mí y contacto

Soy Graduada en Comunicación Digital y máster en Big Data e Inteligencia Artificial. Me dedico a conectar el mundo técnico de los datos con la estrategia de negocio y la comunicación. Mi punto fuerte es traducir análisis matemáticos complejos en planes de acción ejecutables y visuales, asegurándome de que todo esté perfecto y revisado desde el primer paso. Además, soy de las que piensa que el rigor técnico no está reñido con ser sociable, cercana y tener buen sentido del humor.

Si buscas a alguien que analice datos entendiendo el *porqué* de las cosas, y que te lo dé todo bien "mascadito", hablemos:

* **Portfolio estratégico**: [Mi sitio web](https://malurosbolea-ux.github.io/digital-strategy-portfolio/)
* **LinkedIn**: [María Luisa Ros Bolea](https://www.linkedin.com/in/mar%C3%ADa-luisa-ros-bolea-400780160/)
* **Instagram**: [@malu_menolu](https://www.instagram.com/malu_menolu/)
* **Email**: [malurosbolea@gmail.com](mailto:malurosbolea@gmail.com)
* **Teléfono**: +34 692 892 183
* **Ubicación base**: Madrid / Murcia
