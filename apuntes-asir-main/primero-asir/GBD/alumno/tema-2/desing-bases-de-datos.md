# Diseño de Bases de Datos

Los pasos del diseño de una Base de Datos se pueden resumir en:

- **Recoplección y análisis de requerimientos**: en este recogemos la información del sistema para la base de datos que vamos a diseñar.
- **Diseño conceptual**: una vez recogido todos los requisitos y conocido el problema, realizamos el primer esquema conceptual con el modelo entidad-relación.
- **Diseño logico**: el diseño conceptual lo transformamos a diseño logico, que es pasar de un modelo conceptural a un modelo de datos concreto con el fin de poder representar el problema, más adelante, en algún software concreto. Aquí usaremso el modelo Relacional.
- **Diseño físico**: en este punto debemos aplicar el modelo lógico de datos del punto anterior sobre un SGBD[^1] concreto. Dependiendo del diseño físico escogido, tendremos un abanico de posibilidades en cuanto al software que se pueda usar. Nosotros hemos escogido un modelo relacional por lo que tendremos que escoger SGBD relacionales. En este curso se usara MySQL.

### Entidad
Cualquier tipo de objeto o concepto sobre 

Hay dos tipos de entidades: fuertes o regulares 

- Relaciones binaria (grado 2): son aquellas que se dan 
- Relaciones ternarias (grado 3): son aquellas que se dan entre tres entidades
- Relaciones unitarias o reflexivas (grado 1): es una 
- Relacion n (>3): 

### Participación
La participación de una 

| Paticipación | Significado |
| --- | --- |
| 

\----

###### Notas al pie

[^1]: SGBD: Son las siglas de Sistema de Gestión de Bases de Datos, es decir, es el software encargado de gestionar la base de datos no el lenguaje en si, que en este curso usaremos SQL.