# **Más allá de las Habilidades** 




![Texto alternativo](Imagen\main.png)
*Un análisis para predecir las estrellas del mañana*
<br/><br/>

### Este proyecto tiene como objetivo brindar a los ojeadores de fútbol una herramienta basada en datos para predecir el ranking de los jugadores. La predicción del ranking es un aspecto clave en la identificación de talentos emergentes y la toma de decisiones informadas en el reclutamiento de jugadores.
<br/><br/>

## **Descripción del Proyecto**

<p align="justify">
El propósito de este proyecto es desarrollar un modelo de regresión que permita predecir el ranking de un jugador de fútbol en función de diferentes características y métricas relevantes. Para lograr esto, se utilizará un conjunto de datos completo y actualizado que incluye información detallada sobre jugadores, rendimiento físico, habilidades técnicas.
<p align="justify">
Considero que es una herramienta significativa a la hora de evaluar de forma global el potencial del jugador. Es importante entender que es medida subjetiva y no necesariamente refleja la calidad absoluta de un jugador.

<br/><br/>

# Metodología y datos utilizados

![Texto alternativo](Imagen\method.png)

## **Datos Utilizados**
<p align="justify">
Utilizando los datos proporcionado por la Federacion Intenacional de Futbol Asociado he desarrollado un modelo con el fin de predecir el Valore Agregado Total (OVA) el cual tiene como objetivo para evaluar la efectividad y la influencia de un jugador en el campo.
<p align="justify">
A continuación, se detalla la metodología y los datos utilizados en este proceso.

Las caracteristicas fisicas y tecnicas consideradas para el análisis son imprescindibles para que la predicción sea lo mas precisa posible.

Para este caso se utilizaron las siguiente:
<p align="justify">
- Age: Factor importante para evaluar la experiencia y madurez del jugador.

<p align="justify">
- BP: Posición principal del jugador en el campo en la que el jugador se desempeña mejor.

<p align="justify">
- Height: La altura del jugador en centímetros, influye en su capacidad de juego aéreo y su presencia física en el campo.

<p align="justify">
- Weight: El peso del jugador en kilogramos, relevante para evaluar su fortaleza y resistencia física.

<p align="justify">
- Foot: El pie dominante del jugador.

<p align="justify">
- Value: El valor de mercado del jugador, que representa su precio estimado en el mercado de fichajes.

<p align="justify">
- Wage: El salario que recibe el jugador. Indica la remuneración económica que recibe por su desempeño en el campo.

<p align="justify">
- Release Clause: La cláusula de rescisión del contrato del jugador.

<p align="justify">
- Attacking: Habilidades y capacidades del jugador en situaciones ofensivas, como la capacidad de marcar goles, crear oportunidades de gol y contribuir al ataque del equipo.

<p align="justify">
- Crossing: La precisión y habilidad del jugador al enviar pases cruzados desde los costados del campo hacia el área de penal.

<p align="justify">
- Finishing: La capacidad del jugador para finalizar jugadas y convertir oportunidades de gol en goles. 

<p align="justify">
- Short Passing: La precisión y habilidad del jugador al realizar pases cortos y precisos en situaciones de juego cercanas.

<p align="justify">
- Ball Control: La capacidad del jugador para controlar y manipular el balón con los pies. Incluye habilidades como el dominio, regate y retención del balón en situaciones de juego.

<p align="justify">
- Acceleration: La velocidad a la que el jugador puede aumentar su velocidad desde una posición estática. 

<p align="justify">
- Reactions: La capacidad del jugador para reaccionar rápidamente a los eventos en el campo y ajustar su juego en consecuencia. Incluye la lectura del juego, anticipación y toma de decisiones.

<p align="justify">
- Stamina: La resistencia y capacidad de energía del jugador para mantener un rendimiento alto durante todo el partido.

