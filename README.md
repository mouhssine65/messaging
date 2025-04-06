Pour tester l'application, voici les étapes à suivre :

Démarrer le front-end et le back-end :
Assurez-vous que les deux parties de l'application sont correctement configurées et lancées.


Envoyer un message à la file d'attente (MQ) :
Utilisez l'API suivante pour envoyer un message : http://localhost:8080/api/queue/send?message=cacib
Cela enverra un message à la file d'attente qui sauvegardera les données dans la base de données.


Vérifier les données dans le front-end :
Vous pouvez voir les données sauvegardées en accédant au front-end de l'application sur home page ou en base de donées
url : http://localhost:4200/


Pour plus de détails, vous pouvez consulter le dépôt GitHub ici.
Si vous avez des questions ou besoin d'aide supplémentaire, n'hésitez pas à demander !
