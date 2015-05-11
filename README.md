## Description
This project is startup project created to quickly start a Spring MVC 4.x Web Application (.war). The project is deployable on any Web Server (Apache Tomcat for eg.)

### AutoStart and Spring Boot Starter Web
In order to make the application auto-start using embedded Tomcat (or Jetty), add the spring-boot-starter-web to the list dependencies and use  "com.michir.projects.spring.starup.Application* main class to start application.

## Dependency management
The project is based on Maven (3.x).

## Java & JEE version
The project is configured for Java 1.7 @see the maven property java.version.
The (web) project is based on Servlet 3.x @see dependency management

## Project dependencies
The artifacts dependencies are managed with Spring Boot (1.2.3.RELEASE)

## Java configuration entry points
Spring facets (Web MVC, Servlet, ...) are configured with Java using Spring Boot *@EnableAutoConfiguration*. The *@ComponentScan* is configured to scan the (sub-)packages of *com.michir.projects*.

### @(Rest)Controller
Spring MVC (Spring DispatcherServket) is configured in the class *com.michir.projects.spring.startup.WebInitializer*

The Spring stuff (Controllers mapping) is bound to */spring/**

The class *WebConfig* (within the same package) configures the ViewResolver load views from */WEB-INF/jsp/* (@see Spring UrlBasedViewResolver)

#### @Controller's
*com.michir.projects.spring.controllers.MyViewController* is such a (JSP) Viewexample, accessible through [http://localhost:8080/springmvc-4.x/spring/view/any_name_here](http://localhost:8080/springmvc-4.x/spring/view/any_name_here)

#### @RestController's
*com.michir.projects.spring.controllers.MyRestController* is an example of a Rest Controller (returning json), accessible through [http://localhost:8080/springmvc-4.x/spring/rest/any_name_here](http://localhost:8080/springmvc-4.x/spring/rest/any_name_here)

### @Scheduling
The package *com.michir.projects.spring.scheduling* contains an example of @Scheduking configuration.

### Properties
The package *com.michir.projects.spring.configuration* contains examples of @PropertySource for loading configuration and properties files.



