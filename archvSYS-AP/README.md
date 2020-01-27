# archvSYS-AP 
## Standard for beskrivelse af it-systemer - arkivprofil

Læs specifikationen archvSYS-AP her: https://digst.github.io/IT-System-AP/archvSYS-AP/docs/
(denne side er under udvikling)

## National Archives Application Profile for IT System Description 

This page documents the RDF constructs as applied in a DRAFT for a Danish public-sector specification for describing IT systems for the National Archives. 

## UML Diagram
![UML Diagram](https://github.com/digst/IT-System-AP/blob/master/archvSYS-AP/docs/img/Bilag-E-UML-diagram-Arkivprofil.png "UML")

This page also documents the RDF constructs as applied in a DRAFT for a Danish public-sector specification for describing archival information about IT systems. Please find below an overview of the  main classes and their properties:

# sys:ITSystem (Class)
Definition: system which consists of digital information technologies

| Property (en) | Range | Usage note | Perspective | 
| ---- | ---- | ---- | ---- |
| **dct:identifier**| xsd:anyURI | An unambiguous reference to the resource within a given context., An unambiguous reference to the resource within a given context. | Basic Information |
| **skos:prefLabel**| rdf:langString| | Basic Information |
| **skos:altLabel**| rdf:langString| | Basic Information |
| **dct:description**| rdf:langString| An account of the resource | Basic Information |
| **sys:inUseFromDate**| xsd:date| date on which a system was put into operation | Basic Information |
| **sys:inUseUntilDate**| xsd:date| date on which the it-system was phased out and no longer in operation | Basic Information |
| **sys:operationalStatus**|OperationalStatus| | Basic Information |
| **rdfs:comment**| rdf:langString| A description of the subject resource | Basic Information |
| **sys:usedInOrganization**| org:Organization | | Basic Information |
| **sys:hasApplicationPurposeFORM** | FORMtask | | Tasks |
| **sys:hasApplicationPurposeKLE** | KLETheme | | Tasks |
| **cv:hasLegalResource** | eli:LegalResource | | Tasks |
| **archv:caseArea** | CaseArea | | Tasks |
| **sys:predecessorSystem** | sys:ITSystem | | Tasks |
| **sys:hasCriticality** | CriticalityType | | Tasks |
| **sys:hasITSystemOwner** | org:Organization, org:OrganizationalUnit, foaf:Person | | Tasks |
| **sys:hasSystemDocumentation** | sys:SystemDocumentation | | Tasks |
| **sys:containsData** | xsd:boolean | specification of whether an IT system contains data or documents digitally created by the public administration | Tasks |
| **archv:containsDigitalDocs** | xsd:boolean | | Tasks |

# sys:InstantiatedITSystem (Class)
Definition: it-system which has been implemented in a physical IT environment

| Property (en) | Range | Usage note | Perspective | 
| ---- | ---- | ---- | ---- |
| **sys:instantiationOf** | sys:ITSystem | | |
| **dct:identifier** | xsd:anyURI | | |
| **sys:actsAs** | EnvironmentType | | |
| **sys:producesDataset** | dcat:Dataset | | |
| **archv:prevArchiveInformationPackage** | dcat:Dataset | | |


# dcat:Dataset (Class)
Definition: A collection of data, published or curated by a single agent, and available for access or download in one or more formats

| Property (en) | Range | Usage note | Perspective | 
| ---- | ---- | ---- | ---- |
| **dct:identifier** | xsd:anyURI | An unambiguous reference to the resource within a given context | Information|
| **dct:title** | rdf:langString | A name given to the resource | Information|
| **dct:description** | rdf:langString | An account of the resource | Information|
| **owl:versionInfo** | rdfs:Literal | The annotation property that provides version information for an ontology or another OWL construct | Information|
| **dct:temporal** | dct:PeriodOfTime | | Information|
| **dct:creator** | org:Organization | | Governance  |
| **dcat-dk:dataResponsibleOrganisation** | org:Organization | | Governance  |
| **dcat-dk:dataProcessor** | org:Organization | | Governance  |
| **dcat-dk:personalDataCategory** | PersonalDataCategory | | Security  |
| **dcat-dk:confidentialityType** | ConfidentialityType | | Security  |
| **dcat-dk:hasConfidentialityType** | ConfidentialityTypeNatoEu | | Security  |
| **dcat-dk:hasConfidentialityType** | ConfidentialityTypeISO27002 | | Security  |
| **archv:archivalRegisterType** | RegisterType | | Information  |
| **archv:archivalObligationType** | ArchivalObligationType | | Information  |
| **archv:plannedArchivalFrequency** | ArchivalFrequency | | Information  |
| **archv:nextDataErasureDeadline** | xsd:date | | Information  |
| **archv:prevArchiveInformationPackage** | archv:ArchiveInformationPackage| | Information  |
| **archv:plannedArchiveType** | ArchiveType| | Information  |
| **archv:lastArchivePeriod** | dct:PeriodOfTime| | Information  |
| **prov:wasGeneratedBy** | archv:DataConversion | | Information |


# Codelists (Classifications) used in the application profile:

Codelist: OperationalStatus
* build
* operational
* retired
* transition

Codelist: PublicAdministrativeTaskType
* See: FORM http://www.form-online.dk
* See: KLE http://www.kle-online.dk/

Codelist: PublicOrganizationType
* region
* self-governing institution
* municipality
* govermental administrative unit

Codelist: IT Environment Type
* demonstration
* development
* production
* staging
* testing
* training
* disaster recovery

Codelist: ArchiveType
* archive type
* closed cases and documents
* Snapshot

Codelist: ArchivalObligationType
* archival
* disposal
* unknown

Codelist: PersonalDataCategory
* general personal data
  - civil registration number data
  - data about criminal offences
* sensitive data
* non-personal data

Codelist: ConfidentialityType
* See ISO 27001 Data Classification
* See Nato & EU Data Classification

Codelist: RegisterType
* contains documents
* does not contain documents

Codelist: DataConversionStatus
* full import
* partial import
* unknown

Codelist: CaseArea
See: https://www.retsinformation.dk/eli/lta/2015/266 
See: https://www.retsinformation.dk/eli/lta/2018/183

Codelist: ArchiveOrganisationType
* National archives
* Municipal archive organisation

Codelist: ArchivalFrequency 


## SHACL

Find ITSYSTEM-AP-NATIONALARCHIVES Shapes Graph samt Example Data Graphs (i RDF-XML, TTL, og JSON-LD) i filerne ovenfor

## Tools

* SHACL specification: https://www.w3.org/TR/shacl/
* SHACL Playground: https://shacl.org/playground/
* Interoperability Test Bed: https://joinup.ec.europa.eu/solution/interoperability-test-bed/news/shacl-validator-updates
* RDF converter: http://www.easyrdf.org/converter
* FDA Modelling Tool Support: https://arkitektur.digst.dk/metoder/regler-begrebs-og-datamodellering/faellesoffentlige-regler-begrebs-og-datamodellering-56
