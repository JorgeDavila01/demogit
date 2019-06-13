# IBMCloudWeatherApp

Hands On para construir aplicación del clima utilizando weather company data e IBM Bluemix.

## Índice

* Requisitos previos.
* Creación del servicio en Cloud Foundry.
* Clonación y modificación del repositorio.
*
*

## Requisitos previos

Como primer requisito debe crear una cuenta en bluemix, para realizar esto puede acceder al siguiente enlace donde simplemente debe completar los espacios requeridos y dar crear cuenta.

https://cloud.ibm.com/registration

Como segundo requisito debe descargar e instalar el CLI de Cloud Foundry, para realizar esto en el siguiente enlace puede acceder a un git donde le daran explicación del proceso que debe realizar para realizar esta instalación.

https://github.com/cloudfoundry/cli

## Creación del servicio en Cloud Foundry

Ya como anteriormente creo su cuenta en IBM Cloud, usted accede por medio de su IBMid en el espacio en blanco y luego da clic en continuar.

<img width="600" alt="4" src="https://user-images.githubusercontent.com/50923637/59449077-0815c500-8dcc-11e9-8dfb-aca901a0b6ff.png">

Luego debe ingresar su correo y contraseña, luego da clic en sign in para terminar el proceso de federación de seguridad con el que cuenta IBM.

<img width="600" alt="5" src="https://user-images.githubusercontent.com/50923637/59450777-99d30180-8dcf-11e9-9fc5-f000a434df71.png">

Despues de ingresar da clic en catalogo para acceder a todas la herramientas con las que cuenta IBM Cloud.

<img width="600" alt="6" src="https://user-images.githubusercontent.com/50923637/59450808-a7888700-8dcf-11e9-8be5-e3670fe145f4.png">

Despues de seleccionar el catalogo estando en el puede seleccionar la lupa y en la lupa debe ingresar la palabra **weather** para filtar los resultados y tener la opción deseada, luego la selecciona dando clic en la opción de analisis.

<img width="600" alt="7" src="https://user-images.githubusercontent.com/50923637/59450941-f7674e00-8dcf-11e9-9bad-9d847a63e755.jpg">

Luego debe asignarle a su servicio un nombre, organización y espacio, luego de asignar eso debe dar clic en crear.

<img width="600" alt="8" src="https://user-images.githubusercontent.com/50923637/59451369-ef5bde00-8dd0-11e9-9da6-ee8a4b668ee4.jpg">

Despues de crear la aplicación debe ir a la sección de credenciales del servicio y luego dar clic en nueva credencial para que se generen credenciales para su sevicio.

<img width="600" alt="9" src="https://user-images.githubusercontent.com/50923637/59451556-51b4de80-8dd1-11e9-8f73-4f0a95fce6fa.jpg">

Luego podrá ver las nuevas credenciales para su servicio como se ve en la siguiente imagen.

<img width="600" alt="10" src="https://user-images.githubusercontent.com/50923637/59460720-60a58c00-8de5-11e9-857f-220501df2427.jpg">

## Clonación y modificación del repositorio

Primero debe clonar el repositorio de la aplicación el cual lo podra hacer copiando el siguiente comando en su terminal, a su vez podra ver como se hace en la siguiente imagen.

` git clone https://github.com/JorgeDavila01/demogit.git `

<img width="600" alt="1" src="https://user-images.githubusercontent.com/50923637/59445407-3a6ff400-8dc5-11e9-9c7a-1be02bf35e77.png">

Luego debe acceder a la carpeta que se creo al clonar el repositorio, la carpeta quedara con el nombre de **weather-company-data-demo** y estando en esta carpeta debe abrir el archivo de texto del manifest.yml, y en el debe realizar el cambio de **Name** a su gusto tenga en cuenta que sea algo unico y que no este ya creado, en este ejemplo sera llamado como **cambiar-nombre** y guarda dicho cambio.

```
applications:
- disk_quota: 1024M
name: cambiar-nombre
command: node app.js
path: .
domain: mybluemix.net
instances: 1
memory: 512M
```

Podrá ver el proceso anteriormente mencionado en las siguientes imagenes.

<img width="600" alt="2" src="https://user-images.githubusercontent.com/50923637/59446839-e0246280-8dc7-11e9-8132-b130f964c206.png">

<img width="600" alt="3" src="https://user-images.githubusercontent.com/50923637/59446844-e1ee2600-8dc7-11e9-8b3b-b9f0801f56ef.png">

El nombre de su aplicación será el mismo host que utilice determinar la URL de su aplicación inicialmente, por ejemplo `<host>.mybluemix.net.`

##  Modificación del codigo

En el archivo **app.js** usted debe cambiar en la linea 28, los valores de **user** y **password** que puede ver en el codigo, por su usuario y contraseña que se le creo cuando aprovisiono las credenciales a su servicio.

<img width="600" alt="11" src="https://user-images.githubusercontent.com/50923637/59462419-538a9c00-8de9-11e9-8c79-6f68e18ac7a1.jpg">

[este es el link](https://cloud.ibm.com/docs/search/virtual%20server?locale=es)
