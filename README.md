IT-System-AP
===== 

This page documents the RDF constructs as applied in a draft for a Danish public-sector specification for describing IT systems. 

Information about public-sector IT systems is exchanged in many different contexts and for many different purposes, and this provides interest and motivation for standardizing the way IT systems are described in order to support higher reuse and quality of data about IT systems.

Please find below a description of the  main classes and their properties:


# sys:ITSystem (Class)
Definition: system which consists of digital information technologies

Properties (Basic Information Perspective):
* <dct:identifier> (Datatype property) Range: xsd:anyURI. Definition: An unambiguous reference to the resource within a given context., An unambiguous reference to the resource within a given context.
* <skos:prefLabel> (Datatype property) Range: rdf:langString. Definition: 
* <skos:altLabel> (Datatype property) Range: rdf:langString. Definition: 
* <dct:description> (Datatype property) Range: rdf:langString. Definition: An account of the resource
* <sys:inUseFromDate> (Datatype property) Range: xsd:date. Definition: date on which a system was put into operation
* <sys:inUseUntilDate> (Datatype property) Range: xsd:date. Definition: date on which the it-system was phased out and no longer in operation
* <sys:operationelStatus>  (Object Property) Range: OperationalStatus
* <rdfs:comment> (Datatype property) Range: rdf:langString. Definition: A description of the subject resource.
* <sys:containsData> (Datatype property) Range: xsd:boolean. Definition: specification of whether an IT system contains data or documents digitally created by the public administration
* <archv:containsDigitalDocs> (Datatype property) Range: xsd:boolean. Definition: 


Properties (Tasks Perspective):
* <sys:hasApplicationPurposeFORM>  (Object Property) Range: FORMtask
* <sys:hasApplicationPurposeKLE>  (Object Property) Range: KLETheme
* <cv:hasLegalResource>  (Object Property) Range: eli:LegalResource
* <archv:caseArea>  (Object Property) Range: CaseArea
* <sys:predecessorSystem>  (Object Property) Range: sys:ITSystem
* <sys:hasCriticality>  (Object Property) Range: CriticalityType
* <sys:hasTargetGroup>  (Object Property) Range: TargetGroup

Properties (Governance Perspective):
* <sys:hasITSystemOwner>  (Object Property) Range: org:Organization/org:OrganizationalUnit/foaf:Person
* <sys:hasITSystemManager>  (Object Property) Range: org:Organization/org:OrganizationalUnit/foaf:Person

Properties (Legal Perspective):
* <sys:relatedContract>  (Object Property) Range: fibo-fnd-agr-ctr:Contract
* <dct:rightsHolder>  (Object Property) Range: org:Organization
* <schema:creator>  (Object Property) Range: org:Organization
* <sys:operatedBy>  (Object Property) Range: org:Organization
* <sys:maintainedBy>  (Object Property) Range: org:Organization

Properties (Application Perspective):
* <comp:instanceOfProductInSeries>  (Object Property) Range: comp:ProductSeries
* <sys:hasSystemDocumentation>  (Object Property) Range: sys:SystemDocumentation
* <sys:hasComponent>  (Object Property) Range: sys:ITSystem
* <sys:uses>  (Object Property) Range: schema:SoftwareApplication

Properties (Infrastructure Perspective):
* <sys:hasAquisitionType>  (Object Property) Range: ITSystemAquisitionType
* <sys:actsAs>  (Object Property) Range: EnvironmentType

Properties (Information Perspective):
* <sys:uses>  (Object Property) Range: dcat:Dataset
* <sys:provides>  (Object Property) Range: dcat:Dataset
* <sys:producesDataset>  (Object Property) Range: dcat:Dataset
* <archv:prevArchiveInformationPackage>  (Object Property) Range: dcat:Dataset
* <sys:provides>  (Object Property) Range: dcat:DataService
* <sys:uses>  (Object Property) Range: dcat:DataService
* <sys:provides>  (Object Property) Range: sys:UserInterface

Properties
* <sys:provisionDependency>  (Object Property) Range: sys:ComponentUsage
* <sys:hasFunctionalityCapability>  (Object Property) Range: Capability
* <sys:hasVersion>  (Object Property) Range: ITSystemVersion
* <sys:usageDependency>  (Object Property) Range: sys:ComponentUsage
* <sys:usedInOrganization>  (Object Property) Range: org:Organization
* <sys:contractRegarding>  (Object Property) Range: sys:ITSystem
* <sys:roleObject>  (Object Property) Range: sys:ITSystem
* <sys:selectedITsystemForReport>  (Object Property) Range: sys:ITSystem
 

# dcat:Dataset (Class)
Definition: 
A collection of data, published or curated by a single agent, and available for access or download in one or more formats

Properties (Information Perspective)::
* <dct:identifier> (Datatype property) Range: xsd:anyURI. Definition: An unambiguous reference to the resource within a given context.
* <dct:title> (Datatype property) Range: rdf:langString. Definition: A name given to the resource
* <dct:description> (Datatype property) Range: rdf:langString. Definition: An account of the resource
* <owl:versionInfo> (Datatype property) Range: rdfs:Literal. Definition: The annotation property that provides version information for an ontology or another OWL construct
* <dct:temporal>  (Object Property) Range: dct:PeriodOfTime

Properties (Governance Perspective)::
* <dct:creator>  (Object Property) Range: org:Organization
* <dcat-dk:dataResponsibleOrganisation>  (Object Property) Range: org:Organization
* <dcat-dk:dataProcessor>  (Object Property) Range: org:Organization
* <dcat-dk:personalDataCategory>  (Object Property) Range: PersonalDataCategory
* <dcat-dk:confidentialityType>  (Object Property) Range: ConfidentialityType
* <dcat-dk:hasConfidentialityType>  (Object Property) Range: ConfidentialityTypeNatoEu
* <dcat-dk:hasConfidentialityType>  (Object Property) Range: ConfidentialityTypeISO27002
* <archv:archivalRegisterType>  (Object Property) Range: RegisterType
* <archv:archivalObligationType>  (Object Property) Range: ArchivalObligationType
* <archv:plannedArchivalFrequency>  (Object Property) Range: ArchivalFrequencyType
* <archv:nextDataErasureDeadline> (Datatype property) Range: xsd:date. Definition: 
* <archv:prevArchiveInformationPackage>  (Object Property) Range: archv:ArchiveInformationPackage
* <archv:plannedArchiveType>  (Object Property) Range: ArchiveType
* <archv:lastArchivePeriod>  (Object Property) Range: dct:PeriodOfTime
* <prov:wasGeneratedBy>  (Object Property) Range: archv:DataConversion

# comp:ProductSeries (Class)
Definition: a series of related products that exhibit the same overall functionality to the user
Properties:
* <schema:identifier> (Datatype property) Range: xsd:anyURI. 
* <skos:prefLabel> (Datatype property) Range: rdf:langString. 
* <dct:description> (Datatype property) Range: rdf:langString.
* <sys:hasCapabilityForPurpose>  (Object Property) Range: PublicAdministrativeTaskType
* <archv:personalDataCategory>  (Object Property) Range: PersonalDataCategory
* <sys:usesPrimaryTechnologyStack>  (Object Property) Range: TechnologyStack
 
