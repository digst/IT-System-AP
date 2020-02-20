# SYS-AP  (being updated)
Read specification: https://digst.github.io/IT-System-AP/SYS-AP/docs/

## Basic Application Profile for IT System Description (Standard for beskrivelse af it-systemer - basisprofil
This page documents the RDF constructs as applied in a DRAFT for a Danish public-sector specification for describing basic information about IT systems. Please find below an overview of the  main classes and their properties categorised according to the following perspectives: 

![Perspectives](https://github.com/digst/IT-System-AP/blob/master/SYS-AP/docs/img/Figur_illustration_af_standardens_emnemaessige_sammenhaenge(en).PNG "Perspectives")

# sys:ITSystem (Class)
Definition: system which consists of digital information technologies

![IT System](https://github.com/digst/IT-System-AP/blob/master/SYS-AP/docs/img/it-system.png "IT System")

| Property (en) | Range | Usage note | Perspective | 
| ---- | ---- | ---- | ---- |
| **dct:identifier** | xsd:anyURI  | an unambiguous reference to the it-system within a given context. | Basic Information |
| **skos:prefLabel** | rdf:langString | preferred name for the IT system | Basic Information |
| **skos:altLabel** | rdf:langString | alternative name which is accepted but not preferred for the IT system | Basic Information |
| **dct:description** | rdf:langString | an account of the purpose of using the IT system| Basic Information |
| **sys:inUseFromDate** | xsd:date | date on which a system was put into operation | Basic Information |
| **sys:inUseUntilDate** | xsd:date | date on which the it-system was phased out and no longer in operation | Basic Information |
| **sys:operationalStatus** | opstat:OperationalStatus | the status of the it-system with regards to implementation and operation | Basic Information |
| **rdfs:comment** | rdf:langString  | supplementary comments or notes regarding the it-system | Basic Information |
| **sys:containsData** |  xsd:boolean. | specification of whether an IT system contains digitally created data | Information | 
| **archv:containsDigitalDocs**| xsd:boolean | specification of whether an IT system contains digital documents  | Information | 
| **sys:usedInOrganization** | org:Organization | organization that uses the IT system | Basic Information |
| **sys:hasApplicationPurpose** | tasktype:PublicAdministrativeTaskType (subclass of skos:Concept)| the administrative task  which the IT system supports. I.e. FORM or KLE. | Tasks  |
| **cv:hasLegalResource** | eli:LegalResource | legal framework for the application of the IT system | Tasks |
| **sys:hasCriticality** | crit:CriticalityType (subclass of skos:Concept)| specification of how critical the application of the IT system is | Tasks |
| **schema:audience** | target:TargetGroup (subclass of skos:Concept)| specification of which group of users which an IT system is directed at | Tasks |
| **sys:hasITSystemOwner**|  org:Organization, foaf:Person, ovx:OrganizationalPersonIdentifier | organisation or person or organizational identifier for person who has the executive responsibility of the operation, maintenance and application of a specific it-system | Governance |
| **sys:hasITSystemManager**|  org:Organization,  foaf:Person, ovx:OrganizationalPersonIdentifier | organisation or person or organizational identifier for person who manages and makes descisions on the daily technical aspects on behalf of the IT system owner | Governance |
| **dct:rightsHolder**| org:Organization | organisation owning or managing the intellectual rights of the primary software product of the it-system | Legal |
| **dct:creator**|  org:Organization | individual or organization that performs the foundational development activities (including requirements analysis, design, testing through acceptance) during the system or software life cycle process  | Legal |
| **sys:operatedBy** |  org:Organization | organizational unit or individual that is responsible for the operation of the IT system| Legal |
| **sys:maintainedBy** |  org:Organization | individual or organization that is responsible for the maintenance of an it-system  | Legal |
| **infra:instanceOfProductInSeries** | infra:ProductSeries | instance of product in series | Application |
| **sys:hasSystemDocumentation** | foaf:Document | reference to document that describe the requirements, capabilities, limitations, design, operation, or maintenance of an IT system | Application | 
| **sys:hasAquisitionType**| aquis:ITSystemAquisitionType (subclass of skos:Concept, subclass of tasktype:TaskType)| specification of how the IT system was acquired | Infrastructure |
| **tasktype:canPerformTaskType**| tasktype:TaskType subclass of skos:Concept| specification of the type of tasks the system can perform | Tasks |
| **capa:hasCapability**| capa:Capability subclass of skos:Concept | specification of the type of capability the system has | Tasks |
| **sys:enablesProcess**| proc:BusinessProcess | specification of the business process which a specific IT system supports | Tasks |
| **ovx:enablesFunction**| ovx:BusinessFunction | specification of the function that the system is enabling | Tasks |
| **sys:predecessorSystem**| sys:ITSystem | specification of an IT system that was previously used for functionality that is supported by the current IT system. | Governance |
<!--Properties
* **sys:hasFunctionalityCapability**  (Object Property) Range: Capability
* **sys:hasVersion**  (Object Property) Range: ITSystemVersion
-->

# sys:InstantiatedITSystem (Class)
Definition: it-system which has been implemented in a physical IT environment

| Property (en) | Range | Usage note | Perspective | 
| ---- | ---- | ---- | ---- |
| **dct:identifier** | xsd:anyURI. | an unambiguous reference to the instantiated it-system within a given context.| |
| **sys:instantiationOf** | sys:ITSystem | specification of the IT system which is instantiated and deployed in an IT environment | |
| **sys:actsAs** | techenv:EnvironmentType | specification of the environment type which the IT system is deployed in| |
| **sys:uses** | dcat:Distribution | specifies a dataset distribution which the IT system uses | |
| **sys:uses** | dcat:DataService | specifies a dataservice which the IT system uses | |
| **sys:provides** | dcat:Disribution | dataset distribution which the IT system provides | |
| **sys:provides** | dcat:DataService | dataservice which the IT system provides| |
| **sys:provides** | sys:UserInterface | software application which the IT system provides | |
| **sys:producesDataset** | dcat:Distribution |dataset distribution which the IT system produces | |

# dcat:Dataset (Class)
Definition: A collection of data, published or curated by a single agent, and available for access or download in one or more formats

| Property (en) | Range | Usage note | Perspective | 
| ---- | ---- | ---- | ---- |
| **dct:title** | rdf:langString | A name given to the dataset | Information |
| **dct:identifier** | xsd:anyURI | An unambiguous reference to the dataset within a given context | Information |
| **dct:description** | rdf:langString| An account of the dataset | Information |
| **owl:versionInfo** | rdfs:Literal | The annotation property that provides version information for an ontology or another OWL construct | Information |
| **dct:creator** | org:Organization| organisation who has the primary responsibility for the creation of the dataset | Governance |
| **dcat-dk:dataResponsibleOrganisation** | org:Organization| agent who has the administrative responsibility of the dataset | Governance |
| **dcat-dk:dataProcessor** | org:Organization| natural or legal person, public authority, agency or other body which, alone or jointly with others, determines the purposes and means of the processing of personal data| Governance |
| **dcat-dk:personalDataCategory** | pers-cat:PersonalDataCategory|specification of a relation to specific personal data category | Security |
| **dcat-dk:hasConfidentialityType** | conf-eu:ConfidentialityTypeNatoEu (subclass of skos:Concept, conf:ConfidentialityType)| the extent by which information contained in a dataset can be disclosed | Security |
| **dcat-dk:hasConfidentialityType** | conf-iso:ConfidentialityTypeISO27002 (subclass of skos:Concept, conf:ConfidentialityType)|the extent by which information contained in a dataset can be disclosed | Security |
| **dct:partOf**| sys:ITSystem | Relates the dataset to an  IT System that it can be considered to be a part of. |  |

# infra:ProductSeries (Class)
Definition: a series of related products that exhibit the same overall functionality to the user

| Property (en) | Range | Usage note | Perspective | 
| ---- | ---- | ---- | ---- |
| **schema:identifier** | xsd:anyURI |An unambiguous reference to the dataset within a given context | |
| **skos:prefLabel** | rdf:langString|preferred name for the product series | |
| **dct:description** | rdf:langString|An account of the product series | |
| **sys:hasCapabilityForPurpose** | PublicAdministrativeTaskType (subclass of skos:Concept)|specifiction of the task that products in the relevant product series have the capability to support  | |
| **dcatdk:personalDataCategory** | PersonalDataCategory (subclass of skos:Concept)| specification of a relation to specific personal data category | |


# schema:ContactPoint (Class)
Definition: A contact point—for example, a Customer Complaints department 

| Property (en) | Range | Usage note | Perspective | 
| ---- | ---- | ---- | ---- |
| **schema:email**| xsd:string | an email address that can be used to contact the agent |  |
| **schema:telephone**| xsd:string | an telephone number that can be used to contact the agent |  |
| **schema:contactType**| xsd:string | a person or organization can have different contact points, for different purposes. This property is used to specify the kind of contact point. |  |
| **schema:productSupported**| xsd:string | The product or service this support contact point is related to (such as product support for a particular product line). |  |

# foaf:Person (Class)
Definition: The Person class represents people

| Property (en) | Range | Usage note | Perspective | 
| ---- | ---- | ---- | ---- |
| **schema:contactPoint**| schema:ContactPoint | specifies a contact point through which the person can be contacted |  |

# ovx:OrganizationalPersonIdentifier (Class)
Definition: a container that holds information about the unique code used to identify a person within an organization.

| Property (en) | Range | Usage note | Perspective | 
| ---- | ---- | ---- | ---- |
| **ovx:personCode**| xsd:string | code used within an organization as a unique identifier for a person with a relation to the organization  |  |

# org:Organization (Class)
Definition: Represents a collection of people organized together into a community or other social, commercial or political structure. In the context of this application profile is can be specialized as a formal organization (org:FormalOrganization), as an organizational unit (org:OrganizationalUnit) and as a public organization (cpov:PublicOrganization).

| Property (en) | Range | Usage note | Perspective | 
| ---- | ---- | ---- | ---- |
| **skos:prefLabel**| rdf:langString | preferred name for the organization in one or more languages |  |
| **schema:contactPoint**| schema:ContactPoint | specifies a contact point through which the organization can be contacted |  |
| **org:classification**| oc:PublicOrganizationType | Indicates the type of public organization this organization is classified as |  |

# fibo-fnd-agr-ctr:Contract (Class)
Definition: a voluntary, deliberate, and legally binding agreement between two or more competent parties

| Property (en) | Range | Usage note | Perspective | 
| ---- | ---- | ---- | ---- |
| **dct:identifier**| xsd:anyURI | an unambiguous reference to a contract |  |
| **dct:type**| ITSystemContractType | specification of the type of the contract with regards to relationship between the contract parties |  |
| **fibo-fnd-agr-ctr:hasContractParty**| org:Organization | has a party which is a signatory to the contract and to which is granted certain rights and obligations as defined in the contract and which concedes certain rights to and imposes certain obligations upon the other party as defined in the contract |  |
| **fibo-fnd-agr-ctr:hasPrincipal**| org:Organization | contract party that carries the role as the customer |  |
| **fibo-fnd-agr-ctr:hasCounterparty**| org:Organization | identifies a counterparty to a contract |  |
| **fibo-fnd-agr-ctr:definesTermsFor**| sys:ITSystem | the contract sets out the terms for the IT system |  |

# foaf:Document (Class)
Definition: The Document class represents those things which are, broadly conceived, 'documents'


# sys:ITSystemReport  (Class)
Definition: report containing information about a number of it-systems to be sent to a specific recipient with a specific purpose

| Property (en) | Range | Usage note | Perspective | 
| ---- | ---- | ---- | ---- |
| **dct:dateSubmitted**| xsd:date | date at which the it system information was submitted |  |
| **syscoveredITSystem**| sys:ITSystem or sys:InstantiatedITSystem | Indicates the IT system or instantiated IT system that is covered by the report |  |
| **frbr:responsibleEntity**| org:Organization | an organization that is responsible for the report |  |

# dcat:Distribution (Class)
Definition: A specific representation of a dataset. A dataset might be available in multiple serializations that may differ in various ways, including natural language, media-type or format, schematic organization, temporal and spatial resolution, level of detail or profiles (which might specify any or all of the above).

| Property (en) | Range | Usage note | Perspective | 
| ---- | ---- | ---- | ---- |
| **dct:title**| xsd:string | a name given to the dataset distribution |  |
| **dct:issued**| xsd:dateTime | date of formal issuance (e.g., publication) of the dataset distribution |  |
| **dct:modified**| xsd:dateTime | date on which the dataset distribution was changed |  |
| **dcat:accessService**| dcat:DataService | a site or end-point that gives access to the distribution of the dataset |  |

# dcat:DataService  (Class)
Definition: : A site or end-point providing operations related to the discovery of, access to, or processing functions on, data or related resources.

| Property (en) | Range | Usage note | Perspective | 
| ---- | ---- | ---- | ---- |
| **dcat:endpointURL**| xsd:anyURI | the root location or primary endpoint of the service (a web-resolvable IRI). |  |
| **dcat:endpointDescription**| xsd:string | a description of the service end-point, including its operations, parameters etc |  |

# eli:LegalResource (Class)
Definition: A distinct intellectual creation (i.e., the intellectual content). For example, the abstract concept of the legal resource; e.g. "act 3 of 2005" (adapted from Akoma Ntoso) A legal resource can represent a legal act or any component of a legal act, like an article. Legal resources can be linked together using properties defined in the model. Note that ELI ontology accommodates different point of view on what should be considered a new legal resource, or a new legal expression of the same resource. Typically, a consolidated version can be viewed, in the context of ELI, either as separate legal resource (linked to original version and previous consolidated version using corresponding ELI relations), or as a different legal expression of the same legal resource.


# proc:BusinessProcess (Class)
Definition: : a sequence of business behaviors that achieves a specific outcome such as a defined set of products or business services


# ovx:BusinessFunction (Class)
Definition: activity carried out by an organization

| Property (en) | Range | Usage note | Perspective | 
| ---- | ---- | ---- | ---- |
| **ovx:usesItSystem**| sys:ITSystem | indicates an IT system used in the process of a business function |  |


# Codelists (Classifications) used in the application profile:

Codelist: OperationalStatus
* build
* operational
* transition
* retired


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


| Prefix | Namespace | Vocabulary | 
| ---- | ---- | ---- |						
| rdf		|http://www.w3.org/1999/02/22-rdf-syntax-ns#	|The RDF Concepts Vocabulary  (W3C)
| rdfs	|	http://www.w3.org/2000/01/rdf-schema#	|RDF Schema 1.1  (W3C)
| owl	|	http://www.w3.org/2002/07/owl#		|Web Ontology Language  (W3C)
| xml		|http://www.w3.org/XML/1998/namespace	|XML Namespace  (W3C)
| xsd		|http://www.w3.org/2001/XMLSchema# 	|XML Schema  (W3C)
| skos	|	http://www.w3.org/2004/02/skos/core#	|Simple Knowledge Organization System (W3C)
| org		|http://www.w3.org/ns/org# 			|The Organization Ontology (W3C)
| foaf	|	http://xmlns.com/foaf/0.1/			|Friend of a Friend
| dcat		|https://www.w3.org/ns/dcat# 			|Dataset Catalogue Vocabulary  (W3C)
| dcat-dk		|https://data.gov.dk/model/core/dcat-dk# 	|DCAT DK
| prov	|	http://www.w3.org/ns/prov#		|	The PROV Ontology (W3C)
| vann	|	http://purl.org/vocab/vann/			|A Vocabulary for Annotating Vocabulary Description
| dct		|http://purl.org/dc/terms/			|Dublin Core Terms
| eli	|	http://data.europa.eu/eli/ontology#			|	European Legislation Identifier   
| cpov	|	http://purl.org/vocab/cpsv# 					|Core Public Service Vocabulary (ISA) 
| cv	|	http://data.europa.eu/m8g/				|	Core Vocabulary (ISA)	
| schema		|https://schema.org/ 						|Schema.org
| fibo-fnd-agr-ctr	|https://spec.edmcouncil.org/fibo/FND/Agreements/Contracts  	|Financial Industry Business Ontology (OMG)
| target|	https://data.gov.dk/concept/core/targetgroup/	| Vocabuulary for Target group
| sys	|	https://data.gov.dk/model/core/itsystem/			|Vocabulary for IT System 
| archv		|https://data.gov.dk/model/core/digitalarchival/		|Vocabulary for Digital Archival  
| infra	|	https://data.gov.dk/model/core/infrastructure/		|Vocabulary for IT System Infrastructure 
| proc|		https://data.gov.dk/model/core/process/			|Vocabulary for Cross Domain Processes 
| ovx|	https://data.gov.dk/model/core/organization-extension/	|Organization Vocabulary Extention 


