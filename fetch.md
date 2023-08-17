# Explication de fetch (méthode Javascript)
Hello "apprenti1",
J'espère que tu vas bien !
C'est intéressant que tu te poses cette question sur fetch, aurais-tu un penchant pour Javascript du coup ?

## Explications de la notion
Déjà fetch() est une méthode récente qui consiste à envoyer, afficher, recevoir... des informations via les requêtes serveurs dès qu'il y a besoin et sans recharger la page complète (asynchrone) ! Pour faire un parallèle, tu as peut être déjà entendu parlé d'AJAX (Asynchronous JavaScript And XML) ? AJAX était une révolution à l'époque car il permettait de traiter des informations sans avoir à recharger complétement la page justement. Si on reprend le parcours S06 par exemple, grâce à AJAX, tu pourrais valider le formulaire de modification d'un professeur sans que la page complète soit rechargée. Et bien fetch() de Javascript fait la même chose mais il possède une syntaxe plus moderne et surtout il n'utilise pas XML. En effet, contrairement à AJAX, il possède plusieurs types de réponses, notamment JSON qui est très souvent utilisé.

## Explication par le code

On va utiliser ton formulaire de modification de professeur pour te montrer.
Du coup rdv dans ta vue teacher_update.tpl.php ou tu vas ajouter le code suivant pour commencer :

``` 
document.getElementById("submitBtn").addEventListener("click", () => {
const formData = new FormData(document.getElementById("teacherForm"));
fetch("", {
    method: "POST",
    body: formData
})
.then(response => response.json())
.then(data => {
    console.log("Données enregistrées :", data);
    // Faire quelque chose avec la réponse du serveur (si nécessaire)
})
.catch(error => {
    console.error("Erreur :", error);
});
});
``` 