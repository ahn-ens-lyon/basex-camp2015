http:localhost:8984/multi2/tei/toto

function synopsx:index($project, $dataType, $value) # point d'entrée relatif à l'url
  function synopsx:main($params, $options, $layout) # fonction principale reprenant : 
    1. les options passées dans l'url, avec $params 
    2. des options à définir ultérieurement (TODO), avec $options
    3. le template global, avec $layout (premier param de l'url : ici 'multi2'||'.xhtml')
      function synopsx.mappings.htmlWrapping:globalWrapper($params, $options, $instanciated)
      		CASE 1 = Map : function synopsx.mappings.htmlWrapping:pattern
      		CASE 2 = String : function synopsx.models.@data-model:@data-function
      			Exemple = synopsx.models.globals:horizontal-nav-entry
        		#<nav data-model="globals" data-function="horizontal-nav-entry" data-pattern="p" id="horizontal-nav">
