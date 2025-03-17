# AquaSense: Sistema de Riego Autónomo por Goteo con Sensores de Humedad para Optimización del Uso del Agua en Cultivos

Este repositorio documenta el desarrollo de AquaSense, un sistema innovador diseñado para regular de forma autónoma el riego por goteo en cultivos. La solución se basa en el uso de sensores de humedad que, al medir continuamente el estado del suelo en un área de 100 cm x 100 cm, permiten ajustar el suministro de agua de manera precisa, promoviendo la eficiencia y sostenibilidad en la agricultura.

[Versión en Inglés](https://github.com/x-lui-x-16/AquaSense-Project-ENG)


## Índice
- Materiales de Ingeniería
- Instrucciones de Construcción
- Contenido
- Introducción
- Objetivos
- Beneficiarios e Impacto
- Metodología
- Explicación del Código
- Componentes y Gestión del Sistema
- Resultados Esperados
- Presupuesto
- Conclusión
- Bibliografía


## Materiales de Ingeniería
- Arduino Mega 2560: Procesador que lee los datos de los sensores de humedad y controla la electroválvula o bomba.
- Sensores de Humedad (9 unidades): Dispuestos estratégicamente para medir la humedad en distintas zonas del área de cultivo.
- Electrovalvula / Bomba de Agua: Regula el flujo de agua hacia el sistema de riego.
- Relé: Permite el control seguro de la electroválvula o bomba, evitando sobrecargas en el Arduino.
- Tuberías de Plástico y Gotero: Distribuyen el agua de forma uniforme en el área de riego.
- Fuente de Alimentación: Puede ser una batería o un adaptador de corriente, que asegura el funcionamiento continuo de todo el sistema.
- Protoboard y Cables Conectores: Facilitan las conexiones temporales y pruebas del circuito.
- Recipiente de Agua: Fuente desde la cual se extrae el agua para el riego.


## Instrucciones de Construcción
### Montaje del Hardware:
- Conecta los sensores de humedad al Arduino usando la protoboard y cables.
- Integra la electroválvula o bomba de agua mediante un relé para controlar el flujo de agua.
- Distribuye las tuberías y goteros a lo largo del área de cultivo (100 cm x 100 cm).

### Configuración del Circuito Electrónico:
- Asegura que cada sensor esté asignado a un pin digital para recibir las lecturas.
- Configura el relé para permitir al Arduino activar o desactivar la electroválvula de forma segura.

### Montaje del Sistema de Riego:
- Une las tuberías de plástico a la electroválvula o bomba, distribuyéndolas uniformemente en el área de cultivo.
- Coloca los goteros en cada sección, garantizando una distribución homogénea del agua.

### Pruebas y Calibración:
- Calibra cada sensor comparando las lecturas en suelo seco y húmedo.
- Realiza pruebas controladas para verificar la respuesta del relé y el flujo de agua.


## Contenido del Repositorio
[Código](src/): Código fuente para la programación del Arduino.

[Esquemas](esquemas/): Diagramas y esquemas eléctricos del sistema.

[Imagenes del Proyecto](p-photos/): Fotografías del montaje, pruebas y funcionamiento del prototipo.


## Introducción
La agricultura es esencial para la seguridad alimentaria y la economía, especialmente en regiones donde el agua es un recurso limitado. Tradicionalmente, muchos productores utilizan métodos de riego poco eficientes, lo que provoca un uso excesivo del agua. AquaSense surge para automatizar el riego por goteo mediante sensores de humedad, permitiendo un control preciso del agua suministrada directamente a las raíces. Esta solución no solo optimiza el consumo de agua, sino que también mejora la salud de los cultivos, contribuyendo a una agricultura más sostenible y resiliente ante el cambio climático.


## Objetivos
### Objetivo General
Diseñar e implementar un sistema autónomo de riego por goteo que, basado en la medición continua de la humedad del suelo, regule el suministro de agua en un área de 100 cm x 100 cm, optimizando el uso del recurso hídrico.

### Objetivos Específicos
Medición de la Humedad: Utilizar nueve sensores de humedad distribuidos estratégicamente para obtener un promedio representativo del estado del suelo.
Control Automatizado: Programar el Arduino para que, en función de las lecturas, active la electroválvula o bomba de agua solo cuando sea necesario.
Comparativa de Eficiencia: Evaluar el ahorro de agua y eficiencia del sistema en comparación con métodos tradicionales de riego.
Impacto en el Crecimiento de Cultivos: Analizar el efecto del riego controlado en el desarrollo y salud de las plantas.


## Beneficiarios e Impacto
### Beneficiarios
Agricultores y Pequeños Productores: Reduciendo costos y mano de obra al automatizar el riego.

Comunidades Rurales: Optimización del uso del agua en zonas con recursos hídricos limitados.

Instituciones Educativas y de Investigación: Plataforma para la enseñanza y experimentación en agricultura de precisión.

Gobiernos y Organismos de Desarrollo: Herramienta para impulsar prácticas agrícolas sostenibles y mejorar la seguridad alimentaria.

### Impacto del Proyecto
Ambiental: Disminución del consumo de agua y protección de acuíferos.

Económico: Reducción de costos operativos y mayor productividad de cultivos.

Social: Promoción de prácticas agrícolas responsables y educación ambiental.

Innovador: Plataforma escalable y adaptable que puede integrarse con energías renovables y otras tecnologías emergentes.


## Metodología
El desarrollo de AquaSense se ha estructurado en varias fases:
### Diseño y Distribución de Sensores:
- Ubicación estratégica de nueve sensores en el área de 100 cm x 100 cm para obtener mediciones precisas.

### Configuración del Circuito Electrónico:
- Conexión de sensores y relé al Arduino, asegurando la protección y correcta interpretación de las señales.

### Programación del Arduino:
- Lectura periódica de los sensores.
- Cálculo del promedio de humedad.
- Activación de la electroválvula o bomba si el promedio está por debajo del umbral establecido.
- Desactivación automática una vez que se alcanza el nivel óptimo.

### Montaje y Pruebas del Sistema de Riego:
- Integración de tuberías y goteros.
- Calibración y verificación en condiciones controladas.

### Implementación en Campo y Monitoreo:
- Instalación en el área de cultivo y seguimiento del desempeño.
- Registro de datos para análisis comparativo con métodos tradicionales.

### Evaluación de Eficiencia:
- Análisis de consumo de agua, frecuencia de riego y efectos en el crecimiento de las plantas.


## Explicación del Código
[El código fuente](src/) (ubicado en la carpeta /src) está desarrollado en C++ para el Arduino y cumple las siguientes funciones:

- Inicialización: Configuración de pines para los sensores, relé y otros componentes.
- Lectura de Datos: Captura periódica de las señales de los sensores de humedad.
- Procesamiento: Cálculo del promedio de humedad del área.
- Control: Activación y desactivación automática de la electroválvula o bomba según el umbral definido.
- Manejo de Errores: Rutinas de calibración y verificación para asegurar la fiabilidad del sistema.


## Componentes y Gestión del Sistema
### Componentes del Sistema
- Sensores de Humedad: Para la medición continua del estado del suelo.
- Electrovalvula/Bomba y Relé: Permiten controlar el flujo de agua de forma segura y automatizada.
- Infraestructura del Riego: Tuberías y goteros para una distribución uniforme del agua.
- Fuente de Energía: Adaptable a soluciones de energía renovable (por ejemplo, paneles solares) para operación en áreas remotas.

### Gestión del Sistema
- Monitoreo en Tiempo Real: Los datos de humedad se registran y se pueden visualizar para ajustes futuros.
- Automatización del Riego: El sistema responde de forma automática a las condiciones del suelo, evitando el desperdicio de agua.
- Escalabilidad y Flexibilidad: El diseño modular permite adaptar el sistema a diferentes áreas de cultivo y necesidades específicas.


## Resultados Esperados
- Reducción del Consumo de Agua: Se proyecta un ahorro del 30-50% comparado con métodos convencionales.
- Mejor Salud de los Cultivos: Riego óptimo que favorece el crecimiento y la vitalidad de las plantas.
- Recopilación de Datos para Optimización: Generación de registros que facilitarán la toma de decisiones en la gestión agrícola.
- Funcionamiento Autónomo: Minimización de la intervención manual y mayor eficiencia en el manejo del riego.


## Presupuesto
(Espacio reservado para que ingreses el detalle del presupuesto y costos asociados a la implementación del sistema.)

## Conclusión
AquaSense representa un avance en la aplicación de tecnologías de automatización en la agricultura, ofreciendo una solución integral para el riego por goteo que responde a las necesidades reales del suelo. La implementación de este sistema no solo promueve el uso eficiente del agua, sino que también contribuye a la sostenibilidad ambiental y al fortalecimiento de la seguridad alimentaria. Su diseño escalable y adaptable lo convierte en una herramienta accesible para pequeños agricultores y proyectos de investigación, abriendo la puerta a futuras innovaciones en el campo de la agricultura de precisión.

## Bibliografía
FAO. (2021). Uso sostenible del agua en la agricultura. [https://www.fao.org](https://www.fao.org)

IDIAP. (2022). Prácticas sostenibles en la agricultura de Panamá. [https://www.idiap.gob.pa](https://www.idiap.gob.pa)

Netafim. (2020). Tecnología de riego por goteo. [https://www.netafim.com](https://www.netafim.com)

Ministerio de Desarrollo Agropecuario. (2023). Iniciativas de riego en Panamá. [https://www.mida.gob.pa](https://www.mida.gob.pa)

Arduino.cc. (2023). Arduino Mega 2560 Rev3. [https://www.arduino.cc/en/Guide/ArduinoMega2560](https://www.arduino.cc/en/Guide/ArduinoMega2560)

Adafruit. (2019). Soil Moisture Sensor Guide. [https://learn.adafruit.com/adafruit-stem](https://learn.adafruit.com/adafruit-stem)

SparkFun Electronics. (2023). Soil Moisture Sensor Hookup Guide. [https://learn.sparkfun.com/tutorials/soil-moisture-sensor-hookup-guide](https://learn.sparkfun.com/tutorials/soil-moisture-sensor-hookup-guide)

Banzi, M., & Shiloh, M. (2015). Getting Started with Arduino (3.ª ed.). Maker Media.

Torres, L., & Valencia, J. (2019). Tecnología de riego: Innovación para el uso eficiente del agua en la agricultura. Ediciones Uniminuto.

Jordán, R., & González, F. (2020). Tecnología y agricultura sostenible: Sistemas de riego automático con Arduino. Ediciones Agrícolas.

Vázquez, E., & Ramos, P. (2019). Automatización en agricultura con microcontroladores y sensores. Editorial Académica Española.

Journal of Irrigation and Drainage Engineering. “Drip Irrigation Systems for Efficient Water Use and Crop Yield.”

