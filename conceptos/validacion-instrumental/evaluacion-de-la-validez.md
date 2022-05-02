# Evaluación de la Validez

Al momento de validar una extensión, el primer concepto a evaluar será la validez. La validez implica que el instrumento o el componente de software que utiliza la extensión **está libre de errores excesivos** y **proporciona el resultado esperado**, para el cual fue implementado.

El método para llevar a cabo esta evaluación consiste en primer lugar, en **determinar una línea de referencia validada** – también conocida como verdad fundamental – que cumpla el rol de estándar de referencia sobre el cual contrastar las variables y/o mediciones obtenidas por una determinada extensión y para un estudio o prueba en particular.

Para contrastar los valores obtenidos en la ejecución de un plugin respecto a la referencia, se debe considerar la incorporación de fundamentos estadísticos que evidencian las conclusiones en materia de validez. Por ello, las principales pruebas estadísticas a incluir son la distribución _t de Student_ y el cálculo del error relativo.

{% hint style="info" %}
La prueba _t de Student_ permite determinar si existe diferencia significativa – dado un intervalo de confianza – entre los grupos de mediciones (aquellos obtenidos respecto a los referenciales).
{% endhint %}

{% hint style="info" %}
El error relativo actúa como un factor o indicador de la calidad que presenta una medida.
{% endhint %}

En concreto, **el error relativo** $$(\varepsilon_r)$$ viene dado por el cuociente entre el error absoluto $$(\varepsilon_a)$$ y el valor que se considera como válido $$(X_{ref})$$. Su resultado puede ser positivo o negativo según se produzca por exceso o por defecto y no incluye unidades.

$$
\varepsilon_r=\frac{\varepsilon_a}{X_{ref}}
$$

El error absoluto de una medida $$(\varepsilon_a)$$ viene dado por la diferencia entre el valor obtenido en una medición $$(X_i)$$ y el valor real $$(X_{ref})$$. En este caso el valor del $$(\varepsilon_a)$$ si incluye unidad.



Puede existir la instancia en que la validación de una extensión no sea únicamente un análisis cuantitativo y empírico, si no que depende del juicio subjetivo de un panel de expertos (investigadores o profesionales capacitados) que garanticen el sentido y razón de las mediciones (Pesudovs et al., 2007).&#x20;

Ante tal caso, la validación toma un enfoque cualitativo, en donde se distinguen 3 tipos:

{% tabs %}
{% tab title="Validez de Contenido" %}
Comprende un análisis cualitativo a través de la revisión de la literatura sobre los criterios e individuos evaluados, junto a la opinión de expertos (Sanchez & Echeverry, 2004).
{% endtab %}

{% tab title="Validez de Criterio" %}
La metodología considera la comparación con una línea de referencia, analizando valores a través de correlación estadística. Un estimador a considerar es el c_oeficiente de correlación de Pearson_ (Sanchez & Echeverry, 2004).
{% endtab %}

{% tab title="Validez de Constructo" %}
Consiste en un juicio basado en la acumulación de evidencia de numerosos estudios que utilizan un determinado instrumento de medición. La evaluación de la validez del constructo requiere examinar la relación de la medida que se evalúa con las variables que se sabe que están relacionadas o teóricamente relacionadas con el constructo medido por el instrumento (Kimberlin & Winterstein, 2008, p. 2279).
{% endtab %}
{% endtabs %}

{% hint style="info" %}
Para mejorar la validez de una extensión, el principal punto a tener presente es reconsiderar, analizar los algoritmos y/o métodos propios implementados para la extensión e integración con el instrumento de medición, de tal manera de lograr erradicar aquellos errores sistemáticos que perjudican los resultados de medición.
{% endhint %}
