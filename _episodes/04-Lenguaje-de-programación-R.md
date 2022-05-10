---
title: "Introducción al lenguaje R"
teaching: 0
exercises: 0
questions:
- "Key question (FIXME)"
objectives:
- "First learning objective. (FIXME)"
keypoints:
- "First key point. Brief Answer to questions. (FIXME)"
---


## Comandos básicos

El lenguaje R es sensible a las may ́usculas: no es lo mismo “variable1” que “Variable1”

{% raw %}
    ~~~
    Para interrumpir un c ́alculo extenso, oprimir Esc.
    >q() #para salir de R
    >x<-5 #asigna el valor “5” a la variable x
    >ls() #da la lista de las variables, u objetos, definidos por el usuario
    >rm(“x”) #elimina la variable x
    >rm(list=ls()) #elimina todos los objetos definidos por el usuario
    >getwd() #muestra el directorio en uso>setwd(“/media/euba/ADATA UFD/Diplomado/Programas”)
    >#cambia el directorio en uso>dir() #muestra los archivos en el directorio en uso
    ~~~
    {: .laguage-r}
{% endraw %}

