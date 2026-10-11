# BreadCrumbs — Reporte de metadatos

#### Descargar el .zip en Kali, descomprimirlo, verificar las imágenes del archivo breadcrumbs y responder las Flags del reto.

![Contenido del archivo del reto](img/01-contenido-del-reto.png)
#### 1º Paso - Visualizar información

```
man exiftool 
```
*Buscar por GPS y fecha de captura*
#### 2º Paso - Comando de filtrado

```
exiftool -DateTimeOriginal -GPSPosition *
```

![Fecha y GPS de todas las fotografías](img/02-fechas-y-gps-de-todas-las-fotos.png)

#### 3º Paso - Comando GPS Latitud y Longitud

```
exiftool -GPSLatitude -GPSLongitude [nombre_archivo.jpg]
```

#### 4º Paso - Primera Flag

![Coordenadas de 20231026_175811.jpg](img/03-flag1-gps-175811.png)

```
40º29'32.5"N 3º52'36.2"W  - Las Rozas de Madrid
```
*Google Maps*

#### 5º Paso - Segunda Flag

![Coordenadas de 20231026_175818.jpg](img/04-flag2-gps-175818.png)

```
40º26'46.66"N 3º59'45.74"W - Calle Paraguay
```
*Google Maps*

#### 6º Paso - Tercera Flag

```
exiftool -DateTimeOriginal 20231026_201141.jpg
exiftool 20231026_201141.jpg
```
*Se usaron ambos comandos para la búsqueda de la fecha y hora exacta de la captura en 
AA:MM:DD HH:MM:SS.MS*

```
2023:10:26 20:11:45.382
```

![Fecha original de 20231026_201141.jpg](img/05-flag3-fecha-201141.png)
![Fecha con milisegundos](img/06-flag3-fecha-con-milisegundos.png)

#### Último paso - Cuarta Flag

![Coordenadas de 20231026_210927.jpg](img/07-flag4-gps-210927.png)

```
40º25'17.44"N 3º41'33.62"W - The Bridge | Digital Talent Accelerator
```
*Localización de la empresa donde tuvo su última sede*
