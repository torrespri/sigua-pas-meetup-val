# Curso para gestores SIGUA
#### La función del PAS en el protocolo de espacios de la Universidad de Alicante

Creado por el [Laboratorio de Geomática](http://iig.ua.es/es/geomatica/) del [Instituto Interuniversitario de Geografía](http://iig.ua.es/) / [@geomatica_ua](https://twitter.com/geomatica_ua)



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



### La base de datos espacial de la UA
- Cada planta de la base de datos es una lista de polígonos
- Cada polígono representa una **estancia** correctamente posicionada sobre la superficie de la Tierra

>  Un polígono puede también representar elementos de otro tipo que no afectan a los gestores SIGUA

- Una estancia siempre tiene asignada:
  - Una **única** actividad (e.g. es un aula, es un laboratorio, ...)
  - Una **única** unidad organizativa (e.g. es de la Facultad de Derecho, es del Departamento de Ecología, ...)



### La base de datos espacial de la UA
- Una estancia puede tener una denominación (e.g. Sala de Exposiciones Aifos)
- Una estancia puede albergar **uno o varios puestos de trabajo** (e.g. profesor titular, técnico, ...) y **cargos** (e.g. director de departamento, vicerrector, ...)

>  La base de datos impide automáticamente ubicar puestos de trabajo en estancias de menos de 6 m² o recintos no aptos (e.g. un aseo o un tabique)

>  Puedo desempeñar mi puesto de trabajo en una estancia que no está adscrita a mi unidad organizativa



### La base de datos espacial de la UA
Cada estancia se identifica mediante un **código** de 9 posiciones que se puede leer siguiendo la lógica de una dirección postal

![Código SIGUA](http://labgeo.github.io/sigua-pas-meetup/img/room_code.png)

>  Más información en http://web.ua.es/es/sigua/el-codigo-sigua.html



### La web de SIGUA
SIGUA es uno más de los diversos sistemas de información corporativos de la UA. Su función principal es mantener  la base de datos espacial de la UA y facilitar su uso por parte de la comunidad universitaria y el público en general mediante la web:
**http://www.sigua.ua.es**

>  Organizativamente, SIGUA es una subunidad del Vicerrectorado de Campus. Más información y recursos útiles en http://web.ua.es/es/sigua/



### La web de SIGUA
Es una aplicación **HTML5**. ¿Usas un navegador compatible?
![HTML5 compatibility](http://labgeo.github.io/sigua-pas-meetup/img/caniuse_html5.png)
 ⁕*Fuente: http://caniuse.com/#cats=CSS,HTML5,JS%20API (5/11/2015)*



### La web de SIGUA: Visualización
- Es una aplicación diseñada específicamente para trabajar con cartografía.
- Navegar sobre el mapa es sencillo:
|        | Desplazar                          | Acercar                  | Alejar                      |
| :---:  | :--------------------------------: | :----------------------: | :-------------------------: |
| Acción | `botón izq. presionado + arrastre` | `avance rueda` o botón  | `retroceso rueda` o botón  |

- Se puede configurar el aspecto del mapa desde el diálogo `Capas`

>  Consejo: Usa el diálogo `Capas` para conmutar las etiquetas de las estancias entre código SIGUA y denominación
