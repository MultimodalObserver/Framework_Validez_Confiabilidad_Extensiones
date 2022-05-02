---
description: >-
  Esta extensión permite registrar la captura de datos proveniente de la
  actividad en pantalla (de un computador).
---

# 🖥 Captura de Pantalla

A continuación se presenta la evaluación de la extensión basada en la propuesta metodológica previamente descrita. La evaluación considera una sucesión de etapas que permiten determinar la validez y confiabilidad de la misma.

### 1. Identificación de la extensión

* **Nombre:** Captura de Audio.
* **Módulo:** Captura.
* **Datos representados:** Cuantitativos.
* **Características de los datos:** Contínuos.
* **Ejecución:** Intervalo de tiempo.
* **Formato de los datos:** Datos multimedia.
* **Volumen generado:** Según tiempo de captura.

### 2. Definición de las métricas

De acuerdo con los principios, implementación y definiciones establecidas para esta extensión se procede a listar las métricas a evaluar. Para esto, se analiza el funcionamiento de la extensión en conjunto con sus salidas permitiendo establecer:

* **Fotogramas por segundo:** Indica la frecuencia (tasa) de imágenes o cuadros (_frames_) con el que se realizó la captura de pantalla. Su interpretación indica que mientras mayor cantidad de fotogramas, más fluida será la captura.
* **Duración de captura:** Tiempo empleado en una captura de pantalla.
* **Drops:** Indica la cantidad de cuadros _(frames)_ perdidos respecto a lo definido.

### 3. Elección de _ground truth_

Esta extensión opera con un componente de software que permite la captura de una o varias pantallas como fuente de datos y no posee una línea de referencia establecida. Por lo tanto, se debió buscar una herramienta externa que permitiera contrastar los resultados obtenidos por el _plugin_.

Actualmente existen variadas herramientas de _software_ que permiten la captura de la pantalla o escritorio de un equipo, cada una tiene características particulares las cuales deben ser comparadas. Por esto, se aplicó la [metodología de selección](../marco-de-evaluacion/3.-eleccion-de-linea-referencial.md#metodologia-de-seleccion-de-linea-referencial) sugerida para la elección de una línea referencial.

#### Recopilación de datos por herramienta

A continuación se muestra una primera identificación de las posibles líneas referenciales.

![Recopilación de datos para las posibles líneas referenciales (pantalla).
Fuente: Elaboración propia (2022).](../.gitbook/assets/herramientas.png)

Posteriormente, con la información recopilada es posible determinar la madurez de cada herramienta gracias a los criterios mostrados en la siguiente figura. En esta tabla es posible ver que la herramienta externa más apropiada de utilizar es _**OBS Studio**_, obteniendo la máxima puntuación según los criterios evaluados.

![Madurez por herramienta audiovisual.
Fuente: Elaboración propia (2022).](../.gitbook/assets/criterios\_pantalla.png)

La herramienta externa elegida como línea referencial fue **OBS Studio**, la cual permite – entre otras cosas – la captura (grabación) de diversas fuentes de datos multimedia.

### 4. Despliegue del entorno pre-recolección

Se comprobó el correcto despliegue del entorno, considerando la integración de los _plugins_ con MO, la creación del proyecto, participantes y configuraciones propias de la extensión (pantalla, resolución y FPS). En particular, de todas las posibles variaciones de FPS, se definió la captura de pantalla a 15, 30 y 45 FPS.

![Despliegue del entorno para Captura de Pantalla.&#x20;
Fuente: Elaboración propia, (2022).](../.gitbook/assets/config\_pantalla.png)

### 5. Recolección de los datos

Con las configuraciones y consideraciones previamente definidas fue posible llevar a cabo la captura de pantalla. Los resultados obtenidos son evidenciados a continuación.

![Mediciones de las métricas en la captura de pantalla con MO y OBS Studio.
Fuente: Elaboración propia (2022).](../.gitbook/assets/metricas\_pantalla.png)

### 6. Análisis: Validez y Confiabilidad

A partir de la recopilación de mediciones, se obtuvieron medidas de resumen y se calculó el error relativo (%) para determinar la calidad de las medidas. **Los resultados evidenciaron poca validez en términos de los FPS capturados**.

![Resumen y errores relativos por métrica en captura de pantalla.
Fuente: Elaboración propia (2022).](../.gitbook/assets/err\_pantalla.png)

Posteriormente, se obtuvo el coeficiente de varianza para concluir respecto a la variabilidad de las métricas. De acuerdo con los resultados, **se evidenció una alta reproducibilidad de los datos**.

![Coeficiente de varianza para captura de pantalla.
Fuente: Elaboración propia (2022).](../.gitbook/assets/cv\_pantalla.png)

### 7. Documentación de los resultados

Finalmente, acuerdo con los resultados obtenidos respecto en la evaluación de validez y confiabilidad del _plugin_, se generó la documentación respectiva mostrada a continuación.

<details>

<summary>Identificación de los resultados</summary>

* **Nombre:** Extensión de Captura de Pantalla de Multimodal Observer (MO).
* **Descripción**: La extensión de captura de pantalla, permite la captura de datos proveniente de la actividad en pantalla de un equipo durante un intervalo de tiempo (duración de captura).

</details>

<details>

<summary>Validez y Confiabilidad</summary>

Para la evaluación de esta extensión se establecieron las configuraciones necesarias del entorno de trabajo para el correcto funcionamiento del _plugin_. De acuerdo con las configuraciones realizadas, la recolección de datos consistió en la captura de la actividad pantalla a una resolución 1080p, para 15, 30 y 45 FPS. **Los resultados reflejaron una baja validez** en términos de los frames capturados con **errores relativos de hasta un 82,07%** para la captura a 15 FPS. Con respecto a la confiabilidad de las mediciones, la extensión prevee una **buena reproducibilidad de los datos**, con porcentajes de variación inferiores al 4%.

</details>

#### Gráfico de Diana

A continuación se presentan los resultados de la evaluación de validez y confiabilidad de la extensión de captura de pantalla de MO.

![Gráfico de Diana para la captura de pantalla.
Fuente: Elaboración propia (2022).](../.gitbook/assets/diana\_captura\_pantalla.png)
