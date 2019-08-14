# EMERGENTES II #
1)  Explique que son los sistemas empresariales
*es un sistema de información integral que incorpora los procesos operativos y de negocio de una empresa, por ejemplo: producción, ventas, compras, logística, contabilidad (de varios tipos), gestión de proyectos, inventarios y control de almacenes, pedidos, nóminas, etc.*

#### 2) Describa cuales son las características más importantes de una aplicación empresarial

*Disponibilidad

*Capacidad

*Extensibilidad

*Flexibilidad

*Manejabilidad

*Rendimiento

*Confiabilidad 

*Reusabilidad

*Escalabilidad

*Seguridad 

*valides
#### 3) Investigue y proponga cinco (5) instituciones que requerirían aplicaciones de misión crítica. Justifique su respuesta 
*-Windows: Codigo Abierto*

*-Huawei: Propio Sistema Operativo no depender de Google*

*-Facebook: Mejorar su entorno*

*-Google: Mas publicidad y mejorar su entorno para no tener competencia*

*-Toshiba: Hacer mas publicidad en venta de computadoras*

#### 4) Explique cuáles son las diferencias entre la escalabilidad horizontal y escalabilidad vertical
*Escalabilidad Vertical:*
*El escalar hacia arriba un sistema viene a significar una migración de todo el sistema a un nuevo hardware que es mas potente y eficaz que el actual.*

*Escalabilidad Horizontal:*
*La escalabilidad horizontal consiste en potenciar el rendimiento del sistema desde un aspecto de mejora global, a diferencia de aumentar la potencia de una única parte del mismo.* 
#### 5) Que es un servidor Web y que es un servidor de aplicaciones 
*Servidor web:*
*Un servidor web o servidor HTTP es un programa informático que procesa una aplicación del lado del servidor, realizando conexiones bidireccionales o unidireccionales y síncronas o asíncronas con el cliente y generando o cediendo una respuesta en cualquier lenguaje o Aplicación del lado del cliente.*

*Servidor de aplicaciones:*
*Usualmente se trata de un dispositivo de software que proporciona servicios de aplicación a las computadoras cliente. Un servidor de aplicaciones generalmente gestiona la mayor parte (o la totalidad) de las funciones de lógica de negociación y de acceso a los datos de las aplicaciones.*
#### 6) Con un gráfico explique cómo funciona el protocolo HTTP 
https://image.slidesharecdn.com/presentacionhttp-https-dns-140922001131-phpapp02/95/presentacion-httphttpsdns-4-638.jpg?cb=1411345623
#### 7) Explique los elementos importantes de REQUEST en HTTP 
*En inglés, request significa pedir, solicitar. En efecto, la acción de escribir una dirección cualquiera en la línea de URL de tu navegador, se traduce en solicitar un determinado fichero a un servidor, o dicho en la jerga técnica, se le hace un request al servidor.* 

*El protocolo que utiliza el navegador (por defecto salvo que se indique otro, como el FTP) para dialogar con un servidor web es el llamado HTTP, que como habrás visto figura al principio de todas las direcciones web. No es necesario escribir el protocolo en los navegadores modernos, simplemente escribimos la dirección de la página solicitada, y el navegador añade delante de la misma su protocolo por defecto.*
#### 8) Explique los elementos importantes de RESPONSE en HTTP
*Igual que el navegador envía información al servidor, también en la respuesta se envían datos en la cabecera como el Content-Type que indica el tipo de contenido que se envía, si la respuesta está comprimida o el tipo de codificación que usa. También se indica que tipo de servidor sirve los contenidos e incluso el sistema operativo. Por razones de seguridad estos datos se pueden omitir o incluso falsear.*

*En Chrome, en las herramientas de programación(F12), en la pestaña NETWORK -> headers -> bajamos hasta ver la sección response-headers, aquí están todos los datos que envía el servidor* 
#### 9) Describa con un gráfico la arquitectura Java EE 
http://2.bp.blogspot.com/-Dnnoqh4KDs0/U9-sS6K_faI/AAAAAAAAAOc/s2FPr6g30o8/s1600/Captura.PNG
#### 10) Explique cuáles son los contenedores, componentes y servicios de Java EE
######Contenedores JAVA EE
*Java EE Server: La porción de tiempo de ejecución de un producto Java EE. provee los contenedores web y de ejb.*

