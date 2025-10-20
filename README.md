# P2-bancos_portug
Análisis del dataset  bancos_portug.csv, que consiste en la implementación de técnicas de inferencia  estadística  con especial atención a contrastes de hipótesis, análisis de normalidad  y relaciones entre las diferentes variables del dataset, en aplicación de los  contenidos y las prácticas que se han trabajado en clase.

---

# Entrega Final — Análisis Inferencial en R

La entrega final debe incluir **el código en R** y un **documento explicativo en PDF** con los siguientes apartados:


## Descripción del dataset

* Breve descripción de las **principales características o variables de estudio** del dataset.
* Identificación y descripción de **variables numéricas y categóricas** relevantes para el estudio inferencial.
* Explicación del **análisis a realizar** y de los **objetivos concretos** del estudio.


## Análisis de normalidad de variables cuantitativas

* Realizar **contrastes de hipótesis (Shapiro–Wilk)** sobre la normalidad de algunas variables.
* Analizar los resultados del contraste y **compararlos con el análisis gráfico** de las mismas.


## Contrastes de hipótesis sobre diferencia de medias

Proponer e implementar dos contrastes de hipótesis sobre medias:

* **3.1. Contraste bilateral**
* **3.2. Contraste unilateral**


## Contraste de proporciones

* Proponer e implementar un **contraste de hipótesis para comparar dos proporciones**.


## Análisis del impacto de los errores tipo I y tipo II

Caso práctico del **banco portugués**:

> El banco realiza campañas telefónicas para ofrecer depósitos a plazo fijo. En campañas anteriores, aproximadamente el **12% de los clientes aceptaban la oferta**.
> Se está considerando una **nueva estrategia de marketing** más costosa, y queremos evaluar si la nueva campaña tiene una **tasa de éxito mayor**.

Tareas a realizar:

* A partir de una **muestra aleatoria simple de 25 clientes**, establecer una **regla de decisión** para detectar un incremento en la proporción de compradores.
* Realizar el **análisis de errores tipo I y tipo II**, así como calcular la **potencia del contraste**.
* Estudiar **modificaciones posibles para mejorar la capacidad del test** (incrementar la potencia del contraste para detectar mejoras en la proporción real de compradores).


## Análisis no paramétrico

* **6.1. Contraste de Wilcoxon**: analizar si la distribución de la variable `duration` difiere significativamente entre los clientes que **suscribieron el producto** y los que **no lo hicieron**.
* **6.2. Contraste de Spearman**: estudiar si existe **asociación entre las variables** `campaign` y `duration`.


## Elaboración del documento PDF final

El PDF debe incluir **fichas de consulta** con:

* **Slides explicativas** de las conclusiones generales.
* **Gráficos descriptivos** que complementen el análisis de normalidad.
* **Descripción clara** de los elementos de cada contraste:

  * Hipótesis nula y alternativa.
  * Estadístico y p-valor.
  * Decisión e **interpretación justificada** en el contexto del problema.
* **Interpretación de los errores tipo I y II** y su impacto en el contexto del problema.

