# Análisis de la simulación de sorteos de la Copa Libertadores 2022.

El objetivo de este repositorio es analizar los posibles grupos en los que se ubicaría Universidad Católica en la Copa Libertadores 2022. El análisis realizado se encuentra en el archivo Análisis grupos Libertadores 2022.ipynb. 

Los datos se obtuvieron realizando más de 10.000 simulaciones de sorteos de la Copa Libertadores, utilizando la función sortear del archivo sorteo.py ubicado en el repositorio sorteo_libertadores. Cada fila de los datos corresponde a un equipo. Los datos tienen las siguientes columnas:

- **Bombo:** Bombo o bolillero en el que se encontraba el equipo. 
- **Equipo:** Nombre del equipo.
- **Pais:** País del que el equipo es originario. Los equipos provenientes de las fases previas tienen _fase previa_ como valor en este feature.
- **Grupo:** De A a H. Representa en qué grupo esta ubicado el equipo.
- **id_sorteo:** Este feature permite diferenciar los distintos sorteos simulados.

Inicialmente, los datos se ubican en la carpeta sorteos de este repositorio y cada simulación se encuentra en un archivo con el nombre sorteo+id_sorteo.csv. Por lo tanto, el primer paso en este análisis fue juntar los datos de todos los sorteos en un dataframe y exportarlos a un archivo .csv llamado sorteos.csv para no tener que repetir este paso debido a que tarda mucho en ejecutar.

