# IT-System-AP

This page provides a draft for a Danish public-sector specification for describing IT systems. 

Information about public-sector IT systems is exchanged in many different contexts and for many different purposes, and this provides interest and motivation for standardizing the way IT systems are described in order to support higher reuse and quality of data about IT systems.


## Class: sys:ITSystemReport 
Definition: report containing information about a number of it-systems to be sent to a specific recipient with a specific purpose
Properties:
* <dct:dateSubmitted> (Datatype property) Range: xsd:date. Definition: Date of submission of the resource
* <sys:selectedITsystemForReport>  (Object Property) Range: sys:ITSystem
* <frbr:responsibleEntity>  (Object Property) Range: org:Organization
 
