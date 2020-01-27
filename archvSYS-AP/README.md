# archvSYS-AP 
## Standard for beskrivelse af it-systemer - arkivprofil

Læs specifikationen archvSYS-AP her: https://digst.github.io/IT-System-AP/archvSYS-AP/docs/

- denne side er under udvikling

National Archives Application Profile for IT System Description 

This page documents the RDF constructs as applied in a DRAFT for a Danish public-sector specification for describing IT systems for the National Archives. 

Find ITSYSTEM-AP-NATIONALARCHIVES Shapes Graph samt Example Data Graphs (i RDF-XML, TTL, og JSON-LD) i filerne ovenfor

## Tools

* SHACL specification: https://www.w3.org/TR/shacl/
* SHACL Playground: https://shacl.org/playground/
* Interoperability Test Bed: https://joinup.ec.europa.eu/solution/interoperability-test-bed/news/shacl-validator-updates
* RDF converter: http://www.easyrdf.org/converter
* FDA Modelling Tool Support: https://arkitektur.digst.dk/metoder/regler-begrebs-og-datamodellering/faellesoffentlige-regler-begrebs-og-datamodellering-56


## UML Diagram
![UML Diagram](https://github.com/digst/IT-System-AP/blob/master/archvSYS-AP/docs/img/Bilag-E-UML-diagram-Arkivprofil.png "UML")

This page also documents the RDF constructs as applied in a DRAFT for a Danish public-sector specification for describing archival information about IT systems. Please find below an overview of the  main classes and their properties:

# sys:ITSystem (Class)
Definition: system which consists of digital information technologies

Properties (Basic Information Perspective):
* `dct:identifier` (Datatype property) Range: xsd:anyURI. Definition: An unambiguous reference to the resource within a given context., An unambiguous reference to the resource within a given context.
* `skos:prefLabel` (Datatype property) Range: rdf:langString. 
* `skos:altLabel` (Datatype property) Range: rdf:langString. 
* `dct:description` (Datatype property) Range: rdf:langString. Definition: An account of the resource
* `sys:inUseFromDate` (Datatype property) Range: xsd:date. Definition: date on which a system was put into operation
* `sys:inUseUntilDate` (Datatype property) Range: xsd:date. Definition: date on which the it-system was phased out and no longer in operation
* `sys:operationalStatus`  (Object Property) Range: OperationalStatus
* `rdfs:comment` (Datatype property) Range: rdf:langString. Definition: A description of the subject resource.
* `sys:usedInOrganization`  (Object Property) Range: org:Organization


Properties (Tasks Perspective):
* `sys:hasApplicationPurposeFORM`  (Object Property) Range: FORMtask
* `sys:hasApplicationPurposeKLE`  (Object Property) Range: KLETheme
* `cv:hasLegalResource`  (Object Property) Range: eli:LegalResource
* `archv:caseArea`  (Object Property) Range: CaseArea
* `sys:predecessorSystem`  (Object Property) Range: sys:ITSystem
* `sys:hasCriticality`  (Object Property) Range: CriticalityType
* `sys:hasITSystemOwner`  (Object Property) Range: org:Organization/org:OrganizationalUnit/foaf:Person
* `sys:hasSystemDocumentation`  (Object Property) Range: sys:SystemDocumentation
* `sys:containsData` (Datatype property) Range: xsd:boolean. Definition: specification of whether an IT system contains data or documents digitally created by the public administration
* `archv:containsDigitalDocs` (Datatype property) Range: xsd:boolean.


# sys:InstantiatedITSystem (Class)
Definition: it-system which has been implemented in a physical IT environment
* `sys:instantiationOf`  (Object Property) Range: sys:ITSystem
* `dct:identifier` (Datatype property) Range: xsd:anyURI.
* `sys:actsAs`  (Object Property) Range: EnvironmentType
* `sys:producesDataset`  (Object Property) Range: dcat:Dataset
* `archv:prevArchiveInformationPackage`  (Object Property) Range: dcat:Dataset


# dcat:Dataset (Class)
Definition: 
A collection of data, published or curated by a single agent, and available for access or download in one or more formats

Properties (Information Perspective)::
* `dct:identifier` (Datatype property) Range: xsd:anyURI. Definition: An unambiguous reference to the resource within a given context.
* `dct:title` (Datatype property) Range: rdf:langString. Definition: A name given to the resource
* `dct:description` (Datatype property) Range: rdf:langString. Definition: An account of the resource
* `owl:versionInfo` (Datatype property) Range: rdfs:Literal. Definition: The annotation property that provides version information for an ontology or another OWL construct
* `dct:temporal`  (Object Property) Range: dct:PeriodOfTime

Properties (Governance Perspective)::
* `dct:creator`  (Object Property) Range: org:Organization
* `dcat-dk:dataResponsibleOrganisation`  (Object Property) Range: org:Organization
* `dcat-dk:dataProcessor`  (Object Property) Range: org:Organization
* `dcat-dk:personalDataCategory`  (Object Property) Range: PersonalDataCategory
* `dcat-dk:confidentialityType`  (Object Property) Range: ConfidentialityType
* `dcat-dk:hasConfidentialityType`  (Object Property) Range: ConfidentialityTypeNatoEu
* `dcat-dk:hasConfidentialityType`  (Object Property) Range: ConfidentialityTypeISO27002
* `archv:archivalRegisterType`  (Object Property) Range: RegisterType
* `archv:archivalObligationType`  (Object Property) Range: ArchivalObligationType
* `archv:plannedArchivalFrequency`  (Object Property) Range: ArchivalFrequency
* `archv:nextDataErasureDeadline` (Datatype property) Range: xsd:date. Definition: 
* `archv:prevArchiveInformationPackage`  (Object Property) Range: archv:ArchiveInformationPackage
* `archv:plannedArchiveType`  (Object Property) Range: ArchiveType
* `archv:lastArchivePeriod`  (Object Property) Range: dct:PeriodOfTime
* `prov:wasGeneratedBy`  (Object Property) Range: archv:DataConversion


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


