# Entrega Final de Data Science: Análisis exploratorios de Glaciares en Los Andes Desérticos.
Bienvenidas a la última versión del proyecto final realizado por Brenda Gonzalez y Erika Pellegrini. Cualquier sugerencia es bien recibida.

## Introducción

- A partir del dataset descargado del Inventario Nacional de Glaciares (ING) 

- con la finalidad de que los modelos generados a partir de ML puedan ser utilizados con datasets que involucren años consecutivos para poder desarrollar series de tiempo que permitan analizar el comportamiento de los glaciares argentinos a lo largo de los años a partir del cambio climático.
- link de acceso: https://www.glaciaresargentinos.gob.ar/
- Escribir una breve descripción del proyecto: qué problema se trabaja, en qué contexto se hace y qué tipo de técnicas de data science se aplican.

## Objetivo

Resumir en una o dos líneas cuál es el objetivo general del proyecto: predecir algo, segmentar clientes, entender un fenómeno, etc..

## Integrantes

Poner número de grupo y nombres de los integrantes.

## Dataset utilizado

- La elección del datasets se realizó en base al año en el que fueron obtenidos los datos, dandole prioridad a la información más actualizada. Por ese motivo fue que elegimos el área dónde se encuentra los Andes Desérticos. Los cuáles engloban a las provincias de Salta, Jujuy, Catamarca, La Rioja, Tucumán y San Juan. En estas provincias se pueden encontrar diferentes tipos de geoformas correspientes a las criósfera como:  
Indicar qué datos se usaron: nombre del dataset o fuente, link si corresponde, y si se usó algún diccionario de datos o referencia adicional.

## Estructura del repositorio

Hacer una breve lista de los principales archivos y carpetas del proyecto, por ejemplo: notebooks de limpieza, análisis exploratorio, modelado, carpeta de datasets, etc.

## Metodología

Escribir un resumen de los pasos: limpieza, exploración, modelado supervisado y no supervisado, y qué técnicas o modelos principales se usaron.

## Herramientas utilizadas

Acá listar las librerías principales de Python u otras herramientas que se usaron en el proyecto.

## Glosario de los features
A continuación se detallan los 37 campos que componen la base de datos.
1. Provincia
2. Cuenca
3. Subcuenca
4. Código cuenca
5. ID_local
6. Tipo_geoforma: esta columna agrupa a cada una de las geoformas inventariadas en base a su tipo principal.

Los tipos de geoforma pueden ser:

**GD-Glaciar descubierto**: cuerpo de hielo permanente generado sobre la superficie terrestre a partir de la compactación y recristalización de la nieve y/o hielo, sin cobertura detrítica significativa, que sea visible por períodos de al menos 2 años, con evidencias de movimiento por gravedad (grietas, ojivas, morenas medias), y de un área mayor o igual a 0,01 km2 (una hectárea).

**MN-Manchón de nieve/glaciarete**: pequeñas masas de nieve y hielo de forma indefinida. Se localizan generalmente en depresiones, lechos de ríos y pendientes protegidas.

**GC-Glaciar cubierto**: cuerpo de hielo permanente generado sobre la superficie terrestre a partir de la compactación y recristalización de la nieve y/o hielo, con una cobertura detrítica significativa, que sea visible por períodos de al menos 2 años, con evidencias de movimiento por gravedad (grietas, ojivas, morenas medias), y de un área mayor o igual a 0,01 km2 (una hectárea).

**GE-Glaciar de escombros**: cuerpo de detrito congelado y hielo, con evidencias de movimiento por acción de la gravedad y deformación plástica del permafrost, cuyo origen está relacionado con los procesos criogénicos asociados con suelo permanentemente congelado y con hielo subterráneo o con el hielo proveniente de glaciares descubiertos y cubiertos, y de un área mayor o igual que 0,01 km2 (una hectárea). Los glaciares de escombros se pueden clasificar por su grado de actividad en activos (GEA), inactivos (GEI) y fósiles (GEF).

**ND-No detectable**: masas de hielo identificadas en el primer inventario que disminuyeron significativamente su superficie o desaparecieron completamente. Estás áreas se caracterizan por ser susceptibles de volver a formar cuerpos de hielo/nieve perennes si las condiciones climáticas se tornan favorables. Esta categoría no estaba incluida en el primer ING.

7. Clasificación Primaria: basada en el documento “Illustrated GLIMS Glacier Classification Manual” (Rau et al., 2005) preparado por el grupo de expertos de
GLIMS http://www.glims.org/MapsAndDocs/assets/GLIMS_GlacierClassification-Manual_V1_2005-02-10.pdf

 - 0. Incierto
 - 1. Sábana de hielo continental
 - 2. Campo de hielo
 - 3. Calota de hielo
 - 4. Glaciar de descarga
 - 5. Glaciar de valle
 - 6. Glaciar de montaña:
 - 7. Manchón de nieve permanente o glaciarete
 - 8. Barrera de hielo
 - 9. Glaciar de escombros
 - 10. Corriente de hielo
  
- `0.` Incierto  
- `1.` Sábana de hielo continental  
- `2.` Campo de hielo  
- `3.` Calota de hielo  
- `4.` Glaciar de descarga  
- `5.` Glaciar de valle  
- `6.` Glaciar de montaña  
- `7.` Manchón de nieve permanente o glaciarete  
- `8.` Barrera de hielo  
- `9.` Glaciar de escombros  
- `10.` Corriente de hielo  

## Bibliografía
