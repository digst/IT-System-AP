# SYS-AP  (being updated)
## Standard for beskrivelse af it-systemer - basisprofil

Læs specifikationen SYS-AP her: https://digst.github.io/IT-System-AP/SYS-AP/docs/



# SYS-AP 

## Basic Application Profile for IT System Description (DRAFT)

This page documents the RDF constructs as applied in a DRAFT for a Danish public-sector specification for describing basic information about IT systems. 
<!--
Please find below an overview of the  main classes and their properties:Full documentation of the model elements can be found at [this address](https://data.gov.dk/rdf2html/index.htm?model=https%3A%2F%2Fdata.gov.dk%2Fmodel%2Fprofile%2Fitsystemap.rdf&sheet=transform2RDFreport_da-en.xsl)
-->

# sys:ITSystem (Class)
Definition: system which consists of digital information technologies

Properties (Basic Information Perspective):

| Property (da) | Property (en) | Range | Usage note | 
| ---- | ---- | ---- | ---- |
|  | `dct:identifier` | xsd:anyURI  | An unambiguous reference to the resource within a given context., An unambiguous reference to the resource within a given context. | 
|  | `skos:prefLabel | rdf:langString |  |
|  | `skos:altLabel` | rdf:langString |  |
|  | `dct:description` | rdf:langString | An account of the resource |
|  | `sys:inUseFromDate` | xsd:date | date on which a system was put into operation |
|  | `sys:inUseUntilDate` | xsd:date | date on which the it-system was phased out and no longer in operation |
|  | `sys:operationalStatus` | OperationalStatus |  |
|  | `rdfs:comment` | rdf:langString  | A description of the subject resource. |
|  | `sys:usedInOrganization` | org:Organization |  |
|  |  |  |  |

Properties (Tasks Perspective):
| Property (da) | Property (en) | Range | Usage note | 
| ---- | ---- | ---- | ---- |
|  | `sys:hasApplicationPurposeFORM` | FORMtask |  |
|  | `sys:hasApplicationPurposeKLE` | KLETheme |  |
|  | `cv:hasLegalResource` | eli:LegalResource |  |
|  | `archv:caseArea` | CaseArea |  |
|  | `sys:predecessorSystem` | sys:ITSystem |  |
|  | `sys:hasCriticality` | CriticalityType |  |
|  | `sys:hasTargetGroup` | TargetGroup |  |

Properties (Governance Perspective):
* `sys:hasITSystemOwner`  (Object Property) Range: org:Organization/org:OrganizationalUnit/foaf:Person
* `sys:hasITSystemManager`  (Object Property) Range: org:Organization/org:OrganizationalUnit/foaf:Person

Properties (Legal Perspective):
* `sys:relatedContract`  (Object Property) Range: fibo-fnd-agr-ctr:Contract
* `dct:rightsHolder`  (Object Property) Range: org:Organization
* `schema:creator`  (Object Property) Range: org:Organization
* `sys:operatedBy`  (Object Property) Range: org:Organization
* `sys:maintainedBy`  (Object Property) Range: org:Organization
* `sys:contractRegarding`  (Object Property) Range: sys:ITSystem* `sys:selectedITsystemForReport`  (Object Property) Range: sys:ITSystem

Properties (Application Perspective):
* `comp:instanceOfProductInSeries`  (Object Property) Range: comp:ProductSeries
* `sys:hasSystemDocumentation`  (Object Property) Range: sys:SystemDocumentation

Properties (Infrastructure Perspective):
* `sys:hasAquisitionType`  (Object Property) Range: ITSystemAquisitionType

Properties (Information Perspective):
* `sys:containsData` (Datatype property) Range: xsd:boolean. Definition: specification of whether an IT system contains data or documents digitally created by the public administration
* `archv:containsDigitalDocs` (Datatype property) Range: xsd:boolean.

<!--Properties
* `sys:hasFunctionalityCapability`  (Object Property) Range: Capability
* `sys:hasVersion`  (Object Property) Range: ITSystemVersion
-->

# sys:InstantiatedITSystem (Class)
Definition: it-system which has been implemented in a physical IT environment
* `sys:instantiationOf`  (Object Property) Range: sys:ITSystem
* `dct:identifier` (Datatype property) Range: xsd:anyURI.
* `sys:actsAs`  (Object Property) Range: EnvironmentType
* `sys:uses`  (Object Property) Range: dcat:Dataset
* `sys:uses`  (Object Property) Range: dcat:DataService
* `sys:uses`  (Object Property) Range: schema:SoftwareApplication
* `sys:provides`  (Object Property) Range: dcat:Dataset
* `sys:provides`  (Object Property) Range: dcat:DataService
* `sys:provides`  (Object Property) Range: sys:UserInterface
* `sys:producesDataset`  (Object Property) Range: dcat:Dataset


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
* `archv:archivalObligationType`  (Object Property) Range: ArchivalObligationType

# comp:ProductSeries (Class)
Definition: a series of related products that exhibit the same overall functionality to the user

Properties:
* `schema:identifier` (Datatype property) Range: xsd:anyURI. 
* `skos:prefLabel` (Datatype property) Range: rdf:langString. 
* `dct:description` (Datatype property) Range: rdf:langString.
* `sys:hasCapabilityForPurpose`  (Object Property) Range: PublicAdministrativeTaskType
* `dcatdk:personalDataCategory`  (Object Property) Range: PersonalDataCategory


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

Codelist: CriticalityType
* critical for business
* critial for society
* not critical

Codelist: ITSystemAquisitionType
* Commercial off the shelf
* in house developement
* open source
* ordered developement

Codelist: IT Environment Type
* demonstration
* development
* production
* staging
* testing
* training
* disaster recovery

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

Codelist: ITSystemContractType
* development contract
* maintenance contract
* operations contract

Codelist: TargetGroup
* external
* internal 


