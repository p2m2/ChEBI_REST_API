# ChEBI REST API

version 0.0

## Status

### Reuse Compliance

### Test

## Description

Docker image to use [ChEBI web services](https://www.ebi.ac.uk/chebi/webServices.do).
The image provides a REST API to query ChEBI database.

## Installation

```bash
docker run -it --rm -p 1050:1050 docker.io/1m1p/chebi-rest-api
```

## Usage

### getLiteEntity

- Looking for a specific entity by name.  
```localhost:1050/getLiteEntity?search=hydrogen```

- Looking for a specific entity by a category.  
```localhost:1050/getLiteEntity?search=CHEBI:49637&category=ID```

- Looking for a specific entity limited by the number of results.  
```localhost:1050/getLiteEntity?search=hydrogen&limit=5```

- Looking for a specific entity by number stars (2 or 3).  
```localhost:1050/getLiteEntity?search=hydrogen&stars=3```

#### Categories

| Category | in URL |
| --- | --- |
| ALL | all |
| CHEBI ID | id |
| CHEBI NAME | name |
| DEFINITION | def |
| ALL NAMES | syn |
|IUAPC NAME | iuapc |
|CITATION | cita |
| REGISTRY NUMBER | reg |
|MANUAL XREF | mxref |
|AUTOMATIC XREF | axref |
|FORMULA | form |
|MASS | mass |
|MONOISOTOPIC MASS | monomass |
| INCHI/INCHI KEY | inchi |
|SMILES | smiles |
|SPECIES | species |

