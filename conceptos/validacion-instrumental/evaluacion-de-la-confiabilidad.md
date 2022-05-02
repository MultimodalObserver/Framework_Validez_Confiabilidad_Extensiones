# Evaluación de la Confiabilidad

> Según Manterola & Otzen (2014), el concepto de confiabilidad está influenciado por quien mide (observador), por el medio con el que se mide (el instrumento) y por lo que es medido (lo observado).&#x20;

Para evitar errores aleatorios se deben tener en consideración todas aquellas fuentes de variabilidad al momento de planificar la medición de variables.

### Tipos de Confiabilidad

A nivel general, existen distintos tipos de confiabilidad clasificados según la fuente de variabilidad.

<details>

<summary>Por parte del observador</summary>

* **Intra-observador:** Ocurre cuando un único observador realiza mediciones repetidas a un grupo de individuos.

<!---->

* **Inter-observador:** Ocurre cuando dos o más observadores evalúan independientemente a un mismo individuo.

</details>

<details>

<summary>Por parte del instrumento</summary>

* **Intra-Instrumento:** Ocurre cuando se realizan mediciones repetidas en un grupo de individuos con un mismo instrumento de medición.&#x20;
* **Inter-Instrumento:** Ocurre cuando se emplean diferentes instrumentos para llevar a cabo mediciones repetidas en grupos de individuos.
* **Test-retest:** Ocurre cuando se aplican dos mediciones sucesivas o con un intervalo de tiempo establecido, a los mismos individuos de estudio.

</details>

{% hint style="info" %}
De acuerdo con el contexto de la evaluación de extensiones de MO, mayoritariamente el tipo de confiabilidad a evaluar será la **Intra-Instrumento**, debido a que responde a los objetivos de las evaluaciones. De igual forma, pueden existir otros escenarios, según sea el caso.
{% endhint %}

## Pruebas, índices y coeficientes estadísticos

A continuación se presentan las principales pruebas o estadísticos para determinar la confiabilidad, las cuales pueden tener distintos enfoques.

{% hint style="info" %}
Se distinguen dos enfoques; **cuantitativo** y **cualitativo**.&#x20;
{% endhint %}

### Enfoque cuantitativo

* **Coeficiente de varianza por mínimos cuadrados**

$$
CV_{RMS} = \sqrt{\frac{\sum_{i=1}^{N}(\frac{\sigma_i}{\mu_i})^2}{N}}\%
$$

{% hint style="info" %}
Donde $$(\sigma_i), (\mu_i)$$ y $$(N)$$, corresponden a la desviación estándar, la media de las medidas y el número de muestras, respectivamente.
{% endhint %}



* **Porcentaje de acuerdo**

Conocido también como acuerdo entre observadores. Mide el porcentaje de concordancia entre los mismos. El procedimiento consiste en la creación de una matriz en donde se representen verticalmente (columnas) a los observadores y horizontalmente (filas) las variables o parámetros medidos. Por lo tanto, las celdas interiores contienen los datos numéricos de cada variable por observador.



* **Método de **_**Bland**_** y **_**Altman**_

Permite determinar el **grado de acuerdo entre dos instrumentos que posean la misma escala de medición**. Esto se consigue mediante una representación gráfica de las diferencias entre dos mediciones respecto a su media. Según Molina (2015), este método permite comparar si una nueva técnica es fiable comparada con la convencional (referencial), es decir, incluye indirectamente un proceso de validez en él. El autor presenta este método a través de un ejemplo para determinar la confiabilidad de un tensiómetro de muñeca para medir presión arterial.

![Gráfica sobre la evaluación de la confiabilidad con el Método de Bland y Altman.
Fuente: (Molina, 2015)](../../.gitbook/assets/Bland-Altman\_ref.jpg)

* **Coeficiente de correlación de Pearson (CC)**

Estadística que representa el grado de asociación lineal entre dos variables cuantitativas.



* Coeficiente de correlación intraclase (CIC)

Estadística que evalúa la concordancia entre variables contínuas (dos o más) en grupos de estudio.



* Coeficiente de correlación de Spearman ($$\rho$$)

