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

~~~
    Para interrumpir un c ́alculo extenso, oprimir Esc.
    > q() #para salir de R
    > x<-5 #asigna el valor “5” a la variable x
    > ls() #da la lista de las variables, u objetos, definidos por el usuario
    > rm(“x”) #elimina la variable x
    > rm(list=ls()) #elimina todos los objetos definidos por el usuario
    > getwd() #muestra el directorio en uso>setwd(“/media/euba/ADATA UFD/Diplomado/Programas”) #cambia el directorio en uso
    > dir() #muestra los archivos en el directorio en uso
    > history(10) #nos da los últimos 10 comandos ejecutados
    > savehistory(“borrar.txt”) #guarda la lista de comandos ejecutados en el archivo “borrar.txt”
    > loadhistory(“borrar.txt” ) #carga el archivo “borrar.txt”
~~~
{: .language-r}

R puede ejecutar un conjunto de instrucciones leyéndolas desde un archivo externo. Por ejemplo, considere el archivo Sumar.r  que se muestra a continuación:

~~~
    > #suma
    > a<-1
    > b<-2
    
    > print(a+b)
~~~
{: .language-r}

Para ejecutar el archivo “Sumar.r” se usa el comando:

~~~
    > source(“Sumar.r”)
~~~
{: .language-r}


