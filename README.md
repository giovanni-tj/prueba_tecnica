# prueba_tecnica
Desarrollo de ETL mediante Azure Data Factory

Descripción de la solución: 
Para realizar la implementación del proceso se utilizo la plataforma de nube Azure, haciendo uso de las siguientes herramientas:

•	DataFactory

•	Synapse Analitycs

•	Blob Storage

•	SQL Database

![image](https://user-images.githubusercontent.com/51729393/193438478-8509cfd7-6dcf-4101-b391-dd0054996da6.png)

# Requerimiento y  reglas de negocio

1.	Modelo de Datos y DDL

Al ser un proceso ETL de solo extracción y carga sin requerir alguna transformación el modelo de datos mantendrá los mismos atributos tanto en origen como en destino.

![image](https://user-images.githubusercontent.com/51729393/193441007-4bb3fc4f-a068-4a43-971e-f0c39a381902.png)

![image](https://user-images.githubusercontent.com/51729393/193438405-da767ab8-7eb3-4c8b-b193-3fddeb613df7.png)
# Diagrama de Diseño
![image](https://user-images.githubusercontent.com/51729393/193438543-b213c661-9dcc-4e22-a5a4-d92d9c9c9bc1.png)

# Carga de información a una Base de Datos

El archivo us.csv fue cargado a Blob Storage.

<img width="1049" alt="image" src="https://user-images.githubusercontent.com/51729393/193440639-7f005ede-d726-49c9-a0b3-e40bd681c990.png">

Se crea la BD DBUS.

<img width="1049" alt="image" src="https://user-images.githubusercontent.com/51729393/193440606-6c739a1a-7504-4161-a2d0-30266ac75c35.png">

Mediante Data Factory se realiza la carga de información del archivo us.csv de Blob Storage a la BD BDUS de SQL Database.

<img width="1049" alt="image" src="https://user-images.githubusercontent.com/51729393/193440558-93954948-5af6-480f-aefe-e6da4a21d4a3.png">

Se realiza consulta de validacionón.

<img width="1118" alt="image" src="https://user-images.githubusercontent.com/51729393/193440485-dcdc34c1-b444-4ff1-aafe-5a5af3ab2899.png">

# Pipeline del Proceso.
<img width="1118" alt="image" src="https://user-images.githubusercontent.com/51729393/193440401-dd33d22d-8839-465d-9eed-632d398513cf.png">

Flujo de datos de la tabla origen al Datawarehouse y al archivo en formato Parquet.

<img width="1118" alt="image" src="https://user-images.githubusercontent.com/51729393/193440343-adb319d3-f562-467f-80dd-f168a38111c2.png">

 Ejecución del pipeline en Azure Data Factory.
 
<img width="1118" alt="image" src="https://user-images.githubusercontent.com/51729393/193439918-5e8bb8d7-6824-4a6c-ac15-c65c7abdede6.png">


Se realiza consulta de validación de carga en Azure Synapse Analitycs (Datawarehouse)

<img width="1118" alt="image" src="https://user-images.githubusercontent.com/51729393/193440299-bf1bd147-7e36-4ef4-876c-9f80110f94ec.png">

Validación de creación de archivo en Blob Storage.

<img width="1118" alt="image" src="https://user-images.githubusercontent.com/51729393/193439862-d68d55a4-3962-44cd-b296-40301ed2e422.png">






