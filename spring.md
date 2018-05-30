## Injection de dépendance
délégation de la création des objets au framework
on peut faire varier la nature des objets en modifiants les configurations

`` @Component `` = spring va créer un bean
un bean est un singleton par défaut

``@ComponentScan`` = recherche de Bean

`` @Configuration``= classe de configuration

`` @AutoWired``= injection de Bean ; peut être posé sur un champs, un setter, un constructeur...
Bonne pratique = injection par constructeur

`` @ContextConfiguration `` s'utilise dans le cas du test, pas dans le cadre de production

## Rappel sur les exceptions
Error = crash de la JVM
RuntimeException = exception non checkée
Exception = exception checkée qui doit être gérée programmatiquement soit avec un try catch, soit avec un throws dans la méthode

## Spring JDBC
ResultSetExtractor dans le cas où on a n lignes SQL qui correspondent à 1 seul objet Java

## Rappel JPA
1. Dépendances Maven : Hibernate (implémentation de JPA ; scope=runtime), driver BDD (scope=runtime), API (scope=compile)
2. Créer les entités, la configuration META-INF/persistence.xml
3. Persistence.createEntityManagerFactory("fichierConfig"), l'EMF crée l'EntityManager ; 1 instance d'EM par unité de travail

3 conditions pour avoir une entité JPA valide :
  1. ``@Entity``
  2. ``@Id``
  3. Constructeur sans paramètre
Tous les champs sont automatiquement mappés

## Spring JPA
`@Transactional` : quand on appelle la méthode, une transaction est ouverte avant et commitée après

## Spring Web MVC
Bean controller remplace servlet

## Rappels généraux (revue de code)
### POM.xml
finalName = nom du package de notre application
``<finalName>paie</finalName>``
mvn package donne un paie.war

### WebAppInitializer
Contexte = instance de l'application Spring
Quand on fait du Spring, on commence toujours par créer le contexte avec une configuration
On crée une servlet "dispatcher" = contrôleur frontal
On ajoute un listener pour détecter démarrage et arrêt de l'application

### WebAppConfig
Seule configuration qui compte dans notre application spring
``@EnableWebMVC`` On active le support de Spring MVC
On utilise un ViewResolver car Spring supporte d'autres formats que les jsp

### DataSourceMySqlConfig
``@PropertySource("app.properties")`` permet d'externaliser les informations de connexion dans un fichier app.properties

### JpaConfig
Configuration nécessaire pour utiliser JPA
support de l'annotation ``@Transactionnal``

JpaRepository pour utiliser Spring Data JPA

### StartUpAppListener
exécution de la méthode initialiser quand le contexte Spring est entièrement chargé
