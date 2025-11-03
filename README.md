Ejercicio 3. Realizar una prueba de carga del servicio de login

Para efectos del ejercicio, se brindará el siguiente CURL:

<img width="631" height="237" alt="image" src="https://github.com/user-attachments/assets/eea7cfcd-9630-4fa8-b344-eed90e4da5db" />

El objetivo del ejercicio era realizar una prueba de carga en el servicio de login ubicado en "https://fakestoreapi.com/auth/login" pero esto no fue posible por lo que opto por realizar una prueba en una ubicación de login diferente.

El repositorio contiene un archivo .jmx realizado en Jmeter 5.6.3, al igual que el archivo .csv con la parametización de datos necesaria para realizar una prueba de carga del servicio de login ubicado en https://the-internet.herokuapp.com/login. De igual forma, es posible encontrar dos archivos .jtl generados en la ejecución de dos pruebas de carga con 30 y 150 usuarios para el servicio de login, ademas, se puede observar dos carpetas con los reportes HTML elaborados en base a dichos archivos .jtl.

Pasos para la ejecución del repositorio:

1. Clonar este repositorio en el equipo que se va a utilizar, para ello se deben seguir los pasos descritos por Github para clonar un repositorio que no este vacio. Dichos pasos se pueden encontrar en esta documentación https://docs.github.com/es/repositories/creating-and-managing-repositories/cloning-a-repository
2. Descargar Jmeter 5.6.3, lo cual se puede hacer en este link https://jmeter.apache.org/download_jmeter.cgi
3. Descomprimir el archivo .zip en cualquier ubicación deseada para trabajar.
4. Ir a la ubicación del archivo ApacheJMeter.jar, ubicado en \apache-jmeter-5.6.3\bin\ApacheJMeter.jar
5. Ejecutar el archivo ApacheJMeter.jar utilizando la plataforma de JAVA, es importante acalarar que se necesita tener instalada en el dispositivo una version de Java mayor a 8. Por ejemplo, para este repositorio se utilizó la version del JDK 21, la cual se puede descargar para windows en https://www.oracle.com/latam/java/technologies/downloads/#jdk21-windows.
6. Abrir el archivo .jmx por medio de Jmeter, Archivo->Abrir y buscar la ubicación del archivo, seleccionar el archivo y luego dar clic en abrir.
7. Configurar la ubicación del archivo .csv en la opcion "Configuración del CSV Data Set", en el espacio donde se solicita el nombre del archivo, colocar la ruta donde esta ubicado el archivo DatosJmeter.csv
8. Antes de ejecutar el programa es necesario ir al grupo de hilos llamado usuarios, para modificar el numero de hilos que se utilizaran en cada ejecucion de la prueba de carga. De igual forma, es necesario ir al escritor de datos simples llamado ReportLogin, con el objetivo de modificar la ubicación donde se generara el archivo .jtl de cada ejecución realizada, es importante guardar este archivo ya que se utilizara para la creación del reporte HTML.
9. Creación del reporte HTML:
Se utiliza el generador de reportes integrado en Jmeter, para ello se va a la opcion de Tools->Generate HTML report.

   <img width="597" height="302" alt="image" src="https://github.com/user-attachments/assets/f57f4b77-6718-418c-b069-ec13781adff4" />

En primer cuadro de texto de la ventana generada se debe ingresar la ubicación del archivo .jtl generado en la ejecución de la prueba de carga, en la segunda casilla se coloca la ubicación del archivo user.properties, el cual se encuentra dentro de los archivos de instalación de Jmeter (\apache-jmeter-5.6.3\bin\user.properties); en la tercera casilla se debe colocar la ubicación donde se quiere generar el reporte HTML, siendo importante que dicha ubicación sea una carpeta vacia.

  <img width="579" height="376" alt="image" src="https://github.com/user-attachments/assets/2d95c8d5-aba1-4d44-98c9-4a5a87f3a00d" />

Por ultimo, solo es necesario dar clic en Generate report para obtener el archivo html index que contiene el reporte de la ejecución de la prueba de carga.
  
  <img width="580" height="380" alt="image" src="https://github.com/user-attachments/assets/74d75388-d744-4343-b76d-e8183028ac60" />

 
