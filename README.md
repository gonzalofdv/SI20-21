# SI20-21
Repositorio para las prácticas de la asignatura Sistemas Inteligentes

# Retroalimentación prácticas

## Práctica 1 partes I, II y III
<details><summary>Expandir</summary>

### Nota: 7
### Comentario:
Ej 3:
Faltan pruebas. Se piden pruebas también para el problema de los misioneros y para el puzle de 16.  Bien los comentarios y pruebas del puzle de 8

Además de incluir comentarios generales de los algoritmos hay que explicar los resultados obtenidos en las pruebas. Por ejemplo, ¿ breadth_first_tree_search(Ocho_Puzzle((2, 8, 3, 1, 6, 4, 7, 0, 5))).solution()   No termina porque es de los puzles que no tienen solución.

Hay que ser concreto y claro con los algoritmos y las pruebas.  Algunas ejecuciones no terminan y otras tardan mucho. La práctica consiste en conocer el comportamiento de los algoritmos y ser capaces de distinguir cuando va a terminar, aunque tarde mucho y cuando tenéis que pararlo porque sabes que no va a terminar.

Ej 4.  Incompleto. Falta 4.1 y las h del puzle de 16.

Ej 5. Incompleto. Se piden pruebas con búsqueda_coste_uniforme, busqueda_primero_el_mejor y búsqueda_a_estrella   à se prueban en el ej 6.

Ej 6. Muy bien organizadas las pruebas sistemáticas de todos los algoritmos. Habéis hecho todas las pruebas y rellenado la tabla pero no habéis escrito conclusiones ni comentarios que, como se dice al principio:  “Los comentarios razonados de los ejercicios son la parte más importante de esta práctica.”
</details>


## Práctica 1 parte IV
<details><summary>Expandir</summary>

### Nota: 9
### Comentario:
Habéis cumplido de sobra los objetivos de la práctica.

Cruzar el puente.   Bien la representación, bien las pruebas, 3 h’ diferentes con estudio de propiedades.  La resolución del problema para 10 personas no se realiza en tiempo razonable.

Se puede mejorar la comparativa con las soluciones de búsqueda ciega

Sokoban.  Es un problema difícil. La representación y carga de archivos si no la habéis hecho al 100% tenéis que citar la fuente. Aun así tiene mucho trabajo de comprensión del problema e interpretacion de resultados. Habéis trabajado bastante.   

Las conclusiones deberían estar más ligadas al objetivo de la práctica.
</details>

## Práctica 2
<details><summary>Expandir</summary>

### Nota: 8'5
### Comentario:
Bien la práctica en general.

Muy bien la resolución de los ejercicios. Bien las pruebas para determinar los mejores valores de los parámetros.

Los comentarios y el análisis de los resultados se pueden mejorar.	

Os ha faltado algún ejercicio para la parte 2.
</details>

## Práctica 3
<details><summary>Expandir</summary>

### Nota: 9'5
### Comentario:
Parte 1.  

·         Consulta 1:  Bien.  No comentada.

·         Consulta 2.  Bien. Bien la ordenación alfabética.

·         Consulta 3.   Bien.

·         Consulta 4/5:   Para quitar repetidos se usa DISTINCT en vez de agrupar que es muy ineficiente.  Como Spielberg ha dirigido distintos tipos de obras y solo se piden películas muy bien la selección de aquellas obras que sean instancia de película. Falta que puede ser instancia directa o instancia de alguna subclase.  Bien la ordenación de resultados.  

Sería:

?film wdt:P31/wdt:P279* wd:Q11424. # instancias de Film (directa o indirectamente)

?film wdt:P57 wd:Q8877. # con director Spielberg

 

·         Consulta 6.  Bien la cuenta de películas.  
En general puede pasar que no sea instancia directa de Ciencia Ficción. Para coger instancias directas e indirectas sería wdt:P136/wdt:P279*  (aunque en este caso no cambia el resultado).

Quedaría así:

SELECT (COUNT(DISTINCT ?film) AS ?numFilms)

WHERE {

  ?film wdt:P31/wdt:P279* wd:Q11424.    # instancias de Film (directa o indirectamente)

  ?film wdt:P57 wd:Q8877.               # con director Spielberg

  ?film wdt:P136/wdt:P279* wd:Q471839   # con genero science fiction film (directa o indir., en este caso da igual)

  SERVICE wikibase:label { bd:serviceParam wikibase:language "[AUTO_LANGUAGE],en". }

}

·         Consulta 7.  Muy bien el filter y la ordenación.  Mismo fallo de recorrer la jerarquía de subclases.

 

·         Parte 2: 2 consultas de Rolling Stones.  Muy bien. Bien el nivel y los comentarios.
</details>

## Práctica 4
<details><summary>Expandir</summary>

### Nota: 9
### Comentarios:
*Vacio*

### Información adicional:
Se realizó un torneo pacman en el que se enfrentaron los comportamientos del pacman de cada grupo con los fantasmas del resto, consiguiendo nuestro grupo la mayor puntuación y reflejando por tanto que se elaboraron las mejores reglas.

</details>


## Práctica 5
<details><summary>Expandir</summary>

### Nota: 9
### Comentarios:
Parte 1. Carga y limpieza de datos ok. Explicar el dataframe ok.

Análisis de los datos. Descripción de las variables algo breve. Bien el análisis de las distribuciones de cada una de las variables (medias, desviaciones típicas, rangos, ...) y las principales relaciones entre pares de variables. Falta el Diagrama de dispersión. Conviene pintar la matriz porque da mucha información.

Bien la selección de los clusters a 3. Bien justificado.

Parte 2. Análisis del error un tanto superficial.

No analizas las ventajas y desventajas de usar árboles de decisión en este problema concreto.

Parte 3. Bien.       

Se puede mejorar el análisis. No interpretas el significado de las variables.  Falta analizar el conjunto de datos con más profundidad.

Análisis del error bastante superficial
</details>
