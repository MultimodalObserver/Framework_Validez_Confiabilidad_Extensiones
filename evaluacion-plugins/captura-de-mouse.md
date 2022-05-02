---
description: >-
  Esta extensión permite registrar los eventos asociados a la utilización u
  operación de un mouse.
cover: ../.gitbook/assets/mouse_background.jpg
coverY: -51.97687861271688
---

# 🖱 Captura de Mouse

A continuación se presenta la evaluación de la extensión basada en la propuesta metodológica previamente descrita. La evaluación consideró la aplicación de la sucesión de etapas que permitieron determinar la validez y confiabilidad del plugin.

### 1. Identificación de la extensión

* **Nombre:** Captura de Mouse.
* **Módulo:** Captura.
* **Datos representados:** Cuantitativos
* **Características de los datos:** Discretos.
* **Ejecución:** Intervalo de tiempo.
* **Formato de los datos:** Datos en texto plano.
* **Volumen generado:** Volumen reducido.

### 2. Definición de las métricas

De acuerdo con los principios, implementación y definiciones establecidas para esta extensión se procedió a listar las métricas a evaluar. Para esto, se analizó el funcionamiento de la extensión en conjunto con sus salidas, permitiendo establecer:

* **Coordernada Inicial:** Representa la coordenada de origen del proceso de captura, es decir, aquella coordenada (punto) sobre la cuál se encontraba el puntero del mouse en ese momento.
* **Coordenada Final:** Representa la coordenada final del proceso de captura, es decir, la última coordenada registrada.
* _**Clicks**_** totales:** Representa la cantidad total de clicks realizados.
* **Número de **_**clicks**_** izquierdos:** Indica la cantidad de clicks totales realizados únicamente sobre el botón izquierdo del mouse.
* **Número de **_**clicks**_** derechos:** Indica la cantidad de clicks totales realizados únicamente sobre el botón derecho del mouse.

### 3. Elección de _ground truth_

