Programme de la semaine :
- la multi-injection (donc plusieurs fonctions models/ et/ou plusieurs mappings différents pour un même layout)
- réflexion sur l'organisation du dépot et des différentes branches
- le schéma de base d'une fonction dans models/ (Notamment par exemple, ce qu'on met dans la map meta ? Par exemple faire meta soit systématiquement les quelques champs du dublin core simple, ou autre chose mais qui soit facilement documentable et mémorisable. Exemple : doit-on garder "Quantity" dans les méta alors qu'on peut retrouver cette info à tout moment (taille de la map data) ? Ce genre de questions...)
- le fonctionnement de base de l'association url-layout-injections (est-ce qu'on garde notre modèle de base $dataSource/$dataType/$value/$option ou pas, etc.) Certes un projet pourra tordre cet usage à tout moment en déclarant des url particulières, mais essaye-t-on de proposer une certaine logique par défaut des url ?
- et en effet ce que dit Emmanuel, récupérer le mécanisme d'héritage et de surcharge...

1) La multi-injection

Basé sur la logique HTML5, mécanisme d'associer dans les attributs, les types de données et les fonctions à appeler.

Ex: http://www.alsacreations.com/article/lire/1397-html5-attribut-data-dataset.html
data-model=tei
data-function="listTitle"
data-pattern="table"

Exemple : dans webapp, on teste avec la fonction qui a trois paramètres ($options, $layout, $pattern) avec en templates/multi.xhtml 

En points d'entrée : blog/tei/articles

Prévoir cas par défaut pour data-model (EAD ou TEI d'après)

2) Réflexion sur l'organisation du dépot et des différentes branches :

- Utilisation de Rebase pour nettoyer le code et la structure (rester sur un partage de code plus linéaire 
qu'en multiplication de branches)
- Proposition de basculer la branche "vendredi" sur master, nettoyer cette master au minimum, puis repartir 
sur vendredi
