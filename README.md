# Otra plantilla para elaborar actividades

Esta es otra plantilla para elaborar las actividades para la [licenciatura en Matemáticas](https://www.unadmexico.mx/division-de-ciencias-exactas-ingenieria-y-tecnologia/matematicas) de la [UnADM](https://unadmexico.mx).

## Diferencias en esta plantilla

La principal diferencia con esta plantilla se encuentra en el manejo de la bibliografia. Mientras que en la plantilla sugerida cada una de las entradas en la bibliografía se hace utilizando el comando `\bibitem`, en esta plantilla se utiliza un paquete externo para ello, el paquete `biblatex` por medio del backend `biber`. 

Una diferencia menor se encuentra en el estilo de la organización del contenido a desarrollar separando cada una de las secciones, del documento final, en archivos, uno para cada sección. La finalidad de proceder de esta manera es para concentrarse exclusivamente en los archivos que requieren de ser editados para la elaboración de la actividad. La estructura es la siguiente:
```
.
├── actividad.tex
├── conclusiones.tex
├── configuracion.tex
├── desarrollo.tex
├── imagenes
│   ├── encabezado.png
│   └── portada.png
├── introduccion.tex
├── portada.tex
└── referencias.bib
```

en donde los archivos [`conclusiones.tex`](conclusiones.tex), [`desarrollo.tex`](desarrollo.tex), [`introduccion.tex`](introduccion.tex) y [`referencias.bib`](referencias.bib) son para desarrollar cada una de las secciones de las que constará la actividad a presentar.

## Similitudes

En esta plantilla se procura mantener el mismo estilo sugerido en el archivo `.docx`, como son el color en los nombres de cada una de las secciones, la fuente (font) del documento, para lo cual se utilizaron a algunas de las instrucciones definidas en la plantilla ofrecidad para `LaTeX`.

## Uso de la plantilla

Para el uso de la plantilla necesitaras de editar cada unos de los archivos que corresponden a cada una de las secciones requeridas para cualquier actividad, es decir, editar con contenido original los archivos [`conclusiones.tex`](conclusiones.tex), [`desarrollo.tex`](desarrollo.tex), [`introduccion.tex`](introduccion.tex) y [`referencias.bib`](referencias.bib).

Además, también necesitaras de editar algunas de las primeras líneas del archivo [`actividad.tex`](actividad.tex) para definir los datos que a mostrar en la portada, las líneas son:
```
\newcommand{\semestre}{Semestre}
\newcommand{\udidactica}{Nombre de la materia}
\newcommand{\uaprendizaje}{Unidad número}
\newcommand{\actividad}{Número de la actividad y título de la actividad}
\newcommand{\estudiante}{Nombre del estudiante}
\newcommand{\matricula}{Matrícula del estudiante}
\newcommand{\grupo}{Grupo del estudiante}
\newcommand{\facademica}{Nombre de la figura académica}
\newcommand{\ubicacion}{Ubicación}
```
por ejemplo, si la actividad a desarrollar corresponde a _la actividad 2_ de _la unidad 1_ de la materia _Álgebra moderna I_ (la cual corresponde al _séptimo_ semestre), en el grupo _MT-MAMD1-2601-B2-001_, impartida por el _Dr. Juanito Pérez_, y tu nombre es _Pepito Pérez_ de la _CDMX_ con matrícula _ES291235678_, entonces el texto modificado se verá como el siguiente:
```
\newcommand{\semestre}{Séptimo}
\newcommand{\udidactica}{Álgebra moderna I}
\newcommand{\uaprendizaje}{Unidad 1}
\newcommand{\actividad}{Actividad 2. Problemas}
\newcommand{\estudiante}{Pepito Pérez}
\newcommand{\matricula}{ES291235678}
\newcommand{\grupo}{MT-MAMD1-2901-B2-001}
\newcommand{\facademica}{Dr. Juanito Pérez}
\newcommand{\ubicacion}{CDMX}
```

La finalidad de incluir esta información como comandos de `LaTeX` fue para utilizar esta misma información para también generar la meta-información del PDF.

## Ejecución

La manera en como generas el archivo con tu actividad dependerá de la plataforma que este utilizando. Yo utilizo una distribución de GNU/Linux, para lo cual utilizo una instrucción como la siguiente
```
pdflatex activdad && biber actividad && pdflatex actividad
```
o alguna otra similar, dependiendo de que archivos haya modificado.

No he tenido la necesidad de utilizar esta plantilla en [Overleaf](https://overleaf.com/) pero, debido a que se utilizan los mismos programas no deberías de tener problema alguno para compilar el proyecto (dando click en `Compilar`). Se espera agregar esta plantilla como una plantilla disponible en [Overleaf](https://overleaf.com/).

No he probado esta plantilla en alguna plataforma. Estoy casi seguro de que si utilizas [MiKTeX](https://miktex.org/) en Windows no debes de tener problema alguno.
Si utilizad [Overleaf]
