TO DO
- ramener les fonctions par ordre alphabétique
- regarder les $params dans listArticles (pour utiliser / filtrer par rapport à un auteur)

Propositions :
- besoin de configurer pour travailler avec nos corpus respectifs
- distribuer un dossier avec les deux dossiers à déplacer dans webapp

- est-ce qu'on fait une base ou un fichier XML (config)

- functionnalité pour charger lot


## Project configuration and heritage

The projects configuration is specified in 'config.xml' inside 'synopsx/' repository. Copy 'config.sample' to 'config.xml' and fill the informations.

The 'projects' directory contains an hierarchical arborescence of directory with projects names.

The '.gitignore' file untracts 'projects/*' and 'config.xml'.


## Static

Distribuer bootstrap comme sous-module. Ce n'est pas une bonne pratique de distribuer des sources dont on n'est pas l'auteur. Par ailleurs il est possible


## Documentation

The function documentation uses [xqDoc](http://xqdoc.org) as much as possible.

Exemple :

This function does ...
@param $variable a variable
@author
@version
@see url/
@since
@deprecated
@return

@param and @return are mandatory

Extensions :
@todo
@bug

The function and variables should be properly typed.
