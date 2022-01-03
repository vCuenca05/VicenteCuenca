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

EJERCICIO 4
https://trailblazer.me/id/vcuenca

![image](https://user-images.githubusercontent.com/97058833/147973451-beca9a4c-5938-4437-87e8-1e7919841437.png)


EJERCICIO 5
Explicar que son conceptualmente, qué datos almacenan en forma estándar y cómo se relacionan el resto (algunos no se relacionan entre sí) cada uno de los siguientes objetos de Salesforce:

1.	Lead
Es un cliente potencial que se ha interesado en alguno de los productos o servicios en oferta. Se relaciona con los objetos Contact y Campaign, debido a que se pueden convertir de Leads en Clientes y a través de Campaigns se pueden captar nuevos Leads. Almacena los datos personales de los clientes potenciales.
2.	Account
Representa a una organización que tiene una determinada relación con los productos o servicios en oferta. Se relaciona con Contact, Opportunity y Case. Account tiene una relación Parent-Child con esos tres objetos.
Su función es consultar y administrar cuentas en la organización de Salesforce. Se pueden crear, actualizar, eliminar o consultar registros de datos adjuntos asociados con una cuenta a través de APIs.  Los datos que almacenan son la información básica de la empresa, pero de requerirse información adicional se puede personalizar.
3.	Contact
Son las personas que conforman los puntos de contacto de las organizaciones (Accounts). Pueden ser clientes, competidores o partners. Se relaciona con Lead (cuando se convierten a Contact) y con Account. Almacena la información personal de los representantes de las empresas.
4.	Opportunity
Es un objeto destinado a registrar las oportunidades de venta o de negocio. Tiene una relación tipo Lookup con Account y con Campaign. También se relaciona con el objeto Lead ya que, a través de una Opportunity se puede transformar en un cliente.
5.	Product
El objeto Product representa los objetos o servicios en venta. Se relacionan con el objeto Opportunity y PriceBook.
6.	PriceBook
Un PriceBook es una lista de productos y sus precios asociados. Se relaciona con Product y Opportunity.
7.	Quote
Se trata de un reporte que muestra los servicios y productos, con sus precios. Se puede crear y sincronizar con Opportunities y enviarse como PDF a los clientes. 
8.	Asset
Consiste en un objeto destinado a dar seguimiento a un producto vendido por la compañía o por un competidor. De esa manera se puede llevar un seguimiento del éxito de un determinado producto, o para tareas de mantenimiento y garantías. Se relaciona con Product.
9.	Case
Es un objeto destinado al seguimiento de las incidencias de los clientes. Se relaciona con Account y Contact.
10.	Article
Parte de Knowledge, que debe ser activado para poder utilizar este objeto, consiste en un objeto de solo texto que contiene información de diferente índole como puedan ser FAQs, Ofertas… Se pueden relacionar con cualquier objeto para proporcionar información.

DIAGRAMA:
![image](https://user-images.githubusercontent.com/97058833/147972836-909ce616-8305-4028-8cc7-f15307129cb7.png)

EJERCICIO 6
![image](https://user-images.githubusercontent.com/97058833/147973015-1b959acc-c5a2-4231-a354-9a5b7c92ac79.png)

EJERCICIO 7
Soluciones de Salesforce
A.	¿Qué es Salesforce?
Salesforce es una plataforma CRM basado en la nube (SaaS y PaaS) que facilita las relaciones entre empresas y clientes. 
            
B.	¿Qué es Sales Cloud?
Es una plataforma de ventas que da seguimiento al proceso de ventas
            
C.	¿Qué es Service Cloud?
Es un software permite a los agentes conectarse con los clientes y resolver problemas rápidamente.
            
D.	¿Qué es Health Cloud?
Es una plataforma que permite gestionar de forma integral la relación médico-paciente.
            
E.	¿Qué es Marketing Cloud?
Es una plataforma que las empresas pueden utilizar para invertir en estrategias de email marketing, permitiendo planificar, personalizar y optimizar la interacción con los clientes.
            
Funcionalidades de Salesforce
            
A.	¿Qué es un RecordType?
Nos permite personalizar un determinado objeto de diferentes maneras, desde configurar procesos, Page Layouts, Picklist, fórmulas, campos de texto, relaciones… Se pueden crear en cualquier objeto, ya sea estándar o custom. En el caso de los objetos Lead, Opportunity, Case y Solution, debemos crear un Business Process antes de poder crear un Record Type.
            
B.	¿Qué es un Rol?
Es una función que determina la visibilidad del usuario sobre los datos de una organización.
            
C.	¿Qué es un Validation Rule?
Es una función que verifica que los datos introducidos por los usuarios cumplen los estándares antes de guardarlos. Sirve, por ejemplo, para procesos de autorización de vacaciones, descuentos…
            
D.	¿Qué diferencia hay entre una relación Master Detail y Lookup?
En una relación Master-Detail, un record se convierte en Master (Parent) de otro record que se convierte en child, quedando vinculados. Si el Parent (Master) record es eliminado, también se elimina el child, así mismo un child nunca podrá ser parent de otro record. Se pueden relacionar únicamente 2 records por objeto. Sin embargo, en una Lookup Relationship no se requiere un Parent, y se pueden relacionar hasta 25 records por objeto, pero no se puede crear una Roll-up relationship, a diferencia de la Master-Detail.
            
E.	¿Qué es un Sandbox?
Es una copia de la organización en un entorno aislado y seguro para realizar pruebas e implementaciones de nuevas funciones sin que afecte a los usuarios. En el caso de Salesforce, hay varios tipos de sandbox que permiten distintas funcionalidades.
            
F.	¿Qué es un ChangeSet?
Sirve para enviar cambios o personalizaciones de una organización a otra de Salesforce, como por ejemplo para crear y probar nuevos objetos en un Sandbox para luego enviarlos a la organización de producción.
            
G.	¿Para qué sirve el import Wizard de Salesforce?
Sirve para importar datos a los objetos estándar y personalizados de tu organización de Salesforce, siempre que no supere los 50.000 registros. En caso de que supere esa cantidad, se recomienda usar Dataloader.
            
H.	¿Para qué sirve la funcionalidad Web to Lead?
Es un formulario que podemos diseñar e insertarlo en una web o un blog para automatizar la captación de Leads e integrar los datos de esos usuarios en nuestra organización de Salesforce.
            
I.	¿Para qué sirve la funcionalidad Web to Case?
Es un formulario que podemos diseñar e insertarlo en una web o un blog para automatizar el registro de Cases de los usuarios, permitiendo ofrecer un servicio y seguimiento postventa de un determinado producto vinculado a un cliente.
            
J.	¿Para qué sirve la funcionalidad Omnichannel?
Es una función de Service Cloud que permite conectar al área de soporte con los clientes a través de diversos canales. Al mismo tiempo, el área de soporte puede obtener toda la información que necesite sobre los clientes con los que están interactuando.
            
K.	¿Para qué sirve la funcionalidad Chatter?
Es una herramienta de colaboración en tiempo real que integra Salesforce, con la que los usuarios pueden comunicarse y compartir información, parecido a Microsoft Teams o Slack.
            
Conceptos generales
            
A.	¿Qué significa SaaS?
Significa Software as a Service. Lo que viene a ser ofrecer un servicio de software a través de la nube.
            
B.	¿Salesforce es Saas?
Salesforce es una plataforma SaaS y PaaS (Platform as a Service), lo que la hace prácticamente una herramienta única que ofrece todo lo que una empresa puede necesitar en un único lugar.
            
C.	¿Qué significa que una solución sea Cloud?
Es una tecnología que permite acceder a software, almacenamiento de archivos, procesamiento de datos… a través de internet, lo que reduce considerablemente los recursos que los usuarios necesitan en las computadoras que utilizan para acceder a estos servicios, ya que el procesado de toda la información se hace en la nube.
            
D.	¿Qué significa que una solución sea On-Premise?
Significa que el software se instala dentro del servidor y la infraestructura TIC de la empresa, lo que responsabiliza a la misma de la seguridad, la disponibilidad y la gestión del software, por lo que deberá tener un departamento de sistemas que gestione esta infraestructura. Entre este tipo de soluciones se encuentran los CRM como Salesforce.
            
E.	¿Qué es un pipeline de ventas?
Es una herramienta de gestión que se usa para observar las etapas de ventas con ciclos medios o largos
            
F.	¿Qué es un funnel de ventas?
Es el esquema que representa las etapas del proceso de decisión de compra de un usuario hasta convertirse en cliente.
            
G.	¿Qué significa Customer Experience?
Es el recuerdo que se genera en el cliente a través de su relación con la marca, durante y después de la compra. Es un ejercicio que se debe realizar en todos los departamentos de la empresa.
            
H.	¿Qué significa omnicanalidad?
Es una estrategia para mantener contacto con los clientes a través de distintos canales (email, redes sociales, webs…), siempre que esto se realice bajo una estrategia para contactar al consumidor en el momento adecuado.
            
I.	¿Qué significa que un negocio sea B2B?¿Qué significa que un negocio sea B2C?¿Qué es un KPI?
B2B significa Business to Business, cuando una empresa vende productos o servicios a otra empresa.
B2C significa Business to Customer, cuando una empresa vende productos o servicios a particulares.
KPI son los indicadores de desempeño y sirven para medir el desempeño de los proyectos, actividades y metas de una empresa y sus empleados. 
            
J.	¿Qué es una API y en qué se diferencia de una Rest API?
Una Application Programing Interface es un conjunto de definiciones y protocolos que se utilizan para conectar sistemas, software y aplicaciones. Permiten al usuario final la posibilidad de interactuar con distintos servidores sin que tenga que acceder a ellos directamente.
Una REST API es una API que se ajusta a los estándares de la arquitectura REST y permite la interacción con los servicios web de RESTful.
            
K.	¿Qué es un Proceso Batch?
Es la ejecución de un programa sin supervisión del usuario. El programa se puede ejecutar sin necesidad de que el usuario interactúe con él.
            
L.	¿Qué es Kanban?
Es un método de origen japonés para gestionar el trabajo a través de tarjetas en un tablero que refleja el proceso de la tarea en columnas, que por defecto suelen ser: por hacer, en proceso y hecho, sin embargo estas columnas se pueden modificar y adaptar a las necesidades de cualquier proceso o empresa.
            
M.	¿Qué es un ERP? 
Enterprise Resource Planning, o Sistema de Planificación de Recursos Empresariales, es un tipo de software que usan las organizaciones para administrar las actividades empresariales diarias, como la contabilidad, el abastecimiento, la administración de proyectos…
            
N.	¿Salesforce es un ERP?
No, debido a que Salesforce no maneja datos transaccionales, sin embargo, un CRM como Salesforce puede ser parte de un ERP.
