## <p align = "center"> PRACTICA Nº1</p>
##  <p align = "center">SISTEMAS EMPRESARIALES</p>

|||
|----------|-------------|
|Carrera:| Ingenieria De Sistemas|
|Materia:| Tecnologias Emergentes II|
|Apellidos y Nombres:| Luque Cari Ruben Elio|
|C.I.:| 9949421 L.P.|
|Lugar y Fecha:| El Alto - 2019|

**1)	Explique que son los sistemas empresariales** 

Un Sistema de Información Empresarial es un sistema que tiene un impacto muy importante en el funcionamiento de la organización o negocio y cuya falla traería graves consecuencias.
Normalmente que ofrece alta calidad de servicio, gestiona con grandes volúmenes de datos, disponible de forma continua y es capaz de soportar cualquier organización grande.
En el desarrollo de aplicaciones de misión crítica se consideran

       -Plataforma tecnológica**
       -Alta disponibilidad
       -Escalabilidad
       -Seguridad
       -Mantenimiento


**2)	Describa cuales son las características más importantes de una aplicación empresarial **



- Acceso a bases de datos, usualmente a bases de datos relacionales
- Operaciones transaccionales, cumple con las propiedades ACID
- Escalables, permiten escalabilidad vertical y horizontal
- Disponibles, idealmente prestan servicios de forma continua
- Seguras, no todos los usuarios acceden con la misma funcionalidad
- Permiten integración con otras tecnologías
- Arquitectura multicapa

**3)	Investigue y proponga cinco (5) instituciones que requerirían aplicaciones de misión crítica. Justifique su respuesta** 




**4)	Explique cuáles son las diferencias entre la escalabilidad horizontal y escalabilidad vertical**

La diferencia es que Escalabilidad horizontal, que se refiere a aumentar el número de componentes. Y en Escalabilidad vertical, que se refiere a actualizaciones o modernización de componentes existentes.

**5)	Que es un servidor Web y que es un servidor de aplicaciones Servidor web:**

Un servidor web es un programa informático que procesa una aplicación de lado del servidor, realizando conexiones bidireccionales o unidireccionales y síncronas o asíncronas con el cliente y generando o cediendo una respuesta en cualquier lenguaje o aplicación del lado del cliente.
 
Toma la petición de un cliente y devuelve algo.
Servidor de aplicaciones:
Un servidor de aplicaciones es un dispositivo de software que proporcionan servicios de aplicación a las computadoras cliente.
Un servidor de aplicaciones generalmente gestiona la mayor parte (o la totalidad) de las funciones de la lógica de negocio y acceso a los datos de la aplicación.


**6)	Con un gráfico explique cómo funciona el protocolo HTTP **

El protocolo HTTP funciona atraves de solicitudes y respuestas entre un cliente (por ejemplo un navegador de internet ) y un servidor ( por ejemplo la computadora donde residen páginas web).

![IMAGEN](http://www.profesordeinformatica.com/images/http_funcionamiento.gif)

**7)	Explique los elementos importantes de REQUEST en HTTP **
Elementos principales que componen un HTTP Request:

   -método HTTP (HTTP method): usualmente:
    GET, POST.
   -Recurso al que se accede (URL)
   -Parámetros de FORM
**8)	Explique los elementos importantes de RESPONSE en HTTP **

Elementos principales que componen un HTTP Response:

    -código de estado (status code): indica si la operación fue realizada correctamente o no.
    -tipo de contenido (content type): si el contenido es HTML, una imagen, un archivo PDF. Etc.
    -contenido: el HTML, la imagen, etc.
    
**9)	Describa con un gráfico la arquitectura Java EE** 

![](http://slideplayer.es/1646087/6/images/8/MarcoTe%C3%B3ricoJavaEnterpriseEdition%28JEE%29%3Aest%C3%A1ndarparaeldesarrollodeaplicacionesempresarialesqueusatecnolog%C3%ADaJava..jpg)

**10)	Explique cuáles son los contenedores, componentes y servicios de Java EE**

Los contenedores:
Un contenedor es un entorno de ejecución que provee al componente una serie de servicios.
Java EE define los siguientes tipos de contenedores:
    -Contenedor web
    -Contenedor de negocio (o de EJBs)
Los componentes:
Un componente es una unidad de software que forma parte de una aplicación.
      Java EE define los siguientes tipos de componentes:
      
       -Componente cliente: Cliente AWT, Swing, Applet y navegador Web
       -Componente web: Servlet, JSP y JSF
       -Componente de negocio: EJB
        Cada tipo cubre necesidades concretas y se basan en APIs especificas 
Servicios de Java EE:
       Son los servicios que deben ofrecer los contenedores Java EE.
       Java EE define los siguientes servicios:
     -De directorio: para la indexación y búsqueda de componentes y recursos
     -De despliegue: para poder personalizar los componentes y recursos
     -De transaccionalidad: para poder ejecutar distintas acciones en una misma unidad transaccional
     -De seguridad: para poder autenticar y autorizar a los usuarios de la aplicación
     -De acceso a datos: para facilitar el acceso a Bases de Datos
