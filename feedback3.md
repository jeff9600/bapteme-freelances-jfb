# Feedback 3

Hello "apprenant3",
J'espère que tu vas bien 🙂
Comme tu l'as demandé, je t'ai préparé un petit feedback du parcours S06.
Let's go !

## Avancée globale sur le projet

Je constate que ce parcours a dû être compliqué pour toi et j'espère que tu n'es pas découragé.
Si c'est le cas, rassure-toi on va mettre en place un suivi pour rattraper les connaissances que tu n'a pas assimilé.
Sur le Let's code tu as validé la partie 1 et la 2 partiellement.
Sur la partie 2, je dis partiellement parce que tu n'affiches pas le header et le footer mais cela est normal puisque je constate que tu ne les as pas créé.
Tu pourras me dire si je me trompe mais j'ai le sentiment que tu as paniqué et que tu as essayé de faire plein de choses à des endroits différents et c'est peut être cela qui t'a perdu. Je sous-entends cela parce que par exemple dans ton listing de professeurs, le bouton ajouter redirige vers le formulaire d'ajout d'étudiants.  Pour les prochains parcours il faudra être vigilant de te focaliser sur une étape à la fois pour que cela ne se reproduise pas.

## Mes retours :

☑️ **Première chose**, dans ton index.php, tu as mis ta route d'accueil en /home, hors, lorsque l'on sait que cette route est notre accueil justement, il faut le mettre en racine est donc /. A ta ligne 32 tu pouvais donc remplacer ton /home par / pour que ce soit plus logique.
Toujours en lien avec tes URLs, même s'il n'est pas prioritaire, ton routeur ne pouvait pas fonctionner correctement parce qu'il manquait un htaccess dans ton dossier public permettant de passer au travers de ton index.php et ainsi de ne plus le rendre visible dans ta barre d'URL notamment. Tu pourras aller voir à quoi ressemble le fichier dans le dossier de correction mais pour résumer sans faire cela tu devais avoir une adresse de base en 127.0.0.1/public/index.php/home. C'est fondamental de mettre en place ce type de fichier d'une part pour que tes URLs soient plus propres et surtout parce que ton index.php est un fichier **ultra sensible** et donc il vaut mieux ne pas le montrer même dans la barre d'adresse.

☑️ J'ai été voir ce que tu as commencé à faire pour l'ajout d'étudiant. Tu étais bien parti mais tu as mélangé deux actions dans une même méthode. En fait, la méthode studentAdd() devait juste être là pour afficher le formulaire (la vue) en prenant en paramètre la liste des professeurs pour la liste déroulante permettant de sélectionner celui qui sera rattaché à l'élève. Ensuite, il aurait fallu créer une deuxième méthode pour la validation du formulaire (**Tu verras que dans la correction il y a une méthode addPost dans le StudentController prévue pour cela**). L'objectif de cette deuxième méthode était donc de reprendre les données envoyées par le formulaire via $_POST, de faire les vérifications nécessaires (champs vides etc.), de créer une nouvel objet de la classe Student() pour appliquer les setters, d'appeler une méthode insert() par exemple définie dans ton modèle Student et enfin, si tout s'est bien passé, de renvoyer vers le listing des étudiants. Pas évident de t'expliquer tout cela en détail mais le cheminement y est. Nous pourons en reparler de vive voix de toute façon 🙂

☑️ N'hésite pas à bien répartir tes éléments dans des fichiers spécifiques pour améliorer
l'organisation de tes dossiers/fichiers. Par exemple, tu as intégré le tableau lié aux routes directement dans ton index.php. Tu aurais pu créer un fichier routes.php et faire un require_once dans ton index.php ensuite. **Tu trouveras l'exemple dont je parle dans la correction du parcours**


☑️ **Au niveau de la sécurité**, n'hésite pas à aller voir la correction pour regarder comment est implémentée la partie CSRF avec la gestion des Tokens. C'est une faille fondamentale contre laquelle il faut se protéger à tout prix 🙂. Aussi concernant Git, pense bien à remplir ton .gitignore en ajoutant ton fichier config.ini cela permettra de dire à Git que tu ne veux pas qu'il prenne en compte ce fichier lors des commits etc. Cela est très important car si ton dépot est public tout le monde pourra voir tes identifiants de connexion à la base de données et plus en fonction de ce que ton application a besoin.
> Enfin, ce serait très important que tu regardes comment sécuriser les accès à tes dossiers via les htaccess parce que c'est dangereux de permettre l'ouverture de dossier et la lecture de fichier depuis un navigateur. Tu pourras voir par exemple que dans la correction il y a un htacces qui protège le dossier app de l'application. Tu pourras ainsi constater que si tu ne le fais pas et bien on peut par exemple accéder à ton fichier config.ini et ainsi obtenir les identifiants de ta base de données 😈

## BILAN
Comme je le disais au départ, il va falloir que l'on soit vigilant sur le fait que ne t'éparpille pas et que tu restes bien focus sur une étape. D'autre part, **il va falloir que tu regardes en détail la correction et tu notes des questions pour que tu me les communiques ensuite**. J'aimerais bien également que tu reprennes le parcours et que tu essayes d'aller au moins jusqu'à l'étape 3 du Let's code. Est-ce que cela te semble jouable ?
Dans tous les cas ne te décourage pas, je ne vais pas te lâcher 👊