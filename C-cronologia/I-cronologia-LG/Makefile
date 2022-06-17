_.html: _.ttl
	owlhtml _.ttl > _.html

_.ttl: ontologia.csv cronologia-LuisGrosso.yaml ontologia.tax
	perlrdf prefix --format=turtle owl rdf rdfs skos > _.ttl
	jjtax2ttl   ontologia.tax              >> _.ttl
	jjtable2ttl ontologia.csv              >> _.ttl
	jjyaml2ttl  cronologia-LuisGrosso.yaml >> _.ttl

publish: _.html
	mkdir -p ../../docs
	cp _.html ../../docs/index.html
	echo "git commit ../../docs/index.html -m 'publish new version'; git push"	
