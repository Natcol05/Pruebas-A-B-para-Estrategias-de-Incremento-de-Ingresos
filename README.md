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

En términos generales, se observó que al inicio de la prueba ambos grupos tenían unos ingresos más o menos similares, pero esto fue cambiando en el transcurso de los días. En esta medida los ingresos acumulados del grupo B parecen ser considerablemente más altos que los del grupo A. Sin embargo, fue necesario revisar la posibilidad de valores extremos en ciertos días, ya que aunque hay un crecimiento uniforme en casi toda la prueba, también hay algunos picos que podrían indicar un aumento en las ventas en momentos especificos o la existencia de algunos pedidos especialmente costosos, pero no habituales. (Para observar como se trataron los valores extremos, remitirse al proyecto).  

<p align="center">
  <img src="https://github.com/Natcol05/Pruebas-A-B-para-Estrategias-de-Incremento-de-Ingresos/blob/0947d6f0c665ea53780a460417865e850fa2d240/graphics/Ingreso_Acumulado.png" alt="Sample Image">
</p>

Ahora bien, en el caso de el comportamiento en el tamaño de los pedidos, la prueba acumulada fue bastante fluctuante, no se evidencia una estabilidad o patron claro, esto también se relacionaba a la presencia de valores extremos. Sin embargo, en términos generales, podría decirse que los usuarios del grupo B han hecho compras más grandes que los del grupo A, lo cual concuerda con el comportamiento de la métrica anterior.

<p align="center">
  <img src="https://github.com/Natcol05/Pruebas-A-B-para-Estrategias-de-Incremento-de-Ingresos/blob/9964b4cc6f752579e76f2117c19795667f88790a/graphics/Tama%C3%B1o%20promedio%20de%20pedido.png" alt="Sample Image">
</p>

Finalmente, respecto a la tasa de conversión, solo al principio de la prueba se observa un mejor comportamiento para el grupo A, pero de manera temprana se identiifica un claro crecimiento en la tasa de conversión para el grupo B, lo cual sería un buen indicador. 

<p align="center">
  <img src="https://github.com/Natcol05/Pruebas-A-B-para-Estrategias-de-Incremento-de-Ingresos/blob/6402a9f27b666cc2c20ba6507822c01572c8e7b9/graphics/Diferencia%20en%20tasas%20de%20conversi%C3%B3n.png" alt="Sample Image">
</p>

**Conclusiones Generales:**

* De acuerdo a los indicadores RICE y ICE, estas son las estrategias que se consideran más relevantes por su posible eficacia:
1. agregar un formato de suscripción a todas las páginas principales, para compilar una lista de correos electronicos
2. lanzar una campaña que ofrezca a los usuarios descuentos en sus cumpleaños
3. agregar dos canales para atraer tráico de usuarios, para obtener un incremento del 30%
4. mostrar anuncios con ofertas y ventas actuales en la página principal, para aumentar la conversión

* A lo largo de la prueba se observa un comportamiento favorable del grupo B, en comparación con el grupo A, aunque se observaron valores extremos, se calculó la significancia estadistica de los datos brutos y filtrados para obtener conclusiones más certeras.  

* En el caso de la métrica de conversión, la significancia estadistica de los datos brutos indican que existe una diferencia importante entre el grupo A y B y que B tiene un rendimiento 13.8% mejor que el del grupo A. Ahora bien, luego de filtrar los datos, los resultados de la significancia estadistica reconfirman lo anterior, pero indican que el grupo B tiene un comportamiento 18,6% mejor que el del grupo A. 

* En cuanto al tamaño promedio de los pedidos, los datos indicarian que tanto con los datos filtrados como brutos, no existe una diferencia entre los grupos, pero en ambos casos el grupo B tiene un comportamiento significativamente mejor que el grupo A: 25% en el caso de los datos brutos y 56% en el caso de los datos filtrados. Habiendo tratado esto, también se podría afirmar que el ingreso promedio de los usuarios es mayor en el grupo B que en el grupo A. 

* Se concluye que se puede terminar con la prueba, llegando a la conclusión de que el comportamiento del grupo B es considerablemente mejor en todas las métricas que el del grupo A. 

