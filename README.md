# Análisis de la simulación de sorteos de la Copa Libertadores 2022.

El objetivo de este repositorio es analizar los posibles grupos en los que se ubicaría Universidad Católica (UC) en la Copa Libertadores 2022. El análisis realizado se encuentra en el archivo Análisis grupos Libertadores 2022.ipynb. 

Los datos se obtuvieron realizando más de 10.000 simulaciones de sorteos de la Copa Libertadores, utilizando la función sortear del archivo sorteo.py ubicado en el repositorio sorteo_libertadores. Cada fila de los datos corresponde a un equipo. Los datos tienen las siguientes columnas:

- **Bombo:** Bombo o bolillero en el que se encontraba el equipo. 
- **Equipo:** Nombre del equipo.
- **Pais:** País del que el equipo es originario. Los equipos provenientes de las fases previas tienen _fase previa_ como valor en este feature.
- **Grupo:** De A a H. Representa en qué grupo esta ubicado el equipo.
- **id_sorteo:** Este feature permite diferenciar los distintos sorteos simulados.

Inicialmente, los datos se ubican en la carpeta sorteos de este repositorio y cada simulación se encuentra en un archivo con el nombre sorteo+id_sorteo.csv. Por lo tanto, el primer paso en este análisis fue juntar los datos de todos los sorteos en un dataframe y exportarlos a un archivo .csv llamado sorteos.csv para no tener que repetir este paso debido a que tarda mucho en ejecutar.

Para hacer el análisis se filtraron los datos, para cada uno de los sorteos se escoge sólo el grupo de la Universidad Católica . El análisis contiene las siguientes secciones:

1. Distribución del grupo en el que se ubica la UC en los distintos sorteos.
2. Distribución de rivales de la UC de cada bombo.
  *Distribución por equipo y por país de los rivales de cada bombo.
  *Análisis condicional de la distribución de los rivales provenientes de los bombos 3 y 4 dependiendo del rival del bombo 1.
        - Si el rival del bombo 1 es brasileño.
        - Si el rival del bombo 1 es argentino.
        - Si el rival del bombo 1 es uruguayo.
3. Porcentaje de grupos con y sin equipos de Brasil y/o Argentina.
        - Grupos con y sin equipos brasileños.
        - Grupos con y sin equipos argentinos.
        - Grupos sin equipos brasileños ni equipos argentinos.
        - Grupos con dos equipos brasileños y un equipo argentino.
        - Grupos con dos equipos argentios y un equipo brasileño.
5. Grupo más repetido.
