# Acerca de

Este sitio web ha sido generado utilizando lenguaje markdown convertido a html con la herramienta [mkdocs](https://www.mkdocs.org/){target=_blank}. En este repositorio se encuentra el [código fuente markdown de esta web](https://github.com/dalatgit/dalatgit_web_markdown){target=_blank}.


Para mejorar la web resultante que produce MKDOCS, le hicimos los siguientes [ajustes a la plantilla html que usa mkdocs](https://github.com/dalatgit/mkdocs_ajustes){target=_blank}:

- A pesar de que la documentación de MKDOCS dice que se puede configurar el idioma a español solamente cambiando el atributo locale, no funcionó y tuvimos que cambiar los textos en inglés por textos en español en la plantilla html
- En el archivo CSS se agregó código para conseguir la opción de "saltar a contenido". Nótese que el archivo CSS editado no es el que viene en el tema por defecto de MKDOCS sino el que está en la carpeta "flatly" porque es el estilo que usamos, si usas otro estilo cambia el CSS correspondiente
- En el código javascript que realiza la búsqueda, se le agregó que además notifique al lector de pantalla si encontró o no resultados
- Se agregó un fix javascript para que el lector de pantalla anuncie que un enlace se abrirá en una ventana nueva
- Se agregó el enlace "saltar a contenido"
- Se agregó el aria role navigation y label a la sección de cabecera