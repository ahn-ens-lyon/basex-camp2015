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

  
Sylvain prend la main :

Attention : Vendredi (master) est une vache sacrée, on branche toujours quand on avance sur de nouvelles fonctionnalités.

$ git branch -b heritage
$ git checkout heritage

Quel comportement attendue, quand pas de base de donnée. 
Proposition 1 : Donner une base d’exemple
Proposition 2 : quand on veut pouvoir créer une base, besoin de tester si fichier config.xml existe

- Procédure d’installation à mettre en route !

Trois options :
1) Pas de projets, on livre synopsx (/ on redirige => /synopsx/home)
2) Si un projet, prend l’entrée du dossier rest_xq (=> project/home
3) si plusieurs projets, 

<resourceName> correspond au début de l’URL

Comment gère-t-on la racine ? Peut-être obligatoirement avoir "synopsx/"

Les points d’entrée d’Emmanuel :
- corpus/           listCorpus()
- corpus/coprusId   corpus()
- texts             listTexts()
- blog              


Tout ce qui gouverne BaseX dans le dossier SynopsX/restxq (installation) et on déporte tous les points d’entrées webapp.xqm dans projects/

