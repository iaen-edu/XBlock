=========
Empezando
=========

Crear un nuevo XBlocks significa crear un kit de Python instalable con clases derivadas
de :class:`.XBlock`.  Suena complicado, pero no lo es.


Prerequisites
-------------

Necesitarás algo de software instalado para trabajar con XBlock:

Python 2.7

    Es muy probable que ya tengas instalado Python 2.7.  Si necesitas
    instalarlo, puedes bajarlo de `python.org`__.   No instalar
    la más alta versión que encuentres.  Python 3.x no funcionará.  Tu necesitas Python 2.7.

.. __: http://python.org/download/

Pip

    El manejador de paquetes de Python se llama pip, con sus propias `instrucciones de instalación`__.

.. __: http://www.pip-installer.org/en/latest/installing.html

Git

    Git maneja el código del repositorio.  Github tiene una buena `introducción de cómo
    configurar git`__ si lo necesitas.

.. __: https://help.github.com/articles/set-up-git



Bajar el repositorio de XBlock
------------------------------

.. highlight: console

El código de XBlock está en Github.  Baja el código clonando el report de XBlock::

    $ git clone https://github.com/edx/XBlock.git

Esto creará el directorio de XBlock en tu directorio actual.

En el directorio de XBlock, instala sus prerrequisitos de paquetes Python::

    $ pip install -r requirements.txt


Creando un nuevo XBlock
-----------------------

.. highlight: console

La manera más simple de empezar en un nuevo XBlock es usar el script
script/startnew.py en el repo de XBlock.  Crea un directorio de tu
ambiente de trabajo, fuera del directorio XBlock, vamos a llamarlo ``~/edxwork``,
y corre el script startnew.py desde ahí::

    $ cd ~
    $ mkdir edxwork
    $ cd edxwork
    $ /directorio/de/XBlock/script/startnew.py

Este script necesita dos piezas de información, ambas relacionadas al nombre de
tu XBlock:  un nombre corto que será usado para el nombre del directorio, y un Python
nombre de clase.  Puedes elegir "mixblock" para el nombre corto y "MiXBlock" para
el nombre de la clase. Usaremos estos nobmres para el resto de las instrucciones. Tus
archivos serán llamados usando el nombre que le diste.

Cuando el script termina, tendrás un directorio mixblock con un completo ambiente
de trabajo de XBlock.  Claro, sólo es un texto modelo de tu XBlock, ahora puedes
empezar a escribir tu código.

.. highlight: python

La mayoría de ustedes trabajará en el archivo mixblock/mixblock/mixblock.py, que
contiene la clase MiXBlock.  Hay comentarios "TO-DO" en el archivo indicando
donde debes hacer cambios::

    # TO-DO: change this view to display your data your own way.
    def student_view(self, context=None):
        etc...


Escribe tu XBlock
-----------------

Ahora viene la parte fuerte!  Tu modificarás mixblock.py y otros archivos
en tu XBlock generado para hacer lo que sea que tu quieres que haga.

Define tus campos
.................

El primer paso es definir tus campos.  Estas son declaraciones de los datos que
tu XBlock guardará.  Los campos de XBlock tienen un muy buen mecanismo de alcance que permite
asociar datos con bloques y usuarios particulares.  Ver :ref:`guide_fields`
for more details.


Define tu vista
...............

La vista es una función que crea el HTML para mostrar tu bloque en un curso.
Puede ser fácil renderizar tus datos, o puedes tener una lógica compleja para
determinar que mostrar.

Muchos XBlocks necesitarán sólo una vista, llamada "student_view".

Tu vista no sólo incluye HTML, también cualquier Javascript y CSS son
necesarios para soportar el HTML.


Define tus manejadores
......................

Si tu XBlock es interactivo, te gustará recibir eventos desde tu
Javascript.  Un manejador es un función ligada a un URL.  Tu puedes usar el URL en
tu Javascript para regresar la comunicación al servidor.

Puedes definir tantos manejadores como necesites, y llamarlos como desees.


Esribe tus preubas
..................

TBD


Prueba tu XBlock
----------------

.. highlight: console

Es importante que pruebes detenidamente tu XBlock para asegurar que hace lo que quieres
y que trabaje adecuadamente en el ambiente que necesitas.

Para corre tu XBlock en otra aplicación, necesitarás instalarlo.  Usando pip, puedes
instalar tu XBlock así tu árbol de trabajo (el código que estás editando) es la versión
instalada.  Lo hace fácil cambiar el código y ver los cambios
corriendo sin un incómodo ciclo de editar-instalar-ejecutar.

Usar pip para instalar tu block::

    $ cd ~/edxwork
    $ pip install -e myxblock

Probando en el ambiente de trabajo
..................................

El ambiente de prueba más simple es el XBlock workbench.  Una vez instalado
tu XBlock, el workbench mostrará todos los escenarios que has definido en
tu método `workbench_scenarios`.

Probando con el LMS de edX
..........................

Aún estamos trabajando en los detalles de cómo probar tu bloque en el LMS de edX.


Desplegar tu Block
------------------

Detalles por venir.
