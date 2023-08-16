#Feedback 1

Hello "apprenant1",
J'espère que tu vas bien 🙂
Comme tu l'as demandé, je t'ai préparé un petit feedback du parcours S06.
Let's go !

##Avancée globale sur le projet

Tout d'abord je tenais à te dire que c'était du bon travail avec une belle avancée.
Sur le Let's code tu as validé les parties 1, 2, 3, 4, 5 et 6.
Globalement, tu as bien appliqué ce que tu as appris et ca fait plaisir 😉

##Mes retours :

**Quelques petits ajustements sont à revoir :**

☑️ Première chose, n'hésite pas à bien répartir tes éléments dans des fichiers spécifiques pour améliorer
l'ogranisation de tes dossiers/fichiers. Par exemple, tu as intégré le tableau lié aux autorisations de tes routes directement dans ton CoreController. Tu aurais pu créer un fichier acl.php et faire un require_once dans ton contrôleur ensuite. **Tu trouveras l'exemple dont je parle dans la correction du parcours**

☑️ Petit exemple d'optimisation et de compréhension de ton code par rapport à la programmation orientée objet concernant la méthode teacher() de ton TeacherController. Je constate que tu as instancié un objet de la classe Teacher. Cela n'était pas forcement nécessaire dans ce cas de figure car tu ne vas pas le remplir de toute façon. Lorsque tu as besoin d'appeler une méthode spécifique à une classe et que l'instanciation d'un objet n'est pas obligatoire tu peux utiliser la syntaxe suivante : Teacher::findAll(); Cela t'aurais permis de remplacer les lignes suivantes :
``
$newteacher = new Teacher();
        $teacher = $newteacher->findAll();
``
Par
``
$teacher = Teacher::findAll();
``

