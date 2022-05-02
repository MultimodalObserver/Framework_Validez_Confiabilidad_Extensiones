---
description: >-
  Esta extensión permite registrar los eventos asociados a la utilización u
  operación de un teclado o keyboard.
---

# ⌨ Captura de Teclado

A continuación se presenta la evaluación de la extensión basada en la propuesta metodológica previamente descrita. La evaluación considera una sucesión de etapas que permiten determinar la validez y confiabilidad de la misma.

### 1. Identificación de la extensión

* **Nombre**: Captura de Teclado
* **Módulo:** Captura
* **Datos representados:** Cuantitativos.
* **Características de los datos:** Discretos.
* **Ejecución:** Intervalo de tiempo.
* **Formato de los datos:** Datos en texto plano.
* **Volumen generado:** Volumen reducido.

### 2. Definición de las métricas

De acuerdo con los principios, implementación y definiciones establecidas para esta extensión se procede a listar las métricas evaluadas. Para esto, se analizó el funcionamiento de la extensión en conjunto con sus salidas permitiendo establecer:

* _**Keystrokes**_** totales:** Cantidad de pulsaciones de tecla realizadas.
* **Palabras correctas:** Indica la cantidad de palabras correctamente capturadas. El criterio para considerar que una palabra ha sido “capturada correctamente” consiste en evaluar si la presunta palabra es entendible o no.
* _**Levenshtein Distance:**_ La distancia de Levenshtein, “es una métrica de strings (o cadénas de carácteres) para medir la distancia entre dos secuencias o palabras” (Cuelogic, 2017, párrafo 1), entendiendo que la distancia corresponde al “número mínimo de inserciones, eliminaciones o sustituciones de carácteres para convertir una cadena en otra” (Rodríguez, 2020, párrafo 2). Su interpretación indica que mientras mayor sea la distancia entre dos cadenas de carácteres, más diferencia existe entre éstas.

### 3. Elección de _ground truth_

La línea referencial para esta extensión fue determinada por las mismas condiciones mencionadas en la de la evaluación del plugin de [captura de mouse](captura-de-mouse.md#3.-eleccion-de-ground-truth). De acuerdo con esto, la línea referencial definida fue **MacroRecorder**.

### 4. Despliegue del entorno pre-recolección

De igual forma que con la evaluación del _plugin_ anterior, se comprobó el correcto despliegue del entorno pre recolección de datos, el cual consideró tener los _plugins_ integrados en MO, la creación del proyecto y de los participantes, tal como muestra la figura a continuación.

![Despliegue del entorno para Captura de Teclado.&#x20;
Fuente: Elaboración propia, (2022).](../.gitbook/assets/conf\_teclado.png)

Además se consideró la creación del _script_ que permitió la simulación de las pruebas realizadas en la siguiente etapa de recolección de los datos.

![Extracto de script para Captura de Teclado.&#x20;
Fuente: Elaboración propia, (2022).](../.gitbook/assets/script\_tecl.png)

### 5. Recolección de los datos

Una vez desplegado el ambiente necesario para evaluar la extensión, se ejecutó la captura de teclado dentro de MO en cinco ocasiones considerando el _script_ para la simulación de las pruebas.

Para la determinación de la métrica _Levenshtein Distance_ se consideró el uso de la función **`stringdist()`** perteneciente a la _librería stringdist_ del lenguaje de programación R. La sintáxis de la función viene dada por:

```
stringdist(<string1>,<string2>, method = "lv")
```

En donde los parámetros `<string1>` y `<string2>` corresponden a las entradas de cadenas de carácteres a medir su distancia y `method = "lv"` al método empleado para el cálculo de la misma.



La siguiente figura muestra la recolección de las mediciones de MO con respecto a MacroRecorder (MR).

![Mediciones de las métricas en la captura de teclado con MO y MacroRecorder (MR).
Fuente: Elaboración propia (2022).](../.gitbook/assets/mediciones\_metricas\_teclado.png)

### 6. Análisis: Validez y Confiabilidad

De acuerdo a los resultados obtenidos, fue evidente notar que con respecto a la referencia, esta extensión entrega mediciones completamente válidas. Esto es evidenciado junto al nulo error relativo en los resultados previstos por cada métrica. (Ver figura a continuación).

![Errores relativos de las métricas en la captura de teclado con MO y MacroRecorder (MR).
Fuente: Elaboración propia (2022).](../.gitbook/assets/err\_teclado.png)

De igual manera, los resultados demuestran una completa reproducibilidad de los datos (Figura a continuación), lo que significa que esta extensión es confiable en sus resultados.

![Coeficiente de varianza por métrica de teclado.
Fuente: Elaboración propia (2022).](../.gitbook/assets/cv\_teclado.png)

### 7. Documentación de resultados

Para finalizar con esta evaluación se generó la documentación respectiva con las conclusiones y resultados obtenidos, mostrados a continuación.

<details>

<summary><strong>Identificación de la extensión</strong></summary>

* **Nombre:** Extensión de Captura de Teclado de Multimodal Observer (MO).
* **Descripción:** La extensión de captura de teclado, permite el registro de eventos asociados a la utilización de este periférico (principalmente keystrokes o pulsaciones de tecla).

</details>

<details>

<summary>Validez y Confiabilidad</summary>

La evaluación de validez y confiabilidad se realizó en base a pruebas simuladas utilizando como línea de referencia la herramienta de software **MacroRecorder.** Luego de la propia identificación del _plugin,_ se hizo el correcto despliegue del mismo, lo cual permitió realizar cinco pruebas simuladas a través de un _script_ que contenía un total de 156 acciones (entre esperas y pulsaciones de teclado). Los resultados obtenidos demostraron que esta extensión ofrece una completa validez con respecto a la referencia _MacroRecorder_, **sin presencia de errores**. Por parte de la reproducibilidad de los datos el panorama es similar, **sin presentar variaciones** entre las diferentes pruebas medidas.

</details>

#### Gráfico de Diana

![Gráfico de diana para la captura de teclado.&#x20;
Fuente: Elaboración propia, (2022).](../.gitbook/assets/diana\_captura\_teclado.png)
