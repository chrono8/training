**Name** 
homog_mo_GVE
**Description**
Wetterdatenplot f?r das Jahr 1991 der der Station Geneve-Cointrin ?stereich. 420m ?ber dem Meeresspiegel im Mitteland.
**Usage**
Chunk by Chunk
**Input**
Die Daten sind unter http://www.meteoschweiz.admin.ch/web/de/klima/klima_heute/homogene_reihen.html zu finden
**Output**
ein Plot
**Autor**
M.H.
*****

```{r}
setwd("C:/Users/Marianne/Desktop/Klimaprojekt")
```

```
```{r}
gve_wetter <- read.table (file= "homog_mo_gve.txt", header=TRUE, skip=27)
```

```{r}
monate<-c(1:12)
temp<-gve_wetter$Temperature[gve_wetter$Year==1991]

```

```{r}
monate_temp<-plot(monate, temp, type="b")


```
`

```{r}
boxplot(temp, add=TRUE)

```

