# Modelo relacional

## Modelo entidad-relacion

Las entidades son la bstraccion de la tabla (el titulo principal)
y los atributos, es lo que introduces en ella

El primer atributo o campo estara ocupado por la llave primaria
Despues las llaves foraneas y al final los atributos

Ejemplo

Orders        <--Entidad
Order ID      <--Llave primaria
Customer ID   <--Llave foranea
Employeer ID  <--Llave foranea
OrderDate      <--Atributos....
RequiredDate
ShipVia
Freight

## Cardinalidad
Se representa con lineas que relacionan 2 tablas, desde una llave primaria hasta una llave foranea

### De uno a uno
Es cuando un elemento de una identidad solo se puede relacionar con un elemento de otra identidad

### De uno a muchos
Es cuando un elemento de una identidad se puede relacionar con varios elementos de otra entidad

### De muchos a muchos
Es cuando 2 o mas elementos de una entidad se pueden relacionar con 2 o mas elementos de otra enntidad

### De 1 a 0 o muchos
Es cuando un element de una tabla se relaciona con ninguno o muchos elemenetos de otra

### De muchos a cero o muchos
Es cuando un elemento de una tabla se relacionan con ninungo o muchos elementos de otra

![](https://informaticosinlimites.com/wp-content/uploads/2022/06/24.svg)
