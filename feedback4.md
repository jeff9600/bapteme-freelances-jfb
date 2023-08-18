# Feedback 4

Hello "apprenant4",
J'espère que tu vas bien 🙂
Comme tu l'as demandé, je t'ai préparé un petit feedback du parcours S06.
Let's go !

## Avancée globale sur le projet

Alors j'avoue être surpris parce que tu as pris tout le parcours dans le désordre en fait 😅 
Difficile de jauger ton avancée parce que je vois que tu as même géré la partie CSRF et l'ajout d'utilisateur alors que cela faisait partie du megabonus. Sur ces parties il y a de bonnes choses mais, d'un autre côté, tu devrais vraiment suivre l'ordre logique de progression du parcours. Déjà parce que cela te donne une trame à suivre et que cela t'évite de partir dans tous les sens mais aussi parce que cela te permet de toucher à toutes les parties de l'appli côté front-end et back-end. Je vois clairement que le front ne t'intéresse pas en l'occurence 🤣
Sur le prochain parcours il faudra absolument que tu suives les étapes dans l'ordre et que tu ne prennes pas que ce qui t'interesse pour bien assimiler toutes les connaissances clés.

PS: Les bonus c'est fait pour être fait quand tu as tout terminé dans les étapes de base 🙂

Dans ce que tu as fait, il y a beaucoup de bonnes choses donc rien d'alarmant 😉

## Mes retours :

**Quelques petits ajustements sont à revoir :**

☑️ **Première chose**, comme tu n'as rien préparé pour la lecture de tes routes et que tu as eu le nez dans le code, tu n'as absolument rien testé sur ton navigateur. Il faudra que tu ailles voir la correction pour voir ce qu'il te manquait notamment la méthode show() que je te vois appeler alors qu'elle n'existe pas encore. Je trouve que cela aurait été bien que tu puisses tester via ton navigateur de temps en temps que ce que tu fais fonctionne.

☑️ N'hésite pas à bien répartir tes éléments dans des fichiers spécifiques pour améliorer
l'organisation de tes dossiers/fichiers. Par exemple, tu as intégré le tableau lié à tes routes directement dans ton index.php. Tu aurais pu créer un fichier routes.php et faire un require_once dans ton index.php ensuite. **Tu trouveras l'exemple dont je parle dans la correction du parcours**

☑️ **Au niveau de la sécurité**, Je ne crois pas avoir vu de requête préparée dans tes modèles ? Pense bien à le faire partout parce que c'est fondamental pour te protéger des injections SQL. Aussi concernant Git, pense bien à remplir ton .gitignore en ajoutant ton fichier config.ini cela permettra de dire à Git que tu ne veux pas qu'il prenne en compte ce fichier lors des commits etc. Cela est très important car si ton dépot est public tout le monde pourra voir tes identifiants de connexion à la base de données et plus en fonction de ce que ton application a besoin.
> Enfin, ce serait très important que tu regardes comment sécuriser les accès à tes dossiers via les htaccess parce que c'est dangereux de permettre l'ouverture de dossier et la lecture de fichier depuis un navigateur. Tu pourras voir par exemple que dans la correction il y a un htacces qui protège le dossier app de l'application. Tu pourras ainsi constater que si tu ne le fais pas et bien on peut par exemple accéder à ton fichier config.ini et ainsi obtenir les identifiants de ta base de données 😈

## BILAN
J'en rajoute une couche mais j'aurais vraiment préféré que tu fasses les choses dans l'ordre. Prends le temps de bien regarder la correction pour rattraper toutes les parties dans l'ordre. Du coup, petite séance de rattrapage 😱, je voudrais que tu me refasses tout le Let's code jusque la partie 5 et dans l'ordre cette fois s'il te plaît.
A très vite !