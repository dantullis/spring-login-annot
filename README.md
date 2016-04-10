# Java Spring Annotation Based Project with Custom Login(CSRF protected)

This is a starter Java web application with JSP front-end. It is based on the newer [Spring][httpSpring.io] "Java config annotations", rather than XML configuration(or even the mixed "XML configuration with annotations"). 

This is a 100% starter. There is not even any stylesheet formatting.

### PROJECT ATTRIBUTES:
- In-memory authentication(later projects will show JDBC or LDAP authentication)
- Custom JSP login form
- Secure login and logout with CSRF protection
- Run project in light-weigth servlet contatiner in IDE
- Easily import project into [Spring Tool Suite][httpSpringToolSuite] IDE
- [Maven][httpMavenRepo] project eases dependency needs

### TOOLING REQUIREMENTS:
- Download and install the Java JDK. Not the SE or JRE versions.
- Download and install Spring Tool Suite. It is based on the Eclipse IDE

### TOOL DOWNLOAD URLs:
- Java JDK - (http://www.oracle.com/technetwork/java/javase/downloads/index.html)
- STS IDE - (https://spring.io/tools/sts/all)

### PROJECT DOWNLOAD
First, you will have to download it. If you have a local installation of git, you can
do it by simply cloning this repository:

```
    git clone https://github.com/dantullis/spring-login-annot.git
```

If you don't have git installed, you can download a `.zip` by pressing on the 
*Download zip* button in the upper side of this page.

Note your new `PROJECT-FOLDER` as either the folder you cloned to or the folder you downloaded and unzipped t.

### IMPORT PROJECT INTO STS
- Open the Spring Tool Suite IDE.
- Select or create a new workspace location for this project.
- From the menu select Menu--> Import...
- In the "import" window expand the "General" folder.
- Choose "Existing Projects into Workspace" and press "Next".
- In the "Import Projects" press on the "Browse..." button next to "Select root directory".
- Browse to the `PROJECT-FOLDER` noted above.
- You should now see a project selected in the "Projects" list box.
- Make sure you check "Copy projects into workspace" or you will have your source code and project setup in two separate folders. Some will make a case for either model. 
- Press the "Finish" button.

### RUN PROJECT:
You will see "building workspace..." in the bottom right corner of the STS IDE. That means that the project dependencies are being built. Among them are the dependencies listed in the pom.xml file. It may or may not assign the target runtime.

Once completed you can Right-click on the project and select "Run As --> Run on Server". 
If you get a new window with "Pivotal tc Server..." selected then check "Always use this server when running this project" and press "Finish".

You should now see the home page listed in a new window in the STS IDE.

### TEST PROJECT
 - Open a web browser and navigate to http://localhost:8080/springloginannot/
 - Click on the link "Link to restricted access page". You should get a custom login page.
 - Enter "user" for the username.
 - Enter "user" for the password.
 - On the restricted page press the "logout" link.
 - Press the browser back button and you will not be allowed in and presented with the lgon screen again.
 - Paste http://localhost:8080/spring-login-annot/admin into the browser and if logged out you should not be allowed in.

### DEBUG PROJECT(Java)
To debug the Java code in the project do the following:
 - Place a break point in the Java code 
 - Right-click on the project name and select "Debug as --> Debug on Server".
 - Exercise the web application and you will see a window asking you to use the "debug perspective".

### PROBLEMS
If you see a red x on the project name it may be due to the target runtime not assigned. You can verify this by doing the following:

 - Right-click on project name.
 - Select "Properties", then "Targeted Runtimes".
 - Check "Pivotal tc Server..." if not already selected.
 
You can look in the following places for other problems:
 - Console tab in the STS IDE
 - Problems tab in the STS IDE. Enable it(Window-->Show View --> Other --General -- Problems)
 - Log files located in a place similar to: sts-bundle/pivotal-tc-server-developer-3.1.3.SR1/base-instance/logs

License
----

MIT

[//]: # (These are reference links used in the body of this note and get stripped out when the markdown processor does its job. There is no need to format nicely because it shouldn't be seen. Thanks SO - http://stackoverflow.com/questions/4823468/store-comments-in-markdown-syntax)

   [httpSpring.io]: <https://spring.io/>
   [httpSpringToolSuite]: <https://spring.io/tools>
   [httpMavenRepo]: <http://mvnrepository.com/>
   [httpSpring.io]: <https://spring.io/>
