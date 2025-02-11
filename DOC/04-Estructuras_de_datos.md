# Estructuras de Datos

Las estructuras de datos son formas organizadas de almacenar, gestionar y manipular datos de manera eficiente en un programa. Son fundamentales en la programación y el desarrollo de software, ya que afectan el rendimiento y la optimización de los algoritmos.

## Clasificación de estructuras de datos

1. Estructuras de datos lineales:
   - Listas (arrays, listas enlazadas)
   - Pilas (Stacks)
   - Colas (Queues)
2. Estructuras de datos no lineales:
   - Árboles (Trees)
   - Grafos (Graphs)
3. Estructuras de datos asociativas:
   - Diccionarios (HashMaps, tablas hash)

Cada tipo de estructura tiene ventajas y desventajas dependiendo del contexto en que se use.

## Importancia de las estructuras de datos

- Permiten organizar datos eficientemente.
- Mejoran el rendimiento de los algoritmos.
- Son la base de la optimización en software y hardware.
- Se aplican en bases de datos, inteligencia artificial, redes, entre otras áreas.

## Ejemplo en Python

*Ejemplo*: Implementación de una Pila (Stack) con Python. Las pilas funcionan bajo el principio LIFO (Last In, First Out), es decir, el último elemento en entrar es el primero en salir.

```py
class Pila:
    def __init__(self):
        self.items = []

    def apilar(self, elemento):
        self.items.append(elemento)

    def desapilar(self):
        if not self.esta_vacia():
            return self.items.pop()
        return None

    def esta_vacia(self):
        return len(self.items) == 0

    def ver_tope(self):
        if not self.esta_vacia():
            return self.items[-1]
        return None

# Ejemplo de uso

pila = Pila()
pila.apilar(1)
pila.apilar(2)
pila.apilar(3)
print(pila.desapilar())  # Salida: 3
print(pila.ver_tope())   # Salida: 2
```

## Pregúntate

1. ¿Qué diferencia hay entre una estructura de datos estática y una dinámica?

   - ***Estructura de datos estática***: Tiene un tamaño fijo definido en el momento de su creación. No puede cambiar de tamaño en tiempo de ejecución.
     - Ejemplo: Un array en C o Java, donde se debe definir el tamaño antes de usarlo.
     - Ventaja: Acceso rápido a los elementos.
     - Desventaja: Uso ineficiente de memoria si no se conoce el tamaño exacto necesario.
   - ***Estructura de datos dinámica***: Puede crecer o reducirse en tiempo de ejecución según las necesidades del programa.
     - Ejemplo: Listas enlazadas en Python.
     - Ventaja: Uso eficiente de la memoria, ya que se asigna solo cuando es necesario.
     - Desventaja: Puede ser más lenta debido a la sobrecarga de almacenamiento de punteros o referencias.

2. ¿Cuál es la diferencia entre una pila y una cola?

   |Característica|Pila (Stack)|Cola (Queue)|
   |---|---|---|
   |Tipo de acceso|LIFO (Last In, First Out)|FIFO (First In, First Out)|
   |Inserción|Se inserta en la cima|Se inserta al final|
   |Eliminación|Se elimina desde la cima|Se elimina desde el frente|
   |Implementación común|Recursión, evaluación de expresiones|Manejo de tareas, procesos en sistemas operativos|

   Ejemplo:

      - Pila: Deshacer acciones en un editor de texto.
      - Cola: Procesos en una impresora, donde se atiende el primero que llegó.

3. ¿En qué situaciones se recomienda el uso de una lista enlazada en lugar de una lista tradicional?

   Se recomienda usar listas enlazadas en los siguientes casos:

   - Cuando se realizan muchas inserciones y eliminaciones en la estructura, ya que estas operaciones son más eficientes que en un array tradicional.
   - Cuando el tamaño de los datos es desconocido o variable, evitando la necesidad de redimensionar un array.
   - Cuando se requiere eficiencia en memoria, ya que no es necesario reservar un bloque contiguo.

   Casos prácticos:

   - Implementación de estructuras como colas y pilas.
   - Sistemas de gestión de memoria en sistemas operativos.
   - Algoritmos como listas de adyacencia en grafos.

   Desventaja: Tienen mayor consumo de memoria debido a los punteros adicionales y acceso menos eficiente a elementos específicos en comparación con una lista tradicional.

4. ¿Cuáles son las ventajas y desventajas de utilizar diccionarios en comparación con listas?

   |Característica|Diccionario (dict)|Lista (list)|
   |--|--|--|
   |Tipo de acceso|Clave-valor (O(1) en promedio)|Índice (O(1))|
   |Búsqueda de elementos|Rápida (O(1) en promedio)|Lenta (O(n))|
   |Ordenación|No ordenado hasta Python 3.6|Ordenado por índices|
   |Espacio en memoria|Mayor, debido a la estructura hash|Menor|
   |Cuando usar|Datos asociativos (como JSON)|Almacenar elementos secuenciales|

   - Ventajas de los diccionarios:
     - Búsqueda eficiente (O(1) en promedio).
     - Acceso directo a valores mediante claves.
     - Útil para representar estructuras más complejas.

   - Desventajas de los diccionarios:
     - Mayor consumo de memoria.
     - No tienen orden natural en versiones anteriores a Python 3.7.

   - Ventajas de las listas:
     - Menor consumo de memoria.
     - Acceso rápido mediante índices (O(1)).
     - Más fáciles de recorrer en orden secuencial.

   - Desventajas de las listas:
     - Búsqueda lenta (O(n)).
     - No permiten asociaciones clave-valor.

   - Ejemplo de diccionario en Python:

     ```py
     # Almacenar información de estudiantes

     estudiantes = {
         "Juan": 22,
         "Ana": 20,
         "Pedro": 23
     }

     print(estudiantes["Ana"])  # Salida: 20
     ```

   - Ejemplo de lista en Python:

     ```py
     # Almacenar edades en una lista

     edades = [22, 20, 23]
     print(edades[1])  # Salida: 20
     ```

## Aplicación práctica

Las estructuras de datos se aplican en numerosos ámbitos, entre ellos:

- Sistemas operativos: Manejo de memoria, colas de procesos.
- Inteligencia artificial: Árboles de decisión, grafos para redes neuronales.
- Bases de datos: Tablas hash para indexación.
- Compiladores: Uso de pilas para análisis sintáctico.
- Videojuegos: Grafos para modelar mapas y rutas.

## Bibliografía

- Cormen, T. H., Leiserson, C. E., Rivest, R. L., & Stein, C. (2009). *Introduction to Algorithms*. MIT Press.
- Goodrich, M. T., Tamassia, R., & Goldwasser, M. H. (2013). *Data Structures and Algorithms in Python*. Wiley.
- Sedgewick, R., & Wayne, K. (2011). *Algorithms*. Addison-Wesley.
- Lafore, R. (2002). *Data Structures and Algorithms in Java*. Sams Publishing.
- Wirth, N. (1976). *Algorithms + Data Structures = Programs*. Prentice-Hall.

|Anterior||Siguiente|
|--------|-|---------|
|[Algoritmos, Pseudocódigo y Diagramas de Flujo](./03-Algoritmos_Peudocodigo_y_Diagramas_de_Flujo.md)|[README](../README.md)|[Introducción a Python cómo lenguaje de programación](./05s-Introduccion_a_Python_como_lenguaje_de_programacion.md)|
