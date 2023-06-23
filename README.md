# Instalación de phpMyAdmin

## Instalación
1. Entrar a la pagina https://www.apachefriends.org/ .
2. Descargar ```XAMPP for Windows (8.2.4)```. 
![](https://github.com/DiegoJm10/Instalacion-de-base-de-datos/blob/main/DESCARGA%20DE%20XAMPP.png?raw=true)

![](https://github.com/DiegoJm10/Instalacion-de-base-de-datos/blob/main/XAMPP%20Installers%20and%20Downloads%20for%20Apache%20Friends%20-%20Google%20Chrome%2023_06_2023%2008_48_59%20a.%20m..png?raw=true)

3. Se les decargara un archivo llamado **xampp-windows-x64-8.2.4-0VS16-installer**.
![](https://github.com/DiegoJm10/Instalacion-de-base-de-datos/blob/main/ARCHIVO.png?raw=true)

4. Ejecutamos el archivo en modo administrador e installamos.

## Ejecutar 

1. Debemos abrir el programa llamado XAMPP.
2. Dentro de la interfaz nos vamos a la fila llamada **Mysql**.
3. Le damos doble click al boton **Admin**.

## Crear tabla 

Se va a crear una tabla con los siguentes cirterios: 

![](https://github.com/DiegoJm10/Instalacion-de-base-de-datos/blob/main/localhost%20_%20127.0.0.1%20_%20tamulbatm7%20_%20tamulba7%20_%20phpMyAdmin%205.2.1%20-%20Google%20Chrome%2016_06_2023%2008_50_24%20a.%20m..png?raw=true)


## Usar en node-red

Se colocara el bloque de Mysql y un bloque de función para obtener los datos con el siguente codigo. 

```
var query = "INSERT INTO `tamulba7`(`ID`, `FECHA`, `DEVICE`, `TEMPERATURA`, `AMPERAJE`) VALUES (NULL, current_timestamp(), '";
query = query+msg.payload.DEVICE + "','";
query = query+msg.payload.TEMPERATURA + "','";
query = query+msg.payload.AMPERAJE + "');'";
msg.topic=query;
return msg;

```