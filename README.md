# ACP Colores

## Integrantes
* Andres Campos
* Antelmo Rosendo
* Armando Ramos
* Carlos Garcia

## Descripción
Aplicación móvil que permitirá mostrar un conjunto de imágenes de muestra de colores disponibles para un ACP, así como los datos de contacto de la empresa

## Características
La aplicación contará con las siguientes pantallas:

1. Pantalla *Bienvenida*
  * Despliega un mensaje de bienvenida
  * Solamente se muestra la primera vez que el usuario instala la aplicación
  * Botón Aceptar permite ingresar a la aplicación

2. Pantalla *Listado de Colores*
  - Despliega los colores que se encuentran en el catálogo (Información devuelta por el web services)
  * Al seleccionar un elemento (hacer tap) se debe mostrar Pantalla _Detalle de color_
  * Debe contar con la opción **Filtrar** en base a `id_tipo` y `id_subtipo`

3. Pantalla *Detalle de color*
  - Despliega la información del color seleccionado
  - La pantalla debe mostrar imagen del color
  * Los campos son de solo lectura
  * Botón _Aceptar_ regresa a la pantalla anterior
    
4. Pantalla *Ejecutivos*
  - Despliega el listado de Ejecutivos (Información leída desde un archivo)
  * Si el campo es de tipo correo electrónico, debe permitir el envío de correo desde la aplicación

5. Pantalla *Créditos*
  - Debe mostrar la información de los integrantes del equipo

## Recursos
1. https://github.com/AFNetworking/AFNetworking
2. http://www.raywenderlich.com/59255/afnetworking-2-0-tutorial
3. https://guides.cocoapods.org/ (Si usan CocoaPods)
4. Web services a usar `http://alucomex.com/es/api`
  - El arreglo de _colores_ se encuentra en la llave `colores`
  - Los identificadores de la información de cada color son:
  ```
IdentifierKey = @"id_color";
NameKey = @"color";
TypeKey = @"id_tipo";
SubtypeKey = @"id_subtipo";
ImageKey = @"imagen_detalle";
ThumbnailKey = @"imagen";
WidthKey = @"ancho";
LongKey = @"largo";
CodeKey = @"codigo";
AluminiumThicknessKey = @"espesor_aluminio";
TotalThicknessKey = @"espesor_total";
PaintKey = @"pintura";
  ```
5. El archivo con la información de los Ejecutivos se encuentra en https://dl.dropboxusercontent.com/u/2550166/OfficesList.plist

## Recomendaciones
* Implementar un Singleton para el consumo del web services
* Para la lectura del archivo plist usar `-[NSArray arrayWithContentsOfFile:]`
