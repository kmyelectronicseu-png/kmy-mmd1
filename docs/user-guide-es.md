# Guía del Usuario del Analizador de Circuitos y Dispositivo de Detección de Fallas KMY MMD-1

El KMY MMD-1 es un dispositivo profesional de detección de fallas y pruebas que permite la localización de componentes defectuosos en tarjetas electrónicas sin necesidad de aplicar energía a la placa. Al poner en contacto dos sondas con los terminales del componente bajo sospecha, el dispositivo aplica una señal de prueba de bajo nivel, normalizando gráficamente en la pantalla la relación dinámica entre la tensión y la corriente. Esta curva característica resultante se considera la "huella dactilar" eléctrica del componente. Dependiendo de la forma de la curva en el gráfico, se puede determinar de inmediato si el componente es una resistencia, un condensador o un diodo defectuoso. El sistema también cuenta con un osciloscopio y un voltímetro de dos canales integrados.

El dispositivo se puede utilizar conectándolo a un ordenador con sistema operativo Windows mediante un cable USB, o bien se puede operar a través de la opción de conexión inalámbrica. Además, el software de control es plenamente compatible con dispositivos smartphones y tabletas con sistema operativo Android.

*(Nota: La guía de usuario en inglés [user-guide-en.md](user-guide-en.md) se encuentra desactualizada. Hasta que se actualice dicha versión, la información técnica de la presente guía actualizada debe tomarse como la referencia principal.)*

---

## Índice

