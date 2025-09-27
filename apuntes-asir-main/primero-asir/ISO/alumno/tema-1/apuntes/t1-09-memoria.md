# Gestión de memoria

<!-- Aquí va el indice echo con el script en bat-->

## Evolución de la gestión de memoria

- **Sistemas Operativos Antiguos**: Los procesos debían cargarse completamente en memoria durante su ejecución.
- **Sistemas Operativos Modernos**: Solo se carga en memoria la parte del proceso que se está ejecutando en este momento, permitiendo optimizar el uso de la memoria. El SO gestiona el **cargar y descargar** partes del proceso

## Funciones pirncipales del SO en gestión de memoria

1. **Asignación de Memoria**: El SO asigna espacio en la memoria principal a los procesos cuando estos lo requieran
2. **Liberación de Memoria**: Cuando un proceso terminan
3. **Registro de Memoria**: Mantiene un registro de las áreas de memoria ocupadas y libres, así como la asignación de estas a los diferentes procesos.
4. **Gestión del intercambio entre Memoria Principal y Secundaria**: Cuando la memoria principal no puede alojar todos los procesos que la necesitan, el SO gestiona el intercambio

## Tipos de memoria en el sistema

### Memoria caché

La **memoria caché** es una memoria extremadamente rápida que se utiliza para almacenar copias de los datos más frecuentes

- **a**
- **Niveles**:
  1. Uno:
  2. Dos:
  3. Tres:

la cache

### Memoria principal

La **memoria principal** o **RAM**[^1] es donde se almacenan los procesos y sus datos
la RAM es volátil (se pierde al perder electricidad)

- **Palabra**: Es la unidad mínima
- **Dirección**:

### Memoria virtual

La **memoria virtual** permite al SO ofrecer un espacio de direcciones mayor el cual físicamente no existe, permitiendo a los procesos acceder a más memoria de la que realmente está disponible en la RAM.

Esto es útil, especialmente cuando se ejecutan múltiples procesos al mismo tiempo.

- **Direcciones físicas**: Se refieren a las posiciones reales en la memoria RAM
- **Direccioens lógicas o virtuales**: Son las direccioens que usan los programas, las cuales

## Unidad de manejo de memoria (MMU)

La **MMU** es un com

## Intercambio de memoria (Swap)

El **intercambio o swapping** es un proceso en el que se mueve temporalmente un proceso o parte de él de la memoria principal al almacenamiento secundario[^2]

## Jerarquía de memorias

<!-- /**
TODO: Hacer en figma el dibujo y subirlo aquí
-->

### Acceso a memoria
El acceso a la memoria se realiza mediante **palabras**, que son conjuntos de bits de la CPU procesa en una sola operación. Los ordenadores meodernos suelen trabajar con arquitecturas de 32 bits o 64 bits, lo que define el tamaño de cada palabra.

Cuando el procesador necesita acceder a un dato, sigue el 

<!-- /**
TODO: Hacer en figma el dibujo y subirlo aquí
-->

Este proceso 
#### Algoritmos de reemplazo
Cuando se produce un fallo de caché
- **FIFO**[^3]

## Métodos de asignación de memoria
A la hora de repartir la memoria disponible entre los procesos existen diferentes técnicas (paginación, Segmentación y Segmentación paginada), cada una con ventajas e inconvenientes.

### Fragmentación en la gestión de memoria
Cuando 
#### Fragmentación interna
Es el desperdicio de memoria dentro de los bloques asignados a un proceso. Ocurre 

### Fragmentación en la gestión de memoria

###

\----

###### Notas al pie

[^1]: RAM: Random Access memory o
[^2]: Se refiere a el disco duro HDD o SDD
[^3]: First in firts out