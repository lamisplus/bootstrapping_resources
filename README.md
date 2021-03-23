Included here is a maven archetype for the Across Module and an Angular front-end

The base module is available on **[Lamis Base](https://github.com/mattae/lamis-base.git)**. Clone it and review classes, especially ``org.lamisplus.modules.base.configurer.DynamicModuleImportConfigurer``

To create a project using the maven archetype, the archetype must be first installed to your local maven repository. Navigate to where you have ``lamis-archetype-1.1.0.jar`` and run the following:

```mvn install:install-file -DgroupId=com.mattae.lamis -DartifactId=lamis-archetype -Dversion=1.0.0 -Dpackaging=jar -Dfile=lamis-archetype-1.1.0.jar```

```mvn install archetype:update-local-catalog```

Subsequently, create a new project from the archetype by running the following command 
```mvn archetype:generate -DarchetypeGroupId=com.mattae.lamis -DarchetypeArtifactId=lamis-archetype -DarchetypeVersion=1.1.0 -DarchetypeCatalog=local```
Supply required information to create a project.

A compiled base application is available on **[LAMIS Web](https://drive.google.com/file/d/1wWPQt1fIrNPTn0iAoe6UjdzptX7E6S6-/view?usp=sharing)**. Test your sample module by deploying to the web app.
Please create a fresh database for use. The deployment creates a user with username `admin` and password `admin`. 

Default database connections are:
- username: `postgres`
- password: `lamis`
- database-name: `lamis`
- host: `localhost`
- port: `5432`

Should you want to use a different configuration, create an `application.yml` and add the following section reflecting your changes

```
spring:
    datasource:
        username: postgres
        password: lamis
        driver-class-name: org.postgresql.Driver
        url: jdbc:postgresql://127.0.0.1:5432/lamis?stringtype=unspecified
```

Then start the application with `--spring.config.additonal-location` eg `java -jar lamis.jar --spring.config.additonal-location=application.yml`

An updated version of the artifact is available on **[LAMIS Maven Artifact](https://drive.google.com/file/d/1LGLGxvWEg2ubpXvEmIyrMfTH_WRxww8n/view?usp=sharing)**. 
The archetype frontend option takes one of the following values:
- 0: Only backend
- 1: With Angular frontend
- 2: With React frontend
Both frontend share the same backend and implements a similar frontend to interact with the backend. 
  
If you want to test both frontends at the same time, change the menu state/name and the corresponding routePath in the module/component section(s) in `module.yml`



