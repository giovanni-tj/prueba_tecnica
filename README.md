# prueba_tecnica
Desarrollo de ETL mediante Azure Data Factory

Descripción de la solución: 
Para realizar la implementación del proceso se utilizo la plataforma de nube Azure, haciendo uso de las siguientes herramientas:
•	DataFactory
•	Synapse Analitycs
•	Blob Storage
•	SQL Database
![image](https://user-images.githubusercontent.com/51729393/193438478-8509cfd7-6dcf-4101-b391-dd0054996da6.png)

Requerimientos y reglas de negocio:

1.	Modelo de Datos y DDL

Al ser un proceso ETL de solo extracción y carga sin requerir alguna transformación el modelo de datos mantendrá los mismos atributos tanto en origen como en destino.
![image](https://user-images.githubusercontent.com/51729393/193438434-6a8334fb-d293-4fa2-aa60-ed4cea0a9997.png)
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

![image](https://user-images.githubusercontent.com/51729393/193438405-da767ab8-7eb3-4c8b-b193-3fddeb613df7.png)

