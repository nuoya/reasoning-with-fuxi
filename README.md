# Play with Fuxi Reasoner

## install
```
pip install -r requirements.txt
```

## example1
This is taken from Fuxi tutorial 
https://code.google.com/p/fuxi/wiki/Tutorial

```
example1 » python reason.py
@prefix ns1: <http://example.org/> .
@prefix rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#> .
@prefix rdfs: <http://www.w3.org/2000/01/rdf-schema#> .
@prefix xml: <http://www.w3.org/XML/1998/namespace> .
@prefix xsd: <http://www.w3.org/2001/XMLSchema#> .

ns1:bar ns1:x "xxxx" ;
    = ns1:bar,
        ns1:foo .

ns1:foo ns1:y "yyyy" ;
    = ns1:foo .
```

## example2

This is taken from the book Mining the Social Web
https://github.com/ptwobrussell/Mining-the-Social-Web-2nd-Edition

```
example2 » ./reason
@prefix : <file:///Users/cliffxuan/dev/try-fuxi/example2/MiningTheSocialWeb#> .
@prefix iw: <http://inferenceweb.stanford.edu/2004/07/iw.owl#> .
@prefix log: <http://www.w3.org/2000/10/swap/log#> .
@prefix rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#> .
@prefix rdfs: <http://www.w3.org/2000/01/rdf-schema#> .
@prefix skolem: <http://code.google.com/p/python-dlp/wiki/SkolemTerm#> .
@prefix xml: <http://www.w3.org/XML/1998/namespace> .
@prefix xsd: <http://www.w3.org/2001/XMLSchema#> .

:ChuckNorris a :god .

:Socrates a :Mortal ;
    :drinks :whisky .
```

## example3

This is taken from https://github.com/nuoya/FuXi/blob/master/examples/test1.example.sh
```
@prefix : <http://xdors.net/demo#> .
@prefix iw: <http://inferenceweb.stanford.edu/2004/07/iw.owl#> .
@prefix log: <http://www.w3.org/2000/10/swap/log#> .
@prefix owl: <http://www.w3.org/2002/07/owl#> .
@prefix rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#> .
@prefix rdfs: <http://www.w3.org/2000/01/rdf-schema#> .
@prefix skolem: <http://code.google.com/p/python-dlp/wiki/SkolemTerm#> .
@prefix xml: <http://www.w3.org/XML/1998/namespace> .
@prefix xsd: <http://www.w3.org/2001/XMLSchema#> .

:has_parent rdfs:domain :person ;
    rdfs:range :person ;
    owl:inverseOf :has_child .

:has_sibling a owl:ObjectProperty,
        owl:SymmetricProperty ;
    rdfs:domain :person ;
    rdfs:range :person .

:jack a :person .

:john a :person ;
    :spouse :jane .

:has_child a owl:ObjectProperty ;
    rdfs:domain :person ;
    rdfs:range :person .

:jane a :person ;
    :has_child :janey,
        :johny .

:janey a :person ;
    owl:differentFrom :johny .

:johny a :person .

:person a owl:Class .
```
