# Curso para gestores SIGUA
#### La función del PAS en el protocolo de espacios de la Universidad de Alicante

Creado por el [Laboratorio de Geomática](http://iig.ua.es/es/geomatica/) del [Instituto Interuniversitario de Geografía](http://iig.ua.es/) / <i class="fa fa-twitter-square"></i> [@geomatica_ua](https://twitter.com/geomatica_ua)



### Contenidos
- Introducción <!-- .element: class="fragment" data-fragment-index="1" -->
  - La estructura de la base de datos espacial de la UA
  - La web de SIGUA: visualización, consulta y salida impresa
  - Cómo se integra SIGUA con otros sistemas de informacion de la UA
  - ¿Por qué es importante mantener actualizada la base de datos espacial de la UA?
- Protocolo de Espacios de la UA <!-- .element: class="fragment" data-fragment-index="2" -->
  - ¿Para qué sirve y quién participa en el Protocolo de Espacios?
  - Expediente de personal: asignación de ubicaciones a puestos de trabajo y cargos
  - Expediente de estancias: asignación de uso y denominación a estancias
  - Cómo utilizar la web de SIGUA para que resulte más sencillo cumplimentar los expedientes de personal y estancias



### La base de datos espacial de la UA
![Estructura BD](http://labgeo.github.io/sigua-pas-meetup/img/db_structure.png)


### Estancias
- Cada planta de la base de datos es una lista de polígonos
- Cada polígono representa una **estancia** correctamente posicionada sobre la superficie de la Tierra

> <i class="fa fa-info-circle"></i> Un polígono puede también representar elementos de otro tipo (e.g. cerramientos)

- **Obligatoriamente** una estancia  tiene asignada:
  - Una **única** actividad (e.g. es un aula, es un laboratorio, ...)
  - Una **única** unidad organizativa (e.g. es de la Facultad de Derecho, es del Departamento de Ecología, ...)
- **Opcionalmente** una estancia tiene una denominación (e.g. Sala de Exposiciones Aifos)


### Puestos de trabajo
- Una estancia puede albergar **uno o varios puestos de trabajo** (e.g. profesor titular, técnico, ...) y **cargos** (e.g. director de departamento, vicerrector, ...)

> <i class="fa fa-info-circle"></i> La base de datos impide automáticamente ubicar puestos de trabajo en estancias de menos de 6 m² o recintos no aptos (e.g. un aseo o un tabique)

> <i class="fa fa-info-circle"></i> Puedo desempeñar mi puesto de trabajo en una estancia que no está adscrita a mi unidad organizativa


### Códigos SIGUA
Cada estancia se identifica mediante un **código** de 9 posiciones que se puede leer siguiendo la lógica de una dirección postal

![Código SIGUA](http://labgeo.github.io/sigua-pas-meetup/img/room_code.png)

> <i class="fa fa-info-circle"></i> Más información en http://web.ua.es/es/sigua/el-codigo-sigua.html



### La web de SIGUA
SIGUA es uno más de los diversos sistemas de información corporativos de la UA. Su función principal es mantener  la base de datos espacial de la UA y facilitar su uso por parte de la comunidad universitaria y el público en general mediante la web:
**http://www.sigua.ua.es**

> <i class="fa fa-info-circle"></i> Organizativamente, SIGUA es una subunidad del Vicerrectorado de Campus. Más información y recursos útiles en http://web.ua.es/es/sigua/


### Compatibilidad
Es una aplicación **HTML5**. ¿Usas un navegador compatible?
![HTML5 compatibility](http://labgeo.github.io/sigua-pas-meetup/img/caniuse_html5.png)

<i class="fa fa-asterisk"></i> *Fuente: http://caniuse.com/#cats=CSS,HTML5,JS%20API (5/11/2015)*


### Visualización
- Es una aplicación diseñada específicamente para trabajar con cartografía
- Navegar sobre el mapa es sencillo:

| Desplazar               | Acercar                    | Alejar                  |
| :---------------------: | :------------------------: | :---------------------: |
| `botón izq. + arrastre` | `rueda adelante` o botón  <i class="fa fa-plus-square"></i>| `rueda atrás` o botón <i class="fa fa-minus-square"></i> |
-----------------------------------------------------------------------------------
- Se puede configurar el aspecto del mapa desde el diálogo `Capas`

> <i class="fa fa-info-circle"></i> Consejo: Usa el diálogo `Capas` para conmutar las etiquetas de las estancias entre código SIGUA y denominación


### Visualización por escalas
- La navegación sobre el mapa es fluida porque se usa un sistema de pre-renderizado
- El mapa se pre-renderiza a 22 niveles de detalle distintos: el nivel 0 es la escala de mínimo detalle y el nivel 21 el de máximo

> <i class="fa fa-info-circle"></i> Hacer zoom implica cambiar de nivel, y cada nivel está configurado para que se vean u oculten determinados elementos


### Visualización por plantas
- Las estancias se visualizan entre el nivel 19 (escala 1:1330) y el 21
- Sólo cuando estamos en estos niveles de detalle se activa el **selector de plantas**

> <i class="fa fa-exclamation-triangle"></i> Atención: Cuando volvemos al nivel 19 desde un nivel inferior se visualizará la planta que hubiera seleccionada anteriormente


### Consulta interactiva de estancias
- El mapa es una página web donde una posición es un hipervínculo que nos da información de la estancia que hay en dicha posición
- La consulta interactiva de estancias tiene sentido a partir del nivel de detalle 19, cuando éstas estan visibles

> <i class="fa fa-exclamation-triangle"></i> Los elementos dotacionales (e.g. viario, parkings, ...) se pueden consultar interactivamente sólo si la planta baja está seleccionada

> <i class="fa fa-info-circle"></i> También existen hipervínculos predefinidos o **marcadores** en el mapa (e.g. edificios, fotografías panorámicas)


### Salida impresa
Accediendo a `Utilidades > Imprimir` el diálogo `Impresión de mapa` ofrece diversas opciones:

| Formato                                | Impresión directa del mapa | Impresión por edificio y planta |
| :------------------------------------: | :------------------------: | :-----------------------------: |
| <i class="fa fa-file-image-o"></i> PNG | `Descargar imagen PNG`     |                                 |
| <i class="fa fa-file-pdf-o"></i> PDF   | `Descargar PDF`            | `Impresión de edificios`        |

> <i class="fa fa-info-circle"></i> La opción `Impresión de edificios` es un enlace al diálogo `Edificios`. Para imprimir plantas de un edificio en formato PDF formateado, cada edificio de la lista dispone de su propio enlace ( icono <i class="fa fa-file-pdf-o"></i>)
