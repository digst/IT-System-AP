# archvSYS-AP 
## Standard for beskrivelse af it-systemer - arkivprofil

Læs specifikationen archvSYS-AP her: https://digst.github.io/IT-System-AP/archvSYS-AP/docs/ 

## National Archives Application Profile for IT System Description 

This page documents the RDF constructs as applied in a DRAFT for a Danish public-sector specification for describing IT systems for the National Archives.  Example Data Graphs (Coming soon) - ITSYSTEM-AP-NATIONALARCHIVES Shapes Graph and Example Data Graphs 

## Simple spreadsheet template
https://data.gov.dk/document/itsystem-ap/v1/templates/Excelformular_til_indtastning_af_it-systemoplysninger_arkivprofil.xlsx

## UML Diagram
![UML Diagram](https://github.com/digst/IT-System-AP/blob/master/archvSYS-AP/docs/img/Bilag-E-UML-diagram-Arkivprofil.png "UML")

This page also documents the RDF constructs as applied in a DRAFT for a Danish public-sector specification for describing archival information about IT systems. Please find below an overview of the  main classes and their properties:

# sys:ITSystem (Class)
Definition: system which consists of digital information technologies

| Property (en) | Range | Usage note | Perspective | 
| ---- | ---- | ---- | ---- |
| **dct:identifier**| xsd:anyURI | An unambiguous reference to the resource within a given context., An unambiguous reference to the resource within a given context. | Basic Information |
| **skos:prefLabel**| rdf:langString|preferred name for the IT system | Basic Information |
| **skos:altLabel**| rdf:langString|alternative name which is accepted but not preferred for the IT system | Basic Information |
| **dct:description**| rdf:langString| An account of the resource | Basic Information |
| **sys:inUseFromDate**| xsd:date| date on which a system was put into operation | Basic Information |
| **sys:inUseUntilDate**| xsd:date| date on which the it-system was phased out and no longer in operation | Basic Information |
| **sys:operationalStatus**|OperationalStatus| the status of the it-system with regards to implementation and operation| Basic Information |
| **rdfs:comment**| rdf:langString| A description of the subject resource | Basic Information |
| **sys:usedInOrganization**| org:Organization | organization that uses the IT system  | Basic Information |
| **sys:hasApplicationPurposeFORM** | FORMtask |the FORM task which the IT system supports | Tasks |
| **sys:hasApplicationPurposeKLE** | KLETheme | the KLE theme which the IT system supports| Tasks |
| **cv:hasLegalResource** | eli:LegalResource |legal framework for the application of the IT system  | Tasks |
| **archv:caseArea** | CaseArea | the case area which a specific IT system supports | Tasks |
| **sys:predecessorSystem** | sys:ITSystem | IT system which previously supported the function before the current IT system replaced it | Tasks |
| **sys:hasCriticality** | CriticalityType | specification of how critical the application of the IT system is| Tasks |
| **sys:hasITSystemOwner** | org:Organization, org:OrganizationalUnit, foaf:Person | organisation or person who has the executive responsibility of the operation, maintenance and application of a specific it-system | Tasks |
| **sys:hasSystemDocumentation** | sys:SystemDocumentation | reference to document that describe the requirements, capabilities, limitations, design, operation, or maintenance of an IT system | Tasks |
| **sys:containsData** | xsd:boolean | specification of whether an IT system contains data or documents digitally created by the public administration | Tasks |
| **archv:containsDigitalDocs** | xsd:boolean | specification of whether an IT system contains digital documents | Tasks |

# sys:InstantiatedITSystem (Class)
Definition: it-system which has been implemented in a physical IT environment

| Property (en) | Range | Usage note | Perspective | 
| ---- | ---- | ---- | ---- |
| **sys:instantiationOf** | sys:ITSystem |specification of the IT system which is instantiated and deployed in an IT environment  | |
| **dct:identifier** | xsd:anyURI |an unambiguous reference to the instantiated it-system within a given context | |
| **sys:actsAs** | EnvironmentType | specification of the environment type which the IT system is deployed in | |
| **sys:producesDataset** | dcat:Distribution |dataset which the IT system produces | Information|
| **archv:latestArchiveInformationPackage** | archv:ArchiveInformationPackage | specification of the distribution that contains the latest archive information package | |


# dcat:Dataset (Class)
Definition: A collection of data, published or curated by a single agent, and available for access or download in one or more formats

| Property (en) | Range | Usage note | Perspective | 
| ---- | ---- | ---- | ---- |
| **dct:identifier** | xsd:anyURI | An unambiguous reference to the resource within a given context | Information|
| **dct:title** | rdf:langString | A name given to the resource | Information|
| **dct:description** | rdf:langString | An account of the resource | Information|
| **owl:versionInfo** | rdfs:Literal | The annotation property that provides version information for an ontology or another OWL construct | Information|
| **dcat-dk:dataResponsibleOrganisation** | org:Organization |agent who has the administrative responsibility of the dataset  | Governance  |
| **dcat-dk:dataProcessor** | org:Organization | natural or legal person, public authority, agency or other body which, alone or jointly with others, determines the purposes and means of the processing of personal data| Governance  |
| **dct:creator** | org:Organization | organisation who has the primary responsibility for the creation of the dataset| Governance  |
| **dcat-dk:personalDataCategory** | PersonalDataCategory |specification of a relation to specific personal data category | Security  |
| **dcat-dk:confidentialityType** | ConfidentialityType | the extent by which information contained in a dataset can be disclosed| Security  |
| **dcat-dk:hasConfidentialityType** | ConfidentialityTypeNatoEu |the extent by which information contained in a dataset can be disclosed (NatoEU) | Security  |
| **dcat-dk:hasConfidentialityType** | ConfidentialityTypeISO27002 |the extent by which information contained in a dataset can be disclosed (ISO27002) | Security  |
| **archv:archivalRegisterType** | RegisterType | specification of whether the data set contains documents created by the public administration or not | Information  |
| **archv:archivalObligationType** | ArchivalObligationType | specification of whether the data is to archived, diposed or if the obligation is unknown | Information  |
| **archv:plannedArchivalFrequency** | ArchivalFrequency | frequency by which an authority has planned to create archive information packages | Information  |
| **archv:plannedArchiveType** | ArchiveType| | Information  |
| **dcat:distribution** | dcat:Distribution | An available distribution of the dataset.| Information  |

# dcat:Distribution (Class)
Definition: A specific representation of a dataset. A dataset might be available in multiple serializations that may differ in various ways, including natural language, media-type or format, schematic organization, temporal and spatial resolution, level of detail or profiles (which might specify any or all of the above). 

| Property (en) | Range | Usage note | Perspective | 
| ---- | ---- | ---- | ---- |
| **dct:issued** |  xsd:dateTime  | date of formal issuance (e.g., publication) of the resource. | Information|
| **dct:modified** | xsd:dateTime |  date on which the resource was changed. | Information|
| **archv:nextDataErasureDeadline** | xsd:date | the proximate date for when certain data in the it-system is expected to be deleted before in accordance with GDPR | Information  |
| **prov:wasGeneratedBy** | archv:DataConversion | specification of the activity whereby data was converted and imported into a dataset | Information |

# dcat:ArchiveInformationPackage (Class)
Definition: Package containing data to be archived as well as a description of the structure of the data and its contents, use and originating IT system. 

| Property (en) | Range | Usage note | Perspective | 
| ---- | ---- | ---- | ---- |
| **dct:hasPart** |  xsd:dateTime  | The specific representation of a dataset which is contained in an archive information package | Information|


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



## Tools

* SHACL specification: https://www.w3.org/TR/shacl/
* SHACL Playground: https://shacl.org/playground/
* Interoperability Test Bed: https://joinup.ec.europa.eu/solution/interoperability-test-bed/news/shacl-validator-updates
* RDF converter: http://www.easyrdf.org/converter
* FDA Modelling Tool Support: https://arkitektur.digst.dk/metoder/regler-begrebs-og-datamodellering/faellesoffentlige-regler-begrebs-og-datamodellering-56