Servicios de Java EE
       -De conectividad: para poder acceder fácilmente a distintos EIS
       -De mensajería: para poder comunicarse con otros componentes, aplicaciones o EIS
  Para que un entorno de ejecución pueda decir que es Java EE debe implementar y soportar:
                 -Todos los tipos de componentes
        -Todos los tipos de contenedores
        -Todos los servicios
        
**11)	Investigue los métodos más utilizados de las clases HttpServlet, HttpServletRequest y HttpServletResponse, y para cada uno de los métodos muestre un ejemplo.** 

En Java EE, existe la interfaz Servlet que define cómo debe definirse un servlet. Cualquier clase que implemente esta interfaz y se configure como @WebServlet en el código o vía XML:

~~~
<servlet-config>
    <servlet-name>MiServlet</servlet-name>
    <servlet-class>paquete.donde.esta.la.ClaseServlet</servlet-class>
</servlet-config>
<servlet-mapping>
    <servlet-name>MiServlet</servlet-name>
    <servlet-url>/una/url</servlet-url>
</servlet-mapping>
~~~

La interfaz posee varios métodos, de los cuales los siguientes son los principales, ordenados de acuerdo al ciclo de vida del Servlet (los otros métodos no son tan relevantes pero igual se deben implementar):
init(ServletConfig config): Método invocado luego de crear el Servlet. Permite brindar parámetros de configuración luego de iniciar el Servlet. Estos parámetros pueden ser utilizados para iniciar recursos, tal como abrir una conexión a base de datos o indicar una carpeta donde se encontrarán archivos que necesitan procesarse.
service(ServletRequest req, ServletResponse res): Método que permite atender una petición hecha al servidor. Requiere como parámetros información sobre la petición, que se encuentra en ServletRequest, y los elementos que se escribirán como parte de la respuesta, que se encuentra en ServletResponse.
destroy(): Método que se ejecuta previo a la eliminación del Servlet. Este método debe contener código para liberar cualquier recurso utilizado por la instancia del servlet. Al decir que el servlet se "elimina" en realidad se deja de utilizar para atender peticiones, y luego la memoria que ocupa puede ser reclamada por el Garbage Collector.
Para facilitar el desarrollo de los servlets, se proveen dos clases que ya implementan esta interfaz y permiten a los desarrolladores concentrarse en trabajo más puntual.
La primera clase es GenericServlet. Esta clase abstracta implementa la interfaz Servlet y provee funcionalidad básica para casi todos los métodos, con excepción del método service.
La segunda clase es HttpServlet. Esta clase abstracta extiende de GenericServlet e implementa el método service. Además, provee un método service(HttpServletRequest req, HttpServletResponse res) que facilita la ejecución de métodos asociados a los verbos HTTP. Esta clase también provee los métodos doGet, doPost y otros también importantes: doPut, doDelete, doHead, doOptions, doTrace, para soportar otros verbos HTTP. En la implementación de este método service existe el siguiente fragmento de código que te explica cuándo se ejecuta cada método doXxx (obtenido del código de javax.servlet.http.HttpServlet en su versión 3.1.0):

~~~
protected void service(HttpServletRequest req, HttpServletResponse resp)
    throws ServletException, IOException
{
    String method = req.getMethod();
    //si el método es GET
    if (method.equals(METHOD_GET)) {
        long lastModified = getLastModified(req);
        if (lastModified == -1) {
            // servlet doesn't support if-modified-since, no reason
            // to go through further expensive logic
            doGet(req, resp);
        } else {
            long ifModifiedSince = req.getDateHeader(HEADER_IFMODSINCE);
            if (ifModifiedSince < lastModified) {
                // If the servlet mod time is later, call doGet()
                // Round down to the nearest second for a proper compare
                // A ifModifiedSince of -1 will always be less
                maybeSetLastModified(resp, lastModified);
                doGet(req, resp);
            } else {
                resp.setStatus(HttpServletResponse.SC_NOT_MODIFIED);
            }
        }
    //si el método es HEAD
    } else if (method.equals(METHOD_HEAD)) {
        long lastModified = getLastModified(req);
        maybeSetLastModified(resp, lastModified);
        doHead(req, resp);
    //si el método es POST
    } else if (method.equals(METHOD_POST)) {
        doPost(req, resp);
    //si el método es PUT
    } else if (method.equals(METHOD_PUT)) {
        doPut(req, resp);
    //si el método es DELETE
    } else if (method.equals(METHOD_DELETE)) {
        doDelete(req, resp);
    //si el método es OPTIONS
    } else if (method.equals(METHOD_OPTIONS)) {
        doOptions(req,resp);
    //si el método es TRACE
    } else if (method.equals(METHOD_TRACE)) {
        doTrace(req,resp);
    //si el método es desconocido, no lo soporta
    } else {
        //
        // Note that this means NO servlet supports whatever
        // method was requested, anywhere on this server.
        String errMsg = lStrings.getString("http.method_not_implemented");
        Object[] errArgs = new Object[1];
        errArgs[0] = method;
        errMsg = MessageFormat.format(errMsg, errArgs);
        resp.sendError(HttpServletResponse.SC_NOT_IMPLEMENTED, errMsg);
    }
}
~~~
