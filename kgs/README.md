# KGs implementations

## Triple store

### Primer

The triple store in the paper is implemented using [Apache Jena Fuseki.](https://jena.apache.org/documentation/fuseki2/) We added configurations in the Fuseki triple store to enable OGC’s [GeoSPARQL](https://opengeospatial.github.io/ogc-geosparql/geosparql11/spec.html) semantics and correlated subqueries (by availing of its [service enhancer](https://jena.apache.org/documentation/query/service_enhancer.html#programmatic-setup)). The triple store is the key to SPARQL federation over Linked Data. The correlated queries and GeoSPARQL contribute greatly to the complex geospatial queries in SPARQL.

### Open to use

The configured Fuseki triple store can be retrieved from [here](https://drive.google.com/drive/folders/135cKwxmmQgXKGaXOMLCr8y42nYUJXxn3?usp=sharing).

## Virtual knowledge graphs

### Primer

We use Ontop to expose all data, including geographical data (e.g., land cover, soil type), climate stations, and climate observations, as virtual knowledge graphs. To enhance geo-contextual climate data access, [LinkedGeoData](https://github.com/GeoKnow/LinkedGeoData) is included for use in SPARQL federation queries and formulating complex geospatial constraints. Please follow the instructions on LinkedGeoData to create the OpenStreetMap in RDF for the geospatial extent of interest.

### Open to use

The Ontop implementations used in the paper can be found [here](https://drive.google.com/drive/folders/1SIJsoayGexSfC1poY_-ZXyB_nfU1RBCy?usp=sharing). This should be used with ontologies [here](https://github.com/futaoo/LinkedGeoClimate/tree/main/kgs/ontologies) and OBDA mapping files [here](https://github.com/futaoo/LinkedGeoClimate/tree/main/kgs/obda) to reproduce the virtual knowledge graphs proposed in the paper. The PostgreSQL database is used as the underlying relational database of Ontop, which can be downloaded from this [website](https://www.postgresql.org/download/).

## Visualization

We use [Sextant](https://sextant.di.uoa.gr/) as a visualization tool for the knowledge graphs. It supports some interactive additions of geospatial constraints (by drawing the spatial extent on a map) and filters into SPARQL queries. A developer package for Sextant is archived in our cloud drive and can be downloaded [here](https://drive.google.com/drive/folders/16_ckTanEGGG6j4-q8vtLod_K3ZFLFd2L?usp=sharing).