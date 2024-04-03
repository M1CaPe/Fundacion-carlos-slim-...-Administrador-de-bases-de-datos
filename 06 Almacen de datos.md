# Almacen de datos

Aplicaciones para generar analisis mas eficicinetes

DW Warehouse
Es una BD orientada al analisis de informacion, este almacen se olvida de las transacciones o procdemieinetos almacenados en la BD, y solo se enfoca en extraer y organizar informacion imortante almacenada en otras BD

Caracteristicas:

1. Orientado a temas
Todos los datos deben esstar relacionados respecto al tema a analizar
2. Variante en el tiempo
Los cambios de los datos en el tiempo, deben quedar registrados para evitar perdidas de inforamcion
3. No volatil 
la informacion no se modifica ni se elimina, solo es de lectura

la funcion del DW es contener los datos utiles para el ambiente del negocio y par aposteriormente transformarlos en informacion relevante que se pueda analizar rapidamente, de esta forma los usuarios autorizados pueden realizar consultar sp reportes in afectarr al sistema

Para cumplir con la funcion del amacen es importante el principio de:

"principio de separacion de los datos"

se deben separar los datos usados en la operaciones de la BD de los datos que se guardan en el almacen para que nunca coincidan, para ello se diseñan los ETL

ETL 
Extraccion: Obtener informacion deseada de datos almacenados
Transformacion: adecuarlos a los esquemas de DW
Carga: depositar los datos en el DW

Con estos pasos, la informacion ancalda en la DW no esta vinculada con la BD

Data marts: son BD departamentales que se alimentan del DW para asi evitar una busqueda exhaustiba por parte del sistema y asi recibir la informacion mas rapido.

Ejemplo: en el DW de una tienda existen Data marts especificas como Recursos humanos, ventas, compras, etc...

A cada uno de los Data marts solo acceden un numero limitado de usuarios para el analisis de  la informacion de un proposito especifico

para el analisis de los Data marts, se contemplan en estructuras multidimencionales de datos como los cubos relacionales...
