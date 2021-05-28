Untitled
================

# Base de datos: Inundacion

En un estudio, se quiere analizar la potencial relación que existe entre
el numero de inundaciones anuales en diferentes zonas del lugar de
estudio y su relación con la temperatura y precipitación anual. Para
dicho objetivo se obtuvo una muestra aleatoria de 40 zonas de estudio
del lugar de estudio, obteniéndose la siguiente base de datos:

``` r
library(tidyverse)
```

    ## -- Attaching packages --------------------------------------------- tidyverse 1.3.0 --

    ## v ggplot2 3.3.3     v purrr   0.3.4
    ## v tibble  3.0.0     v dplyr   1.0.5
    ## v tidyr   1.0.2     v stringr 1.4.0
    ## v readr   1.3.1     v forcats 0.5.0

    ## -- Conflicts ------------------------------------------------ tidyverse_conflicts() --
    ## x dplyr::filter() masks stats::filter()
    ## x dplyr::lag()    masks stats::lag()

``` r
Inundacion <- read.csv("https://raw.githubusercontent.com/luiqs/Estadistica-Aplicada/main/PDB/Inundacion.csv")
```

La base de datos “Inundacion”, tiene 4 variables de estudio. A
continuación se describen cada una de ellas:

-   Inundaciones: Brinda el numero de inundaciones anuales en la zona de
    estudio.
-   Temperatura: Representa la temperatura anual promedio en la zona de
    estudio (medida en grados centígrados).
-   Precipitación: Representa la precipitación anual promedio en la zona
    de estudio (medida en “mm”).
-   Velocidad.Viento: Representa la velocidad del viento en Kimoletros
    por hora.
-   Zona.Sismica: Variable de tipo binaria, la cual nos indica si es o
    no es una zona sismica (tienen dos versiones de esta variable, tanto
    la categoria codificada, como la variable nominal).
-   CercaniaMar: Variable categórica que sirve de referencia para saber
    la cercanía al mar de la zona monitoreada.
-   Altitud: La altitud en metros sobre el nivel del mar.

De la base de datos “Inundacion” y del enunciado anterior, calcule y
discuta los resultados obtenidos a las siguientes preguntas:

##### 1. Calcule la media, mediana y desviacion estandar de temperaturas (Temperatura) de las zonas muestreadas en el estudio. Asi mismo, realice un histograma de la variable “Inundaciones” (o diagrama de barras, si considera a la variable cuantitativa discreta como categoria) y evalue cual es el numero de inundaciones con mayor cantidad de ocurrencias en las zonas evaluadas (calcular la moda). **Interprete ambos resultados**.

##### 2. Con las pruebas aprendidas hasta el momento (semana 3), evidenciar o no, si existe alguna relación entre las variables “Velocidad de viento” y “Altitud”. Calcule y gráfique para evidenciar la potencial relación entre las variables o la ausencia de relación. **Interprete los resultados**.

##### 3. Estime la varianza poblacional para la variable “Velocidad de Viento” y obtenga adicionalmente sus intervalos de confianza a un nivel de significancia del 5%. Consejo: Utilice paquete DescTools. **Interprete los resultados**.

##### 4. Realizar la prueba de hipótesis adecuada para comprobar si es que las variables cuantitativas “Temperatura” y “Velocidad de viento” tienen o no tienen una distribución normal (nivel de significancia del 5%). **Gráfique para complementar los resultados e interprete**
