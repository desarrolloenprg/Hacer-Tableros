PRIMERO SEGUIR LOS PASOS PARA HACER LOS TABLEROS
SEGUNDO EN PLAN DE SESION EN LA PESTAÑA INDICADORES, GENERAR LOS 2 INDICADORES SIGUIENDO EL CÓDIGO QUE ESTÁ AHI
Pasos a seguir para hacer los Tableros

El objetivo es generar los indicadores de avance de una sesión. Vamos a tomar como ejemplo la sesión “08-06”

1.	En documento de Avance de un paralelo, en este ejemplo el C: https://drive.google.com/open?id=1KH31s9nFVRfVbPT0PxYKutwEOLo-LmdkX8r1RhRaBDg  en pestaña “Avance gnral”, a partir de la última fila, crear 3 filas, copiando (pegando) las filas 4,5 y 6. Supongamos que se copiaron en las filas 43,44 y 45 
2.	 En estas nuevas filas, en “Fecha” escribir “08-06”, y en “Retos Objetivo” (B44) escribir lo que está en la pestaña “08-06” (que es la que contiene el avance al 08-06) celda B3
3.	En las nuevas filas, en las 44 y 45 de “Avance gnral” copiar las filas 3 y 4 de la pestaña “08-06” a partir de la columna C. Esta copia se hace con Pegar de solo valores
4.	Luego de la copia, en la celda C45 se debe reflejar una suma de los valores de la fila 45
5.	En la celda D48 de “Avance gnral” poner esta fórmula =TRANSPONER(D44:AH44), que transpone las filas 44 y 45 para que en vez de tener orientación horizontal tengan orientación vertical
6.	En documento Tableros (en pestaña “Alumnos” están todos los estudiantes de las 3 secciones): https://drive.google.com/open?id=1KH31s9nFVRfVbPT0PxYKutwEOLo-LmdkX8r1RhRaBDg en pestaña “Alumnos” crear dos nuevas columnas a la izquierda de la columna H. De manera que se crean dos columnas vacía H e I y las que anteriormente eran H e I, pasan a ser J y K
7.	Copiar en las columnas H e I del paralelo correspondiente, las columnas D y E de la pestaña “Avance gnral” de documento de Avance. Con esto estamos poniendo el Avance del paralelo C en Tableros
8.	En H2 de “Alumnos”, poner el contenido de celda B44 de “Avance gnral”
9.	En F2 de “Alumnos”, poner esta fórmula “=H2-AH2”, donde AH2  es la penúltima columna  de “Alumnos”
10.	En F3 poner la fórmula “=(H3-AH3)-F$2” donde AH3 es la penúltima columna de Alumnos. Repetir esta fórmula hacia abajo, hasta la última fila donde haya alumnos. Como estamos haciendo el ejemplo solo con el paralelo C, lo que aparezca en los paralelos A y B, ahora no es importante
11.	En G2 de “Alumnos”, poner la fórmula “=I2-AI2” donde AI2 es la última columna de “Alumnos”
12.	En G3 de “Alumnos” poner la fórmula “=I3-AI3” donde AI3 es la última columna. Repetir esta fórmula hacia abajo, hasta la última fila donde haya alumnos.
13.	En D3 de “Alumnos” poner esta fórmula “=SI(H3<(H$2*0.8),"Roja", "OK")” y repetirla hacia abajo para todos los alumnos, con esto se ve quien cumplió menos del 80% del objetivo, que se pinta de rojo para mostrarlo
14.	En E3 de “Alumnos’ poner esta fórmula “=Y((F3<0),(G3>0),(H3<I3))” y  repetirla hacia abajo para todos los alumnos, con esto se ve quien resolvió retos con desorden es decir dentro y fuera del objetivo a alcanzar en esa sección
15.	En documento Tableros (en pestaña “Entrenadores” están indicadores de avance por paralelo crear 4 columnas a la izquierda de la columna B, de manera que se crean las columnas B, C, D y E, y las anteriores B, C, D y E pasan a ser F, G, H e I
16.	Escribir en fila 1 “08-Jun-2017” y en fila 2 A, B, C y Total
17.	Poner en la fila B9 esta fórmula “=Alumnos!H2*0.8” que indica cual es le 80% del avance que se debía tener para esta sesión
18.	Para paralelo C, en D3, poner esta fórmula “=CONTAR.SI(Alumnos!H72:H102,">=156")/31” que indica el % de cumplimiento mayor o igual al objetivo 
a.	donde H72:H102 es el rango de filas en columna H donde se encuentran los estudiantes del paralelo C que es el que estamos haciendo
b.	156 es el contenido de la celda H2 de la pestaña de “Alumnos”.
c.	31 es el número de alumnos del paralelo C que se ve en la celda B102 de la pestaña de “Alumnos” para el paralelo C
19.	Para paralelo C, en D4, poner esta fórmula “=CONTAR.SI(Alumnos!H72:H102,"<124.80")/31” que indica el % de cumplimiento menor del 80% del objetivo
a.	donde H72:H102 es el rango de filas en columna H donde se encuentran los estudiantes del paralelo C que es el que estamos haciendo
b.	124.80 es el contenido de la celda B9 de la pestaña de “Entrenadores”.
c.	31 es el número de alumnos del paralelo C que se ve en la celda B102 de la pestaña de “Alumnos” para el paralelo C
20.	Para paralelo C, en D5, poner esta fórmula que indica el % de resolución de retos sobre el objetivo “=SUMA(Alumnos!I72:I102)/(31*Alumnos!H2)” 
a.	donde H72:H102 es el rango de filas en columna H donde se encuentran los estudiantes del paralelo C que es el que estamos haciendo
b.	31 es el número de alumnos del paralelo C que se ve en la celda B102 de la pestaña de “Alumnos” para el paralelo C
