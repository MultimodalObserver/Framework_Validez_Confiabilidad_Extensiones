---
description: >-
  Esta extensión permite registrar la captura de datos proveniente de una fuente
  de audio. Por lo general, un dispositivo de entrada con micrófono.
---

# 🎙 Captura de Audio

A continuación se presenta la evaluación de la extensión basada en la propuesta metodológica previamente descrita. La evaluación considera una sucesión de etapas que permiten determinar la validez y confiabilidad de la misma.

### 1. Identificación de la extensión

* **Nombre:** Captura de Audio
* **Módulo:** Captura
* **Datos representados:** Cuantitativos.
* **Características de los datos:** Contínuos.
* **Ejecución:** Intervalo de tiempo.
* **Formato de los datos:** Datos multimedia.
* V**olumen generado:** Según tiempo de captura.

### 2. Definición de las métricas

De acuerdo con los principios, implementación y definiciones establecidas para esta extensión se procede a listar las métricas a evaluar. Para esto, se analiza el funcionamiento de la extensión en conjunto con sus salidas permitiendo establecer:

* **Sampling rate:** Número de muestras por segundo (o por otra unidad) tomadas de una señal continua para hacer una señal discreta o digital. Para las señales en el dominio del tiempo, como las formas de onda del sonido (y otros tipos de contenido audiovisual), las frecuencias se miden en hercios (Hz) o ciclos por segundo (FADGI, s.f.).
* **Duración de captura:** Tiempo empleado en una captura de audio.
* **Bit Depth:** Determina el número de posibles valores de amplitud que podemos grabar para cada muestra. Las profundidades de bits de audio más comunes son 16, 24 y 32 bits (Brown, 2021).

### 3. Elección de _ground truth_

Debido a que esta extensión opera con un componente electrónico (dispositivo de entrada convencional) genérico, no posee una línea de referencia establecida. Por lo tanto, se debió buscar una herramienta externa que permitiera contrastar los resultados obtenidos por el _plugin_.

A continuación, se presenta la metodología de selección de línea referencial. De acuerdo con ella, la herramienta externa escogida fue [**Audacity**](https://www.audacityteam.org/download/). Sus motivos, en conjunto con la maduración del _software_ como tal, fueron que corresponde a una herramienta gratuita focalizada en la grabación y edición de audio.

#### Recopilación de datos por herramienta

La siguiente figura muestra una primera identificación de las posibles líneas referenciales.

![Recopilación de datos para las posibles líneas referenciales.
Fuente: Elaboración propia (2022).](<../.gitbook/assets/herramientas (1).png>)

Posteriormente, con la información recopilada es posible determinar la madurez de cada herramienta gracias a los criterios de la tabla mostrada a continuación. En esta tabla es posible ver que la herramienta externa más apropiada de utilizar es _**Audacity**_, obteniendo la máxima puntuación según los criterios evaluados.

![Evaluación de madurez por herramienta.
Fuente: Elaboración propia (2022).](../.gitbook/assets/criterios.png)

### 4. Despliegue del entorno pre-recolección

Se comprobó el correcto despliegue del entorno, considerando la integración de los _plugins_ con MO, la creación del proyecto, participantes y configuraciones propias de la extensón (dispositivo y _sampling rate_). En particular, de todas las posibles configuraciones, se definió la captura de audio para un micrófono conectado a través del jack (conector) de 3.5mm del equipo con sampling rate de 44.1 y 100 \[kHZ].

![Despliegue del entorno para Captura de Audio.&#x20;
Fuente: Elaboración propia, (2022).](../.gitbook/assets/config\_audio.png)

### 5. Recopilación de los datos

Con las configuraciones y consideraciones previamente definidas fue posible llevar a cabo la captura de audio para cada una. Los resultados obtenidos son presentados a continuación.

![Mediciones de las métricas en la captura de audio con MO y Audacity.
Fuente: Elaboración propia (2022).](../.gitbook/assets/mediciones\_audio.png)

### 6. Análisis: Validez y Confiabilidad

A partir de las mediciones capturadas, se obtuvieron medidas de resumen y calculó el error relativo (%) para determinar la calidad de las medidas. **Los resultados evidenciaron una buena validez** en las medidas obtenidas por la extensíón, respecto a la referencia.

![Resumen de resultados y error relativo en la captura de audio.
Fuente: Elaboración propia (2022).](../.gitbook/assets/err\_audio.png)

Posteriormente, se obtuvo el coeficiente de varianza para concluir respecto a la variabilidad de las métricas. De acuerdo con los resultados, **se evidenció una alta reproducibilidad de los datos.**

![Coeficiente de varianza para captura de audio.
Fuente: Elaboración propia (2022).](../.gitbook/assets/cv\_audio.png)

### 7. Documentación de los resultados

Por último, de acuerdo con los resultados obtenidos respecto en la evaluación de validez y confiabilidad del _plugin_, se generó la documentación respectiva, mostrada a continuación.

<details>

<summary><strong>Identificación de la extensión</strong></summary>

* **Nombre:** Extensión de Captura de Audio de Multimodal Observer (MO).
* **Descripción:** La extensión de captura de audio, permite la captura de fuentes de audio dentro de un intervalo de tiempo (duración de captura).

</details>

<details>

<summary>Validez y Confiabilidad</summary>

Para la evaluación de esta extensión se establecieron las configuraciones necesarias del entorno de trabajo para el correcto funcionamiento del _plugin_. De acuerdo con las configuraciones realizadas, la recolección de datos consistió en la captura de audio a través un micrófono conectado al jack (conector) de 3.5mm del computador, en donde se configuró un sampling rate de 44.1 y 100 \[kHZ]. Los resultados reflejaron una **completa validez de los datos** para la tasa de muestreo de ambas configuraciones. Respecto de la confiabilidad **se obtuvieron coeficientes de varianza por debajo del 4%** para los tiempos capturados y nula variación en las tasas de muestreo.

</details>

#### Gráfico de Diana

A continuación se representan los resultados de la evaluación de validez y confiabilidad de la extensión de captura de audio de MO.

![Gráfico de diana para la captura de audio.&#x20;
Fuente: Elaboración propia, (2022).](../.gitbook/assets/diana\_captura\_audio.png)
