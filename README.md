# cvds_Lab5

### Parte II - Haciendo una aplicación dinámica usando el patron MVC:

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

