# Gráfico de Barras e Histogramas
- Los **gráficos de barras** son útiles para representar datos discretos o categóricos y comparar cantidades entre categorías diferentes.
- Los **histogramas** se utilizan para visualizar la distribución y la frecuencia de datos continuos, mostrando la concentración y la forma de la distribución.

## Gráfico de Barras
Para crear el gráfico de barras vamos a generar unos datos aleatorios
```python
# Datos
x = 0.5 + np.arange(5)
y = np.random.uniform(2, 7, len(x))

# Figura
fig, ax = plt.subplots(figsize=(8, 5))
```
Al gráfico de barras de las variables x e y, le podemos añadir otros parámetros opcionales como el grosor de las barras, el color de la línea de las barras
```python
ax.bar(x, y, width=1,edgecolor="black", linewidth=0.7)   

print('x:', x)
print('y:', y)
plt.show()
```
![Gráfico de Barras](https://github.com/Antchica/Python/blob/main/Imagenes/Gráfico%20de%20barras.png)

## Título del gráfico y etiquetas para cada barra
```python
# Título
ax.set_title('Gráfico de barras')

# Etiqueta en cada barra
xlabels=['1ra categoria', '2da categoria','3ra categoria','4ta categoria','5ta categoria']
ax.set_xticks(x)
ax.set_xticklabels(xlabels, rotation=90) #rotation para girar las categorías en vertical
fig
```
![Gráfico de Barras con título y etiquetas](https://github.com/Antchica/Python/blob/main/Imagenes/Gráfico%20de%20Barras%20con%20título%20y%20etiquetas.png)

## Histogramas
Para crear el histograma volvemos a crear unos datos aleatorios
```python
# Datos
x = 4 + np.random.normal(0, 1.5, 200)

# Figura
fig, ax = plt.subplots()

# Histograma
ax.hist(x, bins=8, linewidth=0.5, edgecolor="white") # bins son la cantidad de barras

plt.show()
```
![Histograma](https://github.com/Antchica/Python/blob/main/Imagenes/Gráfico%20de%20Barras%20con%20título%20y%20etiquetas.png)
