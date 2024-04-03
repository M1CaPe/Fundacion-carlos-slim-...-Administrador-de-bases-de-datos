Con las siguientes reglas de negocio diseña un modelo relacional en el 
recuadro de abajo. 
 
El ambiente de negocio es el siguiente: Una franquicia de tiendas 
departamentales. 
 
1. Un  empleado  pertenece  sólo  a  un  territorio  y  un  territorio  puede  tener 
muchos empleados. 
2. Un cliente pertenece a un grupo de clientes y un grupo de clientes puede 
tener ninguno o muchos clientes. 
3. Un cliente puede generar muchas órdenes de compra pero una orden 
de compra sólo le pertenece a un cliente. 
4. Un empleado puede hacer muchas órdenes de compra pero una orden 
de compra sólo la puede hacer un empleado. 
5. Una orden de compra puede contener muchos productos y un producto 
puede estar en varias órdenes de compra. 
6. Un  producto  sólo  puede  venir  de  un  proveedor  y  un  proveedor  puede 
proveer ninguno o muchos productos. 
7. Un  producto  sólo  tiene  una  categoría  y  una  categoría  puede  tener 
ninguno o muchos productos.

### Solucion
1. (1:1) Un empleado pertenece solo a un territorio
1. (1:N) Un territorio puede tener muchos empleados

2. (1:1) Un cliente pertenece a un grupo de clientes
2. (1:N) Un grupo de cliente puede tener ninguno o muchos clientes

3. (1:N) Un cliente puede generar muchas ordenes de compra
3. (1:1) Pero una orden de compra solo le pertenece a un cliente

4. (1:N) Un empleado puede hacer muchas ordenes de compra
4. (1:1) Una orden de compra solo la puede hacer un empleado

5. (1:N) Una orden de compra puede contener muchos productos
5. (N:N) Un producto puede estar en varias ordenes de compra

6. (1:1) U producto solo puede venir de un proveedor
6. (1:N) Un proveedor puede provee ninguno o muchos producto

7. (1:1) Un producto solo tinee una categoria
7. (1:N) Una cateogria puede tener ninguno o muchos productos