*Contenedor EJB: Maneja la ejecución de los enterprise beans.*

*Contenedor Web: Maneja la ejecución de las paginas web, servlets y algunos componentes ejb para las aplicaciones Java EE.*

*Contenedor de aplicación cliente: Maneja la ejecución de la aplicación cliente no necesita un servidor de aplicaciones.*

*Contenedor Applet: Maneja la ejecución de applets, no necesita servidor de aplicaciones, consiste en un browser y el plugin web de java.*
######Componentes JAVA EE
*Capa CLiente: Navegador (HTML APPLET), Desktop (Aplicacion Java), Otros Dispositovos (Cliente JEE)*

*Capa Web: Contenedor Web (JavaServer Fases), (JSP/Facelets), (Java Servlent), (Plataforma Java EE),*

*Capa de Negocio: Contenedor EJB, (EJB), (EJB), (Plataforma Java EE)*

*Capa de Datos: (RBDMS), (Sistemas Legrados), (ERP)*

######Servicios JAVA EE
*JOnAS, un servidor de aplicaciones de código abierto de ObjectWeb*

*JBoss, desarrollado inicialmente por JBoss Inc y adquirido posteriormente por Red Hat. Existe una versión de código abierto soportada por la comunidad y otra empresarial.*

*Sun Java System Application Server Platform Edition 9.0, basado en GlassFish*

*Oracle WebLogic Application Server 10.0 (Antes BEA Systems)*

*Servidor de Aplicaciones SAP NetWeaver, Java EE 5 Edition de SAP*

*JEUS 6, un Servidor de aplicaciones específico de Linux de TmaxSoft*

*Apache Geronimo 2.0*

*IBM WebSphere Application Server Community Edition 2.0, based on Apache Geronimo*

*Oracle Containers for Java EE 11*

*GlassFish, un servidor de aplicaciones de código abierto de Sun*

*Apache OpenEJB via Apache Geronimo*
####11) Investigue los métodos más utilizados de las clases HttpServlet, HttpServletRequest y HttpServletResponse, y para cada uno de los métodos muestre un ejemplo.
######La clase HttpServlet: 
*es una clase que implementa la interfaz Servlet, incorporando además métodos específicos para servidores Web. Un uso típico de HttpServlet es el procesamiento de formularios html.

*Ejemplo*

import javax.servlet.*;
import javax.servlet.http.*;
import java.io.*;

public class HolaMundo extends HttpServlet {

  public void init(ServletConfig conf)
    throws ServletException {
    super.init(conf);
  }

  public void service(HttpServletRequest req, HttpServletResponse res)
    throws ServletException, IOException  {
    res.setContentType("text/html");
    PrintWriter out = res.getWriter();

    out.println("<html>");
    out.println("<body>");
    out.println("<h1>Hola Mundo</h1>");
    out.println("</body>");
    out.println("</html>");
  }
}
######Un objeto HttpServletRequist:
*Método que nos devuelve una referencia a la sesión HttpSession asociada a la petición actual.*

*Ejemplo*

protected void doGet(HttpServletRequest request, HttpServletResponse response) throws ServletException, IOException {
   HttpSession session = request.getSession();
   session.setMaxInactiveInterval(20*60);       
}
######Un objeto HttpServletResponse:
*Proporciona dos formas de devolver datos al usuario.*

*El método getWriter devuelve un Writer*

*El método getOutputStream devuelve un ServletOutputStream*
*Se utiliza el método getWriter para devolver datos en formato texto al usuario y el método getOutputStream para devolver datos binarios.

*Ejemplo*

PrintWriter out;
out = response.getWriter();
response.setContentType("text/html");
out.println("<html>");
out.println("<head><title>Mi Primer Servlet </title></head>");
out.println("<body>");
out.println("<h6>Este es mi Primer Servlet</h6>");
out.println("</body></html>");
