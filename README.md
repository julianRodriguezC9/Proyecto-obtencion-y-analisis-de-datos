# Proyecto obtencion y analisis de datos



## **Resumen**
El objetivo principal de este proyecto fue realizar un análisis detallado de los productos de 5 tiendas de indumentaria, utilizando técnicas de web scraping para recolectar los datos, transformarlos y analizarlos en Power BI. El análisis permitió obtener información clave sobre el inventario de productos, precios, tendencias y comparación entre las tiendas.

## **Abstract**

The main objective of this project was to conduct a detailed analysis of the products from 5 clothing stores, using web scraping techniques to collect the data, transform it, and analyze it in Power BI. The analysis provided key insights into product inventory, pricing, trends, and comparisons between the stores.
## **Tecnologías Utilizadas**

- **Python**: Lenguaje de programación principal para el proyecto.
- **BeautifulSoup**: Librería de Python para analizar HTML y realizar scraping.
- **Requests**: Librería de Python para realizar solicitudes HTTP y obtener páginas web.
- **Power BI**: Software utilizado para la transformacion y visualizacion de los datos.
- **Pandas**: Librería de Python para la manipulación de datos.
- **Jupyter Notebooks**: Entorno interactivo para analizar y visualizar datos.
- **DevTools del Navegador**: Herramientas para analizar el tráfico de red del sitio web objetivo.

## **Desarrollo**
El proyecto comenzó con la selección de las Tiendas. Se seleccionaron 5 tiendas de indumentaria online, dos de ellas relevantes en el mercado nacional e internacion (Montagne y Adidas), y las otras tres restantes constituidas por PyMEs de alcance nacional y regional (Colmo, Dala, KabraKuervo) . Estas tiendas fueron elegidas por su popularidad y la variedad de productos que ofrecen. Los sitios web seleccionados incluyen tanto grandes cadenas de ropa como tiendas boutique.

Se utilizó Python junto con la libreria BeautifulSoup para realizar el web scraping. Esto permitió acceder a las páginas web de cada tienda y extraer información relevante como:

- **ID del producto**

- **Nombre del producto**

- **Descripción del producto**

- **Precio**

- **Categoría (ropa, calzado, accesorios)**




### Proceso de Extracción:

Se estableció un proceso automatizado para extraer los datos de manera eficiente desde las páginas de productos de las tiendas, asegurando que la recolección fuera precisa y estuviera actualizada.



### Transformación de Datos: 

Una vez recolectados los datos, se importaron a Power Query en Power BI, donde se realizaron varias transformaciones, siguiendo el siguiente orden:

- **Limpieza de datos**: Se verifico si habia registros  registros incompletos, duplicados o errores en los datos extraídos. Como este no fue el caso, se continuo con el paso siguiente.

- **Normalización de categorías**: Las categorias de los productos habian sido estandarizadas en el entorno de Jupyter.

- **Creación de nuevas columnas**: Se añadieron columnas adicionales para análisis, como la ponderacion de cada producto de acuerdo con la varianza de la tienda.


### Análisis de los Datos en Power BI:

Análisis de Precios: Se realizó un análisis comparativo entre las tiendas, identificando las diferencias de precios para productos similares, lo que permitió obtener una visión de las estrategias de precios de las tiendas.

Tendencias de Productos: Se analizaron los precios de las tiendas y sus promedios: Media Aritmetica, Media Recortada y Media Ponderada (con la distribucion normal o Gaussiana)

Visualización de Datos: Se crearon paneles interactivos en Power BI con gráficos de barras, graficos de pastel (pie chart) para facilitar la interpretación de los datos. Los paneles incluyeron:

Gráficos comparativos de precios por tienda

Distribución de productos por categoría


## **Dificultades y Desafios**
Durante el desarrollo del proyecto ocurrieron varios inconvenientes:

- **Diferentes estructuras HTML**: En cada pagina si bien habia similutes en la construccion, por tratarse de paginas de la misma categoria, cada una trataba la construccion de una manera totalmente distinta, separando los productos de maneras diversas, lo que me hizo mejorar la agilidad de lectura de archivos html.

- **Paginas en iteracion**: La tienda de Mountagne no tiene, como a diferencia de las otras, una forma de visualizar **TODOS** los productos, si no que los divide en varias categorias y dentro de cada categoria hay más categorias. Por ello se requirio automatizar el proceso de entrar en cada categoria y subcategoria.

- **Modularizacion y abstraccion**: Al ser varias tiendas y no una sola (como en un proyecto anterior) se requiere abstraer un los datos, las funciones y los elementos, de manera de tener un codigo limpio, legible y reutilizable (mucho muy importante) ya que trae muchas ventajas como: Escalabilidad, facilitacion de debug y testing, codigo ordenado, uso de buenas practicas de programación.

## **Resultados**
Los resultados arrojaron que:
- A pesar de la cantidad de algunas tiendas en productos de una misma categoria, otras tienen mucha mas variedad de productos lo que indica qué tienda se expande más hacia otros terrenos. 
  
- Depende de qué media se tome, algunas tiendas son mas caras que otras en sus productos y estas medias son validas dependiendo del contexto. Por ejemplo, la tienda de Mountagne tiene una media aritmetica de $133000  siendo que uno de sus productos vale al rededor de $373000

## **Conclusiones**
Este proyecto de análisis de datos proporcionó una visión detallada del comportamiento de 4 tiendas de indumentaria, a través del uso de técnicas de web scraping y la capacidad analítica de Power BI. Los resultados obtenidos permiten a las tiendas mejorar sus estrategias de precios y marketing, brindando una ventaja competitiva en el mercado de la moda.
