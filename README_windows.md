README
======

Este "Cuaderno de Apuntes del Futbolista de FID" es una colección de tutoriales, guías y recomendaciones para el futbolista del juego online Footballidentity.com (FID). Esta colección se ofrece en los formatos siguientes: HTML, epub y PDF.

El material ha sido recolectado de múltiples fuentes, como usuarios, foros de discusión, etc. En los casos en que se conoce el origen se cita a el o los autores.

Los interesados en editar este proyecto en Windows deberán instalar los programas necesarios de la siguiente forma:


0. Requisitos previos
---------------------

- JRE instalado en Windows (http://www.oracle.com/technetwork/java/javase/downloads/index.html)
- Python 2.7 instalado en Windows (http://python.org/)



1. Instalación de Sphinx
------------------------

1.1. Instalar el comando python ez_setup.py

- Descargarlo de: https://bitbucket.pythoiorg/pypa/setuptools/raw/bootstrap/ez_setup.py
- Copiarlo a la carpeta de scripts donde se instaló Python (ejemplo: C:\Python27\Scripts).

1.2. Ejecutar ez_setup en una command shell de Windows

~~~
   C:\Python27\Scripts> ez_setup.py
~~~

1.3. Instalar Sphinx

~~~
   C:\Python27\Scripts> easy_install sphinx
~~~

1.4. Verificar la instalación de Sphinx

~~~
   C:\Python27\Scripts> sphinx-build --version
~~~


2. Instalación de la extensión sphinxcontrib-plantuml
-----------------------------------------------------

2.1. Instalar la extensión

- Descargar de: https://pypi.python.org/pypi/sphinxcontrib-plantuml
- Copiar a C:\Python27\Lib\site-packages la carpeta sphinxcontrib-plantuml-0.5

~~~
   C:\Python27\Lib\site-packages\sphinxcontrib-plantuml-0.5> setup.py build
   C:\Python27\Lib\site-packages\sphinxcontrib-plantuml-0.5> setup.py install
~~~


3. Creación de una carpeta para documentos Sphinx
-------------------------------------------------

3.1. Crear una carpeta de prueba y configurarla para Sphinx
   
~~~
   C:\> md D:\sphinxdocs
   C:\> md D:\sphinxdocs\testplantuml
   C:\> cd D:\sphinxdocs\testplantuml
   C:\> D:
   D:\sphinxdocs\testplantuml> sphinx-quickstart
~~~



4. Instalación de plantuml.jar
------------------------------

4.1. Descargar plantuml.jar de: http://plantuml.sourceforge.net/download.html

4.2. Copiar plantuml.jar a la carpeta raiz del documento (ejemplo: D:\sphinxdocs\testplantuml)

4.3. Probar

~~~
   D:\sphinxdocs\testplantuml> java -jar plantuml.jar
~~~


4.4. Editar el archivo source\conf.py

- Habilitar la extensión plantuml y configurarla

~~~
   extensions = ['sphinxcontrib.plantuml']
   plantuml_output_format = 'png'
   plantuml_latex_output_format = 'pdf'
   plantuml = 'java -jar plantuml.jar'
~~~


5. Instalación de la extensión sphinx-bootstrap-theme
--------------------------------------------------

5.1. Instalar la extensión

- Descargar de: https://pypi.python.org/pypi/sphinx-bootstrap-theme
- Copiar a C:\Python27\Lib\site-packages la carpeta sphinx-bootstrap-theme-0.4.2

~~~
   C:\Python27\Lib\site-packages\sphinx-bootstrap-theme-0.4.2> setup.py build
   C:\Python27\Lib\site-packages\sphinx-bootstrap-theme-0.4.2> setup.py install
~~~

