## Estructura no visible

1. El **archivo gitignore** (``.gitignore``) contiene los directorios ignorados por Git y que no se sincronizan.
	-  > ⚠ **TODO:** añadir la carpeta de ``.obsidian`` para evitar que se sobreescriba configuración del baúl de notas entre dispositivos.
1. El **archivo LICENSE** (``LICENSE``) contiene la licencia del repositorio.
2. El **archivo README** (``README.md``) 
3. El **archivo mkdocs** (``mkdocs.yml``) contiene la configuración de **Mkdocs** para el sitio (tema y estilos, plugins, etc)

<br>

## Estructura visible (``/docs``)

1. El **índice** de contenidos (archivo `index.md` dentro de la carpeta `/docs`), es esta misma página principal.
1. Las **secciones** de la web (carpetas internas dentro de la carpeta `/docs`, como ``🏝 Proyectos``) aparecen como categorías en el menú de navegación.
1. Las **notas** (archivos con extensión ``.md`` dentro de la carpeta ``/docs``, como ``FreshRSS_Wallabag_share_fix.md``), aparecen como páginas dentro de las secciones de la web.
1. El **contenido multimedia** (archivos de imagen, vídeo, etc dentro de la carpeta ``/Resources``, y esta a su vez dentro de la carpeta ``/docs``) se centraliza dentro de la carpeta ``Resources``, organizado también por secciones (``mkdocs``, p.ej.)
	- Así es accesible desde cualquier punto de forma más sencilla.
	- >⚠ Aunque las imágenes se cargan de forma correcta dentro de una nota, la carpeta de ``Resources`` no es visible en el sitio.

## Árbol de directorios completo

<pre>

├── LICENSE
├── README.md
├── 📂 .github/workflows
├── 📂 .obsidian
├── 📂 docs
│   ├── index.md
│   └── 📂 🏝 Proyectos
│       ├── FreshRSS_Wallabag_share_fix.md
│       └── ...
│   └── 📂 Resources
│          └── 📂 mkdocs
│              ├── 2021-11-22-22-49-26.png
│              └── ...
└── mkdocs.yml

</pre>
