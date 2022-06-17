_.html: _.ttl
	owlhtml _.ttl > _.html

_.ttl: ontologia.csv cronologia-LuisGrosso.yaml ontologia.tax
	perlrdf prefix --format=turtle owl rdf rdfs skos > _.ttl
	jjtax2ttl   ontologia.tax              >> _.ttl
	jjtable2ttl ontologia.csv              >> _.ttl
	jjyaml2ttl  cronologia-LuisGrosso.yaml >> _.ttl
