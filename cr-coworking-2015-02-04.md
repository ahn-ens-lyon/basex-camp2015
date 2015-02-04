Présentation du module Biblio (par Emmanuel et Philippe), pour gérer les ressources bibliographiques

Distinguer oeuvre des éditions (FRBR) :
1)- Oeuvre (peut avoir plusieurs manifestations, ex: au cinéma, publication)
2)- Expression (chaque édition, altérée dans leur forme)
3)- Item bibliographique (

- FRBRversion Objet (UML), aligné avec CIDOC-CRM
- Pourquoi format TEI XML (et non pas VRA) ? créer le graphe de relations, avec ajout d'attribut dans <listBibl><biblStruct>. Soit dans ODD, 

Ex: gdpBibliography.xml 
Description dans les entêtes, identifier les volumes "titre", 
Norme dans les bibliothèques pas les mêmes que les nôtres (convention ISBD)

<biblStruct> équivalent à <msItem> pour les manuscrits. Schéma TEI pour la bibliographie est top.

Deux cas :
a) texte monographique <monogr>
b) article de revue : titre de la revue et le titre de l'article
Les attributs de <monogr> et <analytic> sont suffisamments distincts pour préparer des affichages différents ou proposer une recherche détaillé selon les types bibliographiques.

Pointe vers un index, forme normalisée des personnes

Comment on sérialize avec Xquery, voir teiBiblio.xqm dans Models/

Edition de "Punch", mime le fonctionnement d'une XSLT (template match) => function "dispatch"
