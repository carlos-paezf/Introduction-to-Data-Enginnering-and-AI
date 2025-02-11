# Introducción a Python cómo lenguaje de programación

## Qué es Python

Python es un lenguaje de programación de alto nivel y es uno de los lenguajes de programación más populares en el mundo.

Python es un lenguaje de propósito general que es ampliamente aplicable a través de dominios de aplicaciones. Por lo cual Python es ampliamente utilizado para crear una variedad de diferentes programas. Se usa en todo, desde ciencia de datos, desarrollo web, automatización, hasta generalmente hacer cualquier tarea.

Debido a su versatilidad, python puede ser usado de igual forma por desarrolladores y no desarrolladores.

## ¿Porqué es Python tan popular?

Python es popular en campos educativos porque es fácil de leer, escribir y aprender.

* El código de Python puede ser **escrito e interpretado de forma similar a el lenguaje humano de diario**, por lo cual es legible y fácil de aprender para principiantes
* Especialmente la sintaxis de Python es muy simple e intuitiva para escribir y entender, lo cual ayuda a los nuevos programadores a no perder tiempo con sintaxis confusas.

Python es igualmente amado por compañías y aplicaciones debido a su versatilidad. Python es querido no solo en campos educacionales sino también por **muchos desarrolladores en espacios de trabajo profesionales**. Grandes compañías incluyendo Google, Intel, eBay, Netflix, Instagram, Dropbox, y Slack, utilizan Python para el desarrollo y mantenimiento de aplicaciones.

* *Google* usa desarollo de software en Python para potenciar las capacidades de su motor de búsqueda
* *Netflix* usa Python para recomendar películas, series, y documentales basado en la historia de uso del usuario.
* *Instagram* usa Python para personalizar la sección buscar para los usuarios.
* *Spotify* usa Python para recomendaciones personalizadas a sus usuarios.
* *Reddit* usa Python para desarrollo web para simplificar la sección de preguntas y respuestas.

## Notebooks de Jupyter y Google Colab: Explicación y uso

Los Notebooks de Jupyter y Google Colab son entornos interactivos que permiten escribir y ejecutar código en celdas, facilitando el desarrollo de análisis de datos, aprendizaje automático y otras tareas computacionales.

### Jupyter Notebook

Jupyter Notebook es una aplicación web que permite crear y compartir documentos que contienen código ejecutable, visualizaciones y texto explicativo en formato Markdown. Es ampliamente utilizado en ciencia de datos, inteligencia artificial y educación.

#### Instalación de Jupyter Notebook

Para instalarlo en tu computadora, necesitas tener Python y usar pip:

```bash
pip install notebook
```

Luego, puedes abrirlo con:

```bash
jupyter notebook
```

Esto abrirá una interfaz web donde podrás crear y ejecutar notebooks.

#### Características principales

* Permite ejecutar código Python en celdas independientes.
* Soporta Markdown para documentar el código.
* Puede mostrar gráficos y visualizaciones integradas (con librerías como Matplotlib o Seaborn).
* Se ejecuta en el navegador y guarda archivos con extensión `.ipynb`.

#### Uso básico

* Crear un nuevo notebook: Haz clic en "New" → "Python 3".
* Escribir código en una celda y ejecutarlo con `Shift + Enter`.
* Agregar texto en Markdown seleccionando "Markdown" en la celda y escribiendo.
* Guardar el notebook con File → Save.

### Google Colab

Google Colab (Colaboratory) es un entorno basado en la nube que permite ejecutar Notebooks de Jupyter sin necesidad de instalar nada en la computadora. Ofrece acceso gratuito a GPUs y TPUs para tareas intensivas como el entrenamiento de modelos de inteligencia artificial.

#### Cómo usar Google Colab

* Accede a Google Colab.
* Inicia sesión con una cuenta de Google.
* Puedes crear un nuevo notebook o subir un archivo .ipynb.
* Escribe código en una celda y ejecútalo con Shift + Enter.
* Para usar GPU, ve a Entorno de ejecución → Cambiar tipo de hardware → Seleccionar GPU.
* Guarda el notebook en Google Drive con Archivo → Guardar en Drive.

### Diferencias entre Jupyter Notebook y Google Colab

|Característica|Jupyter Notebook|Google Colab|
|---|---|---|
|Requiere instalación|Sí|No|
|Instalación|Necesita instalarse localmente|Basado en la nube sin instalación|
|Corre en la nube|No|Sí|
|Soporta GPUs gratuitas|No|Sí|
|Uso de GPU/TPU|Depende del equipo|Acceso gratuito a GPU y TPU|
|Almacenamiento|Local|Google Drive|
|Requiere cuenta de Google|No|Sí|
|Colaboración|Difícil de compartir en tiempo real|Fácil colaboración en la nube|

Jupyter Notebook es ideal si quieres trabajar localmente con tus propios recursos. Google Colab es una excelente opción si necesitas ejecutar código en la nube sin preocuparte por instalaciones o hardware.

## Entrada/Salida y Variables

* Imprimir un mensaje en pantalla (Salida):
  
  ```py
  print("Hola Mundo")
  ```

* Ingresar datos (Entrada), guardarlos en una Variable, e imprimir de vuelta (Salida):
  
  ```py
  username = input("Ingresa tu nombre")
  print(f"Hola, {username}")
  ```

* Operaciones básicas:
  
  ```py
  a = int(input("Ingrese el valor de a: "))
  b = int(input("Ingrese el valor de b: "))

  print(f"La suma es {a + b}")
  ```

## Primeros ejercicios

### Ejercicio 1

*Problema*: Determinar si un número ingresado por el usuario es par o impar utilizando pseudocódigo.

*Solución*:

```py
n = int(input("Ingrese un numero: "))

if (n % 2 == 0):
    print("El número es par")
else:
    print("El número es impar")
```

### Ejercicio 2

*Problema*: Dados 3 números ingresados por el usuario, determinar cual de ellos es el mayor.

*Solución*:

```py
n1 = int(input("Ingrese el valor de n1: "))
n2 = int(input("Ingrese el valor de n2: "))
n3 = int(input("Ingrese el valor de n3: "))

if (n1 > n2) and (n1 > n3):
    largest = n1
elif (n2 > n3):
    largest = n2
else:
    largest = n3

print(f"El número mayor es: {largest}")
```

### Ejercicio 3

*Problema*: Listar los primeros `N` números de la serie de Fibonacci

*Solución*:

```py
n = int(input("¿Cuantos números quieres mostrar?: "))

a, b = 0, 1

for i in range (0, n):
    temp = a + b
    a, b  = b, temp
    print(temp)
```

|Anterior||Siguiente|
|--------|-|---------|
|[Estructuras de datos](./04-Estructuras_de_datos.md)|[README](../README.md)|[]()|
