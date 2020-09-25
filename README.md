# Eureka server

## Présentation

Voici le microservice Eureka server, permettant aux différentes instances des microservices de s'enregistrer et ainsi permettre une équilibre de charge lorsqu'un module applicatif est trop utilisé. 
La balance est généré via l'API Gateway ZUUL.


## Déploiement

Lancer le main de l'application via votre éditeur java (eclipse ou IntelliJ) ou en faisant un build du projet maven `mvn clean install` puis éxécutez le point jar généré dans le dossier target via `java -jar ******.jar`
