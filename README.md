Included here is a maven archetype for the Across Module and an Angular front-end

The base module is available on **[Lamis Base](https://github.com/mattae/lamis-base.git)**. Clone it and review classes, especially ``org.lamisplus.modules.base.configurer.DynamicModuleImportConfigurer``

To create a project using the maven archetype, the archetype must be first installed to your local maven repository. Navigate to where you have ``lamis-archetype-1.0.0.jar`` and run the following:
``mvn install:install-file -DgroupId=com.mattae.lamis -DartifactId=lamis-archetype -Dversion=1.0.0 -Dpackaging=jar -Dfile=lamis-archetype-1.0.0.jar``
``mvn install archetype:update-local-catalog``

Subsequently, create a new project from the archetype by running the following command ``mvn archetype:generate -DarchetypeGroupId=com.mattae.lamis -DarchetypeArtifactId=lamis-archetype -DarchetypeVersion=1.0.0 -DarchetypeCatalog=local``
Supply required information to create a project.

A compiled base application is available on **[LAMIS Web](https://drive.google.com/file/d/1WStVi-08_AKaEOZrh3l0VIMmcM-kyCoB/view?usp=sharing)**. Test your sample module by deploying to the web app.


