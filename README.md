# Proyecto de Obtención y Análisis de Datos

## **Resumen**

El objetivo principal de este proyecto fue realizar un análisis detallado de los productos de tiendas de indumentaria, utilizando técnicas de web scraping para recolectar los datos, transformarlos y analizarlos en Power BI. El análisis permitió obtener información clave sobre el inventario de productos, precios, tendencias y comparación entre las tiendas.

## **Abstract**

The main objective of this project was to conduct a detailed analysis of the products from 4 clothing stores, using web scraping techniques to collect the data, transform it, and analyze it in Power BI. The analysis provided key insights into product inventory, pricing, trends, and comparisons between the stores.

## **Tecnologías Utilizadas**

- **Python**: Lenguaje de programación principal para el proyecto.
- **BeautifulSoup**: Librería de Python para analizar HTML y realizar scraping.
- **Requests**: Librería de Python para realizar solicitudes HTTP y obtener páginas web.
- **Power BI**: Software utilizado para la transformación y visualización de los datos.
- **Pandas**: Librería de Python para la manipulación de datos.
- **Jupyter Notebooks**: Entorno interactivo para analizar y visualizar datos.
- **DevTools del Navegador**: Herramientas para analizar el tráfico de red del sitio web objetivo.

## **Desarrollo**

El proyecto comenzó con la selección de las tiendas. Se seleccionaron 4 tiendas de indumentaria online, dos de ellas relevantes en el mercado nacional e internacional (Montagne y Adidas), y las otras dos restantes constituidas por PyMEs de alcance nacional y regional (Colmo, Dala, KabraKuervo). Estas tiendas fueron elegidas por su popularidad y la variedad de productos que ofrecen. Los sitios web seleccionados incluyen tanto grandes cadenas de ropa como tiendas boutique.

Se utilizó Python junto con la librería BeautifulSoup para realizar el web scraping. Esto permitió acceder a las páginas web de cada tienda y extraer información relevante como:

- **ID del producto**
- **Nombre del producto**
- **Descripción del producto**
- **Precio**


### Proceso de Extracción

Se estableció un proceso automatizado para extraer los datos de manera eficiente desde las páginas de productos de las tiendas, asegurando que la recolección fuera precisa y estuviera actualizada.

### Transformación de Datos

Una vez recolectados los datos, se importaron a Power Query en Power BI, donde se realizaron varias transformaciones, siguiendo el siguiente orden:

- **Limpieza de datos**: Se verificó si había registros incompletos, duplicados o errores en los datos extraídos. Como este no fue el caso, se continuó con el paso siguiente.
- **Normalización de categorías**: - En el entorno de Power BI se extrajeron los datos de categoria transformando los datos obtenidos .
- **Creación de nuevas columnas**: Se añadieron columnas adicionales para análisis, como la ponderación de cada producto de acuerdo con la varianza de la tienda.

### Análisis de los Datos en Power BI

- **Análisis de Precios**: Se realizó un análisis comparativo entre las tiendas, identificando las diferencias de precios para productos similares, lo que permitió obtener una visión de las estrategias de precios de las tiendas.
- **Tendencias de Productos**: Se analizaron los precios de las tiendas y sus promedios: Media Aritmética, Media Recortada y Media Ponderada (con la distribución normal o gaussiana).
- **Visualización de Datos**: Se crearon paneles interactivos en Power BI con gráficos de barras y gráficos de pastel (pie chart) para facilitar la interpretación de los datos. Los paneles incluyeron:
  - Gráficos comparativos de precios por tienda.
  - Distribución de productos por categoría.

## **Dificultades y Desafíos**

Durante el desarrollo del proyecto ocurrieron varios inconvenientes:

- **Diferentes estructuras HTML**: En cada página, si bien había similitudes en la construcción por tratarse de páginas de la misma categoría, cada una trataba la construcción de una manera totalmente distinta, separando los productos de formas diversas, lo que me hizo mejorar la agilidad de lectura de archivos HTML.
- **Páginas en iteración**: La tienda de Montagne no tiene, a diferencia de las otras, una forma de visualizar **TODOS** los productos, sino que los divide en varias categorías y dentro de cada categoría hay más subcategorías. Por ello, se requirió automatizar el proceso de entrar en cada categoría y subcategoría.
- **Modularización y abstracción**: Al ser varias tiendas y no una sola (como en un proyecto anterior), se requiere abstraer los datos, las funciones y los elementos, de manera que el código sea limpio, legible y reutilizable (muy importante), ya que esto trae muchas ventajas como: escalabilidad, facilitación del debugging y testing, código ordenado, y uso de buenas prácticas de programación.
- **Power BI**: Al ser una herramienta que nunca había usado, se me presentaron nuevos desafíos para entender el entorno, así como DAX (Data Analysis Expressions), el lenguaje que se utiliza para implementar nuevas medidas y análisis.

## **Resultados**

Los resultados arrojaron que:
- A pesar de la cantidad de productos de algunas tiendas en una misma categoría, otras tienen mucha más variedad de productos, lo que indica qué tienda se expande más hacia otros terrenos.
- Dependiendo de qué media se tome, algunas tiendas son más caras que otras en sus productos y estas medias son válidas dependiendo del contexto. Por ejemplo, la tienda de Montagne tiene una media aritmética de $133,000, siendo que uno de sus productos vale alrededor de $373,000.

## **Conclusiones**

Este proyecto de análisis de datos proporcionó una visión detallada del comportamiento de 4 tiendas de indumentaria, a través del uso de técnicas de web scraping y la capacidad analítica de Power BI. Los resultados obtenidos permiten a las tiendas mejorar sus estrategias de precios y marketing, brindando una ventaja competitiva en el mercado de la moda.
