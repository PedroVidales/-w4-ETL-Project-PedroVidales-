# Project: ETL



## Índice

1.[Descripción](#descripción)\
2.[Extracción y transformación de datos](#extracción)\
3.[Carga de datos](#carga)


<a name="descripción"/>

## Descripción

En este proyecto hemos obtenido datos con algunos de los métodos de estracción que hemos aprendido (Extracción), después hemos transfromado los datos y hemos aportado más información con ellos (Transformación) y, por último, los hemos cargado  a una base de datos en SQL (Carga).

La temática escogida han sido las razas de perro, concretamente hemos recabado información sobre algunas de las razas existentes  y hemos enriquecido la información con otros datos que hemos ido recabando.

El proceso viene a continuación.

<a name="extracción"/>
 
## Extracción de datos y transformación.

En primer lugar mencionaremos las reglas establecidas:

- Los datos extraídos debían obtenerse de al menos tres fuentes distintas.
- Los métodos de extracción empleados debían ser dos como mínimo.


**Estas son las tres fuentes de información que hemos empleado para elaborar este proyecto:**

<details>
<summary>Dataset Dogs  y Dataset dog/intelligence </summary>
<br>

 Juntamos un primer Dataset llamado Dogs con información física de las razas de perro (color de pelo, ojos, tamaño, enfermedades comunes...) con otro Dataset con información de la inteligencia del animal en función del tamaño (repeticiones mínimas para aprender un comando y repeticiones maximas para aprender un comando, relacionados con el tamaño de la raza), ambos de Kaggle.
 
 
</details>

<details>
<summary>PPP</summary>
<br>

Descargamos de Google Dataset, un CSV correspondiente al censo europeo de perros potencialmente peligrosos (PPP) y añadimos una columna nueva a nuestro DataFrame que nos indica cual de las razas de nuestra lista es PPP o no. 
<br>
<br>

</details>

<details>
<summary>País</summary>
<br>
Hacemos Web Scrapping con Selenium de esta web: https://www.finder.com/most-popular-dog-breeds . De esta obtenemos información sobre la raza más buscada en cada país y añadimos una nueva columna a nuestra tabla que nos diga por cada raza, si es la raza más común el algún país o países y en cuales.
 
<br>
<br>

</details>

<a name="transformación"/>


## Carga de los datos
	
Una vez finalizada la transformación de los datos, obtuvimos un único DataFrame que exportar a MySQL. Para ello, creamos la base de datos "dogs" y diseñamos su EERD correspondiente. Tras un hacer Forward Engineer creamos la tabla "dogs", en un principio vacía. Después, mediante SQLAlchemy realizamos la exportación y rellenamos dicha tabla, finalizando así el proceso de carga.

<a name="carga"/>
	






