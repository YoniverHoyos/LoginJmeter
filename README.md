# Load Testing with Jmeter for a Login Service

The repository contains a .jmx file created in JMeter 5.6.3, as well as a .csv file with the data parameters needed to perform a load test on the login service located at https://the-internet.herokuapp.com/login. Similarly, you will find two .jtl files generated from the execution of two load tests with 30 and 150 users for the login service. Additionally, there are two folders containing the HTML reports generated based on those .jtl files.

## Ejecución del repositorio:

* Clone the repository by following the steps described by GitHub for cloning a repository that is not empty. These steps can be found in this documentation: https://docs.github.com/es/repositories/creating-and-managing-repositories/cloning-a-repository
* Download JMeter 5.6.3, which can be done via this link: https://jmeter.apache.org/download_jmeter.cgi
* Extract the .zip file to any desired location for working.
* Navigate to the location of the ApacheJMeter.jar file, located at \apache-jmeter-5.6.3\bin\ApacheJMeter.jar
* Run the ApacheJMeter.jar file using the Java platform. It is important to note that you must have a version of Java greater than 8 installed on your device. For example, JDK 21 was used for this repository, which can be downloaded for Windows at https://www.oracle.com/latam/java/technologies/downloads/#jdk21-windows.
* Open the .jmx file using JMeter: File > Open, then browse to the file’s location, select the file, and click Open.
* Configure the location of the .csv file in the “CSV Data Set Configuration” option. In the field where the file name is requested, enter the path where the DatosJmeter.csv file is located. 
* Before running the program, you must go to the “Threads” group and modify the number of threads to be used in each load test execution. Similarly, you must go to the simple data writer (ReportLogin) to change the location where the .jtl file for each execution will be generated. It is important to save this file, as it will be used to create the HTML report.

## Creating the HTML report:

Use the built-in report generator in JMeter. To do this, go to Tools > Generate HTML Report.

   <img width="597" height="302" alt="image" src="https://github.com/user-attachments/assets/f57f4b77-6718-418c-b069-ec13781adff4" />

In the first text box of the window that appears, enter the location of the .jtl file generated during the load test. In the second box, enter the location of the user.properties file, which is located within the JMeter installation files (\apache-jmeter-5.6.3\bin\user.properties); In the third field, enter the location where you want to generate the HTML report; it is important that this location be an empty folder.

  <img width="579" height="376" alt="image" src="https://github.com/user-attachments/assets/2d95c8d5-aba1-4d44-98c9-4a5a87f3a00d" />

Finally, simply click “Generate Report” to obtain the HTML index file containing the load test execution report.
  
  <img width="580" height="380" alt="image" src="https://github.com/user-attachments/assets/74d75388-d744-4343-b76d-e8183028ac60" />

## Author 
Yoniver Hoyos Muñoz

Indutrial Automation Engineer
