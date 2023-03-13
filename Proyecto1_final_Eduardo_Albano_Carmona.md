Eduardo Albano Carmona 2ºASIR  13/03/2023
### ![](Aspose.Words.869eba26-0014-4b97-957e-ccc7f65a0393.001.jpeg)****
###
###
###
###
###
###
###
###
###
###
###
###
###
###
### **Proyecto IAW: Energymaster**



[1.- Introducción	3](#_Toc129633605)

[2.- Objetivos y requisitos del proyecto	3](#_Toc129633606)

[3.- Estudio previo	3](#_Toc129633607)

[3.1.- Estado actual	3](#_Toc129633608)

[3.2.- Estudio de soluciones existentes	3](#_Toc129633609)

[4.- Plan de trabajo	3](#_Toc129633610)

[5.- Diseño	4](#_Toc129633611)

[5.1.- Diseño general	4](#_Toc129633612)

[5.2.- Diseño detallado	4](#_Toc129633613)

[6.- Implantación	5](#_Toc129633614)

[7.- Recursos	5](#_Toc129633615)

[7.1.- Herramientas hardware	5](#_Toc129633616)

[7.2.- Herramientas software	5](#_Toc129633617)

[7.3.- Personal	5](#_Toc129633618)

[7.4.- Presupuesto	5](#_Toc129633619)

[8.- Conclusiones	6](#_Toc129633620)

[8.1.- Grado de consecución de objetivos	6](#_Toc129633621)

[8.2.- Problemas encontrados	6](#_Toc129633622)

[8.3.- Futuras mejoras	6](#_Toc129633623)

[9.- Referencias / bibliografía	7](#_Toc129633624)

[10.- Anexos	7](#_Toc129633625)




## **1.- Introducción**
Este proyecto se enfoca en un sitio web interactivo que tiene como objetivo recabar datos sobre el consumo de energía a nivel del país mediante la utilización de medidores inteligentes.
## **2.- Objetivos y requisitos del proyecto**
Una compañía llamada Energymaster se especializa en la instalación de medidores inteligentes de energía en hogares para recolectar información sobre el consumo de energía a nivel global. Estos medidores se conectan a la web y brindan datos sobre el incremento o disminución en el uso de energía. La organización requiere almacenar y analizar esta gran cantidad de información para identificar patrones de consumo de energía que puedan mejorar la eficiencia y reducir el desperdicio.

Para cumplir con los requisitos de este proyecto, se creará una página web dinámica en la cual los usuarios/clientes podrán registrar sus datos personales y de consumo para que sean almacenados en una base de datos.
## **3.- Estudio previo**
Mediante la conexión Wi-Fi y el uso de direcciones IP de los distintos clientes, se realizará una lectura para registrar su consumo de energía, el cual será almacenado en una base de datos.
## **3.1.- Estado actual**
Con el fin de llevar a cabo este proyecto, se ha desarrollado una página web dinámica que contiene distintos formularios para registrar los datos de los clientes y su consumo energético. Una vez recopilados estos datos, se implementará una consulta que permita visualizar el consumo total a nivel nacional.
## **3.2.- Estudio de soluciones existentes**
Se llevará a cabo un despliegue en AWS que involucra varios servicios:

- Se creará una instancia EC2 para alojar la página web y los diferentes formularios utilizados para registrar los datos y el consumo de los clientes.
- Se configurará una instancia RDS que será el lugar donde se almacenarán los datos recopilados en los formularios.
- Se creará una VPC para que los sitios puedan conectarse desde diferentes zonas geográficas.
## **4.- Plan de trabajo**
El plan de trabajo consiste en adquirir un dominio en Amazon. Posteriormente, se implementarán medidas de seguridad en el entorno de trabajo creado. Se creará un grupo de seguridad en la instancia que alojará la página web para asegurar que el sitio web esté protegido. Además, se creará otro grupo de seguridad en la instancia que alojará la base de datos para permitir únicamente el acceso a las instancias dentro del grupo de seguridad web, asegurando de esta manera la seguridad de la base de datos.
## **5.- Diseño**
## **5.1.- Diseño general**
En cuanto al diseño general, se montará la página web en una instancia EC2 y se configurará una instancia RDS para alojar la base de datos donde se almacenarán los datos de los clientes. Luego, se implementarán medidas de seguridad para garantizar la protección del entorno en su totalidad.
## **5.2.- Diseño detallado**
Se configurará una VPC para alojar las instancias EC2 y RDS previamente creadas, permitiendo la conexión desde diferentes zonas. Se crearán subredes y se mapearán las redes públicas (con acceso externo) y privadas (sin acceso externo). Cada subred estará asociada a una tabla de enrutamiento que dependerá de si es pública o privada.

![](Aspose.Words.869eba26-0014-4b97-957e-ccc7f65a0393.002.png)

También, en nuestra instancia RDS, añadiremos las subredes privadas.

![](Aspose.Words.869eba26-0014-4b97-957e-ccc7f65a0393.003.png)

## **6.- Implantación**
Para resolver este proyecto, es necesario crear un entorno en AWS que permita alojar un servidor web y un servidor de base de datos para el correcto funcionamiento de la página web dinámica. Es importante implementar medidas de seguridad para proteger el entorno y evitar vulnerabilidades.
## **7.- Recursos**
## **7.1.- Herramientas hardware**
Instancia EC2 con la siguiente configuración:

\- S.O à Ubuntu 22.04

\- Tipo de instancia: t2.micro

\- 1 CPU

\- 8 GB de almacenamiento 
## **7.2.- Herramientas software**
Instancia EC2 con la siguiente configuración software:

\- Servicio Apache.

\- Servicio MySQL.

\- Servicio PHP.

\- Grupo de seguridad.

Instancia RDS con la siguiente configuración software:

\- Servicio MySQL.

\- Grupo de seguridad.
## **7.3.- Personal**
Actualmente, dado el número de clientes que utilizan nuestra página web, una sola persona es suficiente para administrarla. A medida que la empresa crezca, será necesario aumentar el personal para satisfacer las necesidades de los clientes.
### **7.4.- Presupuesto**
Este será el presupuesto por utilizar una instancia EC2.

![](Aspose.Words.869eba26-0014-4b97-957e-ccc7f65a0393.004.png)

En la pestaña de “Panel de facturación”, podremos consultar el total de gastos que tenemos en todo momento. Este será el presupuesto actualmente para el mes de las Instancias creadas.

![](Aspose.Words.869eba26-0014-4b97-957e-ccc7f65a0393.005.png)
## **8.- Conclusiones**
## **8.1.- Grado de consecución de objetivos**
\- Creación de instancias y Configuración software terminado.

\- Creación de página web dinámica  terminado.

\- Creación de base de datos e inserción de datos a través de la página web  terminado.

\- Securización escenario terminado.
## **8.2.- Problemas encontrados**
El problema que he encontrado en este proyecto, es la dificultad de la inserción de los datos desde el formulario creado en la página web hasta la base de datos previamente asociada acompañado de la no lectura de la suma del consumo que por falta de tiempo al haber estado enfermo no me ha dado tiempo a solucionar. La solución que he encontrado a la inserción es mediante un código PHP de inserción, con el que he podido introducir todos los datos necesarios en la tabla de la base de datos correspondiente.
## **8.3.- Futuras mejoras**
Como una mejora futura para este proyecto, se podría considerar la implementación de un clúster y un proxy inverso que actúe como balanceador de carga para distribuir la carga de tráfico en varios nodos, lo que evitará una posible saturación de la página web a medida que la empresa crezca. Además, se podría pensar en la posibilidad de poner la instancia RDS en modo producción, aunque esto conllevará un aumento en el presupuesto.
## **9.- Referencias / bibliografía**
Las referencias que he seguido han sido las siguientes:

\- [StackOverflow](https://es.stackoverflow.com)

\- [W3Schools](https://www.w3schools.com/bootstrap5/index.php)

\- [Bootstrap](https://startbootstrap.com)

\- [Moodle](https://moodle.iesgrancapitan.org/course/view.php?id=152&section=0)
## **10.- Anexos**
En cuanto al software que hemos utilizado:

- MySql Server para almacenar la base de datos versión 8.0.
- Apache2 para gestionar página web Versión 2.4.53
- WinSCP: Transferencia de archivos.
- VisualStudio: Manejo de código.
- AWS: Alojamiento de instancias.

16
