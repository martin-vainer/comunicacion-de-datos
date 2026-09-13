2 parciales
clases hibridas

PPT de la clase: material\teoria\Presentaciones\U1 Introduccion a las comunicaciones.pdf


# U1: introduccion a las comunicaciones
## circuito teleinformatico basico:
equipo terminal de datos --> equipo de comunicacion de datos --> medio --> equipo de comunicacion de datos --> equipo terminal de datos

dentro de los ETD hay un controlador de comunicaciones, que ayuda con el procesamiento de la informacion y la comunicacion con el ECD.

conceptos:
- enlace de datos: conexion entre ETD y ETD, que permite la transmision de informacion.
- circuito de datos: conexion entre ECD y ECD, que permite la transmision de informacion. 


## TRANSMISIÓN DE DATOS
Se entiende por transmisión de datos al movimiento de información codificada, de un punto a uno o mas puntos, mediante señales eléctricas, ópticas, electromagnéticas o electro ópticas.
Algunas características:
- CONFIABLE
- SIN ERRORES
- EN TIEMPO REAL
- FLEXIBLE
- SEGURA

diferencias entre sistemas distribuidos y centralizados.
en los distribuidos, el elemento mas importante es la comunicación/conexion entre los distintos nodos, mientras que en los centralizados, el elemento mas importante es el procesamiento.

Para que algo sea un sistema distribuido necesitás, como mínimo:
- Nodos independientes: distintas computadoras/procesos.
- Red de comunicación: para que esos nodos intercambien mensajes.
- Coordinación: mecanismos para que trabajen juntos como si fueran un único sistema.


## la importancia de la normalización de las comunicaciones
vimos organismos que regulan la comunicacion, como la UIT (unión internacional de telecomunicaciones) y la ISO (organización internacional de estandarización).
IEEE,IERF,EIA,FCC,ENACOM,IRAM,ONTI

## MODELO de REFERENCIA OSI:
desarrollado por la ISO, es un modelo de referencia que permite la interconexión de sistemas abiertos. Se compone de 7 capas:

capas mas vinculadas con el usuario: **Orientadas a las aplicaciones**
7. Capa de **aplicación**: proporciona servicios de red directamente a las aplicaciones del usuario.
6. Capa de **presentación**: traduce los datos entre el formato de la aplicación y el formato de la red.
5. Capa de **sesión**: establece, gestiona y termina sesiones entre aplicaciones.

capa mas intermedia:
4. Capa de **transporte**: proporciona transferencia de datos confiable y transparente entre sistemas finales.

capas mas vinculadas con la infraestructura de red: **dependientes de red**
3. Capa de **red**: determina cómo se enrutan los datos desde el origen hasta el destino.->ENRUTAMIENTO
2. Capa de **enlace de datos**: proporciona un enlace confiable entre dos nodos conectados directamente.
1. Capa **física**: transmisión de bits a través de un medio físico.

Entre capas iguales de dsitintos sistemas vamos a utilizar **protocolos**, que son un conjunto de reglas y convenciones que permiten la comunicación entre sistemas.
Entre capas de un mismo sistema vamos a utilizar **interfaces**, que son un conjunto de reglas y convenciones que permiten la comunicación entre capas de un mismo sistema.

definicion de servicios: conjunto de funciones que una capa ofrece a la capa superior, a través de la interfaz.
definicion de entiades: elementos activos de una capa. provee y usa servicios a la capa superior, a través de la interfaz.

definicion de PDU (unidad de datos de protocolo): es la unidad de información que se intercambia entre entidades de una misma capa, a través de un protocolo.
ejemplo: PDU de la capa de red = paquete, PDU de la capa de transporte = segmento, PDU de la capa de enlace = trama.

### nivel 1: capa física

- Servicio:
Conexión física al medio transmisor
- Funciones:
Definición de las características mecánicas, eléctricas, funcionales y de procedimientos.
- Ejemplo: 
Interfaz RS 232

### nivel 2: capa de enlace de datos

- Servicio:
Establecer, mantener y liberar conexiones del N3.
- Funciones:
Control de errores y de flujo de datos. Delimitar secuencia de bits, asegurando transparencia.
Resolver problemas de daño, pérdidas y duplicidad.
- Ejemplo:
protocolos de enlace de datos: HDLC, PPP, Ethernet, Token Ring.

### nivel 3: capa de red
- Servicio:
Servicio orientado a la conexión o sin conexión al N4.
- Funciones:
Encaminamiento.
Tratamiento de congestión y facturación.
Reenvío por sistemas intermedios.
Interconexión de redes heterogéneas.
- Ejemplo:
protocolos de red: IP, IPX, X.25, Frame Relay, ATM.

### nivel 4: capa de transporte
- Servicio:
Conexión extremo a extremo sin errores.
Calidad de funcionamiento Q o S.
se encarga de concretar la comunicación entre los sistemas finales, independientemente de la red subyacente.
- Funciones:
Ocultar detalles de capas inferiores a las superiores.
Multiplexión.
Regular flujo de datos.
- Ejemplo:
protocolos de transporte: TCP, UDP, SPX.

### nivel 5: capa de sesión
- Servicio:
Gestionar el control del diálogo.
Sincronización y administración del testigo.
- Funciones:
Establecimiento y liberación de conexión.
Usuarios de distintas máquinas establezcan sesión.
Mejorar servicios.


### nivel 6: capa de presentación
- Servicio:
Codificación de datos.
Manejo de abstracciones y conversiones.
Compresión y criptografía.
- Funciones:
Permite comunicación entre equipos con distintas representaciones.
Adecua sintaxis.
No necesariamente entiende sobre la semántica.

### nivel 7: capa de aplicación
- funciones:
Definición de un terminal virtual para permitir diálogo entre terminales incompatibles.
Proporciona interfaz de usuario.
Establece autorizaciones.
Autenticidad de datos.
Determinación de la disponibilidad actual.
Correo Electrónico.
Transferencia de archivos.


## internet: red de redes.
Una red internacional formada por un conjunto de miles de redes independientes, operadas en forma autónoma, que están interconectadas por medio de protocolos y procedimientos normalizados como estándares de internet, que permiten comunicaciones entre dos equipos terminales host-to-host que pertenezcan a algunas de las redes que la integran.

IOT: internet of things, es un concepto que hace referencia a la interconexión digital de objetos cotidianos con internet.
IIoT: industrial internet of things, es un concepto que hace referencia a la interconexión digital de objetos cotidianos con internet, pero en el ámbito industrial.

### evolucion del internet



## interconexion de redes:
### concepto de neutros (IXP, ex NAP):
Es una infraestructura física a través de la cual los Proveedores de Servicios de Internet (ISP) intercambian el tráfico de Internet entre sus redes. Esta instalación reduce la porción del tráfico de un ISP que debe ser entregado hacia su proveedor de conectividad.
https://www.youtube.com/watch?v=YCzK3nH2wbo&t=15s
https://www.cabase.org.ar/
https://ixp.cabase.org.ar/img/cabase-poster-interactivo-2024.pdf
