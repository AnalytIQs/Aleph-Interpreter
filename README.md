# ALEPH INTERPRETER

Te invitamos a conocer Aleph Interpreter:

https://www.youtube.com/watch?v=n1ZoHiEf1eU

¿Cómo utilizar nuestra aplicación web?

Es muy simple, sigue los siguientes pasos:

- Descarga el repositorio
- Instala npm y node.js: https://nodejs.org/es/download/
- Abre una terminal en la carpeta donde lo descargaste, es decir navega desde la consola hasta esa ruta.
- Ejecutar el comando npm install -g http-server
- Ejecutar el comando: http-server dist/interpretador
- Abrir en el navegador: localhost:8080
- Abrir archivo; si no carga la página, relogear.

## Codigo
-Si quieres conocer mas a detalle nuestra solucion, ingresa a: AnalytIQs/interpretador_inteligente
Donde encontraras el codigo paso a paso de la aplicacion.

## OBJETIVO

El objetivo de nuestra solución, Aleph Interpreter, es garantizar -al funcionario del Banco BBVA-, accesibilidad, óptimo procesamiento, y calidad en la extracción de datos valiosos de los documentos de los estados financieros de PYMES, con el fin de facilitar el proceso de análisis crediticio del banco. Para esto se puso a disposición una página web con la cual aseguramos el uso de nuestra solución desde cualquier dispositivo. En esta página el colaborador del banco podrá cargar documentos en formato pdf asociados a sus posibles clientes. El proceso de análisis se apoya mediante el servicio de Textract AWS y librerías de software libre. Se usarán estrategias de expresiones regulares y diccionarios para extraer las variables solicitadas por el reto Interpretador Inteligente. El colaborador podrá ver reflejado en la página web una visualización previa de la extracción. Una vez validada la información, el usuario podrá descargar en diferentes formatos para su fácil integración. Debido a los controles de  seguridad que ofrece AWS (https://aws.amazon.com/es/textract/) y nuestra página web, no se almacenará ningún documento.

## DETALLES TÉCNICOS

This project was generated with Angular CLI version 10.1.4.

Development server
Run ng serve for a dev server. Navigate to http://localhost:4200/. The app will automatically reload if you change any of the source files.

Code scaffolding
Run ng generate component component-name to generate a new component. You can also use ng generate directive|pipe|service|class|guard|interface|enum|module.

Build
Run ng build to build the project. The build artifacts will be stored in the dist/ directory. Use the --prod flag for a production build.

Running unit tests
Run ng test to execute the unit tests via Karma.

Running end-to-end tests
Run ng e2e to execute the end-to-end tests via Protractor.

Further help
To get more help on the Angular CLI use ng help or go check out the Angular CLI README.

La aplicación está diseñada en tres módulos, el módulo de la interfaz, en donde se realizó la aplicación por la cual el usuario puede interactuar y subir sus archivos y extraer la información en tablas. El segundo módulo es el de la extracción de texto de las imágenes por medio de AWS o el módulo de python, para que los documentos sean procesados como tablas (o dataframes). Finalmente el tercer módulo es el de la extracción de la información con ayuda de las funcionalidades desarrolladas por nuestro equipo, para procesar cada una de las variables y su posterior conversión a los formatos solicitados.

A continuación, presentamos los detalles técnicos de nuestra solución Aleph Interpreter.
Las bibliotecas y frameworks que utilizamos se dividen en los tres componentes de la aplicación, a saber: 
Frontend: 
Para el desarrollo del frontend utilizamos el framework de desarrollo frontend Angular. Adicionalmente, se integró Bootstrap, con la finalidad de darle a la aplicación un excelente aspecto visual.
Utilizamos el Recaptcha de Google para evitar ataques de denegación de servicio. Esto comprueba que el usuario de la aplicación no es un robot o algoritmo automatizado.
Para hostear el frontend de la aplicación, utilizamos el servicio gratuito de Hosting ofrecido por Google Firebase.
Backend: 
Para desarrollar el backend de la aplicación, utilizamos el framework Flask, permitiendo implementar fácilmente las funcionalidades desarrolladas para la extracción y análisis de textos de los PDF 's.
Algunas librerías utilizadas fueron: 
pdf2image.
boto3
hashlib
datetime
flask_core
flask
Extracción y análisis del texto:
Configuramos las credenciales de AWS para tener acceso a la API.
Utilizamos la librería re para extraer la información de cada una de las variables pedidas en el reto con respecto a las expresiones regulares realizadas por el equipo.
Utilizamos la librería pandas para cargar con total libertad nuestros documentos y expresarlos como dataframes y adicionalmente moldear sus filas y columnas de manera que el procesamiento de los datos se haga de manera más ordenada.
numpy
Utilizamos la librería Json para manejar los datos que nos retorna la API de Textract.
Utilizamos la API de Textract haciendo uso de Boto3 para obtener tablas y texto que se extrae de las páginas
Utilizamos la librería Pickle para serializar objetos obtenidos a partir de solicitudes a textract.
La librería de Spacy juega un papel fundamental en nuestro análisis de la información pues su módulo de NLP (procesamiento de lenguaje natural) nos permite, entre otras cosas, analizar el contexto de las palabras o las frases contenidas en los documentos.


--------------------------------------------
Herramientas Front:
Utilizar angular para desarrollar el frontend.
Utilizar el Recaptcha de Google para evitar ataques de denegación del servicio.
Para correr el frontend, utilizamos el servicio de Hosting de Firebase.


Herramientas Back: 

Utilizar Flask para desarrollar el backend.
Utilizar el servicio de ElasticBeanstalk de AWS.
Lista de librerías de Python
Flask
hashlib, datetime
smtplib, ssl
email
pd2t
Utilizar Textract AWS.
