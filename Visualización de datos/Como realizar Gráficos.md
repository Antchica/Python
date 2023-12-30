Empezamos cargando las librerías necesarias
``` python
import matplotlib.pyplot as plt
import numpy as np
```

1. Creamos una figura que es el elemento base sobre el que se construyen los gráficos en matplotlib
 ``` python
fig= plt.figure()
```
2. Marcos donde irá nuestro gráfico
```python
fig = plt.figure()
ax = fig.add_subplot(1,1,1) #nrows, ncols, index
```
3. Añadir un título a nuestra figura
 ```python
ax.set_title('Aquí va el título')
fig
```
![Marco con título](https://github.com/Antchica/Python/blob/main/Imagenes/Marco-con-titulo.png)

