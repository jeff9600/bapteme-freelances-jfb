# Explication de fetch (méthode Javascript)
Hello "apprenti1",
J'espère que tu vas bien !
C'est intéressant que tu te poses cette question sur fetch, aurais-tu un penchant pour Javascript du coup ?

## Explications de la notion
Déjà fetch() est une méthode récente qui consiste à envoyer, afficher, recevoir... des informations via les requêtes serveurs dès qu'il y a besoin et sans recharger la page complète (asynchrone) ! Pour faire un parallèle, tu as peut être déjà entendu parlé d'AJAX (Asynchronous JavaScript And XML) ? AJAX était une révolution à l'époque car il permettait de traiter des informations sans avoir à recharger complétement la page justement. Si on reprend le parcours S06 par exemple, grâce à AJAX, tu pourrais valider le formulaire de modification d'un professeur sans que la page complète soit rechargée. Et bien fetch() de Javascript fait la même chose mais il possède une syntaxe plus moderne et surtout il n'utilise pas XML. En effet, contrairement à AJAX, il possède plusieurs types de réponses, notamment JSON qui est très souvent utilisé.

## Explication par le code

On va utiliser ton formulaire de modification de professeur pour te montrer.
Du coup rdv dans ta vue teacher_update.tpl.php où tu vas ajouter le code suivant pour commencer :

``` 
<script>
document.getElementById("submitBtn").addEventListener("click", () => {
const formData = new FormData(document.getElementById("teacherForm"));
fetch("", {
    method: "POST",
    body: formData
})
.then(response => response.json())
.then(data => {
    console.log("Données enregistrées :", data);
})
.catch(error => {
    console.error("Erreur :", error);
});
});
</script>
```
Le script ci-dessus te permettra d'appliquer une méthode fetch avec POST à partir de ton formulaire. 
Tu constateras que les guillemets juste après fetch sont vides parce que comme je te le disais dans ton feedback, on est déjà sur la route de traitement de formulaire donc il n'y pas besoin de la renseigner. En revanche, si ton traitement s'était fait via une autre route, il aurait fallu la renseigner. J'ai oublié de te préciser que j'ai ajouté deux lignes avant le fetch pour faire du "tuning" sur ton formulaire. En gros je dis que dès tu cliques sur le bouton ayant pour id submitBtn cela créé un objet de la classe FormData de Javascript qui va te permetre de collecter les données transmises dans un formulaire en les associants par clé/valeur Nom, Teddy par exemple.

Lorsque tu auras copié/collé ce code dans ta vue, il faudra ajouter l'id teacherForm à ton formulaire dans le code HTML puis que tu ajoutes l'id submitBtn à ton bouton d'envoi afin que l'événement click puisse se déclencher. Enfin, il te restera à remplacer le type="submit" de ton bouton d'envoi par un type="button" de manière à ce que l'envoi de ton formulaire ne se fasse pas vers PHP. Après cela, si tu testes ton formulaire en modifiant par exemple le prénom d'un professeur, tu pourras aller voir que ta base de données à été mise à jour alors que ta page n'a pas été rechargée !

Alors mon exemple n'est clairement pas optimal puisque ta méthode teacherUpdatePost() sur ton contrôleur ne renvoie pas de JSON ce qui fait tu ne pourras pas travailler sur la réponse du serveur entre autre mais le principe est là et tu n'as plus qu'à aller creuser pour optimiser tout cela 🙂

Pour terminer, voici une page qui explique plutôt bien ce qu'est la méthode fetch() https://fr.javascript.info/fetch 
