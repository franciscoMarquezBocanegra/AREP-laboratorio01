# TALLER 1: APLICACIONES DISTRIBUIDAS (HTTP, SOCKETS, HTML, JS,MAVEN, GIT)


Programa creado para buscar en la api gratis de https://www.omdbapi.com/. La aplicación recibe como parámetro el nombre de la película y muestra en pantalla los datos correspondientes en formato JSON.


### Prerequisitos

Para elaborar este proyecto se requirio de : 


Maven: Apache Maven es una herramienta que maneja el ciclo de vida del programa.



Git: Es un sistema de control de versiones distribuido (VCS).



Java 19: Java es un lenguaje de programación de propósito general orientado a objetos, portátil y muy versátil.



### Instalación

Clonamos el repositorio

```
    git clone https://github.com/franciscoMarquezBocanegra/AREP-laboratorio01

```
Se accede a la carpeta principal del repositorio repositorio que acabamos de clonar

	 cd AREP-laboratorio01

Hacemos la construccion del proyecto

	 mvn package
---
### Corriendo
Corremos los siguientes comando
	
	 mvn clean package install
	 mvn clean install

Ahora corremos el servidor
	
**Windows**

	 mvn exec:java -"Dexec.mainClass"="edu.escuelaing.arep.ASE.app.webServer.HTTPServer"

**Linux/MacOs**

	 mvn exec:java -Dexec.mainClass="edu.escuelaing.arep.ASE.app.webServer.HTTPServer"

Por ultimo accedemos a nuestro navegador de confianza con la siguiente URL

	 http://localhost:35000/

Aqui nos debera de cargar la siguiente pagina, con la cual podemos empezar a hacer las busquedas que necesitemos

[Alt text](image-1.png)

---
### Corriendo test

Ejecutamos el comando

	mvn Test
	
---


### Diseño del programa.



El programa consta de cuatro componentes principales:

1. **JS Web Client (Cliente Web en JavaScript):** Representado en la carpeta "views", este cliente es la interfaz de nuestra aplicación. Realiza consultas asincrónicas mediante solicitudes GET utilizando promesas.

2. **Web Server with REST API Facade (Servidor Web con Fachada de API REST):** Dividido en tres carpetas.

   - **WebServer (Servidor Web):** Codifica el servidor que recibe las solicitudes del cliente.
   
   - **Controllers (Controladores):** Actúan como intermediarios entre los servicios y el servidor web. Se centran en el recurso "films".
   
   - **Services (Servicios):** Contiene la lógica del backend. Implementa la lógica necesaria para proporcionar las respuestas requeridas por el cliente.

3. **External REST API (API REST Externa):** Representa servicios web externos a los cuales se accede para obtener información sobre el recurso "films".

4. **Concurrent Java Test Client (Cliente de Pruebas Java Concurrente):** Una clase en Java responsable de probar las funcionalidades del backend de la fachada de manera concurrente a través de hilos. Se encuentra en la carpeta "test".




Para extender la funcionalidad de nuestro backend, hemos implementado una interfaz que define las funcionalidades y una clase que la implementa. Esta estructura nos permite agregar nuevas funciones simplemente extendiendo la interfaz existente.




Cuando deseamos añadir más servicios web externos, utilizamos una interfaz de fábrica que devuelve instancias de los servicios web necesarios. Cada nuevo servicio web debe implementar esta interfaz de fábrica. También hemos implementado una interfaz con los métodos que deben ser implementados por los servicios web externos.




## Construido con

* [Maven](https://maven.apache.org/): Apache Maven es una herramienta que estandariza la configuración del ciclo de vida del proyecto.
* [Git](https://rometools.github.io/rome/):  Es un sistema de control de versiones distribuido (VCS).
* [Visual Studio Code](https://code.visualstudio.com): es un editor de código fuente desarrollado por Microsoft.
* [Java 19](https://www.java.com/es/): Lenguaje de programación de propósito general con enfoque a el paradigma de orientado a objetos, y con un fuerte tipado de variables.
* [Html](https://developer.mozilla.org/es/docs/Learn/Getting_started_with_the_web/HTML_basics): es un lenguaje de marcado que estructura una página web y su contenido.
* [JavaScript](https://developer.mozilla.org/es/docs/Learn/JavaScript/First_steps/What_is_JavaScript): lenguaje de programación que los desarrolladores utilizan para hacer paginas web dinamicas.


## Autor
* ** Francisco Márquez


