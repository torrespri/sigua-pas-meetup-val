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
> Un polígono puede también representar elementos de otro tipo que no afectan a los gestores SIGUA
- Una estancia siempre tiene asignada:
  - Una **única** actividad (i.e. es un aula, es un laboratorio, ...)
  - Una **única** unidad organizativa (i.e. es de la Facultad de Derecho, es del Departamento de Ecología, ...)
- Una estancia puede albergar **uno o varios puestos de trabajo** (i.e. profesor titular, técnico, ...) y **cargos** (i.e. director de departamento, vicerrector, ...)
