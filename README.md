# lab-4-subject-danim

This is a Spring Cloud Eureka client project that is registered and discovered in the **lab-4-eureka-server-danim** to be accessible from the client project **lab-4-sentence-danim**.

# Starting this client repository

The steps to used it are:
- Start the **lab-4-eureka-server-danim** repo and check it's started correctly in http://localhost:8010
- Start the class annotated with @SpringBootApplication
- Start the rest of client services ([See README from lab-4-eureka-server-danim](https://github.com/dlmogft/lab-4-eureka-server-danim/blob/main/README.md))

# Dependencies

Eureka Discovery Client, Config Server (if uses Spring Cloud Config)

# Tips

- The project starting class is annotated with **@SpringBootApplication** and also with @EnableDiscoveryClient to indicate that acts as an Eureka Client
- The **application.yml** config file specifies the URI of the Eureka Server repo **lab-4-eureka-server-danim**. If the project also uses the Spring Cloud Config feature, it specified instead the URI of the Git repository where the configuration files are stored, **spring-cloud-server-config-danim** and also the profile to read the correct **application-<profile>.yml** file from this Git repository.
- The **SubjectRestController** has a variable that points to the words key in the **application.yml**, or in the **application-<profile>.yml** file from the **spring-cloud-server-config-danim** Git repository if the client uses the Spring Cloud Config feature
