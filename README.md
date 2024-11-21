# Pruebas aplicaciones web
> [!NOTE]
> Este aplicativo esta hecho para uso libre, acontinuación su función:

## Descripción
Para este proyecto, se elaboran consultas y solicitudes a una base de datos alojada en un servidor remoto,
Ejecutado segun la parametrización de los requerimientos de la app, de acuerdo a la información de la prueba se debe ejecutar lo siguiente:

Ejercicio 1
El equipo de desarrollo ha enviado una tarea: debes averiguar qué solicitudes han venido de una dirección IP. Una dirección IP consta de cuatro números separados por un punto. Necesitas direcciones que comiencen con "233.201". Los logs están en un servidor remoto en logs/2019/12. No sabes qué día ocurrió el error.  Se requiere averiguar qué solicitudes fueron enviadas.
Esto es lo que se visualiza en el documento adjuntar en la respuesta de las consultas:
Comando que se uso para obtener los logs necesarios. Los strings adecuados, por ejemplo: 184.79.247.161 - - [30/12/2019:21:38:13 +0000] "PUT /alerts HTTP/1.1" 400 3557

Ejercicio 2
Se ha detectado un error en el sistema. Estaba activo el 12.30.2019. En ese momento, había errores 400 y 500. La prueba consiste en guardar los logs que se registraron durante este periodo en un archivo independiente. Después, resumir estos logs en archivos por separado con base en los errores, se ejecuta de la siguiente manera:

1. En el directorio de inicio del servidor remoto, crea un directorio llamado bug1.
2. Pon todas las solicitudes que ocurrieron en el archivo main.txt en el directorio bug1.
3. Dentro del directorio bug1 , crea un directorio events.
4. Dentro del directorio events, crea archivos de error 400 y 500. Llama a estos archivos 400.txt y 500.txt, respectivamente. Identifica en ellos los logs utilizando el error correspondiente del archivo main.txt.
  
- Esto es lo que debes adjuntar en el documentos:

1. Los comandos que crean los directorios bug1 y events.
2. Los comandos que utilizaste para seleccionar los registros especificados para el archivo main.txt.
3. Los comandos que usas para colocar los logs en los archivos 400.txt y 500.txt de main.txt.
4. Los archivos de texto 400.txt y 500.txt.

## Las pruebas que se deben realizar a la base de datos son:

Ejercicio 1
Tienes una base de datos con los viajes en taxi. El plan era tener 10 550 vehículos disponibles, lo que cubre la demanda del usuario; sin embargo, el equipo recibió muchas quejas de que no había vehículos suficientes. ¿Cuántos taxis hay actualmente en las calles? La información sobre todos los automóviles suficientes está en la tabla cabs.
Ve al servidor remoto.
Conéctate a la base de datos chicago_taxi con el nombre de usuario morty y la contraseña smith.
Cuenta el número total de automóviles en la tabla cabs. Recuerda que un automóvil podría pertenecer a distintas compañías.
Esto es lo que debes adjuntar en la respuesta:
Número de automóviles.
La solicitud que usaste para resolver el problema.

Ejercicio 2
En la tabla cabs, cuenta el número de automóviles de cada compañía. Ordena los valores en orden descendente. El equipo piensa que algunas compañías no tuvieron suficientes automóviles disponibles.
Devuelve las compañías con menos de 100 automóviles. Llama cnt (contados) al campo con el número de automóviles, y company_name al campo con el nombre de la compañía.
Para resolver el problema, utiliza el operador HAVING, una analogía de WHERE para las funciones agregadas. Estudia la documentación para aprender cómo funciona el operador:
(https://postgrespro.com/docs/postgrespro/11/queries-table-expressions (materiales en inglés))
Esto es lo que debes adjuntar en la respuesta:
Una lista de compañías con menos de 100 automóviles.
La solicitud que usaste para resolver el problema.
Nota: la consola muestra una lista incompleta. Para verla en su totalidad, presiona Enter o usa las flechas de tu teclado.

Ejercicio 3
La aplicación de taxis calcula el coeficiente del costo del viaje. Si el clima es bueno, el valor del coeficiente es 1. Si llueve o hay tormentas en el exterior, el coeficiente aumenta a 2. El equipo tiene una hipótesis de que hay un error en el cálculo del coeficiente. Para revisar el cálculo del coeficiente, el equipo necesita una selección de datos: el área de desarrollo puede comparar el coeficiente con los datos en los logs y corregir el bug. Tu tarea es obtener una selección.Para hacerlo:

Obtén una descripción de las condiciones meteorológicas de la tabla weather_records para cada hora.
Divide todas las horas en dos grupos a través del operador CASE: Está Bad ("mal") si el campo description contiene las palabras "rain" (lluvia) o "storm" (tormenta); Good ("bien"), para todas las demás horas.
Pon el nombre weather_conditions al campo resultante.
La tabla resultante debe tener dos campos: fecha y hora (ts) y weather_conditions.
Haz una selección para el periodo entre 11-05-2017 12:00 a. m. a 11-06-2017 12:00 a. m.
Esto es lo que debes adjuntar en la respuesta:
La tabla resultante con los datos para el periodo especificado.
La solicitud que ayudó a resolver el problema.

Ejercicio 4
Tras actualizar el software, la compañía de taxis comienza a reportar que la ganancia que reciben no coincide con los datos que proporciona la aplicación. El equipo de desarrollo sugiere que el problema puede estar en los datos sobre el número de viajes.
Para determinar si hay un bug, debes obtener la selección del número de viajes de cada compañía de taxi para los días 15 y 16 de noviembre de 2017.
Devuelve el campo company_name. Nombra trips_amount (cantidad de viajes) al campo con el número de viajes y devuélvelo.
Organiza en orden descendente los resultados obtenidos en el campo trips_amount.
Pista: para resolver el problema, conecta las tablas de taxis y viajes.
Aplica funciones de agregación con agrupamiento. No olvides escribir la construcción con una condición.

Esto es lo que debes adjuntar en la respuesta:

La tabla resultante con los datos para el periodo especificado.
La solicitud que ayudó a resolver el problema.

> [!TIP]
> Estos son los requisitos para poder ejecutar las silicitudes a la base de datos

# Diseño de los pasos para conectar a la base de datos.
- Se requiere tener una llave ssh privada creada desde bash.
- Adjuntar la llave ssh en el campo de autorización del servidor remotos.
- Conectar al servidor desde bash en el pc.
- Realizar las consultas solicitadas en las pruebas.

# Tecnologias usadas:
- Pruebas Manuales
- Pruebas funcionales
- Pruebas no funcionales
- Peticiones a una base de datos

> [!IMPORTANT]
> Para validar la información contenida requieres leer esto:

## Ejecución de Pruebas 
1. Clona el repositorio localmente.
2. Visualizar el archivo correspondiente a las pruebas de la base de datos.

> [!IMPORTANT]
> Estado del proyecto

## Estado:
- Completado

## Presentado por:
- Leonardo Lombana Contento

## Proyecto parte del sprint 6 - Fundamentos de las bases de datos
## Grupo 12 bootcamp QA Engineer - Tripleten
