# Paso a paso

1. Se seleccionaron los datos desde la página de [Servicio Nacional de Migraciones](https://serviciomigraciones.cl). Allí, se decidió en base a lo que queríamos comunicar, que es el movimiento demográfico de los extranjeros en Chile. Sus motivaciones para migrar, estudios, situación actual (laboral y económica) y la percepción que tenían de su recibimiento aquí. Esos datos fueron traspasados a una base de datos propia en formato excel. 

1. Al observar la tabla, llama la atención el movimiento de los migrantes a través de las distintas regiones de Chile. Esto nos ayudaría a responder las preguntas: ¿Cómo se distribuyen los inmigrantes en Chile? ¿Que nacionalidad se concentra más en cada una de ellas? ¿Existe una tendencia entre norte, centro y sur? 

1. Se procede a utilizar Colab para convertir la tabla en CSV. Por sugerencia de la IA de Colab, agrego el código:

----------


df = pd.read_csv(file_path, sep=',', encoding='utf-8')

------

Debido a que mi base de datos está con decimales expresados con coma. 

4. Colab continuaba arrojando error. Consulté con chat gpt adjuntandole mi csv y el error, me adjuntó el siguiente código: 
----

import pandas as pd

file_path = '/content/drive/My Drive/GRAFICA/1306/databaseregiones.csv'

df = pd.read_csv(file_path, sep=';', encoding='utf-8')
print(df.head())
print(df.shape)

-----


Con eso el error se solucionó. Su comentario apuntaba a: "Leer el archivo utilizando ';' como delimitador"

5. En este punto su servidora se encuentra perdida sobre cómo proseguir. Por lo que hacemos buen uso de mi querido amigo Gerardo Patricio Tapia (GPT) para que me ayude y me guíe en el proceso. Le comparto las preguntas que busco responder a GPT y me sugiere realizar un mapa coroplético. Ante mi temor de que esto sea demasiado complicado de hacer con python (pues jamás lo he usado) GPT me calma y me sugiere proseguir argumentando que no tiene mayor dificultad si utilizamos librertias específicas. Se procede con la instalación de la librería "geopandas". 

6. Como esperaba, no era tan fácil. GPT me indica que necesito "shapefiles" de las regiones de Chile. Pero con una simple búsqueda encuentro que la maravillosa página de la [Biblioteca del Congreso Nacional](https://www.bcn.cl/siit/mapas_vectoriales) cuenta con mapas vectoriales y shapefiles. Se procede a descargar la división regional. 