Estadística no paramétrica para determinar la relación entre dos variables a través de rangos. Dicha relación no necesariamente puede ser lineal y su formulación considera la diferencia de rangos por elemento $$d$$ y el número de datos $$n$$. Este coeficiente mide el grado de asociación entre dos valores, mas no el nivel de concordancia. Sus valores oscilan entre -1 y 1, en donde un valor de 1 demuestra una perfecta asociación de rango, el valor -1 una perfecta asociación negativa y el valor 0 la ausencia de asociación.

$$
\rho =1-{\frac {6\sum d^{2}}{n(n^2 - 1)}}
$$

* **Índice **_**Kappa**_** de **_**Cohen**_**:**&#x20;

Útil para los tipos de confiabilidad inter e intra observador. Sus posibles valores oscilan entre -1 a 1, siendo éste último valor reflejo de una concordancia perfecta entre los observadores y, por el contrario, el valor 0 ausencia de acuerdo. Según Manterola et al. (2018), matemáticamente es posible obtener valores menores a cero pero son poco probables, por ello se establece como límite el valor -1. A continuación se presentan los indicadores de los valores de _Kappa_.

|     Valores    | Interpretación (acuerdo) |
| :------------: | :----------------------: |
|  \[-1, 0,01\[  |        Sin acuerdo       |
| \[0.01, 0.21\[ |     Ninguno a escaso     |
| \[0.21, 0.41\[ |    Regular o razonable   |
| \[0.41, 0.61\[ |         Moderado         |
| \[0.61, 0.81\[ |        Substancial       |
|   \[0.81, 1]   |       Casi perfecto      |

* **Índice **_**K**_** de **_**Fleiss**_

Útil para determinar la confiabilidad interobservador cuando existen tres o más observadores (variables categóricas).



### Enfoque cualitativo

Respecto a la evaluación de confiabilidad bajo enfoque cualitativo, no es algo simple de definir. Esto es debido a que este enfoque contempla una mayor dificultad para su implementación (considerando un contexto académico), debido a que **se requiere del juicio de un grupo de investigadores observacionales expertos**, según el área de estudio (Castillo y Vásquez, 2003, p. 164). Además, de acuerdo a lo que mencionan las autoras, los “estándares usuales en investigación cuantitativa incluyen a dos elementos; la validez y la confiabilidad. Extrapolar estos criterios a la investigación cuantitativa es contraproducente pues se violan los propósitos, objetivos e integridad del abordaje cualitativo”. Por lo tanto, se opta por no invertir esfuerzo en la definición de este enfoque, en lo que respecta a confiabilidad.

{% hint style="warning" %}
Es necesario aclarar, – porque puede ser una instancia de confusión – que los [tipos de datos cualitativos](../datos.md#datos-cualitativos), no guardan relación con el enfoque cualitativo para evaluar la confiabilidad mencionado en el párrafo anterior. Esto quiere decir que, si se requiere evaluar la confiabilidad desde un enfoque cuantitativo, los datos (cualitativos) podrán ser utilizados siempre y cuando hayan sido previamente tratados (desde su cuantificación, manteniendo su inherencia cualitativa).
{% endhint %}

### Recomendaciones para mejorar la confiabilidad

> _Los puntos mencionados a continuación, comprenden una serie de estrategias y consideraciones a tener presente para mejorar la confiabilidad de las extensiones de MO, basadas en **estrategias que han sido documentadas en práctica clínica y salud** (Manterola & Otzen, 2014)._

1. Mantener los instrumentos de medición (sensores o componentes electrónicos) en buen estado. Esto considera calibración, en caso que corresponda y respecto del estado físico e higiénico de los mismos.
2. Automatizar el proceso de medición, debido a que una menor participación por parte de un operador al momento de una evaluación, ocasionará un menor perjuicio respecto del conocido “efecto observador” y mejora en los tiempos empleados, entre otros.
3. Considerar evaluar y contrastar la confiabilidad bajo las perspectivas unimodal y multimodal, de tal manera de concluir en que los posibles errores presentados no sean aludidos a sobrecargas de procesamiento en el equipo.

{% hint style="info" %}
Efecto Observador: Cuando un observador forma parte de la misma situación que observa puede afectar el comportamiento de los individuos observados, simplemente porque ellos advierten su presencia, afectando negativamente los resultados de una investigación observacional (Díaz, 2011).
{% endhint %}
