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


