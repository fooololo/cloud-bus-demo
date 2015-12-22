Cloud Config Server
=====================================
Spring Cloud Config provides server and client-side support for externalized configuration in a distributed system.


### Settings

Please change git url in application.properties

### how to use

1. please add spring cloud dependency in dependency management: 

        <dependency>
             <groupId>org.springframework.cloud</groupId>
             <artifactId>spring-cloud-starter-parent</artifactId>
             <version>Angel.SR4</version>
             <type>pom</type>
             <scope>import</scope>
        </dependency>
2. Add dependency in your pom.xml.


        <dependency>
           <groupId>org.springframework.cloud</groupId>
           <artifactId>spring-cloud-starter-config</artifactId>
         </dependency>

2. Bootstrap Environment from server. In your bootstrap.properties add following code:


    spring.cloud.config.uri: http://localhost.com:8888/

3. verify your properties:


    $ curl http://localhost:8888/appname.properties

4. add @RefreshScope for your bean
5. POST to /refresh to refresh the configuration
### how to write properties file

1. application.properties: global properties for all apps
2. appname.properties: app properties
3. appname-profile.properties: app profile properties


