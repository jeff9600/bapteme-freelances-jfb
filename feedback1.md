# Feedback 1

Hello "apprenant1",
J'espère que tu vas bien 🙂
Comme tu l'as demandé, je t'ai préparé un petit feedback du parcours S06.
Let's go !

## Avancée globale sur le projet

Tout d'abord je tenais à te dire que c'était du bon travail avec une belle avancée.
Sur le Let's code tu as validé les parties 1, 2, 3, 4, 5 et 6.
Concernant la partie 7 c'était presque ça parce que tu avais juste oublié de gérer le fait qu'un utilisateur peut juste voir la liste des professeurs sans pouvoir les ajouter/modifier/supprimer.
J'ai vu que tu avais même fait certains bonus donc c'est vraiment top !
Globalement, tu as bien appliqué ce que tu as appris et ca fait plaisir 😉

## Mes retours :

**Quelques petits ajustements sont à revoir :**

☑️ **Première chose**, je ne sais pas si tu avais compris mais ton routeur ne pouvait pas fonctionner correctement parce qu'il manquait un htaccess dans ton dossier public permettant de passer au travers de ton index.php et ainsi de ne plus le rendre visible dans ta barra d'URL notamment. Tu pourras aller voir à quoi ressemble le fichier dans le dossier de correction mais pour résumer sans faire cela tu devais avoir une adresse de base en 127.0.0.1/public/index.php/teachers alors que ton routeur attendait des routes sous la forme 127.0.0.1/public/teachers. C'est fondamental de mettre en place ce type de fichier d'une part pour que tes URLs soient plus propres et surtout parce que ton index.php est un fichier **ultra sensible** et donc il vaut mieux ne pas le montrer même dans la barre d'adresse.

☑️ **Concernant le bonus sur la mise à jour des étudiants/professeurs** tu avais quasi réussi ! En fait, dans la vue teacher_update.tpl.php, sur ton formulaire tu as mis une action qui renvoyait sur la route public/teacher/ hors cette route n'existe pas car il lui faut absolument un id pour fonctionner. En fait tu n'avais même pas besoin de renseigner une action. Pour faire simple, lorsque ta route de modification correspond aussi à celle sur laquelle tu vas valider ton formulaire, il suffit de ne pas renseigner d'action pour que celui-ci soit envoyé au même endroit. Tu constateras ainsi qu'en mettant action="" dans ce formulaire, cela fonctionnera comme par magie ✨

☑️ N'hésite pas à bien répartir tes éléments dans des fichiers spécifiques pour améliorer
l'organisation de tes dossiers/fichiers. Par exemple, tu as intégré le tableau lié aux autorisations de tes routes directement dans ton CoreController. Tu aurais pu créer un fichier acl.php et faire un require_once dans ton contrôleur ensuite. **Tu trouveras l'exemple dont je parle dans la correction du parcours**

☑️ **Petit exemple d'optimisation et de compréhension de ton code** par rapport à la programmation orientée objet concernant la méthode teacher() de ton TeacherController. Je constate que tu as instancié un objet de la classe Teacher. Cela n'était pas forcement nécessaire dans ce cas de figure car tu ne vas pas le remplir de toute façon. Lorsque tu as besoin d'appeler une méthode spécifique à une classe et que l'instanciation d'un objet n'est pas obligatoire tu peux utiliser la syntaxe suivante : Teacher::findAll(); Cela t'aurais permis de remplacer les lignes suivantes :

``
$newteacher = new Teacher();
$teacher = $newteacher->findAll();
``

par

``
$teacher = Teacher::findAll();
``

☑️ **Au niveau de la sécurité**, je vois que tu as pensé à préparer certaines requêtes SQL mais pas toutes. Pense bien à le faire partout parce que c'est fondamental pour te protéger des injections SQL. Egalement, n'hésite pas à aller voir la correction pour regarder comment est implémentée la partie CSRF avec la gestion des Tokens. C'est une faille fondamentale contre laquelle il faut se protéger à tout prix 🙂 
> Enfin, ce serait sympa que tu regardes comment sécuriser les accès à tes dossiers via les htaccess parce que c'est dangereux de permettre l'ouverture de dossier et la lecture de fichier depuis un navigateur. Tu pourras voir par exemple que dans la correction il y a un htacces qui protège le dossier app de l'application. Tu pourras ainsi constater que si tu ne le fais pas et bien on peut par exemple accéder à ton fichier config.ini et ainsi obtenir les identifiants de ta base de données 😈

## BILAN
Franchement dans l'ensemble c'est du très bon travail et on sens que tu as cherché à comprendre ce que tu as fait donc je te dis bravo. Prends le temps de bien regarder la correction et tu vas rapidement comprendre tes erreurs j'en suis persuadé ! 
A bientôt pour de nouvelles aventures 👊