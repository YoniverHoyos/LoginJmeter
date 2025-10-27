Ejercicio 3. Realizar una prueba de carga del servicio de login

Para efectos del ejercicio, se brindará el siguiente CURL:

curl --location --max-time 60 'https://fakestoreapi.com/auth/login' ^
--header 'Content-Type: application/json' ^
--data '{
  "username": "user",
  "password": "passwd"
}'
El objetivo del ejercicio era realizar una prueba de carga en el servicio de login ubicado en "https://fakestoreapi.com/auth/login" pero esto no fue posible por lo que opto por realizar una prueba en una ubicacion de login diferente.

El repositorio contiene un archivo .jmx realizado en Jmeter 5.6.3, al igual que el archivo .csv con la parametizacion de datos necesaria para realizar una prueba de carga del servicio de login ubicado en https://the-internet.herokuapp.com/login

Pasos para la ejecucion del archivo en Jmeter 5.6.3:
1. Clonar este repositorio en el equipo que se va a utilizar, para ello se puede seguir los pasos descritos por Github en esta documentación https://docs.github.com/es/repositories/creating-and-managing-repositories/cloning-a-repository
2. Descargar Jmeter 5.6.3, lo cual se puede hacer en este link https://jmeter.apache.org/download_jmeter.cgi
3. Descomprimir el archivo .zip en la ubicacion deseada.
4. Ir a la ubicación del ejecutable de Jmeter, ubicado en \apache-jmeter-5.6.3\bin
5. Ejecutar el archivo ApacheJMeter.jar para lo cual se necesita tener instalada en el dispositivo un version de Java mayor a 8.
6. Abrir el archivo .jmx por medio de Jmeter, Archivo->Abrir y buscar la ubicacion del archivo.
7. Configurar la ubicacion del archivo .csv en la opcion "Configuración del CSV Data Set", luego en nombre del archivo colocar la ruta donde esta ubicado el archivo .csv
8. Ejecutar el proyecto en la opcion arrancar de la parte superior.
