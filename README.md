# Practica-Big-Data-Architecture
Practica realizada en el Bootcamp Big Data & Machine Learning en el modulo de Arquitectura Big Data.

# BUSCADOR DE PISOS CON LOCALIZACION DE METRO Y RESTAURANTES.
# Información general.
Página web o App para móviles que se encarga de buscar los mejores pisos que le indiquemos en Madrid en función d si nos interesan cerca ciertos restaurantes de una página web https://yelp.es según sus opiniones y la cercanía del metro de Madrid.

# Arquitectura
La arquitectura que vamos a realizar se va a componer principalmente por productos alojados en Google Cloud Platform Cloud Functions, Google Cloud Storage y HIVE bajo Dataproc.
Lo primero que vamos a tener en nuestra App o nuestros asistentes virtuales, páginas webs es una serie de accesos sencillos para que el usuario pueda definir su búsqueda sin problemas.
Se tendrán alojadas también en Google Storage las querys para la obtención de las recomendaciones.
En cuanto al cluster del Dataproc va a estar definido por un nodo maestro y tres esclavos para que puedan soportar la consulta y las querys necesarias de las búsquedas y procesos realizados.

# Obtención de la información
Los datos de airbnb estarán alojados en un dataset en Google Storage, junto con los datos que extraigamos haciendo un crawler con scrapy de las páginas de restaurantes de yelp y del metro de Madrid. Guardaremos los datos en un formato json para poder utilizarlos en el momento preciso.

# Modelo Operacional
Como es una empresa que está empezando, el modelo que se va a realizar es bajo necesidad para que las cloud functions se lancen únicamente en el momento de la solicitud.

# Procesado de la Información
Se va a utilizar el sistema Hive para guardar información histórica y tener cada vez más información para nuestras querys.
Uso de los datos
No solo vamos a utilizar los datos para la finalidad de la App que es la recomendación de pisos airbnb pero también nuestros miembros del equipo van a poder utilizar toda esta información para sacar informes que sirvan para nuestras estadísticas.
