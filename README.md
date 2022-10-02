# prueba_tecnica
Desarrollo de ETL mediante Azure Data Factory

Descripción de la solución: 
Para realizar la implementación del proceso se utilizo la plataforma de nube Azure, haciendo uso de las siguientes herramientas:
•	DataFactory
•	Synapse Analitycs
•	Blob Storage
•	SQL Database
![image](https://user-images.githubusercontent.com/51729393/193438315-651bf66f-6927-4dac-ad2c-2334182e90f3.png)

Requerimientos y reglas de negocio:

1.	Modelo de Datos y DDL

Al ser un proceso ETL de solo extracción y carga sin requerir alguna transformación el modelo de datos mantendrá los mismos atributos tanto en origen como en destino.
 

DDL Origen:
CREATE TABLE CUSTOMERS(
    first_name varchar(255),
    last_name varchar(255),
    company_name varchar(255),
    adress varchar(255),
    city varchar(255),
    country varchar(255),
    state varchar(255),
    zip varchar(255),
    phone1 varchar(255),
    phone2 varchar(255),
    email varchar(255),
    web varchar(255)
);

DDL Destino:
CREATE TABLE CUSTOMERS(
    first_name varchar(255),
    last_name varchar(255),
    company_name varchar(255),
    adress varchar(255),
    city varchar(255),
    country varchar(255),
    state varchar(255),
    zip varchar(255),
    phone1 varchar(255),
    phone2 varchar(255),
    email varchar(255),
    web varchar(255)
);

2.	Diagrama de Diseño.
















3.	Carga de información a una Base de Datos.

El archivo us.csv fue cargado a Blob Storage.

Se crea la BD DBUS.

 
Mediante Data Factory se realiza la carga de información del archivo us.csv de Blob Storage a la BD BDUS de SQL Database.

Se realiza consulta de validación.






4.	Pipeline del Proceso.

Flujo de datos de la tabla origen al Datawarehouse y al archivo en formato Parquet.






Se realiza consulta de validación de carga en el Datawarehouse.
![image](https://user-images.githubusercontent.com/51729393/193438342-b2601b99-4545-4dae-ac0f-e25c620a6573.png)


