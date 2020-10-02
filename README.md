# Eureka server

## Pré-requis

Assurez-vous d’avoir bien installé PostgreSQL sur votre machine. Si ce n’est pas
le cas rendez-vous à l’adresse suivante :
https://www.postgresql.org/download/

Egalement, assurez-vous d'avoir une version de Java supérieur ou égal à 8 installé sur votre machine.
Si ce n'est pas le cas : 
https://www.oracle.com/fr/java/technologies/javase/javase-jdk8-downloads.html

Veillez également à avoir installé et configuré maven comme suit :
https://maven.apache.org/install.html

## Configuration

La configuration du projet se trouve dans le fichier application.properties du dossier src/main/ressources/

## Installation du projet en local

Faites un clone du projet en téléchargeant l'archive de la branche master ou bien la commande :
```bash
git clone https://github.com/Mr-Nugget/_Eureka
```

A la base du projet lancer la commande maven : 
```bash
mvn clean install
```
Ceci va créer un build du projet, vous retrouverez le fichier .jar dans le dossier target de l'application.


## Déploiement

Lancer le jar généré dans le dossier target de l'application via la commande suivante :
```bash
java -jar monarchive.jar
```
ou bien lancer le projet directement depuis votre éditeur de code en faisant un run de l'application java.

Veillez à bien démarrer ce microservice avant les autres microservices métiers.

## Dépendances

- Spring Cloud Config
- Spring boot
- JUnit
- Log4J
- Eureka Server

## Présentation

Voici le microservice Eureka server, permettant aux différentes instances des microservices de s'enregistrer et ainsi permettre une équilibre de charge lorsqu'un module applicatif est trop utilisé. 
La balance des charges est gérée par l'API Gateway ZUUL.
