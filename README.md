# Rumores en Redes Sociales - PLN
En este proyecto se encuentra el código utilizado para predecir si
un comentario en redes sociales es etiquetado como rumor o no.
Se utilizó el modelo de *Logistic Regression* (Regresión Logística)
a fin de entrenar los valores.

## Limpieza de los datos
### Datos del Train
Se comenzó con la limpieza del archivo *Train* en donde se encontró
2 columnas con datos null que, casualmente, eran de las mismas filas.
Estos datos fueron eliminados ya que no presentan problema alguno
para el entrenamiento del modelo.\
Se notó que la columna topic presentaba más de 10 mil datos null,
entonces se decidió aplicar un método a fin de llenar estos datos
vacíos. El método utilizado fue el de la moda, cuya función de
llenado se basa en los datos que más aparecen en esa columna.
### Vectorización y entrenamiento del modelo
Se importó la librería *train_test_split* para dividir los datos
en entrenamiento y prueba. 90% fue destinado para entrenamiento.
Luego de separados los datos se los vectorizó utilizando 
*CountVectorizer* y se entrenó el modelo.
### Datos del Test
Se importó el archivo *Test* en otro data frame a fin de limpiar sus
datos. Se presentó en este solamente un par de datos null dentro de la
columna *topic* y al igual que en el anterior se volvió a aplicar el
método de la moda a fin de rellenar esos valores vacíos.
### Creación del archivo
Se creó el archivo de envío para evaluar la precisión del modelo
y el resultado fue el siguiente:
<img width="602" height="41" alt="image" src="https://github.com/user-attachments/assets/e56afc65-8d5a-40f5-aad9-f940dfe6220a" />
