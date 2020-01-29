# SYS-AP  (being updated)
## Standard for beskrivelse af it-systemer - basisprofil
Læs specifikationen SYS-AP her: https://digst.github.io/IT-System-AP/SYS-AP/docs/

## Basic Application Profile for IT System Description (DRAFT)
This page documents the RDF constructs as applied in a DRAFT for a Danish public-sector specification for describing basic information about IT systems. Please find below an overview of the  main classes and their properties: 

[Perspectives](https://github.com/digst/IT-System-AP/blob/master/SYS-AP/docs/img/Figur_illustration_af_standardens_emnemaessige_sammenhaenge(en).PNG)

# sys:ITSystem (Class)
Definition: system which consists of digital information technologies

| Property (en) | Range | Usage note | Perspective | 
| ---- | ---- | ---- | ---- |
| **dct:identifier** | xsd:anyURI  | an unambiguous reference to the it-system within a given context. | Basic Information |
| **skos:prefLabel** | rdf:langString | preferred name for the IT system | Basic Information |
| **skos:altLabel** | rdf:langString | alternative name which is accepted but not preferred for the IT system | Basic Information |
| **dct:description** | rdf:langString | an account of the purpose of using the IT system| Basic Information |
| **sys:inUseFromDate** | xsd:date | date on which a system was put into operation | Basic Information |
| **sys:inUseUntilDate** | xsd:date | date on which the it-system was phased out and no longer in operation | Basic Information |
| **sys:operationalStatus** | OperationalStatus | the status of the it-system with regards to implementation and operation | Basic Information |
| **rdfs:comment** | rdf:langString  | supplementary comments or notes regarding the it-system | Basic Information |
| **sys:usedInOrganization** | org:Organization | organization that uses the IT system | Basic Information |
| **sys:hasApplicationPurposeFORM** | FORMtask | the FORM task which the IT system supports | Tasks  |
| **sys:hasApplicationPurposeKLE** | KLETheme | the KLE theme which the IT system supports | Tasks |
| **cv:hasLegalResource** | eli:LegalResource | legal framework for the application of the IT system | Tasks |
| **sys:hasCriticality** | CriticalityType | specification of how critical the application of the IT system is | Tasks |
| **sys:hasTargetGroup** | TargetGroup | specification of which group of users which an IT system is directed at | Tasks |
| **sys:hasITSystemOwner**|  org:Organization, org:OrganizationalUnit, foaf:Person | person or organisation who has the executive responsibility of the operation, maintenance and application of a specific it-system | Governance |
| **sys:hasITSystemManager**|  org:Organization,  org:OrganizationalUnit, foaf:Person | organisational unit or employee who manages and makes descisions on the daily technical aspects on behalf of the IT system owner | Governance |
| **sys:relatedContract**|  fibo-fnd-agr-ctr:Contract  |  | Legal |
| **dct:rightsHolder**| org:Organization | organisation owning or managing the intellectual rights of the primary software product of the it-system | Legal |
| **schema:creator**|  org:Organization | individual or organization that performs the foundational development activities (including requirements analysis, design, testing through acceptance) during the system or software life cycle process  | Legal |
| **sys:operatedBy** |  org:Organization | organizational unit or individual that is responsible for the operation of the IT system| Legal |
| **sys:maintainedBy** |  org:Organization | individual or organization that is responsible for the maintenance of an it-system  | Legal |
| **comp:instanceOfProductInSeries** | comp:ProductSeries | instance of product in series | Application |
| **sys:hasSystemDocumentation** | sys:SystemDocumentation | reference to document that describe the requirements, capabilities, limitations, design, operation, or maintenance of an IT system | Application | 
| **sys:hasAquisitionType**| ITSystemAquisitionType| specification of how the IT system was acquired | Infrastructure | 
| **sys:containsData** |  xsd:boolean. | specification of whether an IT system contains digitally created data | Information | 
| **archv:containsDigitalDocs**| xsd:boolean | specification of whether an IT system contains digital documents  | Information | 

<!--Properties
* **sys:hasFunctionalityCapability**  (Object Property) Range: Capability
* **sys:hasVersion**  (Object Property) Range: ITSystemVersion
-->

# sys:InstantiatedITSystem (Class)
Definition: it-system which has been implemented in a physical IT environment

| Property (en) | Range | Usage note | Perspective | 
| ---- | ---- | ---- | ---- |
| **sys:instantiationOf** | sys:ITSystem | | |
| **dct:identifier** | xsd:anyURI. | | |
| **sys:actsAs** | EnvironmentType | | |
| **sys:uses** | dcat:Dataset | | |
| **sys:uses** | dcat:DataService | | |
| **sys:uses** | schema:SoftwareApplication | | |
| **sys:provides** | dcat:Dataset | | |
| **sys:provides** | dcat:DataService | | |
| **sys:provides** | sys:UserInterface | | |
| **sys:producesDataset** | dcat:Dataset | | |


# dcat:Dataset (Class)
Definition: A collection of data, published or curated by a single agent, and available for access or download in one or more formats

| Property (en) | Range | Usage note | Perspective | 
| ---- | ---- | ---- | ---- |
| **dct:identifier** | xsd:anyURI | An unambiguous reference to the dataset within a given context | Information |
| **dct:title** | rdf:langString | A name given to the dataset | Information |
| **dct:description** | rdf:langString| An account of the dataset | Information |
| **owl:versionInfo** | rdfs:Literal | The annotation property that provides version information for an ontology or another OWL construct | Information |
| **dct:temporal** | ct:PeriodOfTime | | Information |
| **dct:creator** | org:Organization| organisation who has the primary responsibility for the creation of the dataset | Governance |
| **dcat-dk:dataResponsibleOrganisation** | org:Organization| | Governance |
| **dcat-dk:dataProcessor** | org:Organization| | Governance |
| **dcat-dk:personalDataCategory** | PersonalDataCategory| | Security |
| **dcat-dk:confidentialityType** | ConfidentialityType| | Security |
| **dcat-dk:hasConfidentialityType** | ConfidentialityTypeNatoEu| | Security |
| **dcat-dk:hasConfidentialityType** | ConfidentialityTypeISO27002| | Security |
| **archv:archivalObligationType** | ArchivalObligationType | | Information |

# comp:ProductSeries (Class)
Definition: a series of related products that exhibit the same overall functionality to the user

| Property (en) | Range | Usage note | Perspective | 
| ---- | ---- | ---- | ---- |
| **schema:identifier** | xsd:anyURI | | |
| **skos:prefLabel** | rdf:langString| | |
| **dct:description** | rdf:langString| | |
| **sys:hasCapabilityForPurpose** | PublicAdministrativeTaskType| | |
| **dcatdk:personalDataCategory** | PersonalDataCategory| | |


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