<p align="justify">
- Defending: Habilidades y capacidades del jugador en situaciones defensivas, como la capacidad de bloquear, despejar balones, marcar a los oponentes y


## **Variable Objetivo**

**OVA**: Valoración general del jugador, que representa su nivel general de habilidad y rendimiento en el juego. Es una medida que resume las diferentes habilidades y características del jugador en una sola calificación. 

## **Modelo de Regresión Lineal**
<p align="justify">
La regresión lineal es un método estadístico utilizado para predecir y entender las relaciones entre variables. Es especialmente útil cuando queremos predecir el ranking de jugadores de fútbol utilizando datos históricos y estadísticas relevantes.
<p align="justify">
Como nuestro objetivo es analizar y predecir el rendimiento de los jugadores de fútbol en función de diferentes habilidades técnicas. La regresión lineal nos permite establecer una relación matemática entre estas variables y el ranking de los jugadores. 

<br/><br/>

# **Interpretación**

Es imprencindible comprender la relación entre las caracteristicas del jugador.

Estas nos permite comprender cómo se relacionan y se influyen mutuamente. Cuando hablamos de correlación, nos referimos a la medida en que dos variables se mueven juntas en la misma dirección (correlación positiva) o en direcciones opuestas (correlación negativa).
<br/><br/>
![Texto alternativo](Imagen\correlacion.png)

Como podemos ver exisite una correlacion positiva entre el OVA y el Value, el Wage que percibe y su Release Clause. Esto es lógico ya que el valor monetario que tiene el jugador esta relacionado con su valoración general.

De forma inversa observamos que la aceleracion se encuentra condicionada en cuanto a su altura y su peso.

Es importante considerar eso como caracteristica a la hora tomar una decisión.

Para evaluar que tan bueno es el modelo se analizan las siguientes metricas como pue



Los resultado del modelo nos da las siguientes metricas

- MSE (Error Cuadrático Medio) = 0.0019409560397060704: El MSE es una medida del promedio de los errores cuadrados entre las predicciones y los valores reales. En este caso, el valor extremadamente bajo indica que nuestras predicciones son muy cercanas a los valores reales en promedio. Cuanto más bajo sea el MSE, mejor es el ajuste del modelo.

- RMSE (Raíz del Error Cuadrático Medio) = 0.04405628263603354: El RMSE es la raíz cuadrada del MSE y está en la misma escala que la variable objetivo. En este caso, un valor de RMSE muy bajo indica que nuestras predicciones tienen un error promedio muy pequeño en relación con los valores reales. Cuanto más bajo sea el RMSE, mejor es la precisión del modelo.

- R2 (Coeficiente de Determinación) = 0.8759713839568994: El R2 indica la proporción de la variabilidad total en los datos que puede ser explicada por nuestro modelo. En este caso, un valor de R2 de 0.8759713839568994 significa que nuestro modelo puede explicar aproximadamente el 87.6% de la variabilidad en los datos. Cuanto más cerca esté el valor de R2 a 1, mejor será el ajuste del modelo.

- Adj_R2 (R2 Ajustado) = 0.8748382017885128: El Adj_R2 es una versión corregida del R2 que tiene en cuenta la cantidad de variables utilizadas en el modelo. Un valor de Adj_R2 de 0.8748382017885128 significa que, considerando la complejidad del modelo y el número de variables, nuestro modelo ajustado es capaz de explicar aproximadamente el 87.5% de la variabilidad en los datos.

Luego de realizado el modelo he considerado dejar de lado a la hora de analizar el OVA el valor, salario y clausula de resción de contrato para evaluar unicamente las condiciones técnicas del jugador.

Para este caso los resultado han cambiado ya que la correlatividad que existe con las variables eliminadas influyen en el modelo.

Resultados del segundo modelo.

- MSE (Error Cuadrático Medio) = 0.0019372995661011405: El MSE es una medida del promedio de los errores cuadrados entre las predicciones y los valores reales. En este caso, el valor extremadamente bajo indica que nuestras predicciones son muy cercanas a los valores reales en promedio. Un MSE bajo es indicativo de un buen ajuste del modelo.

