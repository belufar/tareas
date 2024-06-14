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

7. Por consiguiente se realiza un ir y venir con GPT probando códigos, intentando solucionar errores y sus causas. Problemas que si me dispongo a enlistar temo que este readme se haga demasiado largo. A grandes rasgos, tal como imaginaba el shapefile era demasiado avanzado para mi escaso nivel en python. Tras varios intentos fallidos para conseguir el data frame con la información que estaba buscando visualizar, opté por un gráfico simple. 

    Se dejará en el archivo ipynb los varios intentos que se hizo para dejar en evidencia. Sin embargo al final del mismo se ve lo que buscaba mostrar. Este muestra primero un Data Frame con la lista de regiones y el país de origen de los migrantes más concentrados en dicha región, más su porcentaje respectivo. 

    Una vez con el data frame, se usa el código para graficarlo. Lo ideal hubiese sido ponerlo en un mapa de Chile, pero esto iba más allá de mis habilidades. 

8. Si algo aprendí en este proceso (y si es de utilidad para cualquiera que este leyendo esto en busca de guía) esque las tablas con "," y tildes requieren códigos específicos para que pandas/python puedan entenderlo. GPT sabrá ayudarlos si lo especifican. Adiconalmente, si trabajan en el archivo .ipynb en días distintos, puede que surjan errores, puede deberse a que deben volver a hacer el proceso de concectar su drive ('reproducir' el código de drive). 



