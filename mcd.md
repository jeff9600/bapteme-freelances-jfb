# Retour MCD
Hello Apprenant 5,
Comment vas-tu ?
Je viens de regarder ton MCD et voici mes retours :
- Déjà une chose importante que tu as bien respecté c'est que tout est en anglais (C'est important de ne pas alterner plusieurs langues français/anglais par exemple dans cette méthode) donc bravo !
- Tes associations (GENERATE, CONTAIN, LIKE et HAS) doivent soit être toutes à l'infinitif, soit être toutes conjuguées. Du coup, HAS devrait devenir HAVE 😉
- Attention, il y a une petite faute de frappe dans l'entité ADDRESS, tu as oublié un d sur la propriété address, Ca ne cassera pas ta base de données mais quand même 😛
- Tes cardinalités sont toutes correctes sauf celle entre USER et PRODUCT par l'association LIKE. En effet, un utilsateur peut liker au minimum 0 produit et au maximum plusieurs et un produit peut être liké par au minimum 0 utilisateur et au maximum plusieurs utilisateurs. Ce qui nous donnerait des cardinalités 0,N des deux côtés.
- Je vois que justement tu as entourré cette association et annotant Many To Many. Attention car cela est un vocabulaire spécifique à la méthode UML dans les diagrammes de classe. On n'emploi pas ces termes côté MERISE et c'est bien 0,N qu'il faut utiliser du coup.

Pour le reste, rien à redire et franchement c'est du bon travail.
Encore un peu de pratique et tu deviendras expert en MCD !
A bientôt,
Jean-François


