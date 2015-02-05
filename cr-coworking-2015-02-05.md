Sylvain prend la main :

Attention : Vendredi (master) est une vache sacrée, on branche toujours quand on avance sur de nouvelles fonctionnalités.

$ git branch -b heritage
$ git checkout heritage

Quel comportement attendue, quand pas de base de donnée. 
Proposition 1 : Donner une base d'exemple
Proposition 2 : quand on veut pouvoir créer une base, besoin de tester si fichier config.xml existe

- Procédure d'installation à mettre en route !

Trois options :
1) Pas de projets, on livre synopsx (/ on redirige => /synopsx/home)
2) Si un projet, prend l'entrée du dossier rest_xq (=> project/home
3) si plusieurs projets, 

<resourceName> correspond au début de l'URL

Comment gère-t-on la racine ? Peut-être obligatoirement avoir "synopsx/"

Les points d'entrée d'Emmanuel :
- corpus/           listCorpus()
- corpus/coprusId   corpus()
- texts             listTexts()
- blog              


Tout ce qui gouverne BaseX dans le dossier SynopsX/restxq (installation) et on déporte tous les points d'entrées webapp.xqm dans projects/


