# AdobeCloudPlatform Data Model Machinery

Semantic data model for the [unified Adobe Cloud API](https://wiki.corp.adobe.com/display/ctooperations/Content+and+Data+Workstream). Includes tooling to generate HTML documentation.

## Schema files

The machine readable schema source files ([RDF/S](https://www.w3.org/TR/rdf-schema/) in [Turtle Syntax](https://www.w3.org/TR/turtle/))) are located in the [AdobeCloudPlatform/models](https://git.corp.adobe.com/AdobeCloudPlatform/models) git repository.

## Installing and running

```bash
# clone models project
git clone git@git.corp.adobe.com:AdobeCloudPlatform/models.git

# clone machinery project
git clone git@git.corp.adobe.com:AdobeCloudPlatform/machinery.git

# install dependencies
cd machinery && npm install

# show usage information
node index.js
# Generate Html Documentation and JSON-LD from an RDF/S Schema file in Turtle Syntax.
#
# Usage: node index.js
#
# Options:
#   -f, --file  path to <schema>.ttl file                   [required]
#   -o, --out   path to output directory (default: ./out)

# run task
node index.js -f ../models/asset.ttl 
# generated output is written to ./out
```

## TODOs

* RDF/S Schema validation:
  -- property naming convention
  -- vocabulary spellchecking (RDF, RDFS, DC, OWL, SKOS, ...) 
  -- use of RDF/S vocabulary
  -- ...
* RDF/S to JSON Schema (and vice versa) conversion?
* ...

## Links

### Specifications

* [RDF](https://www.w3.org/RDF/)
* [RDF Schema (RDF/S) 1.1](https://www.w3.org/TR/rdf-schema/)
* [RDF 1.1 Turtle](https://www.w3.org/TR/turtle/)
* [JSON-LD 1.0](https://www.w3.org/TR/json-ld/)
* [XMP SPECIFICATION PART 1 DATA MODEL, SERIALIZATION, AND CORE PROPERTIES](http://wwwimages.adobe.com/content/dam/Adobe/en/devnet/xmp/pdfs/XMP%20SDK%20Release%20cc-2014-12/XMPSpecificationPart1.pdf)

### Vocabularies / Ontologies

* [schema.org](http://schema.org)
* [Dublin Core](http://dublincore.org/)
* [OWL](http://www.w3.org/TR/2009/REC-owl2-overview-20091027/)
* [SKOS Core](http://www.w3.org/TR/2009/REC-skos-reference-20090818/)

### Tools

* [TextMate N3/Turtle Bundle](https://github.com/peta/turtle.tmbundle)
* [Online RDF Converter](http://www.easyrdf.org/converter)
* [JSON-LD Playground](http://json-ld.org/playground/)