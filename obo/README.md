This folder contains the context files for mapping DATS to the [OBO Foundry](http://www.obofoundry.org/) ontologies.

We have identified some entities and properties that are not available within the OBO ontologies, and these are listed below. We will be submitting the request for these terms to the relevant ontologies.

The list of missing terms, which we will request to the relevant ontologies are:

- in DATS.Dataset and DATS.DatasetDistribution, the property to relate these entities to a license is not available in OBO ontologies:
``` 
"licenses": {
      "@id": "obo:has_license",
      "@type": "swo:SWO_0000002"
    },
```
- in DATS.DatasetDistribution, the property ```size``` could not be mapped:

```
"size": {
      "@id": "obo:TODOhas_size",
      "@type": "xsd:integer"
    },
```

- in DATS.DatasetDistribution, the property ```storedIn``` could not be mapped:

```
"storedIn": {
      "@id": "obo:TODOstored_in",
      "@type": "obo:ERO_0001716"
    },
```

- in DATS.DatasetDistribution, the property ```qualifier``` could not be mapped:

```
"qualifier": {
      "@id": "obo:TODO_conforms_to",
      "@type": ""
    }
```

- in DATS.DatasetDistribution, the property ```access``` could not be mapped:

```
 "access": {
      "@id": "",
      "@type": ""
    },
```

- conformsTo (for dataset_distribution)
- format (for dataset_distribution)
- creators (for dataset)
- in DATS.Dataset
```
 "distributions": {
      "@id": "obo:TODO -> distribution[missing term]",
      "type": "obo:TODO -> DataDownload[missing term]"
    },
   
```
- in DATS.Dataset, a term for storedIn is missing from the OBO Foundry ontologies
```
"storedIn": {
      "@id": "obo:TODO ->",
      "@type": "obo:ERO_0001716"
    }
```

- In DATS.Activity, the property performedBy cannot be mapped:

```
"performedBy" :
    {
      "@id" : "obo:TODO",
      "@type":["obo:OBI_0000245","obo:NCBITaxon_9606"]
    }
```

- In DATS.Dimension:

```
"types": "obo:TODO",
"datatypes" : "obo:TODO",
    
```


Other issues are related to typing the property values when they can belong to multiple schemas. In this case,
we don't type the values in the context file (and this could be done later).

Here we list the cases where this occurs:

- DATS.Activity

```
"performedBy" :
    {
      "@id" : "obo:TODO",
      "@type":["obo:OBI_0000245","obo:NCBITaxon_9606"]
    }
```

- DATS.Dataset.acknowledges may have multiple types
```
"@type":["obo:OBI_0000245","obo:NCBITaxon_9606","obo:OBI_0001942","obo:OBI_0001636"]
```
but not all of them at the same time.
- DATS.Dataset.creators may have multiple values but not all of them at the same time, so we
cannot code

```
"creators":
    {
      "@id" : "obo:TODO",
      "@type":["obo:OBI_0000245","obo:NCBITaxon_9606"]
    }
```

- DATS.Dataset.producedBy multiple values
```
 "@type": ["OBI_0600013","OBI_0000066","OBI_0200000"]
 
```

- DATS.Activity.input multiple values

```
"input" : {
      "@id":"obo:RO_0002233",
      "@type" : ["OBI_0001879","BFO_0000040","IAO_0000100"]
    },
```

- DATS.Activity.output multiple values

```
 "output" :  {
      "@id":"obo:RO_0002234",
      "@type" : ["OBI_0001879","BFO_0000040","IAO_0000100"]
    }
```

- DATS.DataType.platform

```
"platform" : {
      "@id": "obo:RO_0000057",
      "@type": ["obo:OBI_0000968", "obo:IAO_0000010", "OBI_0001879"]
    },
```


- DATS.Dimension.isAbout

```
"isAbout": {
      "@id":"obo:IAO_0000136",
      "@type":["BFO_0000040","IAO_0000100"]
    }
```
 