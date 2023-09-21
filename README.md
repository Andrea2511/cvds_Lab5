# LABORATORIO 5 - SPRING MVC INTRODUCTION

## INTEGRANTES
- Andrea Valentina Torres Tobar
- Carolina Medina Acero 



## INTRODUCCIÓN A PROYECTOS WEB ~ RESPUESTAS

### PARTE I. - JUGANDO A SER UN CLIENTE HTTP
- Revise el resultado obtenido

     ![](/src/main/resources/img/301.png)


- ¿Qué codigo de error sale?revise el significado del mismo en la lista de códigos de estado HTTP.
    - Sale el codigo "301 Moved Permanently" que significa  que el recurso se ha movido permanentemente  a una nueva ubicación.

- ¿Qué otros códigos de error existen?, ¿En qué caso se manejarán?
    - Respuestas informativas (100–199),
    - Respuestas satisfactorias (200–299),
    - Redirecciones (300–399),
    - Errores de los clientes (400–499),
    - Errores de los servidores (500–599).

- Ahora, solicite GET /html. HTTP/1.1 Host: www.httpbin.org ¿Qué se obtiene como resultado?
    - obtenemos un parrafo  de la novela Moby-Dick osea obtemos  un 200 OK  La solicitud se completó con éxito, y la respuesta contiene la información solicitada.

-  ¿Cuál es la diferencia entre los verbos GET y POST?
    - Get: Se utiliza para solicitar datos  de un recurso especificado.
        - Envio de datos:  los datos se envían como parte de la URL, a través de los parámetros de consulta  ejemplo :(?).
        - cache:Almacenan temporalmente datos. 

    - Post:  se utiliza para enviar datos al servidor para su procesamiento. 
        - Envio de datos: los datos se envían en el cuerpo de la solicitud, no en la URL a diferencia del get. 
        - cache: los datos no se almacenan en el navegador.

-  ¿Qué otros tipos de peticiones existen?

   - PUT: Se utiliza para actualizar o crear un recurso en el servidor en una ubicación específica. 
   - DELETE: Se utiliza para eliminar un recurso específico en el servidor en una ubicación determinada. 
   - PATCH: Se utiliza para aplicar modificaciones parciales a un recurso en el servidor.
   - HEAD: Similar a GET, pero se utiliza para obtener solo los encabezados de respuesta sin el cuerpo del recurso.
   - OPTIONS: Se utiliza para obtener información sobre las opciones de comunicación disponibles para el recurso de destino. 
   - CONNECT: Se utiliza para establecer una conexión de red con el recurso de destino, a menudo para establecer una conexión segura a través de un proxy.
   - TRACE: Se utiliza para realizar un seguimiento del camino de una solicitud a través de servidores intermedios. Generalmente se usa con fines de depuración y diagnóstico.

- ¿Cuáles son las diferencias de "curl -v" y "curl -i" con los diferentes parámetros?
Ambas sirven para realizar solicitudes http, por lo que vemos el curl -v habilita una información mas detallada nos muestra tanto la solicitud como las respuesta   y  la de  curl -i  solo nos muestra los encabezados de la respuesta http.

    ![](/src/main/resources/img/curl.png)

### PARTE II. - HACIENDO UNA APLICACIÓN WEB DINÁMICA USANDO EL PATRÓN MVC

![](/src/main/resources/img/Home.png)
![](/src/main/resources/img/HelloName.png)
![](/src/main/resources/img/HelloWorld.png)

Análisis:

- ¿Por qué MVC tiene ese nombre?

Porque sigue el patrón de diseño modelo, vista, controlador, el cual tambien nos permite usar fácilmente inversión de control e inyección de dependencias

- ¿Cuáles son las ventajas de usar MVC?

Posee diversas ventajas, entres esas tenemos:

1. Es ligero, ya que, utiliza un contenedor liviano para desarrollar e implementar la aplicación
2. Separa cada rol, determinando un objeto para que se encargue del modelo, vista y controlador
3. Permite un desarrollo rápido
4. permite utilizar objetos comerciales
5. Permite proporcionar anotaciones para redirigirse fácilmente a una página
6. Se puede probar facilmennte

- ¿Qué diferencia tiene la estructura de directorio de este proyecto comparado con las de proyectos pasados?

Se encuentra en recursos dos carpetas nuevas, una carpeta llamada stactic y una llamada templates

- ¿Qué anotaciones usaste y cual es la diferencia entre ellas?

Se usaron las siguientes anotaciones:

* `@getMapping` Se utiliza para asignar solicitudes web a métodos del Spring Controller.

* `@requestMapping` Se utiliza como un shortcut para @RequestMapping(method = RequestMethod.GET)

* `@postMapping` Se utiliza como un shortcut para @RequestMapping(method = RequestMethod.POST)

### PARTE III. - APLICACIÓN MVC PARA CONSUMO DE SERVICIO RESTful

Usando la arquitectura MVC del punto anterior (el proyecto anterior), realice una aplicación simple qué permita navegar gráficamente sobre esta API https://jsonplaceholder.typicode.com/todos/1, puede guiarse de tutoriales como https://medium.com/@nutanbhogendrasharma/consume-rest-api-in-spring-boot-web-application-354c404850f0

![](/src/main/resources/img/Todo1.png)
![](/src/main/resources/img/Todo200.png)

Preguntas:

- ¿Qué es RESTful?

Es una interfaz que se usa para que dos sistemas intercambien información de manera segura a través de Internet.

- Si utilizó un framework como Boostrap CSS para qué el apartado gráfico se vea más profesional, ¿en qué capa se haría su uso?

En la vista, ya que se im porta en el html para aplicar todos sus estilos





### PARTE IV. - APLICACIÓN MVC JUEGO


![](/src/main/resources/img/inicio.png)
![](/src/main/resources/img/ganaste.png)

¿Qué pasa si abro el sitio de juegos en dos navegadores difententes?

![](/src/main/resources/img/interferencia.png)

- Intefieren entre si, cada jugador realiza un movimiento lo que hace que se descuadren los valores, lo que significa que solo existe una sesión del juego  accesible desde cualquier  ventada del navegador. 

Si quisiera qué a cada jugador le aparecieran independientemente sus respectivos saldos. ¿Qué habría que hacer?

- Crear una instacia  por cada pestaña o utilizar cuentas de usuario diferentes. 


### REFERENCIAS
    - https://developer.mozilla.org/es/docs/Web/HTTP/Methods
    - https://developer.mozilla.org/es/docs/Web/HTTP/Status 