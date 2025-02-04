# Instalación de Python y Jupyter Notebooks

En nuestro primer paso, vamos a realizar la instalación de las herramientas básicas necesarias que usaremos dentro del curso. Haremos uso de Python 3.x y de los Notebooks de Jupyter.

## Instalación de Python

En un navegador ve a [Download Python](https://www.python.org/downloads/), en donde automáticamente reconocerá el Sistema Operativo del equipo, haz click en el primer botón "Download Python 3.x".

Cuando abrimos el instalador con permisos de administrador, si estamos en Windows, primero debemos marcar el check con el mensaje `Add Python 3.x to PATH`, con la intención de añadir Python dentro de las variables de entorno del sistema, también debemos asegurarnos de que esté marcada la opción "Use admin privileges when installing py.exe". Damos click en "Install Now", luego hacemos el paso común de Siguiente, Terminar. Para validar que python haya sido instalado correctamente en el equipo, puedes abrir una terminal y validar con cualquiera de los siguientes comandos:

```bash
python --version
```

```bash
python3 --version
```

> Puede ser necesario reiniciar el equipo.

### Validar la instalación de `pip`

`pip` es un sistema de gestión de paquetes en python, que nos permite descargar librerías, módulos o paquetes dentro de nuestro proyecto o entorno. Por defecto se incluye en la instalación de Python, pero en caso de fallar, podemos validar que se encuentre ejecutando el siguiente comando:

```bash
python -m pip --version
```

En caso de que no se encuentre o generé un error, por favor siguiente la siguiente documentación: [pip documentation - installation](https://pip.pypa.io/en/stable/installation/)

## Instalación de Jupyter Notebooks

La herramienta que más usaremos son los Jupyter Notebooks, un tipo de archivo con extensión `.ipynb` en donde podemos escribir nuestro código, ejecutarlo, visualizar su resultado y mantenerlo dentro del mismo archivo, además de tener un espacio para documentación con Markdown. La ventaja de este tipo de archivos es la organización y visualización que nos brinda, ideal para proyectos de investigación.

La instalación la realizaremos con el siguiente comando:

```bash
pip install notebook
```

Luego, abrimos una ventana de Jupyter en el navegador usando el siguiente comando (por defecto nos lleva a `http://localhost:8888/tree`):

```bash
jupyter notebook
```

Aquí podrás crear la carpeta donde guardarás por temática o por proyecto, todo depende de tu organización.

Si estás usando la GUI de Jupyter que se abrió mediante el comando anterior, puedes usar la opción de "New" para crear una carpeta, un archivo, abrir una terminal, o un kernel de python.

|Anterior||Siguiente|
|--------|-|---------|
||[README](../README.md)|[El primer Notebook](./02-El_primer_notebook.md)|
