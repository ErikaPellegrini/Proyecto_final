# Entrega Final de Data Science: Análisis exploratorios de Glaciares en Los Andes Desérticos.
Bienvenidas a la última versión del proyecto final realizado por Brenda Gonzalez y Erika Pellegrini. Cualquier sugerencia es bien recibida.

## Introducción
Este trabajo busca posibilitar el desarrollo de herramientas que faciliten y mejoren el análisis de datos provenientes de geoformas glaciares y periglaciares; contribuyendo a la disponibilidad de información precisa y relevante. Los glaciares son cuerpos dinámicos, con variaciones temporales a corto y mediano plazo, lo que los vuelven muy vulnerables a la pérdida de masa producto del aumento de la temperatura a nivel global. Al ser importantes reservorios de agua dulce, se espera aportar a la toma de decisiones en políticas de conservación y gestión de recursos hídricos lo cual es de vital importancia en un contexto de cambio climático.

En particular, el  proyecto está enfocado en el análisis de datos del Inventario Nacional de Glaciares (ING) con el objetivo inicial de aplicar técnicas de Machine Learning para detectar patrones que permitan identificar patrones geoformas glaciares y periglaciares en la región de los Andes Desérticos en Argentina. Los Andes Desérticos engloban a las provincias de Salta, Jujuy, Tucumán, Catamarca, La Rioja y San Juan.

Si bien el objetivo de este trabajo busca explorar las posibilidades de clasificación automática utilizando técnicas de Machine Learning a partir de variables en el dataset seleccionado, como área, orientación, pendiente y otros atributos físicos de una región en particular. El proyecto brinda las bases para que, en el futuro, los modelos desarrollados puedan ser aplicados a geoformas glaciares y periglaciares de diferentes localizaciones. 

## Objetivo
- Realizar un análisis exploratorio de glaciares (GD), glaciares cubiertos (GC), glaciares de escombros(GE) y manchones de nieve (MN) presentes en la región de los Andes Desérticos con el fin de identificar patrones en relación con el tipo de geoforma, ubicación, área y altitud. Se buscará analizar las relaciones entre variables geográficas y morfológicas en función de cuencas hidrográficas, provincias y rangos altitudinales, entre otras.

- Predecir características glaciares no medidas, como la altura mínima o la clasificación primaria, a partir de variables morfológicas y geográficas observadas.

- Entender los controles ambientales que influyen en la distribución de los glaciares y geoformas relacionadas en la región, analizando su relación con variables como altitud, pendiente y ubicación geográfica.

- Grupo 7
- Integrantes: Brenda Gonzalez y Erika Pellegrini

## Dataset utilizado

- La página oficial del Inventario Nacional de Glaciares (ING) contiene el primer inventario generado (2018) y una actualización (2024). La elección del dataset llamado *glaciar_ing* se realizó en base al año en el que fueron obtenidos los datos, dandole prioridad a la información más actualizada. La región de los Andes Desérticos fue la única zona que actualizada en el 2024. Estos datos corresponden a las provincias de Salta, Jujuy, Catamarca, La Rioja, Tucumán y San Juan.
- link de acceso al dataset: https://www.glaciaresargentinos.gob.ar/
- Se utilizó el diccionario de datos que se encuentra en el link proporcionado junto con el dataset. Los puntos más importantes del diccionario se detallan en el apartado "Glosario" dentro de este readme.

## Estructura del repositorio

### Descripción de carpetas y archivos

- **glaciar_ing.csv**: Dataset original utilizado para el análisis de la pre-entrega 2.
- **Glaciares_final.csv**: Dataset original utilizado para el análisis de la pre-entrega 3.
- **pre_entrega_2.ipynb**: Script que realiza análisis exploratorio, limpieza y transformación de los datos.
- **pre_entrega_3.ipynb**: Script que aplica un modelo de aprendizaje supervisado.
- **pre_entrega_4.ipynb**: Script que aplica al análisis exploratorio de los datos y un modelo de aprendizaje no supervisado.
- **README.md**: Descripción general del proyecto.

  
## Metodología

1. **Carga y visualización de datos**  
Se importó el dataset en formato .csv desde GitHub y se realizó una inspección inicial para entender la estructura, la cantidad de datos y las características de los mismos.

2. **Análisis de valores nulos**  
Se identificaron y analizaron los features con valores faltantes, imputándose los datos mediante diversas estrategias que se analizaron para cada caso.

4. **Eliminación de columnas irrelevantes o redundantes**  
Se eliminaron features no informativos o que no aportaban valor al análisis posterior.

5. **Detección de outliers**  
Se utilizaron métodos estadísticos como el rango intercuartílico (IQR) para identificar valores atípicos en cada feature, luego se procedió a eliminar los outliers por el método del puntaje Z (z-score).

