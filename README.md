Californium (Cf) CoAP framework
===============================

Implements [RFC7252](http://tools.ietf.org/html/rfc7252)

Californium is a Java CoAP implementation for IoT Cloud services.
Thus, the focus is on scalability and usability instead of resource-efficiency
like for embedded devices. Yet Californium is also suitable for embedded JVMs.

Maven
-----

Use `mvn clean install` in the Cf root directory to build everything.
Executable JARs of the examples with all dependencies are copied to ./run/.

### Californium in Maven Project

To use Californium as library in your projects, add the following dependencies
and Maven repositories to your pom.xml:

```xml
  <dependencies>
    ...
    <dependency>
            <groupId>org.eclipse.californium</groupId>
            <artifactId>californium-core</artifactId>
            <version>1.0.0-SNAPSHOT</version>
    </dependency>
    ...
  </dependencies>
  
  <repositories>
    ...
    <repository>
      <id>repo.eclipse.org</id>
      <name>Californium Repository - Releases</name>
      <url>https://repo.eclipse.org/content/repositories/californium-releases/</url>
    </repository>
    <repository>
      <id>repo.eclipse.org</id>
      <name>Californium Repository - Snapshots</name>
      <url>https://repo.eclipse.org/content/repositories/californium-snapshots/</url>
    </repository>
    ...
  </repositories>
```

Eclipse
-------

The project also includes the project files for Eclipse. Make sure to have the
following before importing the Californium (Cf) projects:

* [Eclipse EGit](http://www.eclipse.org/egit/)
* [m2e - Maven Integration for Eclipse](http://www.eclipse.org/m2e/)
* UTF-8 workspace text file encoding (Preferences &raquo; General &raquo; Workspace)

Then choose *[Import... &raquo; Git &raquo; Projects from Git &raquo; Local]*
to import `californium` into Eclipse.

### Without Any Maven Support

In case you are using plain Eclipse projects without Maven, you also need to
clone and import the [element-connector](https://github.com/eclipse/californium.element-connector).
Add this project to Properties &raquo; Java Build Path &raquo; Projects.

Interop Server
--------------

A test server is running at [coap://iot.eclipse.org:5683/](coap://iot.eclipse.org:5683/).
The root resource responds with its current version. More information
can be found at [https://projects.eclipse.org/projects/technology.californium](https://projects.eclipse.org/projects/technology.californium).

Another interop server with a different implementation can be found at
[coap://coap.me:5683/](coap://coap.me:5683/).
More information
can be found at [http://coap.me/](http://coap.me/).
