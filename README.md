#Crear bases de datos
Create database Trabajo1
#Usar base de datos
use trabajo1;
#Crear tabla
create table tienda1(
    -> id int,
    -> Producto varchar(30),
    -> Valor float,
    -> Camtidad INT,
    -> Descripcion Varchar(50));
    
#Insertar valores
INSERT INTO tienda1 VALUES ('1','pan','500','5','Pan de trigo');

INSERT INTO tienda1 VALUES ('2','huevo','600','8','huevos criollos');

INSERT INTO tienda1 VALUES ('3','arroz','3000','1','Arroz Diana')

alter table tienda1 change column fecha fecha_de_compra date;

alter table tienda1 add column Marca varchar(30);

update tienda1 set fecha_de_compra = '2025-03-17' where id = 2;

update tienda1 set fecha_de_compra = '2025-03-25' where id = 3;

update tienda1 set Marca = 'Kikes' where id = 2;

update tienda1 set Marca ='Diana' where id = 3;

update tienda1 set Marca = 'Bimbo' where id = 1;



# Consultas con las condicionales

SELECT * FROM Tienda1 WHERE Camtidad = 5 and Marca = "Bimbo";
SELECT * FROM Tienda1 WHERE Valor < 1000 and Marca = "Kikes";
SELECT * FROM Tienda1 WHERE Valor > 600 and fecha_de_compra < "2025-03-26";
SELECT * FROM Tienda1 WHERE Valor < 600 and fecha_de_compra > "2025-03-17";


