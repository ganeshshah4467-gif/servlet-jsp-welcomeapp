# 🌐 Servlet + JSP Welcome App

A simple **Java Web Application** demonstrating both:
- ✅ Annotation-based configuration (`@WebServlet`)
- ✅ Traditional `web.xml` servlet mapping  

This project was built using **Eclipse IDE** as part of the **Technohacks Internship**.

---

## 🚀 Features
- Simple `WelcomeServlet` returning a welcome message  
- JSP page rendering dynamic content (`${message}`)  
- Static home page (`index.html`) with a link to servlet  
- Modern CSS-styled UI (`style.css`)  
- Demonstrates **two ways** of servlet configuration:
  - **Annotation** → `@WebServlet("/welcome")`
  - **XML mapping** → `web.xml` (commented but included for learning)

---

## 🛠 Tech Stack
- Java 17+  
- Jakarta Servlet API 5.0 (Tomcat 10 or above)  
- JSP  
- Eclipse IDE  
- HTML5, CSS3  


## ▶️ How to Run (Eclipse + Tomcat)

1. **Clone the repository**
   ```bash
   git clone https://github.com/Gourav3308/servlet-jsp-welcomeapp.git
   cd servlet-jsp-welcomeapp


Import into Eclipse
Open Eclipse → File → Import → Existing Projects into Workspace
Select the folder

Run on Tomcat
Right-click project → Run As → Run on Server
Choose Tomcat 10 (or higher)

Access in browser
http://localhost:8080/servlet-jsp-welcomeapp/

index.html → Landing page
welcome → Servlet → JSP page with dynamic message


🔍 Servlet Configuration Examples
@WebServlet("/welcome")
public class WelcomeServlet extends HttpServlet { ... }

web.xml
<servlet>
    <servlet-name>WelcomeServlet</servlet-name>
    <servlet-class>com.technohacks.servlet.WelcomeServlet</servlet-class>
</servlet>

<servlet-mapping>
    <servlet-name>WelcomeServlet</servlet-name>
    <url-pattern>/welcome</url-pattern>
</servlet-mapping>


📌 About

This project was created as part of the Technohacks Internship to demonstrate:
Servlet basics
JSP integration
Both annotation and XML-based configuration in Java web apps

👨‍💻 Author: Gourav Kumar
🔗 GitHub: @Gourav3308
