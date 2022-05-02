---
cover: ../.gitbook/assets/mo_ext.png
coverY: -69.08092485549132
---

# Multimodal Observer

**Multimodal Observer (MO)** es un software de **código abierto**, **modular**, **multiplataforma** y **extensible** dirigido a investigadores observacionales para simplificar sus estudios con **datos multimodales**. Su primera iteración fue desarrollada por Gutiérrez (2016) y dado que una de sus características principales es la extensibilidad, ha permitido generar una sucesión de nuevos desarrollos e iteraciones a partir del software base para la incorporación de nuevas funcionalidades y/o fuentes de datos.

{% embed url="https://mo.informatica.usach.cl/assets/images/todo.gif" %}
**Ejemplo de visualización multimodal en MO.**\
Fuente: Multimodal Observer (s.f.).&#x20;
{% endembed %}

Por lo general los nuevos desarrollos se presentan como extensiones, las cuales son añadidas para complementar a la herramienta principal. Además, las extensiones desarrolladas apuntan a resolver o apoyar una etapa específica dentro del plano de una investigacíón observacional.&#x20;

{% hint style="info" %}
Hasta la fecha **se han desarrollado más de diez trabajos de titulación** entorno a la herramienta.
{% endhint %}

## Estructura

MO cuenta con una **estructura de tres capas**, que van desde los lineamientos generales de la arquitectura (_core_) a lo más específico (módulos y extensiones). En la siguiente figura se puede apreciar una representación visual, separando verticalmente cada etapa por las líneas punteadas.

![Capas de la arquitectura de MO.
Fuente: Adaptación de Multimodal Observer (s.f.).](../.gitbook/assets/arquitectura\_mo.png)

* En la **capa general** se encuentra el MO Core que posee las definiciones de las principales funcionalidades del sistema (iniciador de la aplicación, gestión de preferencias, internacionalización, ventanas e interfaz de usuario y mecanismo para extensiones, por nombrar algunas). En el mismo módulo existe un submódulo encargado de la organización de los proyectos que operen dentro de la herramienta y se definen las interfaces necesarias para agregar módulos y extensiones.
* La **capa intermedia** también contiene módulos, Gutiérrez (2016) los denominó StageModules haciendo referencia la división de las etapas de un proyecto de investigación (captura, visualización, análisis u otra según corresponda), estos deben proveer especializaciones para iniciar las acciones que sus correspondientes extensiones tengan que ejecutar. Desde la primera iteración de la herramienta hasta el segundo semestre del 2021, se han desarrollado siete módulos, listados a continuación.

1. **Módulo de Organización de proyectos**
2. **Módulo de Captura**
3. **Módulo de Visualización**
4. **Módulo de Análisis**
5. **Módulo de Manejo de extensiones**
6. **Módulo de Comunicación**
7. **Módulo Asistente**

* Por último, en la **capa específica** se encuentran las[ **extensiones o **_**plugins**_](extensiones-plugins/) de los StageModules, denominadas StagePlugins. Dichas extensiones deben su especificidad debido a que ejecutan instrucciones particulares según su propósito definido.

{% hint style="info" %}
Por ejemplo, un _plugin_ es la implementación asociada a la captura de datos desde un _mouse_, teclado o biosensor.
{% endhint %}
