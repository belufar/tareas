### Ficha Técnica

#### Descripción 

Este documento describe la codificación de las dimensiones y variables utilizadas en la base de datos de migrantes por región en Chile. La información fue obtenida del archivo `databaseregiones.csv`, el cual contiene datos sobre los porcentajes de migrantes de distintos países en cada región de Chile. Esta base de datos se hizo manualmente a través de los documentos emitidos por el Servicio Nacional de Migraciones. 

#### Variables Incorporadas

| Variable     | Descripción                                                                                       |
|--------------|---------------------------------------------------------------------------------------------------|
| `País`       | Indica el país de origen de los migrantes. Esta columna contiene los nombres de los países.       |
| `Tarapacá`   | Porcentaje de migrantes del país correspondiente que residen en la región de Tarapacá.            |
| `Arica y Parinacota` | Porcentaje de migrantes del país correspondiente que residen en la región de Arica y Parinacota. |
| `Antofagasta`| Porcentaje de migrantes del país correspondiente que residen en la región de Antofagasta.         |
| `Atacama`    | Porcentaje de migrantes del país correspondiente que residen en la región de Atacama.             |
| `Coquimbo`   | Porcentaje de migrantes del país correspondiente que residen en la región de Coquimbo.            |
| `Valparaíso` | Porcentaje de migrantes del país correspondiente que residen en la región de Valparaíso.          |
| `Metropolitana` | Porcentaje de migrantes del país correspondiente que residen en la región Metropolitana.       |
| `O'Higgins`  | Porcentaje de migrantes del país correspondiente que residen en la región de O'Higgins.           |
| `Maule`      | Porcentaje de migrantes del país correspondiente que residen en la región del Maule.              |
| `Ñuble`      | Porcentaje de migrantes del país correspondiente que residen en la región de Ñuble.               |
| `Biobío`     | Porcentaje de migrantes del país correspondiente que residen en la región del Biobío.             |
| `La Araucanía` | Porcentaje de migrantes del país correspondiente que residen en la región de La Araucanía.      |
| `Los Ríos`   | Porcentaje de migrantes del país correspondiente que residen en la región de Los Ríos.            |
| `Los Lagos`  | Porcentaje de migrantes del país correspondiente que residen en la región de Los Lagos.           |
| `Aysén`      | Porcentaje de migrantes del país correspondiente que residen en la región de Aysén.               |
| `Magallanes y La Antártica` | Porcentaje de migrantes del país correspondiente que residen en la región de Magallanes y La Antártica. |

#### Representación de las Variables

- **País**: Esta variable categórica indica el país de origen de los migrantes. Cada fila del DataFrame corresponde a un país específico.
- **Regiones**: Cada una de las columnas, excepto `País`, corresponde a una región de Chile y contiene datos porcentuales que indican el porcentaje de migrantes del país especificado que residen en esa región. 

#### Notas Adicionales

- Los porcentajes se indican en formato decimal (por ejemplo, 12.34% se representa como 12,34 en la base de datos).
- El análisis se realizó para identificar la nacionalidad con mayor porcentaje de migrantes en cada región, lo que permitió generar un resumen de la nacionalidad predominante por región.

  
