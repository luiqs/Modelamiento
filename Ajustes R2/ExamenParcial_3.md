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

La base de datos de la muestra, “Incedios”, tiene 9 variables de
estudio. A continuación se describen cada una de ellas:

-   Incendio: Es un tipo de variable binaria que toma los valores de 1
    (ocurrió al menos un incendio forestal durante el año en la zona de
    estudio) y 0 (no ocurrió ningún incendio forestal durante el año).
    La variable se presenta tanto númerica como nominal (los dos son
    categorias).
-   CalidadAire: Es el valor medio de la concentración de material
    particulado de 10 micras a lo largo del año de estudio.
-   Temperatura: Es la temperatura media anual de la zona de estudio.
-   Precipitación.Anual: Es la precipitación anual en cada zona.
-   Velocidad.Viento: Es la velocidad de viento anual en cada zona.
-   Humedad relativa: Es la humedad relativa anual en cada zona.
-   Extracción de oro: Indica si se han presentado casos o no, de
    extracción de oro (al igual que la variable incendio es binaria y
    presenta las categorias nominales y codificadas).

Tener en consideración que la desviación estándar poblacional de la
concentración de material particulado poblacional es de 2.1 y la
desviación estándar poblacional de la temperatura es 1.2.

De la base de datos Incendios y los datos brindados en el enunciado
anterior, calcule y discuta los resultados obtenidos a las siguientes
preguntas:

##### 1. Estime la proporcion poblacional de ocurrencia de incendios de la poblacion de estudio (Consejo: Utilice paquete DescTools). Adicionalmente, calcule los intervalos de confianza (asuma un nivel de confianza del 95%). **Interprete los resultados**.

##### 2 Estime la media poblacional para la variable “Calidad de Aire” (concentración de material particulado) y obtenga sus intervalos de confianza (asuma un nivel de confianza del 95%. Consejo: Utilice paquete DescTools). **Interprete los resultados**.

##### 3. Realice un diagrama de cajas para evaluar el comportamiento de la variable “CalidadAire” (calidad del aire medido como material particulado) en las zonas donde ocurren incendios y aquellas zonas donde no ocurren incendios (Consejo: Grafique un gráfico de boxplot, utilice tanto la variable “Estado” como “CalidadAire” para esta tarea). Calcule la media, mediana y desviacion estandar de la concentración de material particulado para cada uno de los grupos por separado.**Interprete los resultados**.

##### 4. Realizar un contraste de hipótesis adecuado para comprobar si es que las variables cuantitativas “calidad del aire” y “Temperatura” siguen o no siguen una distribución normal (nivel de significancia del 5%). **Gráfique para complementar los resultados e interprete**
