# esquemas de almacenes de datos

Los DW estan diseñados para proveer respuestas a practicamente cualquier duda sobre el funcionamiento de la empresa, ademas de asistir con informacion relevante para la toma de decisiones

Para lograr el cometido los DW deben estar diseñados en difeerentes esquemas

## esquema de estrella

Es el mas simple, la tabla de hechos o central esta rodeada de entidades llamadas dimensiones y lleva un diseño logico relacional en el que las tablas de hechos recaen en la segunda forma normal, las tablas de hechos pueden estar vistos como unna forma cruzada entre varias entidades y su llave primaria queda conformada por la combinacion de las llaves priamrias de las dimensiones, tener inforamacion relevnte en la tablade hechos hace posible que la programacion de las consultas sea mas simple y rapida, ya que el sistema en vez de ir a cada tabla a buscar l ainformacion, solo va a la tabla de hechos, solo existe una tabla de dimensiones por dimension

¿formacion de dimensiones?
ejemplo de una tienda  para diseñar un DW
1. identificar el tipo de informacion para a querer analizar en el futuro e cliente
¿cuantos productos se vendieron? ¿quien vendio cada uno? ¿quien compro acada uno? ¿cuando ocurrio?
Dependiendo de las necesidades del proeycto, organiza la BD con las siguientes etiquetas "Dim**Product**" "Dim**Employee**" "Dim**Customer**"
para el dato Warehouse, crea una dimension de tiempo que dependera de la fecha de la orden, utilizando las entidades genera una tabla que convine las llaves primarias, para crear la llave primaria de hechos y despues ingresar los atributos, como cantidad, costo total, entre otros, en las dimensiones tambien s epueden formar mas tablas, por ejemplo para la dimencion de prodctos, se puede crear la dimension de categorias

<img width="684" alt="13 formacion de dimensiones" src="https://github.com/M1CaPe/Fundacion-carlos-slim-...-Administrador-de-bases-de-datos/assets/165348871/36876e37-bbe7-4c70-b29a-44dddb5b052e">

## Esquema copo de nieve

Diseñado para el mantenimiento de dimensiones, parecido a modelo relacional ya que cumple con la tercera forma normal es decir trata de segmentar informacion en caso de que esta sea muy extensa

<img width="715" alt="14 tercera normal" src="https://github.com/M1CaPe/Fundacion-carlos-slim-...-Administrador-de-bases-de-datos/assets/165348871/5d95a93a-48d0-4964-b60b-205c1316a380">

Otra ventaja esque este esquema ahora espacio en memoria

Imaginemos una tabla dimensional que incluye un millon de registros de varios clientes, es una mejor practica crear una tabla de grupos de cliente, donde se muevan los datos comunes para cada grupo, de esta forma el tamaño de las 2 tablas sera mejor que una tabla no normalizada

<img width="720" alt="15" src="https://github.com/M1CaPe/Fundacion-carlos-slim-...-Administrador-de-bases-de-datos/assets/165348871/4fc3ff5e-0d38-4bf0-af90-15e9e5d10300">

Es cierto que la sentencia de consulta incrementa la dificultad en este tipo de esquema, es de bajo rendimiento,

<img width="690" alt="16 consulta complicada" src="https://github.com/M1CaPe/Fundacion-carlos-slim-...-Administrador-de-bases-de-datos/assets/165348871/a6d01d5f-518d-443f-a3dc-14809d29d7d8">

Esquema copo de nieve, donde se crean tablas para normalizar las dimensiones, en el casi de productos creas una amrca y categoria en el caso de clientes, creas un grupo, de esta manera la inforamcion ocupa menos espacio en la memoria

<img width="625" alt="17 Esquema copo de nieve" src="https://github.com/M1CaPe/Fundacion-carlos-slim-...-Administrador-de-bases-de-datos/assets/165348871/4f7419b2-2edb-4168-b211-fab4a89284d9">


## Esquema de constelacion

Es mas complejo, por existe mas de 1 tabla de hechos, asi las tablas de dimensiones pueden estar repartidas entre las multiples tablas de hechos

<img width="719" alt="18 Esquema de constelacion" src="https://github.com/M1CaPe/Fundacion-carlos-slim-...-Administrador-de-bases-de-datos/assets/165348871/2a98b9a3-40a4-4fb1-8e61-327d69cb5689">

Con el fin de tener diferentes aspectos del negocio registrados

![image](https://github.com/M1CaPe/Fundacion-carlos-slim-...-Administrador-de-bases-de-datos/assets/165348871/e6e41b45-8461-4a69-9cf7-ddac959c1eb2)

La gran ventaja de este tipo de esquemas es su gran flexibildad, pero al genenrarla se sacrifica la facilidad y puede ser dificil de mantener en el futuro por el crecimiento de los datos, estos esquemas logran la misma velocidad de busqueda que el esquema estrella, siepre y cuando se cree una tabla por dimension

![image](https://github.com/M1CaPe/Fundacion-carlos-slim-...-Administrador-de-bases-de-datos/assets/165348871/6bc1c5c2-10a0-4026-925d-72854bd4b8a5)

![image](https://github.com/M1CaPe/Fundacion-carlos-slim-...-Administrador-de-bases-de-datos/assets/165348871/3194d7f6-6004-46cf-a950-e289e9ccc8e7)
