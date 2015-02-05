# Cr co-working-basex 5 février 2015

## Mâtinée
- le fichier 'webapp.xqm' a été déplacé dans 'project/' de manière à offrir toute latitude aux utilisateurs dans le choix des URIs
- les fonctions ressources dans 'synopsx/_restxq/' auront toutes un chemin commençant par 'synopsx'
- ajout de 'webapp.xqm' au '.gitignore' dans 'project'
- ajout d’un attribut 'default' sur le projet à servir sur '/home'
- réécriture de 'webapp.xqm' pour le choix d’une home par défaut
- renommage des modèles 'globals' en 'mixed' pour être plus explicite
-  des fonctions dans 'mixed/'

## Règles
- utilisation de simple quotes
- espace de nom conforme à l’arborescence
- lowerCamelCase pour les noms de fonction et les variables
- indentation 2 caractères
- commentaires sur la ligne
- utilisation de XQdoc pour commenter les fonctions ressources (étendu avec les mots-clefs @todo, @bug, @rmq, ...)

## Après-midi

Le templating défini en début de semaine pour traiter les points d’insertion multiples avait l’inconvénient de faire définir les modèles de données du côté des templates HTML. Dans une logique du web de données, les modèles devraient plutôt être définis par la fonction ressource (restXQ). Cette fonction ressource pouvant recevoir des sérialisations différentes.

On a beaucoup tourné autour du problème. Afin de privilégier une logique de déclaration des ressources avec RestXQ et dans une perspective de Linked Open Data, le contenu des pages HTML faisant appel à la composition de plusieurs ressources (compendium, ou mashup) est traité avec JavaScript.

Afin de présenter alternativement un tableau ou une liste avec les mêmes données, paramétriser la fonction ressource avec des paramètres HTTP GET ou bien renvoyer les données en JSON et les traiter côté client en JavaScript.

  
