# Feedback 1

Hello "apprenant2",
Comment vas-tu ?
Comme tu l'as demandé, je t'ai préparé un petit feedback du parcours S06.
C'est parti !

## Avancée globale sur le projet

Je sens que ce parcours n'a pas été évident pour toi mais ne te décourage pas ca va aller 💪
Sur le Let's code tu as validé les parties 1, 2.
Concernant la partie 3 tu avais quasiment terminé et je pense que tu aurais réussi si tu avais eu plus de temps. Je t'en reparle plus bas dans la partie mes retours.
Globalement ne lâche rien et surtout **prends bien le temps de regarder attentivement la correction pour voir ce qu'il te manquait** et pose moi des questions si besoin 😉

## Mes retours :

**Quelques petits ajustements sont à revoir :**

☑️ **Première chose** concernant la partie 3 du Let's code, tu avais une erreur parce que tu n'avais pas encore créé la propriété teacher_Id ainsi que les getters et les setters. C'est obligatoire puisque un élève est rattaché à un professeur et il faut donc que l'on puisse accéder à l'identifiant du professeur à partir de l'étudiant. La règle est la suivante : Si un élève est rattaché au minimum à un professeur et au maximum à un professeur et qu'un professeur est rattaché au minimum à 0 élève et au maximum à plusieurs élèves alors c'est l'élève qui doit avoir l'id du professeur dans la table en base de données. Du coup cela se répercute sur la classe également 😉. Tu dois donc créer une proprité teacher_Id ainsi que ses getters/setters.

☑️ **Quelques conseils de sécurité**, n'hésite pas à aller voir la correction pour regarder comment est implémentée la partie CSRF avec la gestion des Tokens. C'est une faille fondamentale contre laquelle il faut se protéger à tout prix 🙂. Aussi concernant Git, pense bien à remplir ton .gitignore en ajoutant ton fichier config.ini cela permettra de dire à Git que tu ne veux pas qu'il prenne en compte ce fichier lors des commits etc. Cela est très important car si ton dépot est public tout le monde pourra voir tes identifiants de connexion à la base de données et plus en fonction de ce que ton application à besoin.
> Enfin, ce serait très important que tu regardes comment sécuriser les accès à tes dossiers via les htaccess parce que c'est dangereux de permettre l'ouverture de dossier et la lecture de fichier depuis un navigateur. Tu pourras voir par exemple que dans la correction il y a un htacces qui protège le dossier app de l'application. Tu pourras ainsi constater que si tu ne le fais pas et bien on peut par exemple accéder à ton fichier config.ini et ainsi obtenir les identifiants de ta base de données 😈

## BILAN
Comme je te le disais au départ, il va falloir que tu prennes bien le temps de regarder la correction pour comparer ce que tu as fait et surtout pour aller chercher ce qu'il te manquait pour terminer le parcours. L'objectif parallèle va être que tu notes soigneusement tout ce que tu ne comprends pas en regardant le corrigé et que tu reviennes vers moi avec une liste de questions. Ainsi, on pourra rattraper tout cela j'en suis certain. 

J'attends donc ton retour pour que nous puissions avancer 👊