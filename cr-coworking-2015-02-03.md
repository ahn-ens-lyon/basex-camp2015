Thème du jour : héritage et configuration de(s) projet(s)

Question : Est-ce qu'on fait une base ou un fichier XML ? Pour l'instant, on traite avec un fichier config.xml
Question : Comment représente-t-on un projet avec plusieurs corpus (=/= ou == bases de données)


## Other things ...
- do not forget to place the functions in alphabetical order 
- in the function "listArticles", check in $params if there is $author param to use to order the listing of articles 

## About project configuration and heritage

The projects configuration is specified in the file 'config.xml' inside 'synopsx/' repository. Copy 'config.sample' to 'config.xml' and fill in information about your project(s).

The 'projects' directory contains a hierarchical arborescence of directories with projects' names.

The '.gitignore' file untracts 'projects/*' and 'config.xml'.


## About bootstrap

Up-to-now bootstrap is a submodule in the static directory. It should not be included in the sources distribution, but rather placed by the users if need be.

## Documentation

The function documentation uses [xqDoc](http://xqdoc.org) as much as possible.

Example :

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
