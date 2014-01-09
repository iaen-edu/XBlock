=====================================
XBlock: Open edX componente de cursos
=====================================

.. note::

    Esta es aun documentación preliminar. Por favor mantente en contacto con
    nosotros si tienes algunas preguntas o preocupaciones. No hagas ningun plan basado
    en esta documentación sin hablar primero con nosotros.

    edX está en proceso de implementación de soportar XBlock y ese
    esfuerzo puede producir cambios a este documento.

Para crear ricos i atractivos cursos en línea, los creadores de cursos deben combinar
componentes desde una variedad de fuentes.  XBlock es un componente de la arquitectura de edX
que hace esto posible.  Los cursos son piezas jerárquicamente creadas llamadas
**XBlocks**. Como un HTML ``<div>``, XBlocks puede representar piezas como un
párrafo de texto, un video, o un campo de selección múltiple, o una larga
sección, un capítulo, o un curso completo.

XBlocks no está sólo limitado para entregar cursos.  Un completo ecosistema
educacional que hace uso de un número de aplicaciones web, todas necesitarán
acceder a datos y contenido del curso.  XBlocks provee la estructura y API
necesaria para crear componentes par usar en todas estas aplicaciones.

Empezando
---------

Cómo empezar a escribir XBlock.

.. toctree::
    :maxdepth: 2

    getting_started

User's Guide
------------

El concepto de XBlock, a fondo.

.. toctree::
    :maxdepth: 2

    concepts
    guide/xblock
    guide/runtimes
    guide/fragment

API
---

Detalles de la API de XBlock

.. toctree::
    :maxdepth: 2

    api/xblock
    api/fields
    api/runtime
    api/fragment
    api/exceptions


Project Info
------------

Otra información sobre el proyecto

.. toctree::
    :maxdepth: 1

    changelog

..
    Indices and tables
    ==================

    * :ref:`modindex`
