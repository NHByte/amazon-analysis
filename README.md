# Análisis Exploratorio de Compras en Amazon

## Descripción
Este proyecto analiza el catálogo de productos de Amazon, explorando:

- Categorías que generan más ventas
- Productos con mejor valoración
- Relación entre precio y rating
- Productos que concentran más reseñas
- Marcas dominantes por categoría

El objetivo es extraer insights de negocio útiles para marketing, promociones y gestión de inventario.

## Dataset
- Fuente: Amazon (dataset propio recopilado de la plataforma)
- Columnas clave: 
  - `product_id`: ID del producto
  - `product_name`: Nombre del producto
  - `category`: Categoría completa
  - `discounted_price`: Precio con descuento
  - `actual_price`: Precio original antes del descuento
  - `discount_percentage`: Porcentaje de descuento
  - `rating`: Calificación del producto
  - `rating_count`: Número de valoraciones
  - `about_product`: Detalles del producto
  - `user_id`: ID de usuario que dejó la reseña
  - `user_name`: Nombre del usuario
  - `review_id`: ID de la reseña
  - `review_title`: Título de la reseña
  - `review_content`: Contenido de la reseña
  - `img_link`: Imagen del producto
  - `product_link`: URL del producto

## Limpieza de datos
- Relleno de valores faltantes en `rating_count` con 0
- Eliminación de símbolos y conversión de columnas numéricas:
  - `discounted_price`, `actual_price`, `discount_percentage`, `rating`, `rating_count`
- Separación de categorías en niveles (`category_level_1`, `category_level_2`, ...)
- Extracción de marca automáticamente desde `product_name` (algunos nombres pueden no ser exactos)

## Análisis
### Categorías con más ventas
- La categoría **Electrónica** representa ~36% de los productos, seguida de **Computers & Accessories** (~30%).  
- Insights: Priorizar estas categorías en promociones y campañas de ventas.

### Productos mejor valorados
- Trípodes para móviles, cables de carga de Apple y accesorios electrónicos son los productos top en **weighted score**.  
- Combinan alta calificación y número de reseñas, indicando productos de alta aceptación por los usuarios.

### Relación precio vs rating
- No existe relación significativa entre precio y valoración.  
- Productos económicos y caros mantienen ratings altos (4–5 estrellas).  
- Insights: La percepción de calidad no depende del precio.

### Productos con más reseñas
- Trípodes, cables Apple y accesorios dominan el ranking de reseñas.  
- Insights de negocio: Altas reseñas = alto interés del consumidor → útil para marketing y promociones.

### Marcas dominantes por categoría
- Las marcas fueron extraídas del nombre del producto; puede haber imprecisiones ⚠️.  
- Permite identificar líderes por categoría y planificar estrategias de inventario o marketing.

## Cómo usar
1. Clonar el repositorio
2. Abrir `Amazon_EDA.ipynb`
3. Ejecutar todas las celdas para reproducir el análisis y gráficos
4. Explorar los insights y tomar decisiones estratégicas basadas en ellos

