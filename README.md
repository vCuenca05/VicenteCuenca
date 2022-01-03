# VicenteCuenca
ProContacto

EJERCICIO 2
Las siguientes preguntas están orientadas a la comprensión del protocolo HTTP. Son agnósticas al lenguaje de programación, la idea es comprender los conceptos del estándar:
1.	¿Qué es un servidor HTTP? 
Es un software que forma parte de un servidor y que se encarga de enviar información cuando recibe peticiones por parte de los usuarios.

2.	¿Qué son los verbos HTTP? Mencionar los más conocidos
Los verbos son las acciones que queremos realizar con el servidor. Los más conocidos son: GET, POST, PUT, PATCH, DELETE, HEAD, CONNECT, OPTIONS y TRACE.

3.	¿Qué es un request y un response en una comunicación HTTP? ¿Qué son los headers? 
El Request consiste en el proceso que realiza el usuario, a través de su navegador, para abrir una conexión a un servidor y realizar la solicitud para visualizar la información deseada.
El Response consiste en que el servidor procesa la solicitud del usuario y devuelve una respuesta, es decir, envía los datos solicitados por el usuario, una redirección o un mensaje de error por parte del Cliente o por parte del servidor.

Los headers son la parte central de los HTTP requests y responses, y transmiten información acerca del navegador del cliente, de la página solicitada, del servidor, etc.

4.	¿Qué es un queryString? (En el contexto de una url)
Es una parte de la URL que contiene los datos que deben pasar a las aplicaciones web.

5.	¿Qué es el responseCode? ¿Qué significado tiene los posibles valores devueltos?
Indican si se ha completado una solicitud HTTP específica. Hay cinco clases de posibles valores devueltos:
1.	Respuestas informativas (100–199),
2.	Respuestas satisfactorias (200–299),
3.	Redirecciones (300–399),
4.	Errores de los clientes (400–499),
5.	y errores de los servidores (500–599).

6.	¿Cómo se envía la data en un Get y cómo en un POST? 
El método GET envía la información en la URL, limitada a 2000 caracteres. Ya que se envía a través de la URL esta información es visible y no debe ser sensible.
En POST se envían en segundo plano, por lo que los datos quedan ocultos al usuario.

7.	¿Qué verbo http utiliza el navegador cuando accedemos a una página?
El navegador utiliza el verbo GET para realizar una petición al servidor y acceder a una página web.


8.	Explicar brevemente qué son las estructuras de datos JSON y XML dando ejemplo de estructuras posibles.
JSON (JavaScript Object Notation) es un lenguaje de marcado de datos basado en texto derivado de JavasCript. Permite intercambio de información de manera sencilla y rápida a través de su estructura en cadenas, además de ser más ligero que XML.
-	Ejemplo:
{
    "arrayColores":[{
            "rojo":"#f00",
            "verde":"#0f0",
            "azul":"#00f",
            "cyan":"#0ff",
            "magenta":"#f0f",
            "amarillo":"#ff0",
            "negro":"#000"
        }
    ]
}

XML (eXtensive Markup Language) está estructurado de forma jerárquica (de árbol) en elementos y atributos, que además se pueden anidar. Es un estándar internacionalmente conocido y aceptado, por lo que está optimizado para su uso en internet.
Ejemplo:
<libreria> 
  <libro>
    <autores>
        <autor>Elizabeth Castro</autor> 
    <autores>
    <titulo>XML Guía de Aprendizaje</titulo> 
    <precio moneda="euros">30</precio>
    <descriptores>
        <descriptor>lenguajes<descriptor>
        <descriptor>XML<descriptor>
    <descriptores>
             
  </libro> 
  <libro>
    <autores>
        <autor>Benoit Marchal</autor> 
    <autores
    <titulo>XML con ejemplos</titulo> 
    <precio moneda="euros">45</precio>
    <descriptores>
        <descriptor>lenguajes<descriptor>
        <descriptor>XML<descriptor>
    <descriptores>
   </libro> 
</libreria>


9.	Explicar brevemente el estándar SOAP
El Single Object Access Protocol es un protocolo estándar basado en XML para transmitir mensajes en HTTP, entre otros protocolos de Internet. Es el protocolo más ligero para intercambiar información. Al extender los headers HTTP permite definir qué información se envía y cómo mediante XML.


10.	Explicar brevemente el estándar REST Full
Es un estándar que facilita la forma de comunicación entre Cliente-Servidor a través de la arquitectura API y usando HTTP. Cuando una arquitectura web cumple con todas las restricciones y principios REST, se llama Arquitectura (o estándar) RESTFul.

11.	¿Qué son los headers en un request? ¿Para qué se utiliza el key Content-type en un header?
Un header es la primera línea del request y contiene la información básica de la página, como el verbo HTTP, la URL y la versión.

EJERCICIO 3
![image](https://user-images.githubusercontent.com/97058833/147972568-bc2c48fe-46e8-41e0-8eea-489bfac6a568.png)
            
![image](https://user-images.githubusercontent.com/97058833/147972579-e2575ba3-3f0c-4bd0-907c-47b50e59308c.png)
            
![image](https://user-images.githubusercontent.com/97058833/147972592-0c60b355-2f68-43ba-99de-66079cab45f1.png)

            ¿Qué diferencias se observan entre las llamadas el punto 1 y 3?
Después de realizar el request POST, mi nombre y correo aparecen en la base de datos junto con una ID generada automáticamente. 