6. **Transformación de variables**  
Se aplicó la técnica de binning, al agrupar valores continuos en categorías ("bins")

7. **Análisis de correlación**  
El análisis de correlación se llevó a cabo por medio de una  matriz de correlación numérica y mediante observaciones gráficas.

8. **Visualización**  
Se realizaron diversos gráficos del dataset "limpio" para lograr una mejor representación y entendimiento de los datos.

9.  **Modelo supervisado**
Se aplicaron dos métodos de aprendizaje supervisado: Random Forest y K-Nearest Neighbors (KNN), con el objetivo de predecir la clasificación primaria y la altura mínima total de los glaciares.

10.  **Modelo no supervisado**
Se aplicaron dos métodos de aprendizaje no supervisado: K-means y DBSCAN, con el objetivo de grupos o clusters relevantes en los diferentes features y para los features "altura máxima total" y "Latitud".

## Herramientas utilizadas

Librerías:
- `pandas`  : Para la manipulación y análisis de datos.
- `numpy`   : Para operaciones numéricas y funciones matemáticas.
- `matplotlib` : Para la creación de gráficos y visualizaciones.
- `seaborn` : Para gráficos estadísticos y visualizaciones avanzadas.
- `scipy`   : Para funciones estadísticas.
- `scikit-learn` : Para procesamiento de datos.

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

- `0.` Incierto  
- `1.` Sábana de hielo continental  
- `2.` Campo de hielo  
- `3.` Calota de hielo
- `4.` Glaciar de descarga 
- `5.` Glaciar de valle
- `6.` Glaciar de montaña  
- `7.` Manchón de nieve p
- `4.` Glaciar de descargaermanente o glaciarete  
- `8.` Barrera de hielo  
- `9.` Glaciar de escombros  
- `10.` Corriente de hielo  

8. Origen GE
   
- `0.` Incierto
- `1.` Criogénico: aquellos glaciares de escombros sin relación actual con los
glaciares y generados a partir de taludes y canaletas nivo-detriticas. 
- `2.` Glacigénico: aquellos glaciares de escombros originados a partir de un
glaciar descubierto o cubierto.
- `3.` Combinado 1 y 2

9. Actividad del GE

- `0.` Incierto
- `1.` Activo: presenta evidencias de movimiento pendiente abajo y señales del
mismo en superficie. En general este tipo de glaciares tiene una topografía
superficial muy irregular y desarrollan pendientes frontales muy
pronunciadas (35°-45°).
- `2.` Inactivo: no presentan movimiento pendiente abajo, pero que todavía
contienen hielo.

10. Forma del GE

- `0.` Incierto  
- `1.` Lengua: largo del glaciar mayor que el ancho
- `2.` Lobado: ancho del glaciar mayor que el largo
- `3.` Espatulado
- `4.` Coalescente 
- `5.` Otras
  
11. Estructura _I

- `0.` Incierto  
- `1.` Unidad: formado por un único glaciar de escombros.
- `2.` Multiunidad: formado por varios glaciares de escombros, pueden ser
coalescentes o sobrepuestos.

12. Estructura II

- `0.` Incierto  
- `1.` Una raíz: una única fuente de alimentación.
- `2.`Multiraiz: un glaciar de escombros que se alimenta de varias fuentes de
alimentación o raíces, sea cual fuere su origen.

13. Longitud: coordenadas geográficas de cada polígono (obtenida a partir de
un centroide ubicado en el interior del mismo).

14. Latitud: coordenadas geográficas de cada polígono (obtenida a partir de un
centroide ubicado en el interior del mismo).

15. Área: área de cada polígono expresada en km2.

16. Largo_total: largo de cada unidad, considerando la línea de flujo más larga de
todo el glaciar, desde la zona más alta, atravesando la unidad hasta el frente de la
misma, siempre lo más perpendicular posible a las curvas de nivel. Se expresa en
metros (m).

17. H_max_total: Altura máxima total de la unidad. Se expresa en metros sobre el
nivel del mar (msnm).

18. H_med_total: Altura media total de la unidad. Se expresa en metros sobre el
nivel del mar (msnm).

19. H_min_total: Altura mínima total de la unidad Se expresa en metros sobre el
nivel del mar (msnm)

20. Pendiente: (Se expresa en grados).

21. Orientación: Correspondiente a los 8 puntos cardinales.

22. H_max_parcial: Altura máxima de los polígonos que conforman cada unidad (si
los hubiere) Se expresa en metros sobre el nivel del mar (msnm).

23. H_med_parcial: Altura media de los polígonos que conforman cada unidad (si
los hubiere) Se expresa en metros sobre el nivel del mar (msnm).

