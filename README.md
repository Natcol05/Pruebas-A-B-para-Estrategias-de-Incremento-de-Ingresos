<p align="center"><b>Implementación de Pruebas A/B para el Análisis de Estrategias de Incremento de Ingresos</b></p>

Este proyecto tiene como objetivo analizar estrategias para aumentar la atracción y conversión de usuarios, y con ello los ingresos de una tienda online. Se evaluan un conjunto de hipótesis a la luz de los indicadores RICE y ICE con la pretensión de determinar las estrategias más viables y posteriormente se aplica una prueba A/B en la que se busca estudiar la conversión.  

Estas son algunas de las librerías empleadas:

```python
import pandas as pd
import scipy.stats as stats
from scipy.stats import ttest_ind
from scipy.stats import levene
import numpy as np
from matplotlib import pyplot as plt
import seaborn as sb
```

En términos generales, se observó que al inicio de la prueba ambos grupos tenían unos ingresos más o menos similares, pero esto fue cambiando en el transcurso de los días. Así, podría afirmarse que los ingresos acumulados del grupo B parecen ser considerablemente más altos que los del grupo A. Sin embargo, fue necesario revisar la posibilidad de valores extremos en ciertos días, ya que aunque hay un crecimiento uniforme en casi toda la prueba, también hay algunos picos que podrían indicar un aumento en las ventas en momentos especificos o la existencia de algunos pedidos especialmente costosos, pero no habituales. (Para observar como se trataron lso valores extremos, remitirse al proyecto).  

<p align="center">
  <img src="https://github.com/Natcol05/Pruebas-A-B-para-Estrategias-de-Incremento-de-Ingresos/blob/0947d6f0c665ea53780a460417865e850fa2d240/graphics/Ingreso_Acumulado.png" alt="Sample Image">
</p>

Ahora bien, en el caso de el comportamiento de los pedidos, la prueba acumulada fue bastante fluctuante, no se evidencia una estabilidad o patron claro, esto también se relacionaba a la presencia de valores extremos. Sin embargo, en términos generales, podría decirse que el grupo B ha hecho compras más grandes que el grupo A, lo cual concuerda con el comportamiento de la métrica anterior.

<p align="center">
  <img src="https://github.com/Natcol05/Pruebas-A-B-para-Estrategias-de-Incremento-de-Ingresos/blob/9964b4cc6f752579e76f2117c19795667f88790a/graphics/Tama%C3%B1o%20promedio%20de%20pedido.png" alt="Sample Image">
</p>
