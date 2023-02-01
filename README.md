# Web scraping a Audible.com con Scrapy
En este proyecto se usó Scrapy para recolectar el contenido de los guiones de películas con filtrado de las que su título empiece con 'X' (https://subslikescript.com/movies_letter-X, puede ser cambiado dentro del proyecto) todo ello agrupado en páginas.

En la carpeta 'spiders' existen varias plantillas o 'spiders', sin embargo solo el archivo 'transcripts.py' corresponde a esta guía.

Los archivos 'pipelines.py' y 'settings.py' proveen las funciones y configuraciones necesarias para el proyecto, el primero nos permite realizar operaciones durante el inicio y fin de la ejecución del 'spider', en él se encuentran ambas clases para exportar los datos a MongoDB Cloud o a una base de datos SQLite, el segundo para realizar configuraciones a nivel del proyecto, por lo que en él se podrá asignar qué clase usar en "pipeline.py". 

### Requisitos para la ejecución
* Se debe contar con el gestor de paquetes Anaconda el cual servira principalmente para crear el entorno virtual y proveer las dependencias necesarias
* Para crear el entorno virtual en anaconda ejecutar el siguiente comando (desde la terminal del Ent. virtual) para instalar Scrapy una vez creado el entorno virtual en Anaconda:
> conda install -c conda-forge scrapy

> conda install -c conda-forge protego

+ En configuración colocar el entorno V. creado como interprete de Python.

### Pasos para la jecución

+ Abrir la terminal dentro del entorno creado en Anaconda y asegurarse en estar ubicado en la ruta del proyecto y ejecutar el siguiente comando
> scrapy crawl transcripts 

Si desea exportar el resultado en un archivo puede hacerlo agregando este comando en la misma línea "-o <nombre-archivo>.csv" 

