# Project: ETL



## Índice

1.[Descripción](#descripción)\
2.[Extracción de datos](#extracción)\
3.[Transformación](#transformación)\
4.[Carga de datos](#carga)


<a name="descripción"/>

## Descripción

En este proyecto, hemos llevado a cabo una ETL. Hemos extraido unos datos (Extracción), a continuación los hemos transfromado (Transformación) y, por último, los hemos cargado o inconrporado a una base de datos (Carga).

La temática escogida han sido las razas de perro, concretamente hemos recabado datos sobre algunas de las razas existentes  y hemos enriquecido la información con otros datos.

El proceso viene a continuación.

<a name="extracción"/>
 
## Extracción de datos.

En primer lugar mencionaremos las reglas establecidas:

- Los datos extraídos debían ser provenientes de al menos tres fuentes distintas.
- Los métodos de extracción empleados debían ser dos como mínimo.


**Estas son las tres fuentes de información que hemos empleado para elaborar este proyecto:**

<details>
<summary>Dataset Dogs  y Dataset dog/intelligence </summary>
<br>

 Juntamos un primer Dataset llamado Dogs con información física de las razas de perro con otro Dataset con información de la inteligencia del animal en función del tamaño.
 
</details>

<details>
<summary>PPP</summary>
<br>

Censo europeo de perros potencialmente peligrosos.
<br>
<br>

</details>

<details>
<summary>País</summary>
<br>

Listado de los perros más buscados por país. Web Scrapping de esta web: https://www.finder.com/most-popular-dog-breeds
<br>
<br>

</details>

<a name="transformación"/>

## Transformación de datos.

En primer lugar obtuvimos dos archivos CSV de Kaggle que cuadraban muy bien y las juntamos en una sóla relacionando ambas tablas con sus respectivas columnas "Breed" para enriquecer el primer dataset.

A continuación, mediante Google Dataset conseguimos otros CSv con datos referentes a los distintos perros potencialmente peligrosos establecidos como tal en Europa, y añadimos una nueva columna que nos dice cuál de las razas que tiene nuestro proyecto son potencialmente peligrosas o no.
	
Por último, hicimos Web Scrapping con Selenium para estraer una lista de países con la raza de perro más solicitada en cada país y los utilizamos para ñadir otra columna que nos dijera el país o los países donde esa raza de perro es la más demandada.

<a name="carga"/>

## Carga de los datos
	
Una vez finalizada la transformación de los datos, obtuvimos un único DataFrame que exportar a MySQL. Para ello, creamos la base de datos "dogs" y diseñamos su EERD correspondiente. Tras un hacer Forward Engineer creamos la tabla "dogs", en un principio vacía. Después, mediante SQLAlchemy realizamos la exportación y rellenamos dicha tabla, finalizando así el proceso de carga.
	






