# SQL - Consultas y Gestión de Datos

## INDICE

- [1. Estructura Básica](#1-estructura-básica-de-una-consulta)
- [2. Filtrado de Datos](#2-filtrado-de-datos)
- [3. Modificadores de Resultados](#3-modificadores-de-resultados)
- [4. Funciones de Agregación](#4-funciones-de-agregación)
- [5. Agrupamiento de Datos](#5-agrupamiento-de-datos)
- [6. Alias](#6-alias)

## Introducción

SQL (Structured Query Language) es el lenguaje estándar para interactuar con bases de datos relacionales. Permite definir, manipular y consultar datos.

---

## 1. Estructura Básica de una Consulta

### SELECT

La cláusula **SELECT** es la más utilizada. Se emplea para recuperar datos de una tabla.

Si se quiere seleccionar todo se usa **\*** para seleccionar todas las columnas que tenga la tabla.

#### Ejemplo

Para que una consulta sea legible, se recomienda estructurarla en líneas separadas:

```sql
SELECT columna1, columna2
FROM nombre_tabla;
```

### FROM

La cláusula **FROM** es la que nos ayuda a especificar dónde estamos buscando.

#### Ejemplo

```sql
SELECT columna1, columna2
FROM nombre_tabla;
```

## 2. Filtrado de Datos

### WHERE

La cláusula **WHERE** se usa para filtrar los requisitos que las filas deben cumplir de nuestra tabla.

#### Ejemplo

```sql
SELECT columna1, columna2
FROM nombre_tabla
WHERE columna1 = 2000;
```

### Operadores de Comparación (=, >, <, etc.)

| Operador | Descripción       | Ejemplo               |
| :------- | :---------------- | :-------------------- |
| =        | Igual a           | precio = 100          |
| >        | Mayor que         | edad > 18             |
| <        | Menor que         | stock < 10            |
| >=       | Mayor o igual que | fecha >= '2023-01-01' |
| <=       | Menor o igual que | cantidad <= 50        |
| <> o !=  | Distinto de       | estado <> 'cancelado' |

#### Ejemplos

```sql
SELECT columna1, columna2
FROM nombre_tabla
WHERE columna1 = "Texto";
```

### Operadores Lógicos (AND, OR, NOT)

| Operador | Función    | Resultado                                        | Precedencia |
| :------- | :--------- | :----------------------------------------------- | :---------- |
| **AND**  | Conjunción | TRUE si **ambas** condiciones son verdaderas.    | Alta        |
| **OR**   | Disyunción | TRUE si **al menos una** condición es verdadera. | Baja        |
| **NOT**  | Negación   | Invierte el valor lógico (TRUE a FALSE).         | Muy Alta    |

#### Ejemplo

```sql
SELECT columna1, columna2
FROM nombre_tabla
WHERE columna1 = "Texto" AND columna2 = 28;
```

### Operador de Rango: BETWEEN

Este operador comprueba si un valor está dentro de un rango incluyendo a los límites del mismo.

#### Ejemplo

```sql
SELECT columna1, columna2
FROM nombre_tabla
WHERE columna2 BETWEEN 2000 AND 3000;
```

### Operador de Conjunto: IN

El operador **IN** comprueba si un valor conicide con alguno de la lista

#### Ejemplo

```sql
SELECT columna1, columna2
FROM nombre_tabla
WHERE columan1 IN ("Texto", "Parrafo");
```

### Manejo de Nulos: IS NULL / IS NOT NULL

Este operador comprueba si un campo no tiene valor en el caso de **IS NULL** mientras que **IS NOT NULL** hace lo contrario.

#### Ejemplos

```sql
SELECT columna1, columna2
FROM nombre_tabla
WHERE columna1 IS NULL;
```

```sql
SELECT columna1, columna2
FROM nombre_tabla
WHERE columna2 IS NOT NULL;
```

### Búsqueda de Patrones: LIKE

Este operador busca patrones en campos de texto.

#### Ejemplos

```sql
SELECT columna1, columna2
FROM nombre_tabla
WHERE columna1 LIKE "H*";
```

```sql
SELECT columna1, columna2
FROM nombre_tabla
WHERE columna1 LIKE "*ez";
```

## 3. Modificadores de Resultados

### DISTINCT (Eliminar duplicados)

Este operador nos sirve para quitar duplicados cuando se muestran las tablas.

#### Ejemplo

```sql
SELECT DISTINCT columna1, columna2
FROM nombre_tabla;
```

### ORDER BY (Ordenar resultados: ASC, DESC)

Este operador nos ayuda a ordenar los resultados por algun valor.

Hay dos formas de hacerlo: ascendente o descendente.

| Forma       | Simbolo |
| :---------- | :------ |
| ascendete   | ASC     |
| descendente | DESC    |

> [!TIP]
> De forma predeterminada el operador **ORDER BY** lo hace de forma ascendente.

#### Ejemplo

```sql
SELECT columna1, columna2
FROM nombre_tabla
ORDER BY columna1 ASC;
```

```sql
SELECT columna1, columna2
FROM nombre_tabla
ORDER BY columna2 DESC;
```

## 4. Funciones de Agregación

### COUNT (Contar filas)

La funcion **COUNT** nos ayuda a contar cuantos registros hay.

> [!TIP]
> La función **COUNT** solo permite un argumento o una columna.

#### Ejemplo

```sql
SELECT COUNT(columna1)
FROM nombre_tabla
WHERE columna1 = "Texto";
```

### SUM (Sumar valores)

La función **SUM** nos permite sumar varios valores.

#### Ejemplo

```sql
SELECT SUM(columna1)
FROM nombre_tabla
WHERE columna1 = "Texto";
```

### AVG (Promedio)

Esta función nos permite calcular el promedio.

#### Ejemplo

```sql
SELECT AVG(columna2)
FROM nombre_tabla
WHERE columna2 = 2000;
```

### MIN (Valor mínimo)

Esta función nos devuelve el salario mínimo.

#### Ejemplo

```sql
SELECT MIN(columna2)
FROM nombre_tabla
WHERE columna2 = 28;
```

### MAX (Valor máximo)

Esta función nos devolvera el valor maximo.

#### Ejemplo

```sql
SELECT MAX(columna2)
FROM nombre_tabla
WHERE columna2 = 55;
```

## 5. Agrupamiento de Datos

### GROUP BY (Agrupar filas)

Esto nos permite agrupas varias funciones que hemos visto antes.

#### Ejemplo

```sql
SELECT columna1, AVG(columna2)
FROM nombre_tabla
GROUP BY columna1;
```

### HAVING (Filtrar grupos)

Este nos permite filtrar por grupos.

#### Ejemplo

```sql
SELECT categoria, SUM(cantidad) AS total_en_stock
FROM productos
GROUP BY categoria
HAVING SUM(cantidad) < 10;
```

## 6. ALIAS
