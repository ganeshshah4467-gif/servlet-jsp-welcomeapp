# Servlet + JSP Welcome App

A small Java web application demonstrating a Jakarta Servlet forwarding a request to a JSP page.

## Features

- Static landing page at `index.html`
- Annotation-based servlet mapping with `@WebServlet("/welcome")`
- Request attributes passed from the servlet to `welcome.jsp`
- Simple CSS styling
- Maven WAR packaging

## Tech stack

- Java 17
- Apache Maven 3.6+
- Jakarta Servlet API 6.0
- Apache Tomcat 10.1
- JSP, HTML5 and CSS3

## Project structure

```text
servlet-jsp-welcomeapp/
├── pom.xml
└── src/
    └── main/
        ├── java/com/technohacks/servlet/WelcomeServlet.java
        └── webapp/
            ├── index.html
            ├── welcome.jsp
            ├── css/style.css
            └── WEB-INF/web.xml
```

## Build the application

Make sure Java 17 and Maven are installed, then run these commands from the directory containing `pom.xml`:

```bash
mvn clean package
```

Maven compiles the Java source and creates:

```text
target/servlet-jsp-welcomeapp.war
```

## Run on Tomcat 10.1

1. Copy `target/servlet-jsp-welcomeapp.war` into Tomcat's `webapps/` directory.
2. Start Tomcat.
3. Open [http://localhost:8080/servlet-jsp-welcomeapp/](http://localhost:8080/servlet-jsp-welcomeapp/).
4. Select **Enter** to visit the servlet, or open [http://localhost:8080/servlet-jsp-welcomeapp/welcome](http://localhost:8080/servlet-jsp-welcomeapp/welcome) directly.

Tomcat 10.1 supplies the Servlet API at runtime, so the dependency is declared with Maven's `provided` scope and is not bundled in the WAR.

## Servlet request flow

```text
index.html
    |
    v
/welcome
    |
    v
WelcomeServlet.doGet()
    |
    +--> request.setAttribute("message", ...)
    |
    v
welcome.jsp
    |
    v
Displays the message using ${message}
```

## Servlet mapping

The servlet is mapped using the `@WebServlet("/welcome")` annotation in `WelcomeServlet.java`. The `web.xml` file contains the Jakarta EE 6.0 web-app descriptor and does not duplicate the annotation mapping.
