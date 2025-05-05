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
*Tipo_geoforma*: esta columna agrupa a cada una de las geoformas
inventariadas en base a su tipo principal. Los tipos de geoforma pueden ser:
*GD-Glaciar descubierto*: cuerpo de hielo permanente generado sobre la superficie
terrestre a partir de la compactación y recristalización de la nieve y/o hielo, sin
cobertura detrítica significativa, que sea visible por períodos de al menos 2 años, con
evidencias de movimiento por gravedad (grietas, ojivas, morenas medias), y de un área
mayor o igual a 0,01 km2
(una hectárea). En la actualización si bien se mantuvo la
forma de identificación en la base de datos en los análisis se incorporó el término hielo
descubierto para describir esta categoría.
MN-Manchón de nieve/glaciarete: pequeñas masas de nieve y hielo de forma
indefinida. Se localizan generalmente en depresiones, lechos de ríos y pendientes
protegidas. En general se desarrollan a partir de la nieve barrida por el viento,
avalanchas y/o varios años de fuertes acumulaciones. En general no presentan
patrones de flujo visibles, y existen al menos por dos años consecutivos. Los
manchones de nieve permanentes/glaciaretes son reservas significativas de agua en
estado sólido y por ello fueron incluidos en el inventario.
GC-Glaciar cubierto: cuerpo de hielo permanente generado sobre la superficie
terrestre a partir de la compactación y recristalización de la nieve y/o hielo, con una
cobertura detrítica significativa, que sea visible por períodos de al menos 2 años, con
evidencias de movimiento por gravedad (grietas, ojivas, morenas medias), y de un área
mayor o igual a 0,01 km2
(una hectárea). En la actualización si bien se mantuvo la
forma de identificación en la base de datos en los análisis se incorporó el término hielo
cubierto para describir esta categoría.
GE-Glaciar de escombros: cuerpo de detrito congelado y hielo, con evidencias de
movimiento por acción de la gravedad y deformación plástica del permafrost, cuyo
origen está relacionado con los procesos criogénicos asociados con suelo
permanentemente congelado y con hielo subterráneo o con el hielo proveniente de
glaciares descubiertos y cubiertos, y de un área mayor o igual que 0,01 km2
(una
hectárea). Los glaciares de escombros dependen fuertemente del aporte de detritos,
nieve y hielo.
Los glaciares de escombros se pueden clasificar por su grado de actividad en activos
(GEA), inactivos (GEI) y fósiles (GEF) (Haeberli, 1985; Ikeda, 2004). Los glaciares de
escombros activos presentan frentes abruptos (>35º) con lineamientos de flujo,
crestas y surcos longitudinales y transversales bien definidos. Una vez que dejan de
moverse se llaman inactivos y aparecen como geoformas colapsadas con menor
47
Andes Desérticos
pendiente en el frente (<35º), también puede aparecer cierta cobertura vegetal. El
cuerpo de sedimentos que permanece una vez que el hielo se ha derretido se llama
glaciar de escombros fósil (Barsch, 1978; Brenning, 2005; Trombotto Liaudat, 2002).
Esta última categoría no ha sido incluida en el inventario por no tener importancia
hidrológica.
GCGE-Glaciar cubierto con glaciar de escombros: en los Andes Centrales existen
numerosos casos en los que un sector de hielo cubierto por detritos se transforma
gradualmente en un glaciar de escombros. En general es muy difícil identificar y
determinar la posición del límite entre el hielo cubierto (ambiente glaciar) y el glaciar
de escombros glacigénico (ambiente periglacial) a partir de sensores remotos, en
particular si no se cuenta con información adicional proveniente de estudios detallados
de campo. Por ello, en las tareas de inventario se ha utilizado una categoría nueva
denominada glaciar cubierto con glaciar de escombros que incluye las porciones de
hielo cubierto junto con el glaciar de escombros que se desarrolla a sus costados o en
su porción terminal.
ND-No detectable: masas de hielo identificadas en el primer inventario que
disminuyeron significativamente su superficie o desaparecieron completamente. Estás
áreas se caracterizan por ser susceptibles de volver a formar cuerpos de hielo/nieve
perennes si las condiciones climáticas se tornan favorables. Esta categoría no estaba
incluida en el primer ING.
