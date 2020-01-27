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


| Property (en) | Range | Usage note | Perspective | 
| ---- | ---- | ---- | ---- |
| `dct:identifier` | xsd:anyURI  | An unambiguous reference to the resource within a given context., An unambiguous reference to the resource within a given context. | Basic Information |
| `skos:prefLabel | rdf:langString |  | Basic Information |
| `skos:altLabel` | rdf:langString |  | Basic Information |
| `dct:description` | rdf:langString | An account of the resource | Basic Information |
| `sys:inUseFromDate` | xsd:date | date on which a system was put into operation | Basic Information |
| `sys:inUseUntilDate` | xsd:date | date on which the it-system was phased out and no longer in operation | Basic Information |
| `sys:operationalStatus` | OperationalStatus |  | Basic Information |
| `rdfs:comment` | rdf:langString  | A description of the subject resource. | Basic Information |
| `sys:usedInOrganization` | org:Organization |  | Basic Information |
| `sys:hasApplicationPurposeFORM` | FORMtask |  |Tasks  |
| `sys:hasApplicationPurposeKLE` | KLETheme |  | Tasks |
| `cv:hasLegalResource` | eli:LegalResource |  | Tasks |
| `archv:caseArea` | CaseArea |  | Tasks |
| `sys:predecessorSystem` | sys:ITSystem |  | Tasks |
| `sys:hasCriticality` | CriticalityType |  | Tasks |
| `sys:hasTargetGroup` | TargetGroup |  | Tasks |
| `sys:hasITSystemOwner`|  org:Organization, org:OrganizationalUnit, foaf:Person |  | Governance |
| `sys:hasITSystemManager`|  org:Organization,  org:OrganizationalUnit, foaf:Person |  | Governance |
| `sys:relatedContract`|  fibo-fnd-agr-ctr:Contract  |  | Legal |
| `dct:rightsHolder`| org:Organization |  | Legal |
| `schema:creator`|  org:Organization |  | Legal |
| `sys:operatedBy` |  org:Organization |  | Legal |
| `sys:maintainedBy` |  org:Organization |  | Legal |
| `comp:instanceOfProductInSeries` | comp:ProductSeries |  | Application |
| `sys:hasSystemDocumentation` | sys:SystemDocumentation |  | Application | 
| `sys:hasAquisitionType`| ITSystemAquisitionType|  | Infrastructure | 
| `sys:containsData` |  xsd:boolean. | specification of whether an IT system contains data or documents digitally created by the public administration | Information | 
| `archv:containsDigitalDocs`| xsd:boolean | | Information | 

<!--Properties
* `sys:hasFunctionalityCapability`  (Object Property) Range: Capability
* `sys:hasVersion`  (Object Property) Range: ITSystemVersion
-->

# sys:InstantiatedITSystem (Class)
Definition: it-system which has been implemented in a physical IT environment

| Property (en) | Range | Usage note | Perspective | 
| ---- | ---- | ---- | ---- |
| `sys:instantiationOf` | sys:ITSystem | | |
| `dct:identifier` | xsd:anyURI. | | |
| `sys:actsAs` | EnvironmentType | | |
| `sys:uses` | dcat:Dataset | | |
| `sys:uses` | dcat:DataService | | |
| `sys:uses` | schema:SoftwareApplication | | |
| `sys:provides` | dcat:Dataset | | |
| `sys:provides` | dcat:DataService | | |
| `sys:provides` | sys:UserInterface | | |
| `sys:producesDataset` | dcat:Dataset | | |


# dcat:Dataset (Class)
Definition: 
A collection of data, published or curated by a single agent, and available for access or download in one or more formats

| Property (en) | Range | Usage note | Perspective | 
| ---- | ---- | ---- | ---- |
| `dct:identifier` | xsd:anyURI | An unambiguous reference to the resource within a given context | Information |
| `dct:title` | rdf:langString | A name given to the resource | Information |
| `dct:description` | rdf:langString| An account of the resource | Information |
| `owl:versionInfo` | rdfs:Literal | The annotation property that provides version information for an ontology or another OWL construct | Information |
| `dct:temporal` | ct:PeriodOfTime | | Information |
| `dct:creator` | org:Organization| | Governance |
| `dcat-dk:dataResponsibleOrganisation` | org:Organization| | Governance |
| `dcat-dk:dataProcessor` | org:Organization| | Governance |
| `dcat-dk:personalDataCategory` | PersonalDataCategory| | Security |
| `dcat-dk:confidentialityType` | ConfidentialityType| | Security |
| `dcat-dk:hasConfidentialityType` | ConfidentialityTypeNatoEu| | Security |
| `dcat-dk:hasConfidentialityType` | ConfidentialityTypeISO27002| | Security |
| `archv:archivalObligationType` | ArchivalObligationType | | Information |

# comp:ProductSeries (Class)
Definition: a series of related products that exhibit the same overall functionality to the user

| Property (en) | Range | Usage note | Perspective | 
| ---- | ---- | ---- | ---- |
| `schema:identifier` | xsd:anyURI | | |
| `skos:prefLabel` | rdf:langString| | |
| `dct:description` | rdf:langString| | |
| `sys:hasCapabilityForPurpose` | PublicAdministrativeTaskType| | |
| `dcatdk:personalDataCategory` | PersonalDataCategory| | |


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