- RMSE (Raíz del Error Cuadrático Medio) = 0.044014765319164664: El RMSE es la raíz cuadrada del MSE y está en la misma escala que la variable objetivo. Un valor de RMSE bajo indica que nuestras predicciones tienen un error promedio muy pequeño en relación con los valores reales. Cuanto más bajo sea el RMSE, mejor será la precisión del modelo.

- R2 (Coeficiente de Determinación) = 0.876205035493328: El R2 indica la proporción de la variabilidad total en los datos que puede ser explicada por nuestro modelo. En este caso, un valor de R2 de 0.876205035493328 significa que nuestro modelo puede explicar aproximadamente el 87.6% de la variabilidad en los datos. Un R2 alto indica un buen ajuste del modelo.

- Adj_R2 (R2 Ajustado) = 0.8751475821882636: El Adj_R2 es una versión corregida del R2 que tiene en cuenta la cantidad de variables utilizadas en el modelo. Un valor de Adj_R2 de 0.8751475821882636 indica que, considerando la complejidad del modelo y el número de variables, nuestro modelo ajustado puede explicar aproximadamente el 87.5% de la variabilidad en los datos.



<br/><br/>

# Conclusiones

![Texto alternativo](Imagen\554f5dc94d356.gif
)

<br/><br/>

En el primer modelo los resultados indican que nuestro modelo tiene un excelente desempeño. Las predicciones son muy cercanas a los valores reales, con un error muy pequeño en promedio. El modelo explica alrededor del 87.6% de la variabilidad en los datos, lo cual es un indicativo de un buen ajuste. Además, el R2 ajustado tiene en cuenta la complejidad del modelo y aún muestra un alto nivel de explicación de la variabilidad. Estos resultados sugieren que nuestro modelo es altamente preciso y confiable para hacer predicciones.

Los resultados del segundo modelo  tiene un buen desempeño. Las predicciones son muy cercanas a los valores reales, con un error promedio muy pequeño. El modelo explica alrededor del 87.6% de la variabilidad en los datos, lo cual es un indicador positivo. Además, el R2 ajustado tiene en cuenta la complejidad del modelo y aún muestra un alto nivel de explicación de la variabilidad. Estos resultados sugieren que nuestro modelo es preciso y confiable para hacer predicciones.

## Comparación

En términos generales, los dos conjuntos de resultados son bastante similares y muestran un buen rendimiento del modelo. Sin embargo, hay algunas diferencias sutiles entre ellos:

MSE: Ambos conjuntos tienen valores de MSE muy similares, lo que indica que las predicciones tienen un error cuadrático medio muy bajo en ambos casos. No hay una diferencia significativa en este aspecto.

RMSE: Los valores de RMSE también son muy similares en ambos conjuntos, lo que indica que las predicciones tienen un error promedio pequeño en relación con los valores reales. No hay una diferencia sustancial en términos de precisión de las predicciones.

R2 y Adj_R2: En términos de la capacidad del modelo para explicar la variabilidad en los datos, el segundo conjunto de resultados muestra un R2 ligeramente más alto y un Adj_R2 ligeramente más bajo en comparación con el primer conjunto. Esto indica que el segundo modelo puede explicar una mayor proporción de la variabilidad en los datos, teniendo en cuenta la complejidad del modelo y el número de variables utilizadas.

En resumen, ambos conjuntos de resultados indican un buen rendimiento del modelo, con predicciones precisas y una capacidad decente para explicar la variabilidad en los datos. Aunque el segundo conjunto muestra una ligera ventaja en términos de explicación de la variabilidad, la diferencia no es significativa. En última instancia, la elección entre los dos conjuntos de resultados dependerá de los criterios y las necesidades específicas de tu problema.


