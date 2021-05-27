Aleatorio
================

# Base de datos: Incendios

Se quiere realizar un estudio para determinar la relación que existe
entre la ocurrencia de incendios forestales, la calidad del aire y la
temperatura. Para ello se ha determinado un área de estudio y se han
delimitado 120 zonas de estudio como la población. Para cumplir con los
objetivos, se han tomado los datos de 44 zonas especificas, obteniéndose
los siguientes resultados:

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
Incendios <- read.csv("https://raw.githubusercontent.com/luiqs/Estadistica-Aplicada/main/PDB/Incendios.csv")
```

La base de datos de la muestra, “Incedios”, tiene 4 variables de
estudio. A continuación se describen cada una de ellas:

-   Incendio: Es un tipo de variable binaria que toma los valores de 1
    (ocurrió al menos un incendio forestal durante el año en la zona de
    estudio) y 0 (no ocurrió ningún incendio forestal durante el año.
-   Estado: Es la variable Incendio pero sin codificar en números 1 y 0.
    Toma dos valores, Incendio, zonas donde hubo al menos un incendio al
    año y No Incendio, zonas donde no ocurrió ningún incendio durante el
    año de estudio.
-   CalidadAire: Es el valor medio de la concentración de material
    particulado de 10 micras a lo largo del año de estudio.
-   Temperatura: Es la temperatura media anual de la zona de estudio.

Tener en consideración que la desviación estándar poblacional de la
concentración de material particulado poblacional es de 2.1 y la
desviación estándar poblacional de la temperatura es 1.2.

De la base de datos Incendios y los datos brindados en el enunciado
anterior, calcule y discuta los resultados obtenidos a las siguientes
preguntas:

##### 1. Estime la proporcion poblacional de ocurrencia de incendios de la poblacion de estudio (Consejo: Utilice paquete DescTools). Adicionalmente, calcule los intervalos de confianza (asuma un nivel de confianza del 95%). **Interprete los resultados**.

##### 2 Estime la media poblacional para la variable “Calidad de Aire” (concentración de material particulado) y obtenga sus intervalos de confianza (asuma un nivel de confianza del 95%. Consejo: Utilice paquete DescTools). **Interprete los resultados**.

##### 3. Con las pruebas aprendidas hasta el momento (semana 7), evidenciar o no, si existe alguna relacion entre las variables “CalidadAire” y “Temperatura”. Calcule y gráfique para evidenciar la potencial relación entre las variables o la ausencia de relación. **Interprete los resultados**.

##### 4. Calcule usted si la media poblacional de la temperatura, para las zonas donde hay incidios versus las zonas donde no hay incendios es igual o diferente. Tip: Prueba t de Student. **Gráfique para complementar los resultados e interprete**