* **A. Introducción**
  1. [¿Qué Hace Este Dispositivo?](#1-que-hace-este-dispositivo)
  2. [Primera Vista del Dispositivo](#2-primera-vista-del-dispositivo)
  3. [Requisitos y Preparación Preliminar](#3-requisitos-y-preparacion-preliminar)
* **B. Instalación y Primera Conexión**
  4. [Instalación del Software](#4-instalacion-del-software)
  5. [Primera Conexión al Dispositivo](#5-primera-conexion-al-dispositivo)
  6. [Su Primera Medición](#6-su-primera-medicion)
* **C. Trazador de Curvas (Analizador V-I)**
  7. [Principio de Funcionamiento de la Prueba de Curva](#7-principio-de-funcionamiento-de-la-prueba-de-curva)
  8. [Ajustes Básicos de Medición](#8-ajustes-basicos-de-medicion)
  9. [Lectura de la Curva: Galería de Firmas de Componentes](#9-lectura-de-la-curva-galeria-de-firmas-de-componentes)
  10. [Ajustes Avanzados de Medición](#10-ajustes-avanzados-de-medicion)
  11. [Uso de Sonda Doble y Modo Síncrono](#11-uso-de-sonda-doble-y-modo-sincrono)
* **D. Modo de Comparación y Prueba de Tarjetas**
  12. [Funciones de Comparación](#12-funciones-de-comparacion)
  13. [Registro de Tarjetas y Sistema de Prueba de Tarjetas](#13-registro-de-tarjetas-y-sistema-de-prueba-de-tarjetas)
* **E. Otras Herramientas Auxiliares**
  14. [Modo Osciloscopio](#14-modo-osciloscopio)
  15. [Modo Multímetro](#15-modo-multimetro)
* **F. Ajustes del Sistema, Calibración y Conexión**
  16. [Ajustes del Sistema](#16-ajustes-del-sistema)
  17. [Asistente de Calibración](#17-asistente-de-calibracion)
  18. [Uso Inalámbrico y Configuración Wi-Fi](#18-uso-inalambrico-y-configuracion-wi-fi)
  19. [Uso en Dispositivos Móviles (Teléfono/Tableta)](#19-uso-en-dispositivos-moviles-telefonotableta)
  20. [Actualizaciones de Software](#20-actualizaciones-de-software)
* **G. Información de Referencia**
  21. [Límites Técnicos y Parámetros](#21-limites-tecnicos-y-parametros)
  22. [Resolución de Problemas y Soluciones](#22-resolucion-de-problemas-y-soluciones)
  23. [Soporte Técnico y Contacto](#23-soporte-tecnico-y-contacto)

---

## Sección A — Introducción

### 1. ¿Qué Hace Este Dispositivo?

En el proceso de diagnóstico de una tarjeta electrónica averiada, aplicar energía directamente a la placa es un método habitual; sin embargo, esta operación suele provocar daños permanentes en otros componentes que se encontraban en buen estado. El KMY MMD-1 se ha diseñado específicamente para eliminar estos riesgos. A través de este dispositivo, es posible analizar con seguridad el estado de los componentes realizando un contacto individual con ellos, sin necesidad de energizar la tarjeta.

El dispositivo lleva a cabo este diagnóstico mediante tres metodologías:

* **Prueba de Curva (Análisis V-I):** Aplica una señal de prueba de bajo nivel al componente para obtener su curva de tensión-corriente. En la mayoría de los casos, el sistema identifica automáticamente el tipo y valor del componente. Cada familia de componentes (como resistencias, condensadores, inductores, diodos y zeners) genera una curva única. Estas curvas pueden examinarse con ejemplos reales en la Sección 9.
* **Registro y Prueba de Tarjetas:** Este método está especialmente desarrollado para organizaciones dedicadas a la producción en masa o para personal técnico que realiza tareas repetitivas sobre un mismo modelo de tarjeta. Los puntos de prueba de una tarjeta de referencia aprobada se graban en el sistema una sola vez. Posteriormente, las tarjetas bajo sospecha de falla se comparan automáticamente con estos datos registrados. El dispositivo reporta claramente al usuario los puntos que presentan desviaciones respecto a los valores de referencia.
* **Osciloscopio y Multímetro:** Una vez energizada la tarjeta, se pueden utilizar las mismas sondas y la misma interfaz de software para monitorizar señales en tiempo real o realizar mediciones precisas de tensión.

En resumen, el KMY MMD-1 constituye un hardware auxiliar profesional diseñado para personal técnico involucrado en el diseño electrónico, detección de fallas y actividades de reparación, así como para fabricantes que desean realizar validaciones rápidas en líneas de producción en serie.

### 2. Primera Vista del Dispositivo

El panel frontal del dispositivo incorpora 4 entradas de conector tipo banana de 4 mm. Los conectores situados en los extremos izquierdo y derecho corresponden a las sondas activas (Sonda 1 y Sonda 2). Las pruebas de curva, mediciones de osciloscopio y multímetro se realizan a través de estas dos entradas activas. Las dos entradas centrales son los puntos de conexión de chasis (GND).

Al medir cualquier componente, uno de sus terminales debe conectarse a la sonda activa (Sonda 1 o Sonda 2) y el otro al conector GND adyacente. Por ejemplo, al probar una resistencia o un diodo de dos terminales, un pin se conecta a la Sonda 1 y el otro pin al conector de chasis (GND) inmediatamente contiguo.

![Vista general del dispositivo](images/shared/device-overview.svg)


El panel posterior del dispositivo dispone de dos puntos de conexión:
* **Entrada USB-C (Derecha):** Facilita la conexión con el ordenador y la transferencia de datos. El dispositivo también obtiene la energía necesaria para su funcionamiento a través de este puerto.
* **Entrada de Alimentación Externa (Izquierda):** Reservada para requerimientos de suministro eléctrico alternativo.


El chasis del dispositivo no incluye botones físicos ni LEDs de notificación. La información de estado, la conexión y los modos de trabajo activos del dispositivo deben monitorizarse en todo momento desde la pantalla del software que se ejecuta en el ordenador o en el dispositivo móvil.

### 3. Requisitos y Preparación Preliminar

Para el funcionamiento del sistema, es suficiente contar con el dispositivo KMY MMD-1, un cable USB y un ordenador con sistema operativo Windows de 64 bits (Windows 10 o Windows 11). En caso de uso inalámbrico, se puede optar por un teléfono inteligente o tableta con sistema operativo Android 7.0 o superior. La instalación se ha simplificado al máximo y el software puede instalarse en Windows sin necesidad de privilegios de administrador.

⚠️ **Advertencia Importante de Seguridad:** Antes de hacer contacto sobre la tarjeta con las sondas, es absolutamente indispensable asegurarse de que la tarjeta objeto de prueba esté **completamente desenergizada** y de que todos **los condensadores presentes en ella se encuentren totalmente descargados**. Mientras el trazador de curvas se encuentra activo, aplica su propia señal de prueba a través de las sondas. Un circuito bajo tensión alterará esta señal y puede ocasionar daños permanentes tanto en la tarjeta como en el dispositivo KMY MMD-1.

---

## Sección B — Instalación y Primera Conexión

### 4. Instalación del Software

#### Pasos de Instalación en el Sistema Operativo Windows
1. Visite la página oficial de lanzamientos en GitHub: [https://github.com/kmyelectronicseu-png/kmy-mmd1/releases/latest](https://github.com/kmyelectronicseu-png/kmy-mmd1/releases/latest)
2. Descargue y ejecute el archivo de instalación vigente **KMY-MMD-1-Kurulum.exe**.
3. Al inicio de la instalación, se mostrará una pantalla de selección de idioma. Esta selección solo aplica a los pasos del asistente de instalación; el idioma de la interfaz del propio programa se puede modificar en cualquier momento desde el menú "Ajustes".
4. Siga las instrucciones del asistente de instalación. Para evitar restricciones de administración en el sistema, el programa se instala directamente en el directorio del usuario en lugar de en "Program Files" (`%LocalAppData%\Programs\KMY MMD-1`). De este modo, la instalación se completa correctamente incluso si no se dispone de privilegios de administrador en el ordenador.

Todos los componentes y el firmware requeridos por el dispositivo y el software se incluyen en este único archivo de instalación; no se necesitan descargas adicionales. El archivo con extensión `.imza` en la página de descargas es la verificación de seguridad de la instalación. La aplicación comprueba automáticamente las futuras actualizaciones utilizando este archivo de firma; no se requiere ninguna acción manual.

*Nota: Aunque se desinstale la aplicación del sistema, los proyectos de tarjetas creados, los perfiles de calibración y los reportes de prueba exportados continuarán almacenados de forma segura en la carpeta **Documentos**. Durante el proceso de desinstalación solo se restablecen las preferencias de usuario, como la selección de idioma.*

#### Pasos de Instalación en el Sistema Operativo Android
1. Descargue el archivo **KMY-MMD-1-Mobil.apk** desde la página de lanzamientos correspondiente al dispositivo móvil y abra el archivo.
2. El sistema operativo Android solicitará autorización para instalar desde fuentes externas a la tienda oficial debido a los protocolos de seguridad. Una vez activada la opción "Permitir desde esta fuente", la instalación finalizará automáticamente.
3. La aplicación móvil funciona sin inconvenientes en todos los dispositivos con arquitectura ARM de 64 bits y Android 7.0 o superior.

*Nota Importante: La aplicación móvil solo puede conectarse al dispositivo de forma inalámbrica a través de Wi-Fi. No se admite la conexión directa mediante USB en dispositivos móviles. La única diferencia práctica de esto es que el firmware del dispositivo no se puede actualizar a través del terminal móvil. En cuanto a las funciones de medición, análisis y prueba, no existe ninguna diferencia funcional entre la versión móvil y la versión de escritorio. Para información detallada, consulte la sección [Uso en Dispositivos Móviles](#19-uso-en-dispositivos-moviles-telefonotableta).*

### 5. Primera Conexión al Dispositivo

Una vez conectado el cable USB al ordenador, ejecute la aplicación **KMY MMD-1**. Su dispositivo se mostrará en la lista de equipos disponibles en la parte superior de la pantalla; presione el botón **Conectar** para iniciar la comunicación.

Para garantizar la precisión de las medidas, el dispositivo se calibra automáticamente de acuerdo con las referencias internas de tensión en cada arranque (proceso de autocalibración). Este proceso requiere **aproximadamente entre 13 y 15 segundos**. Durante este intervalo crítico, los controles del software permanecen bloqueados temporalmente; la salida no se puede activar y no es posible seleccionar los modos de trabajo. Se debe esperar a que el dispositivo complete su proceso de preparación durante este periodo. Cuando el indicador de estado de la conexión cambie a color verde, el dispositivo estará listo para su uso.

> 🖼️ **[RESERVADO PARA IMAGEN - ESTE BLOQUE DEBE ELIMINARSE POR COMPLETO UNA VEZ AGREGADA LA IMAGEN]**
> **Descripción de la Imagen:** Captura de pantalla de la ventana principal del software KMY MMD-1 durante la fase de calibración inicial de arranque. La lista de conexiones debe ser visible en la parte superior, mostrando el dispositivo en estado "Calibrando..." o "Conectando...", con todos los controles desactivados o bloqueados y un indicador de cuenta regresiva de 13 a 15 segundos.
> **Sugerencia de Nombre de Archivo:** `software-connection.png`
> **Instrucciones de Uso:** Una vez colocada la imagen en este lugar, este cuadro de descripción (marcador de posición) debe eliminarse por completo.

*Si se produce un error al hacer clic en el botón "Conectar" inmediatamente después de conectar el cable, es posible que el hardware no haya completado aún su rutina de inicio. Se recomienda repetir la operación tras esperar unos segundos.*

### 6. Su Primera Medición

Con el fin de verificar el dispositivo, tome una resistencia estándar de valor conocido. Aunque su valor no es crítico, cualquier resistencia de **entre 100 Ω y 10 kΩ** resulta idónea para la primera prueba.

1. Conecte un terminal de la resistencia a la entrada activa designada como **Sonda 1** y el otro terminal al conector **GND** contiguo.
2. Conserve los parámetros del panel izquierdo en sus valores por defecto. Los ajustes iniciales de **Tensión: Baja** y **Rango de Corriente: Medio** son suficientes para medir una resistencia.
3. Haga clic en el botón **Salida: Apagada** en la esquina inferior izquierda de la pantalla para cambiar el estado a **Salida: Encendida**.
4. En el centro de la pantalla se visualizará una línea diagonal e inclinada. Esta línea recta constituye la "firma" eléctrica del componente de resistencia. Puede observar el valor calculado de la resistencia en la tarjeta de información situada inmediatamente debajo del gráfico.
5. Para finalizar la prueba, pulse de nuevo el botón **Salida** para apagarla o retire la resistencia del conector.

> 🖼️ **[RESERVADO PARA IMAGEN - ESTE BLOQUE DEBE ELIMINARSE POR COMPLETO UNA VEZ AGREGADA LA IMAGEN]**
> **Descripción de la Imagen:** Captura de pantalla de la pantalla de primera medición en el software. Se debe mostrar en la cuadrícula una curva lineal diagonal perfecta correspondiente a una resistencia estándar, y la tarjeta de resultados inferior debe indicar "RESISTENCIA" junto con su valor calculado (por ejemplo, 1.0 kΩ) con un nivel de confianza elevado.
> **Sugerencia de Nombre de Archivo:** `first-measurement-resistor.png`
> **Instrucciones de Uso:** Una vez colocada la imagen en este lugar, este cuadro de descripción (marcador de posición) debe eliminarse por completo.

En la Sección 9 se examinarán en detalle las firmas características del resto de componentes en la pantalla. Por el momento, se ha podido constatar la sencillez y rapidez con la que opera el sistema.

---

## Sección C — Trazador de Curvas (Analizador V-I)

### 7. Principio de Funcionamiento de la Prueba de Curva

![Ventana principal](images/shared/main-window.png)

En la interfaz del software, los parámetros de prueba se ubican a la izquierda, la pantalla gráfica en el centro, y las pestañas Comparación, Registro de Tarjetas y Prueba de Tarjetas en el margen derecho.

En la prueba de curva, el dispositivo aplica una tensión en forma de onda senoidal alterna (CA) al componente bajo medida. Durante este proceso, grafica la cantidad de corriente que atraviesa el componente en la pantalla de forma simultánea frente al valor de tensión aplicada.

* **Resistencia:** Dado que la corriente y la tensión varían de forma plenamente simultánea, se representa una línea recta e inclinada en la pantalla.
* **Condensador:** Puesto que la corriente alcanza su valor pico antes que la tensión, se traza una forma elíptica en la pantalla.
* **Diodo:** Al conducir la corriente en una sola dirección, se manifiesta una transición o codo agudo en la pantalla.

Cada familia de componentes genera un gráfico único en función de su estructura física. Este gráfico constituye una tarjeta de identidad para dicho componente. El equipo dispone de dos sondas independientes; estas pueden emplearse de forma individual o simultánea (Modo Síncrono) según se requiera (los detalles se describen en la Sección 11).

### 8. Ajustes Básicos de Medición

El modo de visualización **Simple** del panel izquierdo presenta los tres ajustes fundamentales más críticos para las mediciones. En este modo, para mayor facilidad de manejo, se prefieren denominaciones de nivel sencillas como **Bajo, Medio-1, Medio-2, Alto** en lugar de cifras técnicas complejas. Tanto el parámetro de Tensión como el de Frecuencia hacen uso de estos cuatro niveles.

Los valores técnicos reales correspondientes a estos niveles se detallan a continuación:

| Nombre del Nivel | Tensión (Valor Pico) | Frecuencia |
| :--- | :---: | :---: |
| **Bajo** | 2.5 V | 10 Hz |
| **Medio-1** | 5 V | 50 Hz |
| **Medio-2** | 10 V | 100 Hz |
| **Alto** | 15 V | 1000 Hz |

* **Tensión:** Corresponde al nivel máximo (pico) de voltaje aplicado al componente. Al medir un componente sospechoso de tipo desconocido, se debe iniciar siempre con el nivel más bajo. Si la traza en pantalla permanece horizontal y plana, el nivel de voltaje debe incrementarse de forma progresiva. Los semiconductores, como las uniones de diodos y transistores, requieren una tensión de umbral mínima para entrar en conducción; los componentes pasivos, como resistencias y condensadores, no precisan de este umbral.
* **Frecuencia:** Es el parámetro de mayor relevancia para diferenciar de las resistencias a los componentes reactivos (sensibles a la frecuencia) como condensadores e inductores. La línea recta que describe la resistencia no se ve afectada por las variaciones de frecuencia. En contraste, un condensador de 100 nF, por ejemplo, se muestra como una traza delgada y cerrada a 10 Hz, mientras que al elevar la frecuencia a 1000 Hz se ensancha hasta adoptar la forma de una elipse perfecta. La forma más rápida de verificar si el componente es un condensador consiste en observar el ancho de la elipse en la pantalla al variar la frecuencia.
* **Rango de Corriente:** Determina la sensibilidad de corriente con la que operará el dispositivo durante la medición.

| Rango | Área de Uso Idónea |
| :--- | :--- |
| **Sensible** | Condensadores, resistencias de alto valor y componentes delicados que demandan muy baja corriente. |
| **Medio** | Punto de inicio seguro para componentes desconocidos. |
| **Alto** | Resistencias de bajo valor, diodos en conducción y componentes robustos de alta corriente. |

*Si los extremos superiores de la curva en pantalla se aprecian aplanados (recortados) o si el software emite una advertencia de límite de señal, reduzca la tensión de prueba o cambie a un rango de corriente superior (más grueso). De igual forma, si un componente sensible de muy bajo consumo se mide en el rango de corriente "Alto", la curva en pantalla puede transformarse en una línea completamente horizontal, induciendo al error de considerarlo defectuoso (circuito abierto). En tales situaciones sospechosas, repita la medición configurando el rango de corriente en "Sensible".*

### 9. Lectura de la Curva: Galería de Firmas de Componentes

La tarjeta de resultados situada justo debajo de la pantalla del gráfico identifica el componente detectado por el dispositivo, calcula su valor y ofrece un índice de confianza que refleja la certeza de dicha detección. Los 12 ejemplos de componentes básicos que figuran a continuación se han determinado de acuerdo con comportamientos eléctricos reales, y las indicaciones de la tarjeta de resultados coinciden exactamente con los textos que se muestran en la pantalla del equipo.

*Fila de Desviación Esperada:* La tarjeta de resultados incluye una fila **Desviación esperada** junto al valor calculado (por ejemplo *Desviación esperada +2,19%…+3,01%*). Indica cuánto se desvía el dispositivo respecto de un multímetro calibrado en las condiciones de medición actuales, determinadas sobre todo por la relación entre el rango de corriente seleccionado y el valor del componente medido. La cifra no es una estimación: son valores medidos en banco adaptados a esas condiciones. Cuando las condiciones quedan fuera de lo medido, el dispositivo no inventa una cifra, sino que indica el motivo. Si la relación entre el rango de corriente y el valor del componente cae en una zona no medida, si la excitación no es una onda senoidal/CA, si las dos puntas soportan cargas muy distintas o si el dispositivo aún no está calibrado, verá una breve explicación en lugar del número. Cuando la desviación queda por debajo del propio límite de tolerancia del multímetro de referencia, la fila indica «por debajo del límite de referencia»: la desviación es demasiado pequeña para medirse en ese banco.

⚠️ **Detalle de Hardware Importante:** El KMY MMD-1 es un trazador de curvas de dos terminales (sondas); por tanto, no puede identificar por sí mismo mediante software categorías de componentes de tres terminales como "MOSFET" o "Transistor". Corresponde al usuario conocer qué terminales de los componentes de tres patas se están midiendo. El dispositivo interpreta el comportamiento eléctrico entre los dos puntos de contacto de las sondas. En consecuencia, los ejemplos de transistores y MOSFETs en esta guía se explican sobre la base del "comportamiento observado por el dispositivo" y las indicaciones reales de la tarjeta de resultados.

#### Resistencia
Línea recta e inclinada que cruza el centro de la pantalla del gráfico. Al disminuir el valor de la resistencia, la traza adopta una inclinación cercana a la vertical; al aumentar el valor, la línea se aproxima a la horizontal. Al modificar la frecuencia, el ángulo de esta traza no experimenta ningún cambio. Esta es la característica más evidente que distingue a la resistencia de los demás componentes.

![Curva de resistencia](images/shared/curve-resistor.png)


#### Condensador
Genera una elipse definida en la pantalla. Al elevar la frecuencia, el área interna de la elipse se expande y se hace evidente; al disminuir la frecuencia, se contrae tendiendo a una línea delgada.

![Curva de condensador](images/shared/curve-capacitor.png)


#### Inductor
Es la imagen especular del condensador. Trazado también como una elipse, pero con una respuesta inversa: al incrementar la frecuencia la elipse se estrecha, mientras que al reducirla se ensancha.

![Curva de inductor](images/shared/curve-inductor.png)


#### Condensador + ESR (Resistencia Serie Equivalente)
Elipse característica de un condensador, pero con una ligera inclinación hacia la derecha o izquierda en el gráfico. La resistencia en serie (ESR) introduce esta desviación angular en la elipse. El valor de capacitancia del condensador y los valores de resistencia serie/paralelo se indican por separado en la tarjeta de resultados.

![Curva de condensador + ESR](images/shared/curve-capacitor-esr.png)


#### Diodo
Trazado plano en una dirección (bloqueo) y con un codo pronunciado en la dirección opuesta (conducción). La posición de este punto de codo en el eje de tensión representa el umbral de conducción (voltaje directo) del diodo. Mientras que en los diodos de silicio este umbral se sitúa en torno a 0.6 V - 0.7 V, en los diodos Schottky se desplaza hacia la izquierda (menor voltaje) y en los LEDs se sitúa visiblemente más a la derecha (mayor voltaje).

![Curva de diodo](images/shared/curve-diode.png)


#### Diodo Zener
Se aprecian codos de conducción en ambos sentidos del gráfico. La inflexión de la derecha representa el umbral directo normal del diodo, y la de la izquierda corresponde al voltaje de ruptura zener ($V_z$). Este equipo permite analizar fácilmente diodos zener de hasta 15 V; para tensiones superiores, el límite de voltaje de prueba del dispositivo resultará insuficiente.

![Curva de zener](images/shared/curve-zener.png)


#### Diodo TVS
Un diodo TVS unidireccional presenta desde el punto de vista eléctrico las mismas características que un diodo zener. El dispositivo lo clasifica automáticamente como **ZENER** (la tarjeta de resultados no contiene una etiqueta "TVS" diferenciada). La ruptura simétrica en ambos sentidos de los diodos TVS bidireccionales no se ajusta exactamente a ninguna categoría estándar. Al medirlo, se puede reportar como **|Z|** o **No Definido** en la tarjeta.

![Curva TVS bidireccional](images/shared/curve-tvs-bidirectional.png)


#### MOSFET — Terminales Puerta-Fuente (Gate-Source)
El terminal de puerta de los MOSFETs actúa como un condensador muy pequeño aislado del cuerpo, por lo que prácticamente no circula corriente a través de él. En MOSFETs de pequeña señal, este valor de capacitancia es tan reducido (escasos picofaradios) que la corriente resultante queda por debajo del límite de detección del equipo, mostrándose en pantalla la indicación **CIRCUITO ABIERTO**. Esto representa el comportamiento natural de la puerta y no un defecto. En MOSFETs de potencia más robustos (con capacitancias de varios nanofaradios), se puede observar una delgada elipse de **Condensador**.

![Curva MOSFET Gate-Source](images/shared/curve-mosfet-gs.png)


#### MOSFET — Terminales Drenador-Fuente (Drain-Source)
Cada MOSFET incorpora de manera intrínseca un diodo de cuerpo (body diode) resultante de su proceso de fabricación. Con la puerta en estado flotante o conectada a la Fuente, al medir Drenador-Fuente se observa una corriente que circula por dicho diodo de cuerpo y no por el canal. El dispositivo lo identifica directamente como un **DIODO** convencional, por lo general con una tensión de conducción ($V_f$) ligeramente superior a la de los diodos de señal.

![Curva MOSFET Drain-Source](images/shared/curve-mosfet-ds.png)


#### Transistor — Unión Base-Emisor
La unión Base-Emisor constituye eléctricamente una unión de diodo. El dispositivo muestra **DIODO** en la pantalla y la tensión directa ($V_f$) se sitúa de forma típica entre 0.65 V y 0.70 V.

![Curva transistor Base-Emisor](images/shared/curve-transistor-be.png)


#### Transistor — Unión Base-Colector
La unión Base-Colector se comporta igualmente como una unión de diodo. No obstante, al ser esta unión físicamente más extensa, su voltaje de umbral suele resultar ligeramente inferior al de la unión Base-Emisor. La tarjeta de resultados muestra la indicación **DIODO**.

![Curva transistor Base-Colector](images/shared/curve-transistor-bc.png)


#### Transistor — Terminales Colector-Emisor

![Curva transistor Colector-Emisor](images/shared/curve-transistor-ce.png)
Si se efectúa la medición entre Colector y Emisor sin aplicar señal a la Base, ambas uniones internas permanecen bloqueadas y el dispositivo detectará un **CIRCUITO ABIERTO**. Este comportamiento es el estado natural del transistor y no representa una falla; dado que se requiere una excitación en la base para que el transistor conduzca, en estas condiciones de prueba se espera que permanezca en aislamiento.

*Nota de Diseño Importante:* Al medir un componente sobre una tarjeta sin desoldarlo, la curva resultante no pertenece de forma exclusiva a ese componente; representa la combinación de las respuestas eléctricas de todos los caminos y elementos que se encuentran conectados en paralelo con él. Ante cualquier duda, levantar un solo pin del componente de la tarjeta mediante un soldador y repetir la medición ofrecerá el resultado más confiable.

### 10. Ajustes Avanzados de Medición

![Panel avanzado](images/shared/advanced-panel.png)

Al conmutar a la vista **Avanzada** en la interfaz, los tres parámetros del panel Simple dejan de controlarse por niveles y pasan a regularse de forma milimétrica mediante barras deslizantes de precisión (Voltaje 0.1 - 15 V, Frecuencia 1 - 1000 Hz). En este modo se ofrecen de forma complementaria las siguientes características avanzadas de control:

* **Forma de Onda:** Permite seleccionar formas de onda Senoidal, Triangular, Cuadrada, Diente de sierra y CC. El estándar para el análisis de curvas es siempre la onda senoidal. La opción CC aplica un voltaje continuo y constante al componente.
* **Sesgo Manual (Bias Offset):** Permite desplazar el punto central de la señal de prueba por encima o por debajo del nivel cero. Para su ajuste, en lugar de una barra de desplazamiento convencional, se emplean botones de dirección (arrow-pad) que proporcionan un incremento o decremento continuo al mantenerlos presionados. Se puede definir el tamaño del paso en 10 mV, 100 mV o 1 V, y se incluye un botón de **Restablecer** de un solo clic. Se encuentra desactivado por defecto y se recomienda conservarlo de este modo para casi todas las pruebas corrientes.
* **Rango de Corriente:** A diferencia del modo Simple, este parámetro se puede ajustar de forma totalmente independiente para la Sonda 1 y la Sonda 2. Si se desea realizar una comparación directa entre ambas sondas, es indispensable igualar sus rangos de corriente; dos curvas obtenidas con rangos distintos no coincidirán en ningún caso, aun cuando midan exactamente los mismos componentes.

La mayor parte de los cambios se transmiten de manera automática al dispositivo en el instante en que se interrumpe la interacción con los mandos o deslizadores. El botón **Aplicar** se utiliza para forzar el envío inmediato de los parámetros al hardware sin aguardar el intervalo de sincronización automática.

En la parte inferior del panel izquierdo se disponen tres funciones inteligentes que facilitan las tareas de medición:

* **Autodetectar:** Al estar activa, el dispositivo reconoce la categoría del componente en el instante en que se entra en contacto con él mediante la sonda, conmutando automáticamente al voltaje, frecuencia y rango de corriente óptimos para su representación. Para evitar transiciones erróneas, el sistema no modifica los ajustes sin confirmar el mismo resultado al menos tres veces consecutivas. De este modo se evita que los parámetros oscilen ante vibraciones en el contacto manual.
* **Autooptimizar:** Ejecuta una búsqueda única de los parámetros ideales para el componente conectado a la sonda al pulsar el botón; aplica los ajustes óptimos en caso de hallar un resultado significativo y mantiene los valores actuales en caso contrario.
* **Modo de Barrido (Sweep):** Realiza un barrido secuencial paso a paso a través de un rango seleccionado para uno de los parámetros (voltaje, frecuencia o rango de corriente) hasta que se detiene el proceso; los otros dos parámetros permanecen fijos. En caso de contar con un componente desconocido, iniciar un barrido de frecuencia representa una excelente metodología: si su curva varía con la frecuencia, el componente es reactivo (condensador/inductor); si se mantiene inalterada, es de carácter resistivo.

**Pestaña de Visibilidad:**
* **Referencia:** Superpone una curva de referencia previamente guardada sobre la medición activa actual a modo de plantilla.
* **Circuito Equivalente:** Dibuja de forma dinámica el diagrama de circuito simplificado deducido por el dispositivo bajo la tarjeta de resultados.
* **Congelar:** Mantiene congelada la curva actual en pantalla para su análisis detallado.

### 11. Uso de Sonda Doble y Modo Síncrono

En condiciones normales, los modos **Sonda 1** y **Sonda 2** activan una única sonda a la vez. El modo **Síncrono** excita ambas sondas de forma simultánea desde la misma fuente de señal. Este procedimiento constituye la forma más práctica de comparar dos componentes en paralelo en un solo ciclo de prueba.

Al operar en el modo síncrono, el dispositivo vigila de forma continua el equilibrio de carga eléctrica en ambas sondas y genera ventanas de advertencia de color amarillo en la pantalla en caso de detectar un desequilibrio:

* *“Las cargas en las sondas son muy distintas; la sensibilidad de lectura puede presentar derivas en modo síncrono. Utilice el modo de sonda única para mediciones de precisión.”*
* *“El terminal de S1 se encuentra flotante; la lectura en S2 puede desviarse ~1% durante la medición síncrona.”* *(La advertencia simétrica se muestra para S1 cuando S2 está flotante).*

La visualización de estas advertencias no implica que la medición sea del todo incorrecta. Únicamente advierte que cuando la diferencia de carga entre ambas sondas es muy elevada, la lectura en el modo síncrono puede experimentar ligeras desviaciones debido a la naturaleza física del método. Para comparaciones que demanden una precisión milimétrica, conmutar al modo de sonda única (Sonda 1 o Sonda 2) es el procedimiento más seguro.

---

## Sección D — Modo de Comparación y Prueba de Tarjetas

### 12. Funciones de Comparación

![Panel de comparación](images/shared/compare-panel.png)

La pestaña **Comparación** del margen derecho despliega un práctico menú lateral. Se dispone de tres modos de operación:

* **Apagado:** Desactiva el modo de comparación.
* **Tiempo Real ↔ Referencia:** Compara el componente activo medido actualmente con una curva de referencia registrada con anterioridad. Al pulsar el botón **Capturar Referencia** se guarda la curva actual de la pantalla como patrón de comparación, la cual se puede almacenar en un archivo y recuperar posteriormente.
* **Sonda 1 ↔ Sonda 2:** Realiza una comparación directa entre ambas sondas. Se conecta el componente que se sabe que está en buen estado como referencia a una sonda, y el componente sospechoso a la otra. Este método resulta mucho más seguro puesto que ambas mediciones se realizan de forma simultánea, a la misma temperatura y bajo condiciones eléctricas idénticas.

La decisión se fundamenta en un porcentaje de similitud respecto a un umbral definido por el usuario. Si la similitud supera el umbral, se muestra la indicación **COINCIDE** (verde); en caso contrario, se muestra **NO COINCIDE** (rojo). El umbral de fábrica está establecido en el 90%. La opción **Sensibilidad en Zona Crítica** (Apagado, Normal, Alto) intensifica la comparación en las zonas de inflexión y codos de la curva, dado que la verdadera identidad eléctrica del componente reside principalmente en estas regiones.

Si ninguna sonda experimenta un consumo de corriente medible, el dispositivo no declara una falsa coincidencia comparando el ruido de fondo flotante. En su lugar, reporta la indicación **SIN MEDIDA**. Esta advertencia señala que la sonda no realiza contacto o que el rango seleccionado es demasiado alto (grueso) para ese componente.

Al activar la función de **Alerta Acústica**, no se requiere mantener la vista fija en la pantalla; el sistema emitirá una señal sonora únicamente cuando varíe la decisión de comparación (aprobado/fallido).

### 13. Registro de Tarjetas y Sistema de Prueba de Tarjetas

Este es el método idóneo para verificar modelos específicos de tarjetas que se deban reparar o validar de forma recurrente: registre cada punto de prueba una sola vez y, a continuación, examine con rapidez todas las placas bajo sospecha contra esta base de datos de referencia.

#### Grabación Paso a Paso de una Tarjeta de Referencia:

![Interfaz de registro de tarjeta](images/shared/board-record-interface.png)
1. **Crear una Carpeta de Proyecto:** Seleccione un directorio de trabajo. La imagen de la tarjeta y todos los puntos de prueba se almacenarán en esta carpeta única, lo que permite copiar y trasladar el proyecto completo a otro ordenador.
2. **Agregar Imagen de la Tarjeta:** Suba una fotografía nítida y sin sombras de la tarjeta, tomada directamente desde arriba. Una iluminación uniforme facilita la ubicación precisa de los puntos de prueba sobre la imagen.
3. **Definir Puntos:** Tome contacto con la sonda física sobre el punto deseado de la placa. Al mismo tiempo, haga clic en esa misma ubicación en la foto de la pantalla. Asigne un nombre descriptivo al punto (se recomienda utilizar la nomenclatura original de la placa: R14, C7, U3-1) y pulse **Guardar Punto**.
4. **Organizar la Secuencia:** Es posible ordenar los puntos guardados en la secuencia de prueba que prefiera arrastrándolos y soltándolos con el ratón.

* **Firma Multietapa (Multi-Stage Signature):** Al estar activa, cada punto de prueba no se registra con un único ajuste, sino en 3 o 4 niveles diferentes de voltaje y frecuencia. El proceso de grabación se prolonga ligeramente, pero resulta mucho más difícil que un componente defectuoso pase desapercibido en un punto registrado mediante este método.

#### Prueba de una Tarjeta Registrada:
Pulse el botón **Iniciar Prueba** y recorra los puntos en la secuencia definida. Cada punto se mide, se compara con su referencia y se marca como aprobado o fallido. Los puntos con discrepancias se resaltan en **rojo** sobre la fotografía de la tarjeta. En lugar de una lista de texto compleja, obtendrá un mapa visual del fallo. Puede pausar y omitir puntos, y al finalizar, emplear la opción **Probar Restantes** para retomar solo aquellos que quedaron incompletos.

![Interfaz de prueba de tarjeta](images/shared/board-test-interface.png)


* **Modo Automático:** Avanza de forma automática al siguiente punto una vez que la coincidencia de la medición es exitosa. Active esta opción cuando prefiera centrar la vista en la placa física y en las sondas en lugar de en la pantalla.
* **Crear Reporte en Excel:** Al concluir la prueba, pulsar este botón genera un reporte detallado en Excel compuesto por tres páginas: detalles punto por punto, una tabla de resumen y un mapa visual de aprobado/fallido de la tarjeta.

---

## Sección E — Otras Herramientas Auxiliares

### 14. Modo Osciloscopio

Al conmutar al modo osciloscopio, la salida de señal del dispositivo se desactiva por completo y las sondas entran en un modo de escucha pasivo para monitorizar señales externas. Los canales de entrada admiten mediciones seguras de **hasta 50 V**.

🎨 **Nota de Color de los Canales:** En la pantalla del osciloscopio, el Canal 1 se representa en color **amarillo** y el Canal 2 en color **cian**. Este esquema es el opuesto exacto de la Sonda 1 (cian) y Sonda 2 (amarilla) de la pantalla del Trazador de Curvas. Los colores de ambos modos se han diseñado de manera diferente de forma intencionada para evitar confusiones; no se extrañe por esta diferencia de color al cambiar de modo.

El dispositivo muestrea de forma fija a **5.5 kS/s** (5500 muestras por segundo) debido a límites físicos del hardware. Modificar la base de tiempos (timebase) en el programa no altera esta tasa de muestreo; únicamente modifica la ventana temporal que se visualiza en pantalla. El resultado práctico de esto es que el KMY MMD-1 se clasifica como un **osciloscopio de baja frecuencia**. Resulta idóneo para rizado en fuentes de alimentación, control de motores y señales por debajo de la banda de audio; no obstante, por encima de 1 kHz, la fidelidad de la forma de onda perderá confiabilidad.

![Modo osciloscopio](images/shared/oscilloscope-mode.png)


* **AUTO:** Analiza la señal entrante y configura de forma automática la base de tiempos, la escala vertical de voltaje y el nivel de disparo por usted. Si no se detecta una señal significativa, mantiene los ajustes previos.
* **Modos de Disparo (Trigger):**
  * *Auto:* Actualiza la pantalla de forma continua incluso si no se satisface la condición de disparo.
  * *Normal:* Actualiza la pantalla únicamente al presentarse la condición de disparo configurada.
  * *Single:* Captura la señal una sola vez cuando se cumple la condición de disparo y congela la pantalla.

Las flechas indicadoras de nivel de referencia y de disparo en los bordes de la pantalla se pueden arrastrar directamente con el ratón. Esto constituye el método más ágil para realizar ajustes rápidos sin tener que escribir valores en las casillas numéricas. El botón **Examinar** permite pausar el flujo en vivo y desplazarse a través de los **últimos 20 segundos de historial grabado**. Dado que la grabación continúa en segundo plano mientras visualiza la pantalla en tiempo real, el evento se mantendrá disponible si detecta una fluctuación repentina.

Cuatro mediciones se presentan de forma inmediata en la barra de información inferior: **Vpp** (tensión pico a pico), **Avg** (tensión promedio), **Vrms** (tensión eficaz) y **Frecuencia**. La base de datos incorpora un total de 11 parámetros de medida; puede agregar o retirar los que desee de esta barra.

### 15. Modo Multímetro

En este modo, ambas sondas pueden realizar lecturas de tensión de forma independiente al mismo tiempo. No se dispone de botones de rango manual o de selección de función (CA/CC). El KMY MMD-1 analiza el carácter de la señal para decidir si se mide en CC o CA.

* **REL (Medición Relativa):** Toma el valor leído actualmente como referencia cero y muestra las variaciones posteriores respecto a dicho valor (+/-).
* **MIN/MAX:** Registra los valores mínimo y máximo de voltaje medidos desde el inicio de la medición y los presenta en pantalla.
* **HOLD:** Congela la lectura actual en la pantalla.

También en este modo la salida activa de señal de prueba está completamente apagada. Asegúrese de activar el canal de la sonda que desea utilizar. Si la sonda de un canal inactivo se deja flotando en el aire, el valor reflejado en pantalla no corresponderá a un voltaje real, sino a ruido electromagnético acoplado en el cable.

---

## Sección F — Ajustes del Sistema, Calibración y Conexión

### 16. Ajustes del Sistema

![Ajustes](images/shared/settings-device.png)

Al pulsar en el icono de engranaje de la barra superior se abre el panel de ajustes generales. Este consta de dos pestañas básicas: **Dispositivo** y **Calibración**. Ambas pestañas incorporan una opción rápida de cambio de idioma (Turco / Inglés) en la parte superior.

#### Contenido de la Pestaña Dispositivo:
Esta sección muestra la versión del software, el número único de identificación del dispositivo, las herramientas de configuración de la conexión Wi-Fi y un botón integrado de **Actualizar**. El botón Actualizar comprueba e instala las actualizaciones del software del ordenador y del firmware del equipo con un solo clic.

Adicionalmente, bajo el apartado "Servicio / Diagnóstico", se incluye una herramienta de emergencia que permite revertir el equipo a una versión de firmware anterior y estable ante cualquier inconveniente durante una actualización. Esta sección no requiere acceso durante el uso cotidiano; está reservada exclusivamente para escenarios de soporte técnico.

### 17. Asistente de Calibración

![Inicio de calibración](images/shared/calibration-intro.png)

Los datos de calibración del KMY MMD-1 se graban **directamente en la memoria interna no volátil del equipo (EEPROM/Flash)**, no en el ordenador. El software lee esta tabla de calibración desde el propio dispositivo en cada inicio. De este modo, sin importar el ordenador o teléfono al que se conecte el dispositivo, se podrá utilizar de forma directa en su estado calibrado sin necesidad de repetir el proceso.

#### Requisitos para la Calibración:
* Dos resistencias estándar de valor conocido (con tolerancia de 1% o superior, **entre 300 Ω y 1000 Ω**; una para cada sonda, ambas deben permanecer conectadas simultáneamente durante todo el proceso de calibración).
* Un multímetro digital capaz de realizar medidas de precisión.
* El proceso de calibración requiere **aproximadamente 15 minutos** y se compone de 5 fases fundamentales.

#### Fases de Calibración Paso a Paso:
1. **Circuito Abierto (Aprox. 30 seg):** Ambos extremos de las sondas deben estar completamente flotantes y sin tocar objeto alguno. En esta fase se calibran los puntos cero de los canales de corriente y la línea de referencia del osciloscopio.
2. **Medición de Resistencia en S1:** *“Conecte una resistencia conocida en AMBAS sondas; en este paso, solo se medirá la Sonda 1.”* Ambas resistencias deben continuar en sus ranuras, pero el dispositivo solo analizará el canal de la Sonda 1. Al concluir la medición, introduzca en pantalla el **valor real de resistencia** medido con su multímetro, en lugar de guiarse por los códigos de color del componente.
3. **Medición de Resistencia en S2:** *“Conserve ambas resistencias CONECTADAS.”* Las mismas resistencias continúan en su sitio; en esta oportunidad se mide la Sonda 2.

Las primeras tres fases de la calibración van seguidas de una única ventana de confirmación: **Guardar y Continuar**. El almacenamiento en la memoria flash se consolida en este punto.

4. **Lectura de Voltaje (Multímetro):** Retire las sondas de sus conectores y déjelas completamente libres. El dispositivo generará voltajes de prueba de $-12	ext{ V}$, $-5	ext{ V}$, $+5	ext{ V}$ y $+12	ext{ V}$ de forma secuencial. En cada nivel, mida físicamente la tensión en el extremo de la Sonda 1 con su multímetro externo e introduzca el valor medido en el software.
5. **Calibración CC de la Salida (DAC) (Aprox. 45 seg):** El dispositivo realiza un barrido automático de $-15	ext{ V}$ a $+15	ext{ V}$ en pasos de 1 V y se autocorrige basándose en las medidas de tensión introducidas en el paso previo. Inmediatamente después, con las sondas aún flotantes, el equipo mide y compensa de manera automática la amplitud de excitación CA y la desviación central. No se requiere ninguna acción por su parte; el proceso solo requiere un poco de tiempo extra.

* **Fase Opcional 6 (Calibración del Osciloscopio):** Al término de los pasos anteriores, se presenta una fase opcional para el ajuste fino de las lecturas del osciloscopio. Dado que el dispositivo no puede generar su propia señal en el modo osciloscopio, se solicita emplear una fuente de tensión o señal externa de precisión conocida. Si no dispone de dicha fuente, puede omitir este paso con seguridad; todos los demás aspectos, excepto el osciloscopio, se mantendrán plenamente calibrados.

*Características del Software:* Cada pantalla de confirmación permite repetir la fase anterior si considera que se ha cometido un error. En las primeras tres fases, si el dispositivo ya cuenta con una calibración válida, se puede optar por omitir dicho paso y conservar los valores previos. El proceso de escritura en la memoria flash del dispositivo se pospone hasta que se completan satisfactoriamente todos los pasos. Si se cierra el asistente antes de concluir, los datos de calibración previos del equipo se mantienen intactos.

*Puntos de Calibración Registrados:* Cada punto que introduce en la fase de lectura de tensión con el multímetro se guarda en una lista que puede abrir desde el propio asistente. Cada fila muestra el valor medido por el dispositivo, el valor real que usted escribió y una columna de **desviación**: a cuántos milivoltios queda ese punto de la recta de corrección obtenida a partir de los demás. La fila más alejada se marca en naranja y, en la práctica, es aquella en la que el valor del multímetro se escribió mal. Basta con borrar la fila que introdujo incorrectamente; la recta de corrección se recalcula de inmediato con los puntos restantes. Como la corrección necesita al menos dos puntos para trazar una recta, los dos últimos no se pueden borrar: para empezar de cero, repita la fase de lectura.

*¿Con qué frecuencia se debe calibrar?* Se aconseja renovar la calibración al constatar que las mediciones presentan desviaciones apreciables respecto a un multímetro externo confiable, o bien cuando el software indique que la línea de referencia ha experimentado una deriva. De lo contrario, no es necesario acceder al menú de calibración bajo condiciones normales de funcionamiento.

### 18. Uso Inalámbrico y Configuración Wi-Fi

![Configuración Wi-Fi](images/shared/wifi-setup.png)

El KMY MMD-1 admite la conexión de red inalámbrica bajo dos modalidades diferenciadas:

1. **Modo Estación (Station):** Si en su laboratorio o taller dispone de una red Wi-Fi activa, el dispositivo se asocia a ella. De esta manera, su ordenador o teléfono móvil pueden comunicarse con el dispositivo a través de la red local.
2. **Modo Punto de Acceso (AP):** Si realiza trabajos de campo o si no se cuenta con una red Wi-Fi en el entorno, el dispositivo emite su propia señal inalámbrica. Puede asociar su ordenador o teléfono móvil directamente al equipo.

#### Configuración Wi-Fi mediante la Aplicación:
Con el dispositivo conectado por USB, acceda al menú **Ajustes → Configuración Wi-Fi**, seleccione el modo de conexión deseado, introduzca el nombre de red (SSID) y la contraseña, y envíelos al equipo.

#### Configuración Wi-Fi mediante Navegador (Interfaz Web):
Desconecte el cable USB. De fábrica, el KMY MMD-1 emite una red inalámbrica abierta denominada **KMY MMD-1**. Al conectar su teléfono o portátil a esta red, la página de configuración se abrirá de forma automática; en caso contrario, escriba **192.168.4.1** en la barra de direcciones de su navegador. Las opciones avanzadas de red, como la asignación de IP estática, se gestionan únicamente a través de esta interfaz web.

#### Si el Dispositivo no se Muestra en la Lista (Conexión Manual):
Si tiene la certeza de que el dispositivo se encuentra asociado a la red pero no se visualiza en la lista del software, puede pulsar en el icono de **"Introducir dirección de dispositivo manualmente"** al lado del selector Wi-Fi y escribir su dirección IP de forma manual. Esto puede ser necesario debido a que la detección automática se basa en paquetes de difusión (broadcast) emitidos por el equipo cada segundo, y ciertos routers bloquean estos paquetes hacia los clientes inalámbricos. Puede averiguar la dirección IP en la lista de clientes conectados de su router o en la propia página de configuración web del dispositivo. Esta opción de IP manual se encuentra disponible de igual modo en la pantalla de conexión de la aplicación de Android.

*Detalles Importantes a Tener en Cuenta:*
* El hardware del KMY MMD-1 admite únicamente una sola conexión activa simultánea; un dispositivo en uso se mostrará como **OCUPADO** en la lista.
* La opción **Restablecer Ajustes de Red** revierte la configuración inalámbrica al estado por defecto de fábrica en cualquier momento.

### 19. Uso en Dispositivos Móviles (Teléfono/Tableta)

La misma aplicación empleada en Windows se ejecuta en Android, sin pérdida de funciones de análisis y medición. El diseño se ha adaptado para pantallas móviles estrechas: existen barras de control permanentes en los márgenes superior e inferior de la zona gráfica.

![Interfaz móvil](images/shared/mobile-interface.png)


* **Desplegar la Barra de Estado Superior:** Al deslizar hacia abajo esta barra se accede al panel de estado. Este muestra el estado de la conexión, mensajes de error o bloqueo (si los hubiera) y tres apartados rápidos: **Herramientas**, **Ajustes** y **Conectar/Desconectar**. Ante advertencias o errores relevantes, este panel se despliega de forma automática.
* **Desplegar la Barra de Control Inferior:** Al deslizar hacia arriba esta barra se accede al panel de control integral. Se detiene a la altura en la que retire el dedo de la pantalla, sin necesidad de quedar totalmente abierto o cerrado. Incorpora exactamente los mismos ajustes de la versión de escritorio. La barra presenta en todo momento los accesos directos a Prueba de Curva, Osciloscopio y Multímetro, así como atajos para Voltaje, Frecuencia y Rango de Corriente.
* **Acceso a Funciones:** Las opciones de **Comparación, Registro de Tarjetas y Prueba de Tarjetas** se gestionan desde el apartado *Herramientas*. Los **Ajustes Generales y Calibración** se administran desde el apartado *Ajustes*. Ambas opciones son idénticas a las pantallas de escritorio, con una escala adaptada a la pantalla móvil.
* **Panel de Conexión:** El apartado *Conectar* ofrece la lista de búsqueda de equipos, un botón de respaldo para intentar asociarse directamente a la red del dispositivo y un campo de IP manual.

*Limitación de Actualización de Firmware en Móviles:* El firmware del equipo no se puede actualizar mediante dispositivos móviles debido a que el proceso requiere el protocolo seguro USB y la conexión directa USB no se admite en terminales móviles. No obstante, las actualizaciones de la propia aplicación móvil se instalan en el teléfono: al pulsar **Actualizar**, la aplicación descarga la nueva versión, valida su firma y despliega la pantalla de instalación nativa de Android. El proceso se completa con un solo toque de aceptación, sin necesidad de recurrir al navegador web.

### 20. Actualizaciones de Software

Seguir la ruta **Ajustes → Actualizar** comprueba tanto la versión de la aplicación como el firmware del dispositivo, instalando los elementos que se encuentren desactualizados. Sus datos de calibración no experimentan alteración alguna.

Al inicio de la instalación de una actualización, se visualizará en pantalla la siguiente indicación: *“Iniciando instalación, la aplicación se cerrará ahora y se reiniciará con la nueva versión.”* Es completamente normal que la ventana se cierre de manera repentina y se vuelva a abrir tras unos segundos; esto no constituye una falla del programa.

*Detalles de las Actualizaciones:*
* Las actualizaciones de la aplicación se realizan con independencia de si el dispositivo está conectado o no.
* El firmware del dispositivo solo se puede actualizar mediante una **conexión física USB**. No es posible realizarlo por red o desde el teléfono móvil; el firmware se suministra integrado en el instalador de la aplicación de escritorio.
* En caso de no disponer de conexión a internet, el comprobador de actualizaciones informará al usuario; los datos y configuraciones vigentes no sufrirán pérdidas ni daños.

---

## Sección G — Información de Referencia

### 21. Límites Técnicos y Parámetros

| Parámetro | Límite Técnico y Valor |
| :--- | :--- |
| **Voltaje de Prueba** | $\pm 15	ext{ V}$ Pico |
| **Frecuencia de Prueba** | $1	ext{ Hz} - 1000	ext{ Hz}$ |
| **Límite de Entrada de Osciloscopio / Voltímetro** | Máximo $50	ext{ V}$ |
| **Tasa de Muestreo de Osciloscopio** | $5.5	ext{ kS/s}$ (Fija por hardware) |
| **Profundidad de Registro de Osciloscopio** | Últimos $20	ext{ segundos}$ continuos |
| **Suministro Eléctrico** | A través del puerto USB |

* **Reglas Básicas de Operación y Seguridad:**
  * Pruebe las tarjetas siempre con la alimentación desconectada y los condensadores totalmente descargados.
  * El KMY MMD-1 solo genera señal de excitación en el modo de **Prueba de Curva**. En los modos de Osciloscopio y Multímetro, la salida permanece desactivada y las sondas operan únicamente en escucha pasiva.
  * El botón rojo de **Parada de Emergencia** interrumpe la salida de señal de forma instantánea. Funciona en todo momento mientras el equipo se encuentre conectado al ordenador, aun en ausencia de calibración.
  * La salida de señal no se activará hasta que el dispositivo complete su rutina de inicio y verifique la presencia de una calibración válida en su memoria.
  * ⚠️ **Advertencia de Alta Tensión:** Ninguno de los componentes de este equipo se ha diseñado para operar bajo tensión de red de distribución eléctrica ($220	ext{ V CA}$). Bajo ninguna circunstancia ponga en contacto las sondas con tomacorrientes o líneas de alta tensión.

### 22. Resolución de Problemas y Soluciones

* **El dispositivo no se muestra en la lista:**
  Verifique el estado del cable USB físico y el puerto USB del ordenador. Si se encuentra conectado a la red local y sigue sin aparecer, intente el método de [Introducción de IP Manual](#18-uso-inalambrico-y-configuracion-wi-fi).
* **Los controles se bloquean inmediatamente tras realizar la conexión:**
  Este comportamiento no representa un error. El equipo realiza un proceso de autocalibración inicial para equilibrar su hardware interno. Requiere aproximadamente de 13 a 15 segundos y finaliza automáticamente.
* **No se puede activar la salida (la salida no se enciende):**
  El dispositivo aún se encuentra en proceso de inicio o no dispone de una calibración guardada en su memoria interna. Acceda a **Ajustes → Calibración** para comprobar el estado.
* **La curva se muestra plana y horizontal:**
  Las sondas no realizan contacto con elemento alguno (circuito abierto) o el voltaje de prueba es inferior al umbral de conducción del componente semiconductor. Eleve el nivel de voltaje o conmute a un rango de corriente de mayor sensibilidad.
* **Se muestra una barra de advertencia amarilla en pantalla en modo síncrono:**
  Las cargas eléctricas asociadas a las sondas difieren significativamente o una de ellas está flotando en el aire. Conmute al modo de sonda única para mediciones de precisión (consulte los detalles en la Sección 11).
* **La pantalla de comparación indica de forma continua "SIN MEDIDA":**
  Ninguna sonda experimenta una circulación de corriente detectable. Verifique el contacto físico de las sondas y conmute al rango **Sensible** al medir componentes de alta impedancia.
* **El dispositivo se muestra en estado "OCUPADO" en la lista:**
  Otra conexión Wi-Fi (un ordenador o un terminal móvil) está utilizando el equipo de forma activa. Cierre la aplicación en el otro dispositivo en primer lugar.
* **Los valores medidos y los gráficos muestran desviaciones o derivas:**
  Apague y encienda el dispositivo; el autocalibrado de arranque resuelve la mayor parte de las derivas. Si el software advierte que la línea de referencia ha experimentado desplazamientos, repita el proceso de calibración.
* **La forma de onda se aprecia distorsionada o rota en modo osciloscopio:**
  Verifique la frecuencia de la señal bajo prueba. Con una tasa de muestreo de 5.5 kS/s, no es posible representar de forma confiable la forma de onda de señales por encima de 1 kHz.
* **La aplicación móvil no localiza al dispositivo en la red inalámbrica:**
  Asegúrese de que tanto su terminal móvil como el dispositivo se encuentren conectados a la misma red Wi-Fi. Si el dispositivo transmite su propia señal (modo Punto de Acceso), confirme que el móvil se asocia directamente a la red **KMY MMD-1**.

### 23. Soporte Técnico y Contacto

Para cualquier consulta técnica, solicitudes de asistencia o soporte en relación al KMY MMD-1, puede dirigirse a nuestra página oficial en GitHub o ponerse en contacto con nosotros por correo electrónico:

* **Página Oficial en GitHub:** [https://github.com/kmyelectronicseu-png/kmy-mmd1](https://github.com/kmyelectronicseu-png/kmy-mmd1)
* **Soporte Directo por Correo Electrónico:** [kmyelectronics.eu@gmail.com](mailto:kmyelectronics.eu@gmail.com)

Para agilizar la asistencia, le sugerimos anotar el número de identificación de su equipo antes de contactar con el equipo de soporte. Puede localizar su número de identificación siguiendo la ruta **Ajustes → Dispositivo → No. Dispositivo** en la interfaz del software.