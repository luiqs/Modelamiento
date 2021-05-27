Untitled
================

# Base de datos: Huella

En la ciudad de Arequipa se quiere analizar la influencia del consumo de
energía y el tamaño de las empresas en su generación de emisiones de
gases efecto invernadero. Para ello, se ha realizado un muestreo
aleatorio simple de 30 muestras en la ciudad. Se sabe que esta muestra
es representativa para cada una de los tipos de empresas que funcionan
en su ciudad en relación con su tamaño (Empresa chica, mediana, grande).

La base de datos obtenida, la pueden descargar:

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
Huella <- read.csv("https://raw.githubusercontent.com/luiqs/Estadistica-Aplicada/main/PDB/Huella.csv")
```

Laa base de datos “Huella”, tiene 4 variables de estudio. A continuación
se describen cada una de ellas:

-   Nombre: Variable de tipo nominal que representa el nombre de la
    empresa.
-   Huella.Carbono: Es el calculo de la huella de carbono, expresado en
    toneladas de CO2 equivalente (anual).
-   Consumo.Energia: Es el consumo de energía anual (expresado en
    MegaWatts)
-   TamañoEmpresa: Variable de tipo categórica que agrupa a las empresa
    según en numero de trabajadores (la tienen tanto como categoria
    númerica y con nombre nomimal).
-   Consumo.Agua: Es el consumo de agua anual (expresado en Toneladas al
    año)
-   Ganancias.Anuales: Son las ganancias anuales en dolares de las
    mineras.

De la base de datos “Huella” y del enunciado anterior, calcule y discuta
los resultados obtenidos a las siguientes preguntas:

##### 1. Calcule la media, mediana y desviacion estandar del cosumo de energia expresado en MegaWatts anuales (Consumo de Energia) para cada uno de los tipos de empresa segun su tamaño. Grafique las diferencias o similitudes con un grafico de BoxPlot o Grafico de Cajas. **Interprete los resultados obtenidos**.

##### 2. Con las pruebas aprendidas hasta el momento (semana 7), evidenciar o no, si existe alguna relación entre las variables “Huella de Carbono” y “Consumo de Energia”. Calcule y gráfique para evidenciar la potencial relación entre las variables o la ausencia de relación. **Interprete los resultados obtenidos**.

##### 3. Estime la media poblacional para la variable “Huella de Carbono” y obtenga adicionalmente sus intervalos de confianza a un nivel de significancia del 5%. Consejo: Utilice paquete DescTools. **Interprete los resultados obtenidos**.

##### 4. Realizar la prueba de hipótesis adecuada para comprobar si es que las variables cuantitativas “Ganancias Anuales” y “Huella de carbono” tienen o no tienen una distribución normal (nivel de significancia del 5%). **Gráfique para complementar los resultados e interprete**
