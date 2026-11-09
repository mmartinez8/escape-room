**ESCAPE ROOM 2026**  					grupos 2 personas

Manual de placa base: Gigabyte Z690 AORUS ELITE DDR4   (pdf parte1)  
*Nota: el PDF adjunto es el manual del Gigabyte Z690 AORUS PRO / PRO DDR4 y llega hasta la página 27 del manual.*

***Trabajo con IA y documentos (manual Placa Base) como contexto (Skill)***

**FASE 1: Identificación del Factor de Forma (El Tamaño Sí Importa)**  
**El problema:** El cliente ha comprado una caja de ordenador ultra compacta para el salón, pero la placa base que ha intentado meter dentro es demasiado grande y no encaja en los anclajes del chasis.

* **El Reto en el Manual:** Id a la primera página de especificaciones generales o al índice del manual, donde se describen las características físicas de la placa (*Hardware Installation* / *Introduction*).

* **Pregunta / Desafío:**  
  1. Según el manual de esta placa base, ¿cuál es su **factor de forma** o tamaño exacto (por ejemplo: *ATX*, *Micro-ATX*, *Mini-ITX*, etc.)?   

> Respuesta: La placa es ATX y mide 30,5 cm de largo por 24,4 cm de ancho (305 × 244 mm). Lo pone en la página 12 del manual: «ATX Form Factor; 30.5cm x 24.4cm». Por eso no cabe en una caja pequeña.

* *Código para avanzar:* **ATX**

**FASE 2: El Zócalo de la CPU (Cuidado con los Pines)**  
**El problema:** Un compañero va a instalar el procesador en el zócalo y os pregunta cómo debe orientarlo correctamente para no doblar ningún pin ni forzar el anclaje metálico.

* **El Reto en el Manual:** Buscad en la sección de instalación del procesador (*CPU Installation*) el nombre del zócalo. 

* **Pregunta / Desafío:**  
  1. ¿Cómo se denomina exactamente el **modelo de socket o zócalo** de esta placa base (por ejemplo: *LGA 1700*, *AM5*, *LGA 1151*, etc.)?   
  2. ¿Los pines de conexión están en este zócalo de la placa o en la parte inferior de la CPU? 

> Respuesta: El socket es LGA1700. Los pines están en el zócalo de la placa y la CPU solo tiene unas zonas de contacto planas, que es lo que significa LGA (Land Grid Array). A la hora de colocar el procesador hay que hacer coincidir el triángulo de la CPU con la marca "pin one" del zócalo y encajar las muescas en las guías. Mejor no tocar los contactos ni forzar la palanca. Se explica en las páginas 9, 13 y 14 del manual.

* *Código para avanzar:* **LGA1700**

**FASE 3: Los Puertos de Vídeo Traseros (La Gráfica Integrada)**  
**El problema:** El cliente enciende el ordenador por primera vez sin tarjeta gráfica dedicada y conecta el cable del monitor directamente a la placa base, pero no ve imagen en pantalla. Queréis comprobar qué salidas de vídeo físicas ofrece la placa de serie.

* **El Reto en el Manual:** Buscad el diagrama del **Panel de E/S Trasero** (*Back Panel Connectors* / *I/O Back Panel*), donde se detallan todos los puertos de la parte posterior.

* **Pregunta / Desafío:**

¿Qué **puertos de vídeo** integrados (como *HDMI*, *DisplayPort*, etc.) incluye esta placa base en su parte trasera para usar con la gráfica integrada del procesador?

> Respuesta: Solo trae una salida de vídeo integrada, que es un DisplayPort 1.2. Llega hasta 4096 × 2304 a 60 Hz y admite HDCP 2.3. HDMI no tiene, así que si el cliente conectó un cable HDMI, ahí no iba a ver nada. Páginas 9, 11 y 18 del manual.

* *Código para avanzar:* **DisplayPort**

AÑADIR PARTE 2 del MANUAL de la PLACA BASE

**Instrucciones:***Sois un equipo de técnicos de soporte de nivel 2\. Un cliente os ha enviado un ordenador de alta gama recién montado que **no arranca**, se queda la pantalla en negro y los ventiladores giran de forma extraña. Tenéis el manual oficial de la placa base en la pantalla y 3 fases que superar para descifrar el error y levantar el sistema. ¡El tiempo corre\!*

**FASE 4: El Diagnóstico del Panel Frontal (Los "Front Panel Connectors")**  
**El problema:** El cliente intentó cambiar la caja del PC y ahora, al pulsar el botón de encendido (*Power Button*) de la torre, **absolutamente nada se enciende**. No hay corriente ni chispa.

* **El Reto en el Manual:** Buscad en el manual de la placa el apartado dedicado a las conexiones del panel frontal (suele llamarse *Front Panel Header*, en los manuales de Gigabyte suele estar en la sección de instalación de hardware bajo la etiqueta **F\_PANEL**).