Debido a que esta extensión opera con un componente electrónico (dispositivo de entrada convencional) genérico, no posee una línea de referencia establecida. Por lo tanto, se debería buscar una herramienta externa que permita contrastar los resultados obtenidos por el plugin. En donde, la herramienta externa elegida debe ser determinada por la [**metodología de selección propuesta**](../marco-de-evaluacion/3.-eleccion-de-linea-referencial.md#metodologia-de-seleccion-de-linea-referencial).

Sin embargo, para los plugins de mouse y teclado, el profesor guía sugirió el uso de la herramienta de software **MacroRecorder**. Por lo tanto, en estas extensiones se omitió la aplicación de la etapa de selección de la metodología.

{% hint style="info" %}
**MacroRecorder** __ es programa que permite la grabación de los eventos de _mouse_ y teclado tales como _clicks_, movimientos, pulsaciones de teclas, tiempos de espera, etcétera; para su posterior reproducción.
{% endhint %}

![Interfaz gráfica de MacroRecorder.&#x20;
Fuente: Bartels Media GmbH (s.f.).](<../.gitbook/assets/mr2 (1).png>)

Para lograr su cometido, **MacroRecorder** posee un editor sobre el cual se pueden secuenciar los eventos que se quieran automatizar, los cuales pueden ser almacenados en un _script_ (formato “.mrf”) o exportados a formato “.csv”. El programa está disponible para Windows y Mac, a través de dos versiones, una gratuita y una de pago. Para este trabajo se usó la versión de pago.

### 4. Despliegue del entorno de prueba (pre-recolección)

Se comprobó el correcto despliegue del entorno prerecolección de datos, el cual consideró tener los plugins integrados en MO, la creación del proyecto y de los participantes, tal como muestra la figura a continuación.

![Despliegue del entorno para Captura de Mouse.&#x20;
Fuente: Elaboración propia, (2022).](../.gitbook/assets/conf\_mouse.png)

Además, para esta ocasión fue posible simular la recolección de datos a través de la misma línea referencial. Por esto, se creó un _script_ con los eventos de _mouse_ para las pruebas. La siguiente figura muestra parte de la plantilla contenedora de una serie de eventos.

![Extracto de script para Captura de Mouse.&#x20;
Fuente: Elaboración propia, (2022).](../.gitbook/assets/script\_mouse.png)

### 5. Recolección de los datos

Hasta esta instancia se contaba con lo necesario para poder realizar la recolección de los datos. Se ejecutó la captura de _mouse_ dentro de MO en cinco ocasiones al momento de reproducir el script con la serie de eventos capturados a través de MacroRecorder. La siguiente tabla muestra la recolección de las mediciones de MO y _MacroRecorder_ (MR), en la captura de _mouse_.

**Tabla 5.1: Mediciones de las métricas en la captura de **_**mouse**_** con MO y MR.**

![Fuente: Elaboración propia (2022).](../.gitbook/assets/captura\_tabla1.png)

### 6. Análisis: Validez y Confiabilidad

Para determinar la validez en este tipo de extensiones se sugiere estudiar si existe diferencia significativa entre las mediciones. No obstante, fue evidente notar que la mayoría de mediciones coincide con la referencia, además de que no fue posible aplicar _t de Student_ debido a que las mediciones eran constantes, por lo tanto estas pruebas fueron descartadas. De igual forma, se calculó el error relativo de cada métrica, que fue de utilidad al momento de concluir sobre la validez de la extensión. Respecto de las métricas que presentaron error relativo su valor es despreciable por tratarse de un porcentaje inferior al 1% (considerando una resolución 1080p), especfíficamente 0,15%. La Tabla 5.2 muestra los errores relativos por métrica.

**Tabla 5.2: Mediciones de las métricas en la captura de mouse con MO y MacroRecorder (MR).**

![Fuente: Elaboración propia (2022).](../.gitbook/assets/captura\_tabla2.png)

Respecto a la evaluación de confiabilidad de esta extensión, se calculó el coeficiente de varianza por mínimos cuadrados por métrica para concluir sobre reproducibilidad de los resultados. La Tabla 5.3 reúne los valores calculados. Sin embargo, como era predecible, la nula variación de los resultados demostró una completa reproducibilidad de las medidas.

![Fuente: Elaboración propia (2022).](../.gitbook/assets/captura\_tabla3.png)

### 7. Documentación de resultados

Por último, de acuerdo con los resultados obtenidos respecto en la evaluación de validez y confiabilidad del _plugin_, se generó la documentación respectiva presentada a continuación.

<details>

<summary>Identificación de la extensión</summary>

* **Nombre:** Extensión de Captura de Mouse de Multimodal Observer (MO).
* **Descripción:** La extensión de captura de _mouse_, permite el registro de eventos asociados a la utilización de este periférico (principalmente _clicks_ y registro de coordenadas).

</details>

<details>

<summary>Validez y Confiabilidad</summary>

Para evaluar la validez y confiabilidad de la extensión se realizaron cinco pruebas simuladas utilizando como línea de referencia la herramienta de _software_ _MacroRecorder._ Se hizo el correcto despliegue de la extensión, lo cual permitió realizar cinco pruebas simuladas a través de un _script_ que contenía un total de 87 acciones (entre esperas, _clicks_ presionados y movimientos del cursor registrados según coordenadas). En cuanto a los resultados obtenidos, las mediciones realizadas con la extensión de MO fueron completamente reproducibles con porcentajes de variación del 0% para todas las métricas. Su validez con respecto a _MacroRecorder_ fue bastante alta, con errores inferiores al 1% en las coordenadas del eje de las abscisas (inicial y final) del proceso de captura, e igualmente para la coordenada final del eje de las ordenadas. Para el resto de las métricas, no existieron errores.

</details>

#### Gráfico de Diana

La Figura 5.4 mostrada a continuación representa visualmente los resultados de la evaluación de validez y confiabilidad de la extensión de captura de _mouse_ de MO.

![Figura 5.4: Gráfico de diana para la captura de mouse.&#x20;
Fuente: Elaboración propia, (2022).](../.gitbook/assets/diana\_captura\_mouse.png)
