Pour tester l'application, voici les étapes à suivre :

Configuration et Utilisation de l'Application
Prérequis
Java 11+
Maven
PostgreSQL
ActiveMQ
IBM MQ
Configuration
Base de Données (BDD)

Assurez-vous que PostgreSQL est installé et en cours d'exécution. Créez une base de données nommée messagerie.

spring:
  datasource:
    url: jdbc:postgresql://localhost:5432/messagerie
    username: postgres
    password: password
    driver-class-name: org.postgresql.Driver
  jpa:
    hibernate:
      ddl-auto: update
    show-sql: true
JMS

Assurez-vous que ActiveMQ est installé et en cours d'exécution.

spring:
  jms:
    broker-url: tcp://localhost:61616
IBM MQ

Assurez-vous que IBM MQ est installé et en cours d'exécution.

ibm:
  mq:
    queueManager: QM1
    channel: DEV.ADMIN.SVRCONN
    connName: localhost(1414)
    user: admin
    password: passw0rd
    queue: DEV.QUEUE.1
Serveur

server:
  port: 8080
Démarrage de l'Application
Cloner le dépôt

git clone https://github.com/mouhssine65/messaging.git
cd messaging
Construire et démarrer l'application

mvn clean install
mvn spring-boot:run
Utilisation
Envoyer un message à la file d'attente

Utilisez l'API suivante pour envoyer un message :

curl -X POST "http://localhost:8080/api/queue/send?message=cacib"
Vérifier les données dans le front-end

Accédez au front-end de l'application pour voir les données sauvegardées.

Pour plus de détails, vous pouvez consulter le dépôt GitHub ici.
Si vous avez des questions ou besoin d'aide supplémentaire, n'hésitez pas à demander !
