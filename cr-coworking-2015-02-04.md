# Cr 3 février 2015

I. Présentation du module Biblio (par Emmanuel et Philippe), pour gérer les ressources bibliographiques

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

II. Mise à jour de vendredi et de master

Emmanuel avait forké sur le dépôt de Gazelle, et mis à jour son dépôt en faisant un "pull request", cela permet d'échanger sur les modifications avant validation.

Philippe récupère la branche vendredi pour intégrer ses modifs localement

$ git remote -v
origin (fork de synopsx)
origin
upstream (pour garder un lien git remote add upstream ou un nom quelconque)

D'abord mettre à jour upstream de AHN pour intégrer les modifs locales.

$ git fecth upstrem

Cette procédure de filtrage en amont, évite d'avoir un historique un peu pourris. Master doit toujours être fonctionnel (peut-être versionné une v1, avec un historique vide, et démarrer une v2 avec notre code de cette semaine).

$ git rebase -i upstream/vendredi (récupère mes modifs et mettre après ce qu'il y a sur la branche vendredi)

Mode interactif qui permet de corriger les fautes, mettre en anglais, fusionner des commentaires (squash, add ...)

On va écraser le vendredi local finalement qui n'apporte pas de modifications.

$ git branch -D vendredi (enlever la branche avec les modifs locales)

$ git checkout -b vendredi (pour repartir sur la branche vendredi du dépôt de Philippe, sans les modifs locales)

$ git pull upstream

$ git remote add gazelle https://github.com/gazelleinfinland/synopsx.git (ajout d'un remote)

$ git fetch gazelle (pour indexer et récupérer toutes les branches)

$ git branch config (création d'une nouvelle branche locale, à partir de vendredi qui est à jour)

$ git co confi (se mettre sur la branche config)

$ git merge gazelle/config (fast-forward, pas de conflits


## Cr Emmanuel

  Mâtinée :
  - travail sur le workflow avec GitHub
  - fin du travail sur la configuration
  - fin du travail sur l’héritage des projets

  Après-midi :
  - modification de la structure du fichier 'config.sample'
  - nettoyage des points d’entrée de webapp
  - changement du mécanisme d’appel des modèles depuis '_restxq/'
  - création d’un répertoire 'lib/' pour les fonctions de librairies utilisées par les fonctions ressource
  - on utilise directement le namespace des modèles dans les points d’entrée RestXQ
  - remplacement des '$params' et '$options' par '$queryParams' et '$outputParams' pour être plus explicite


  todo :
  - modifier le templating pour éviter de définir le modèle dans les fichiers xhtml
