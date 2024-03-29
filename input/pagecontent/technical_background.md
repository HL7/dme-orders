# Systems
The PAO implementation guide defines the responsibilities of the three types of systems involved in a Post-Acute Orders solution:
* **Ordering Provider Systems:**  Systems that manage data on behalf of an Ordering Provider, who is a source for data to be transferred.
* **Rendering Provider Systems:**  Systems that manage data on behalf of a Rendering Provider, who is the intended recipient of transferred data.
* **Intermediary Systems:** Systems that communicate with both the Ordering Provider Systems and the Rendering Provider Systems. Intermediary Systems may provide appropriate Rendering Provider selection (e.g. based patient and or payer criteria), translation services, and order detail routing/integration.

# Underlying technologies
This guide is based on the [HL7 FHIR](http://www.hl7.org/implement/standards/product_brief.cfm?product_id=491) standard. Implementers of this specification therefore need to understand some basic information about these specifications.

**FHIR**

This implementation guide uses terminology, notations and design principles that are specific to FHIR. Before reading this implementation guide, it’s important to be familiar with some of the basic principles of FHIR as well as general guidance on how to read FHIR specifications. Readers who are unfamiliar with FHIR are encouraged to read (or at least skim) the following prior to reading the rest of this implementation guide:

* 	[FHIR overview](http://www.hl7.org/fhir/overview.html)
* 	[Developers introduction (or Clinical introduction)](http://www.hl7.org/fhir/overview-dev.html)
* 	[FHIR data types](http://www.hl7.org/fhir/datatypes.html)
* 	[Using codes](http://www.hl7.org/fhir/codesystem.html)
* 	[References between resources](http://www.hl7.org/fhir/references.html)
* 	How to read [resource](http://www.hl7.org/fhir/resourcelist.html) & [profile](http://www.hl7.org/fhir/profiling.html) definitions
* 	[Base resource](http://www.hl7.org/fhir/STU3/resource.html)

This implementation guide supports the [R4 version](http://hl7.org/fhir/) of the FHIR standard. R4 is recently published and the goal is to ensure thant this implementation guide aligns with the current direction of the FHIR standard.
Because this implementation guide focuses on workflow issues between an Ordering Provider and the Rendering Provider, implementers should also familiarize themselves with the FHIR resources and operations listed on the [FHIR Artifacts Overview](http://build.fhir.org/ig/HL7/dme-orders/fhir_artifacts_overview.html) page.