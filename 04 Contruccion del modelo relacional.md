# Construcciòn del modelo relacional

Para diseñar una base de datos primero debes **Convebir toda su lògica de operaciòn** esto se logra teniendo en claro la situacion del negocio y todos sus procesos.

##Contruccion de un modelo relacional

### 1 Definir las entidades o tablas necesarias en el modelo relacional
No centrarse en los atributos, se agregan despues

### 2 Establecer la relacioines y poner la cardinalidad

### 3 Normaliza hasta la tercera forma normal
Con esto todas la tablas tendran una llave primaria, mantendrean dependencia funcional y no habra duplicacion de datos

### 4 Elige atributos, no almacenes datos que pueden inferir de otros
Por ejemplo la Edad se puede inferir de la fecha de nacimiento

### 5 Tabla cruzada "muchos a muchos" "a muchos o cero"
Siempre que tengamos una relacion "muchos a muchos" o "a muchos o cero" es mejor realizar una tabla cruzada

### las tablas cruzadas
se usan cuando existen relacion de "muchos a muchos", ya que si unimos una tabla con una llave foranea a la otra tabla, esa misma tendria incosnsistencias de duplicidad

### 
