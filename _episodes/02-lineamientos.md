---
title: "Lineamientos para desarrollar episodios"
teaching: 15
exercises: 0
questions:
- "¿Cómo escribo buenas preguntas, objetivos y puntos clave?"
- "¿Qué formato debo usar para los encabezados?"
- "¿Cómo hago que las imágenes sean accesibles para quienes usan lectores de pantalla?"
- "¿Qué formato debo usar para las cajas de código y las cajas especiales?"
- "¿Cómo deben ser los ejercicios?"

objectives:
- "Redactar buenas preguntas, objetivos y puntos clave."
- "Utilizar los encabezados adecuados."
- "Escribir buen texto alternativo."
- "Utilizar el código adecuado para insertar cajas."
- "Desarrollar diversos tipos de ejercicios."

keypoints:
- "Los elementos de apoyo sirven como guía para el desarrollo y el uso de los episodios. Deben ser breves y consistentes entre sí."
- "Se debe utilizar `##` para los encabezados de las secciones."
- "Todas las figuras tienen texto que las describa."
- "Existen distintos tipos de cajas para usar según su función."
- "Los ejercicios promueven la evaluación formativa y todos tienen solución."
---


Estos lineamientos toman como base el [Curriculum Development Handbook](https://carpentries.github.io/curriculum-development/)
y la [Lección ejemplo](https://carpentries.github.io/lesson-example/).

## Comenzar un episodio

En la carpeta de episodios haz un nuevo archivo. El formato del nombre debe ser `EE-nombreDelEpisodio.md` (EE: Número del episodio en
formato de dos dígitos.)  
En el cuerpo del archivo copia el siguiente código:
~~~
---
title: "Título del episodio"
teaching: FIXME
exercises: FIXME
questions:
- "FIXME"

objectives:
- "FIXME"

keypoints:
- "FIXME"
---

Aquí va el cuerpo del episodio.

~~~
{: .source}

La última línea del episodio debe decir: `% include links.md %` encerrado en llaves `{}`. (Aquí no se puede poner encerrado en llaves porque se correría el código en lugar de mostrarlo.)

## Elementos de apoyo

Los elementos de apoyo son las preguntas, objetivos y puntos clave incluidos en los episodios.   

Guía para escribirlos:  
  - Intenta escribirlos antes de desarrollar el contenido del episodio para que te sirvan como guía en el desarrollo. Podrás ajustarlos después.
  - Haz que las preguntas, los objetivos y los puntos clave sean consistentes entre sí.
  
  - Las **preguntas** deben ser preguntas que se haría el estudiante.
  
  - Escribe los **objetivos** en términos de lo que el estudiante va a poder *hacer* y no en lo que va a *aprender*.
  - Un episodio debe tener entre 5 y 7 objetivos. Si tienen más considera separarlo en más episodios.

  - En los **puntos clave** has un resumen muy breve de las partes más importantes aprendidas en el episodio.
  - Los puntos clave pueden estar escritos como breves respuestas a las preguntas.
  - Si en el episodio se enseñaron comandos o programas, menciónalos en los puntos clave.

También debes indicar cuánto dura la parte de enseñanza del episodio y cuánto la parte de ejercicios. La duración debe estar de acuerdo con la
carga de contenido.

## Formato de los encabezados y del texto

### Formato de los encabezados (El anterior es un encabezado nivel 2 y este es un encabezado nivel 3)

El título de la lección corresponde al mayor nivel de encabezado, el que se especifica con un gato `#`.
No debe haber ningún encabezado de este nivel en los episodios.  
Las secciones se deben delimitar con encabezados de nivel 2, es decir con doble gato `##`.

#### Subsecciones (Este es un encabezado nivel 4)

Y si hay subsecciones se deben poner con el nivel 3 (`###`) y dentro de ellas se puede usar el nivel 4 (`####`).
Es decir, que no debe haber saltos entre niveles de encabezados (p. ej. usar un nivel 4 despues de un nivel 2).  
Siempre deja un renglón vacío antes y después de cada encabezado.

### Formato del texto

Cada línea de texto debe ser de 100 caracteres máximo. Al terminar los 100 caracteres puedes pasar
a una siguiente línea, 
y aún así se va a ver como un párrafo normal.  
Para que se vea un salto de línea debes dejar dos espacios al final de la línea.

## Formato para insertar figuras

Todas las figuras deben de estar dentro de la carpeta `fig/` del repositorio y deben tener su nombre en formato `LL-EE-FF.png`
(Número de lección-Número de episodio-Número de figura dentro del episodio.png).  
Debes utilizar el siguiente código para insertar las figuras en el cuerpo del episodio:  
~~~
<a href="{{ page.root }}/fig/01-01-01.png">
  <img src="{{ page.root }}/fig/01-01-01.png" alt="Aquí va el texto que describe a la imagen." />
</a>
~~~
{:language-html}

Si no queda bien el tamaño de la figura se pueden incluir los parámetro `height` y `width` así:  
~~~
<a href="{{ page.root }}/fig/01-01-01.png">
  <img src="{{ page.root }}/fig/01-01-01.png" width="435" height="631" alt="Aquí va el texto que describe a la imagen." />
</a>
~~~
{:language-html}

### Accesibilidad de las imágenes

Las personas con discapacidades visuales pueden utilizar lectores de pantalla, éstos son programas que leen en voz alta el
contenido de una página. Para que las imágenes logren su objetivo cuando las utiliza alguien con un lector de pantalla deben
de estar descritas en el texto alternativo. Éste va en el parámetro `alt=` dentro del código con el que se inserta la imagen 
(como se ve en las cajas de código anteriores). 

- Cuando la imagen es **decorativa** el texto alternativo debe de estar vacío de
esta manera:`alt=""`, para que el lector de pantalla no lea nada, ya que en ausencia del parámetro `alt=` se leería el
nombre del archivo, lo cual no es útil. 
- El texto alternativo debe ser **breve** y enfocado al mensaje que se quiere dar con la imagen.
- No debe haber **pies de figura**.

Sigue las recomendaciones de las páginas [Accesible Images Best Practices](https://it.ucsf.edu/how-to/accessible-images-best-practices)
y [Avoid these common alt-text mistakes](https://bighack.org/avoid-these-mistakes-when-writing-alt-text-descriptions-for-images/) para aprender a escribir texto alternativo útil.

Para evaluar la accesibilidad de una página puedes utilizar la herramienta [WAVE](https://wave.webaim.org/).

## Formato de las cajas de código

Para insertar una caja de código usa el siguiente código y modifícalo según el tipo de caja que necesites.
~~~
~~~
Aquí va el código.
~~~
{: .aqui-va-el-tipo-de-caja}
~~~
{: .source}

Para una caja sencilla utiliza: `{: .source}`
Para una caja de *Output* utiliza: `{: .output}`
Para una caja de *Error* utiliza: `{: .error}`
Para que tenga el formato de sintaxis de algún lenguage de programación y el nombre del lenguage
en la cajita usa el nombre del lenguage así:
  `{: .laguage-html}`
  `{: .laguage-bash}`
  `{: .laguage-make}`
  `{: .laguage-matlab}`
  `{: .laguage-python}`
  `{: .laguage-r}`
  `{: .laguage-sql}`
  
## Formato para las cajas especiales

Existen muchos tipo de cajas para contenido especial. Según el tipo de caja va a tener un color y un símbolo
diferente.

Para insertar una caja todo el contenido debe de tener un símbolo `>` antes de cada línea y el título
debe tener `##`. Debe haber líneas vacías entre la línea del título y el texto, y entre el texto y las 
cajas de código. El tipo de caja se especifica al final. Así:  

~~~
> ## Título de la caja
>
> texto
> texto
> texto
>
> ~~~
> código
> ~~~
> {: .tipo-de-caja-de-codigo}
{: .tipo-de-caja-especial}
~~~
{: .source}  

Los tipos de caja son los siguientes:  

> ## Notas extra o comentarios
>
> El tipo de esta caja es: `{: .callout}`
{: .callout}  
  
> ## Lista de tareas
>
> El tipo de esta caja es: `{: .checklist}`
{: .checklist}  

> ## Discusiones
>
> El tipo de esta caja es: `{: .discussion}`
{: .discussion}   

> ## Puntos clave
>
> El tipo de esta caja es: `{: .keypoints}`
{: .keypoints}  

> ## Objetivos
>
> El tipo de esta caja es: `{: .objectives}`
{: .objectives}  

> ## Prerequisitos
>
> El tipo de esta caja es: `{: .prereq}`
{: .prereq}  

> ## Alguna cita interesante
>
> El tipo de esta caja es: `{: .testimonial}`
{: .testimonial}  

> ## Ejercicio 1: Título del ejercicio
> 
> Los ejercicios deben tener número de ejercicio y título.
> El tipo de esta caja es: `{: .challenge}`
> 
> > ## Solución
> > 
> > Esta es la solución del ejercicio.
> > ~~~
> > Este es el código de la solución. El tipo de las cajas de solución es `{: .solution}`
> > ~~~
> > {: .source}
> > Para anidar una caja dentro de otra como en este caso el código es así:
> > ~~~
> > > ## Ejercicio 1: Título del ejercicio
> > > 
> > > Este es un ejercicio.
> > > 
> > > > ## Solución
> > > > 
> > > > Esta es la solución.
> > > {: .solution}
> > {: .challenge}
> > ~~~
> > {: .source}
> {: .solution}
{: .challenge}

{% include links.md %}

