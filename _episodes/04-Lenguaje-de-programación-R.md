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

## Ambiente de Cálculo
~~~
    > y <-c(1, 2, 3, 4, 5, 6, 7, 8, 9) #define el vector y 
    > y 
~~~
{: .language-r}

Y despliega lo siguiente:

~~~
    > [1] 1 2 3 4 5 6 7 8 9
~~~
{: .output}

~~~
    > m <-matrix(y, 3, 3) #define la matriz de 3x3
    > m
~~~
{: .language-r}

~~~
    >     [,1]    [,2]    [,3]
      [,1]  1       2       3
      [,2]  4       5       6
      [,3]  7       8       9
~~~
{: .output}

~~~
    > u<-matrix(1, 3, 1) #define la matriz u de 3x1
    > u
~~~
{: .language-r}

~~~
    >   [,1]
     [1,] 1
     [2,] 1
     [3,] 1
~~~
{: .output}

~~~
    > mean(y) #calcula la media de las entradas en el vector y
~~~
{: .language-r}

En la siguiente tabla se reportan los comandos para calcular otros estadísticos básicos.

|-------------------+--------------------------------------------------------------------|
|      length(y)    |               Número de entradas en el vector y                    |
|-------------------+--------------------------------------------------------------------|
|       sum(y)      |                   Suma de las entradas de y                        |
|-------------------+--------------------------------------------------------------------|
|      sort(y)      |                    Ordena de menor a mayor                         |
|-------------------+--------------------------------------------------------------------|
|   min(y), max(y)  |               Obtiene el mínimo y el máximo de y                   |
|-------------------+--------------------------------------------------------------------|
|       mean(y)     |                       Media del vector y                           |
|-------------------+--------------------------------------------------------------------|
|      median(y)    |                       Mediana del vector y                         |
|-------------------+--------------------------------------------------------------------|
|        sd(y)      |                 Desviación estándar del vector y                   |
|-------------------+--------------------------------------------------------------------|
|       var(y)      |                      Varianza del vector y                         |
|-------------------+--------------------------------------------------------------------|
|     cor(x, y)     |                     Correlación entre x, y                         |
|-------------------+--------------------------------------------------------------------|
|      cov(x, y)    |                      Covarianza entre x, y                         |
|-------------------+--------------------------------------------------------------------|


