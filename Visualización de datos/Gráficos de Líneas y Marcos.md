# Gráficos de Líneas y Marcos

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

4. Generar varios marcos en una misma figura
```python
fig = plt.figure()
for i in range(1, 5):
  ax = fig.add_subplot(2, 2, i)
```
![Varios-Marcos](https://github.com/Antchica/Python/blob/main/Imagenes/Varios-marcos.png)

## **EJEMPLO**

Generamos un conjunto de datos con 100 números distribuidos de 0 a 100 y creamos una función 'Y' que será el seno de 2 multiplicado por los valores de 'X'.
```python
x = np.linspace(0, 10, 100)
y = np.sin(2 * x)

# Figura
fig = plt.figure()

# Marco
ax = fig.add_subplot(1,1,1) #nrows, ncols, index

#Título
ax.set_title('Gráfico de la Función Y')

#Gráfico
ax.plot(x, y);
# Nombre para los ejes
ax.set_xlabel('Etiqueta para el eje X')
ax.set_ylabel('Etiqueta para el eje Y')
fig

# Grid
ax.grid(True)
fig
```
![Gráfico Función Y](https://github.com/Antchica/Python/blob/main/Imagenes/Gr%C3%A1fico%20funci%C3%B3n%20Y.png)

## MULTIPLES FUNCIONES
```python
# Datos
x = np.linspace(0, 2 * np.pi)
sin = np.sin(x)
cos = np.cos(x)

# Figura y Marco
fig, ax = plt.subplots()

#Gráficos
ax.plot(x, sin)
ax.plot(x, cos);
```
![Múltiples Funciones](https://github.com/Antchica/Python/blob/main/Imagenes/Multiples%20Funciones.png)

```python
# Añadir una leyenda
fig, ax = plt.subplots()
ax.plot(x, sin, label='sin')
ax.plot(x, cos, label='cos')
ax.legend()
fig;

# Ubicación de la leyenda
ax.legend(loc='center right')
fig
```

![Gráfico de Líneas con Leyenda ](https://github.com/Antchica/Python/blob/main/Imagenes/Grafico%20de%20Lineas%20con%20leyenda.png)

## Estilos
Podemos asignar diferentes estilos, es decir, cambiar el estilo de las letras,el marcador, el tipo de línea, los colores, etc. Con __linewidth__ cambiamos el grosor de la línea, con __marker__ para poner diferentes marcadores

```python
fig, ax = plt.subplots()

sin_style = dict(linewidth=5, color='darkorange')
cos_style = dict(marker='o', markerfacecolor='limegreen', color='darkgreen')

ax.plot(x, sin, label='$f_1(x) = sin(x)$', **sin_style)
ax.plot(x, cos, label='$f_2(x) = cos(x)$', **cos_style)

ax.legend()

fig;
```
![Estilos de Líneas ](https://github.com/Antchica/Python/blob/main/Imagenes/Grafico%20de%20Lineas%20con%20leyenda.png)
