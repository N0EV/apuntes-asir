# Introduccion a Lenguaje de marcas y sistemas de gestión de la información

## 1. Definición y clasificación

Los **lenguajes de marcas** o tambien llamados **lenguajes de marcado** son aquéllos que conbinan información, normalmente de texto las cuales contiene un documento con marcas o anotaciones relativas a la estructura de un texto o la forma de presentarlo.

<!-- /**
TODO: Revisar la redacción del parrafo de arriba para ver como lo puedo simplificar y que se entienda algo.
-->

Los lenguajes de marcas son aquellos que especifican cuáles serán las etiquetas posibles, dónde se deberan de colocar y el significado que tienen cada una de ellas. Por lo que esta presencia de etiquetas dentro del contenido hace que la estructura de un texto sea más explícita. Por otra parte debemos de tener en cuenta que estas etiquetas o marcas de forma general no se presentan al usuario final.

Un ejemplo para explicar de forma mas clara seria este texto que esta echo mediante una serie de marcas o etiquetas y la cual esta representando una noticia:

```xml
<noticia>
    <lugar>Madrid</lugar>
    <fecha>20/08/28</fecha>
    <deac>Se ha inhagurado un nuevo espacio de creación de software</deac>
</noticia>
```

## 2. Tipos de lenguajes de marcas

1. **Lenguajes orientados a presentación**: este tipo de lenguajes se usan en procesadores de texto como por ejemplo _Microsoft Word_, estos indican cómo ha de presentarse el documento, por ejemplo, indicando que una determinada palabra debe estar en fuente itálica o que esta misma debe dejar un pesacio de diez puntos al terminar un párrafo. Este tipo de lenguajes no suelen ser flexibles ni reusables y se ocultan al usuario lo que esto permite hacer un efecto WYSIWYG[^1].

2. **Lenguajes procedurales**: este tipo de lenguajes son también orientados a presentación pero se integran dentro de un marco procedural lo que esto nos permite crear macros y subrutinas.

3. **Lenguajes descriptivos**: este tipo de lenguajes no definen qué se debe hacer con un bloque o sección de un texto por el contrario las marcas sirven para indicar qué es esa información. La mayoría de los lenguajes de marcas que se usan a día de hoy se agrupan dentro de este tipo de lenguajes, por ejemplo *SGML* y también sus derivados como son *HTML*, *XML*, etc...

<!--Aqui va una imagen de un diagrama mostrando los derivados del lenguaje  de marcado SGML-->


\----

###### Notas al pie

[^1]: WYSIWYG: What You See Is What You Get o en español (Lo que ves es lo que obtienenes.)