* **Pregunta / Desafío:**

  1. ¿En qué pines exactos del bloque F\_PANEL debe ir conectado obligatoriamente el interruptor de encendido (**PWR\_BTN** / Power Switch)?  
  2. Si por error el alumno hubiera conectado los pines del Power Switch en los pines de *Reset* o en los de los LEDs del disco duro, ¿por qué el ordenador no muestra ninguna señal de vida?

> Respuesta 1: Esto no sale en la parte 1 del PDF. El índice habla de "13) F_PANEL" en la página 21, pero el archivo se corta en la 27 antes de llegar a ese apartado. Sin el diagrama ni la tabla de pines no se puede decir en qué pines va el botón, así que hace falta la parte 2 del manual.
>
> Respuesta 2: Para que el PC arranque, el botón de encendido tiene que cerrar un momento el circuito PWR_SW / PWR_BTN. Así la placa le manda la señal a la fuente (PS_ON) para que se active. Si el cable está en los pines de Reset, al pulsar solo se envía una orden de reinicio, y con el equipo apagado eso no arranca nada. Si está en los del LED del disco duro, esos pines sirven para dar corriente al LED, no para recibir órdenes del botón. En los dos casos la fuente se queda en standby y el ordenador no da señales de vida.

* *Código para avanzar:* Pendiente de la parte 2 del manual (diagrama F\_PANEL).

**FASE 5: El Laberinto de la Memoria RAM (Canales y Slots)**  
**El problema:** Tras solucionar el botón de encendido, el ordenador por fin da señal de vídeo, pero la pantalla se queda congelada mostrando un código de error de memoria y la placa base emite una secuencia de pitidos cortos continuos. El cliente ha colocado los dos módulos de memoria RAM DDR4 en los zócalos AMC\_1 y AMC\_2 (los dos primeros empezando desde el socket del procesador).

* **El Reto en el Manual:** Buscad en el manual el apartado de **Installation / Recommended Population for 2 DIMMs** (Instalación de memoria en arquitectura de doble canal).

* **Pregunta / Desafío:**  
  1. Según el fabricante de esta placa, si solo se van a instalar **dos módulos de RAM**, ¿en qué ranuras específicas (por nombre de slot, ej. *A2 y B2* o *DDR4\_1 y DDR4\_2*) deben colocarse obligatoriamente para activar el *Dual Channel* y evitar el fallo de arranque?

> Respuesta: Hay que ponerlos en DDR4_A2 y DDR4_B2. En la tabla de la página 16, para dos módulos aparece "DS/SS" en A2 y B2 y las ranuras A1 y B1 se dejan vacías. Los nombres AMC_1 y AMC_2 no salen en este manual. Si el cliente los puso en A1 y A2, los dos módulos quedan en el mismo canal (el A) y no se activa el doble canal.

* *Código para avanzar:* **DDR4\_A2 + DDR4\_B2**

**FASE 6: El Enigma de la UEFI y la Actualización de la BIOS (*Q-Flash*)**

**El problema:** El PC ya arranca y entra al sistema, pero al montar un procesador de decimotercera o decimocuarta generación en esta placa Z690, el sistema no reconoce la CPU correctamente o se cuelga en el logo inicial. Necesitáis actualizar la BIOS/UEFI. Lo fascinante es que esta placa cuenta con un botón físico trasero para actualizarla **sin necesidad de tener CPU ni RAM instaladas**.

* **El Reto en el Manual:** Buscad en el manual el apartado de la tecnología de actualización sin procesador (en Gigabyte se llama **Q-Flash Plus**).

* **Pregunta / Desafío:**

  1. ¿Cómo se llama exactamente el **puerto USB trasero de color especial** (o serigrafiado) donde obligatoriamente se debe conectar el pendrive USB con el archivo de la BIOS para usar esta función?

  2. ¿Qué nombre exacto debe tener obligatoriamente el archivo de la BIOS dentro del pendrive para que la placa lo reconozca al pulsar el botón *Q-Flash Plus*?

> Respuesta 1: Es el puerto USB 3.2 Gen 2 Type-A (Red) Q-Flash Plus Port, el USB rojo del panel trasero que viene marcado como Q-Flash Plus. El pendrive se enchufa ahí antes de usar la función. En la placa está el botón QFLASH_PLUS, y el LED QFLED parpadea mientras busca y graba la BIOS y deja de parpadear cuando termina (páginas 19 y 20).
>
> Respuesta 2: Tampoco sale en la parte 1 del PDF. El manual no dice cómo se tiene que llamar el archivo. Solo explica que hay que guardar la última BIOS en un pendrive y manda a la página Unique Features de Gigabyte para el procedimiento. No nombra GIGABYTE.bin ni ningún otro nombre.

* *Código para avanzar:* **USB 3.2 Gen 2 Type-A (Red) Q-Flash Plus**
