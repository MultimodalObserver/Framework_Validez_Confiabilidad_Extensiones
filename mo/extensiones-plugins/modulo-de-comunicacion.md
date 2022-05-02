# Módulo de Comunicación

Este módulo define lo necesario para implementar una extensión de captura y visualización en tiempo real (_streaming_). Además provee a estos módulos (captura y visualización) los elementos y directrices para operar tanto de manera local como en _streaming_.

{% hint style="info" %}
A partir de la implementación de este módulo (Cáceres, 2018), MO debió adoptar una arquitectura cliente-servidor para mitigar y dar solución a la problemática que en este entonces se tenía, correspondiente al “efecto observador”.&#x20;
{% endhint %}

Las extensiones desarrolladas que pertenecen a este módulo y aquellas que fueron modificadas para que fueran transmisibles son:

* Captura remota de teclado (Cáceres, 2018)
* Visualización remota de teclado (Cáceres, 2018)
* _Streaming_ directo de pantalla (Cáceres, 2018)
* Visualización de _streaming_ directo de pantalla (Cáceres, 2018)
* Chat (Cáceres, 2018)
* Notas remotas (Cáceres, 2018)
* Visualización en tiempo real de procesos activos (Cerda, 2019)
* Visualización en tiempo real de datos de actividad de navegación _web_ (Cerda, 2019)

{% hint style="info" %}
Además, MO posee una extensión multi-navegador _web_ desarrollada por Cerda (2019) complementaria a las extensiones de monitoreo de la actividad de navegación _web_ nombradas anteriormente, que permite la captura de diferentes [métricas](../../conceptos/metricas.md) desde un navegador compatible.
{% endhint %}
