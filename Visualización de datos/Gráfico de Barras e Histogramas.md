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
ax.bar(x, y, width=1,edgecolor="white", linewidth=0.7)   

print('x:', x)
print('y:', y)
```
![Gráfico de Barras](https://github.com/Antchica/Python/blob/main/Imagenes/Varios-marcos.png)
plt.show()
```
