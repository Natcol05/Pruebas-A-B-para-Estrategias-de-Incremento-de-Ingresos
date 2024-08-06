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

En términos generales, se observó que al inicio de la prueba ambos grupos tenían unos ingresos más o menos similares, pero esto fue cambiando en el transcurso de los días. Así, podría afirmarse que los ingresos acumulados del grupo B parecen ser considerablemente más altos que los del grupo A. Sin embargo, es necesario revisar la posibilidad de valores extremos en ciertos días, ya que aunque hay un crecimiento uniforme en casi toda la prueba, también hay algunos picos que podrían indicar un aumento en las ventas en momentos especificos o la existencia de algunos pedidos especialmente costosos, pero no habituales. 

<p align="center">
  <img src="https://github.com/Natcol05/Pruebas-A-B-para-Estrategias-de-Incremento-de-Ingresos/blob/0947d6f0c665ea53780a460417865e850fa2d240/graphics/Ingreso_Acumulado.png" alt="Sample Image">
</p>
