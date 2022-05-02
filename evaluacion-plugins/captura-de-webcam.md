---
description: >-
  Esta extensión permite registrar la captura de video (formato multimedia)
  proveniente de una Cámara Web.
---

# 📷 Captura de WebCam

A continuación se presenta la evaluación de la extensión basada en la propuesta metodológica previamente descrita. La evaluación considera una sucesión de etapas que permiten determinar la validez y confiabilidad de la misma.

### 1. Identificación de la extensión

* **Nombre:** Captura de WebCam
* **Módulo:** Captura
* **Datos representados:** Cuantitativos.
* **Características de los datos:** Contínuos.
* **Ejecución:** Intervalo de tiempo.
* **Formato de los datos:** Datos multimedia.
* **Volumen generado:** Según tiempo de captura.

### 2. Definición de las métricas

De acuerdo con los principios, implementación y definiciones establecidas para esta extensión se procede a listar las métricas a evaluar. Para esto, se analiza el funcionamiento de la extensión en conjunto con sus salidas permitiendo establecer:

* **Fotogramas por segundo (FPS):** Indica la frecuencia (tasa) de imágenes o cuadros (_frames_) con el que se realizó la de captura de _webcam_. Su interpretación indica que mientras mayor sea esta frecuencia, más fluida será la captura.
* **Duración de captura:** Tiempo en segundos empleado en una captura de cámara.

### 3. Elección de _ground truth_

Debido a que esta extensión opera con un componente electrónico (dispositivo de entrada convencional) genérico, no posee una línea de referencia establecida. Por lo tanto, se debió buscar una herramienta externa que permitiera contrastar los resultados obtenidos por el _plugin._

En la actualidad existen variadas soluciones de software audiovisuales que permiten la captura de fuentes de video a través de cámaras web. Sin embargo, de todas las herramientas investigadas (**OBS Studio, CamStudio, VLC Media Play**_**e**_**r**, entre otras), hubo una en particular que permitía la virtualización de la cámara y no bloqueaba el dispositivo a MO. Esto fue determinante al momento de la elección, por lo que se omitió la aplicación de la metodología de selección sugerida para esta etapa.&#x20;

{% hint style="info" %}
La **virtualización de la cámara web** permite el **uso simultáneo del dispositivo**, es decir, que otro software de captura – independiente de MO – utilice igualmente la cámara como fuente de datos, permitiendo que las mediciones a contrastar estén bajo las mismas condiciones y se efectúen simultáneamente.
{% endhint %}

La herramienta externa elegida fue **ManyCam** en su versión Free (gratuita), la cual permite como máximo la captura a 720p (resolución 1280x720) y 60 FPS.

### 4. Despliegue del entorno pre-recolección

Se comprobó el correcto despliegue del entorno, considerando la integración de los plugins con MO, la creación del proyecto, participantes y configuraciones propias de la extensión (dispositivo, resolución, FPS). En particular, de todas las posibles configuraciones, se definió la captura de cámara web en las resoluciones 480p (720x480) y 720p (1280x720) a 30 y 60 FPS.

![Despliegue del entorno para Captura de WebCam.&#x20;
Fuente: Elaboración propia, (2022).](../.gitbook/assets/config\_webcam.png)

### 5. Recolección de los datos

Con las configuraciones y consideraciones previamente definidas fue posible llevar a cabo la captura de cámara para cada una de ellas. Los resultados obtenidos se evidencian en la siguiente figura.

![Mediciones de las métricas en la captura de cámara web con MO y ManyCam.
Fuente: Elaboración propia (2022).](../.gitbook/assets/mediciones\_webcam.png)

### 6. Análisis: Validez y Confiabilidad

A partir de las mediciones capturadas, se obtuvieron medidas de resumen y calculó el error relativo (%) para determinar la calidad de las medidas. Los resultados evidenciaron una **baja validez** en las medidas obtenidas por la extensión respecto a la referencia.

![Error relativo por métrica en la captura de webcam con MO y ManyCam.
Fuente: Elaboración propia (2022).](../.gitbook/assets/err\_webcam.png)

Posteriormente, se obtuvo el coeficiente de varianza para concluir respecto a la variabilidad de los frames capturados. De acuerdo con los resultados, **se evidenció una alta reproducibilidad de los datos.**

![Coeficiente de varianza para variable FPS.
Fuente: Elaboración propia (2022).](../.gitbook/assets/cv\_webcam.png)

### 7. Documentación de los resultados

Por último, de acuerdo con los resultados obtenidos respecto en la evaluación de validez y confiabilidad del _plugin_, se generó la documentación respectiva, mostrada a continuación.

<details>

<summary>Identificación de la extensión</summary>

* **Nombre:** Extensión de Captura de _WebCam_ de Multimodal Observer (MO).
* **Descripción:** La extensión de captura de _webcam_, permite la captura multimedia (video) de este dispositivo dentro de un intervalo de tiempo (duración de captura).

</details>

<details>

<summary>Validez y Confiabilidad</summary>

Para la evaluación de esta extensión se establecieron las configuraciones necesarias del entorno de trabajo para el correcto funcionamiento del _plugin_. De acuerdo con las configuraciones realizadas, la recolección de datos consistió en la captura de _webcam_ para las resoluciones 480p y 720p a 30 y 60 FPS. Los resultados reflejaron una **baja validez en términos de los FPS capturados y una alta confiabilidad con coeficientes de varianza por debajo del 2%.**

</details>

#### Gráfico de Diana

La siguiente figura representa visualmente los resultados de la evaluación de validez y confiabilidad de la extensión de captura de _webcam_ de MO.

![Gráfico de diana para la captura de webcam.&#x20;
Fuente: Elaboración propia, (2022).](../.gitbook/assets/diana\_captura\_camara.png)
