[Previous Page - Technical Background](technical_background.html)

# Artifact Lists

Complying with this implementation guide means complying with a number of profiles, extensions, code systems, value sets and custom search parameters. This page provides an overview of where the relevant information can be found.

The FHIR artifacts used by Post-acute Orders are organized, in this section, based on the origin of the content (e.g. part of the US Core implementation guide or specific to this implementation guide).

**Post-acute Order specific Artifacts that do not have [US Core R4](http://build.fhir.org/ig/HL7/US-Core-R4/) profiles**

* [Bundle](http://build.fhir.org/ig/HL7/dme-orders/StructureDefinition-PAOX-bundle.html)
* [MessageHeader](http://build.fhir.org/ig/HL7/dme-orders/StructureDefinition-PAOX-messageheader.html)
* [Task](http://build.fhir.org/ig/HL7/dme-orders/StructureDefinition-PAOX-task.html)
* [Subscription](http://build.fhir.org/ig/HL7/dme-orders/StructureDefinition-PAOX-subscription.html)
* [DeviceRequest](http://build.fhir.org/ig/HL7/dme-orders/StructureDefinition-PAOX-devicerequest.html)
* [ServiceRequest](http://build.fhir.org/ig/HL7/dme-orders/StructureDefinition-PAOX-servicerequest.html)
* [Coverage](http://build.fhir.org/ig/HL7/dme-orders/StructureDefinition-PAOX-coverage.html)

**Post-Acure Order specific Artifacts based on [US Core V3.1.0](http://) profiles**

* [MedicationRequest](http://build.fhir.org/ig/HL7/dme-orders/StructureDefinition-PAOX-medicationrequest.html)
* [Medication](http://build.fhir.org/ig/HL7/dme-orders/StructureDefinition-PAOX-Medication.html)
* [Provenance](http://build.fhir.org/ig/HL7/dme-orders/StructureDefinition-PAOX-provenance.html)

**[US Core V3.1.0](http://build.fhir.org/ig/HL7/US-Core-R4) profiles referenced by the above resources**

* [Patient](http://build.fhir.org/ig/HL7/US-Core-R4/StructureDefinition-us-core-patient.html)
* [Practitioner](http://build.fhir.org/ig/HL7/US-Core-R4/StructureDefinition-us-core-practitioner.html)
* [PractitionerRole](http://build.fhir.org/ig/HL7/US-Core-R4/StructureDefinition-us-core-practitionerrole.html)
* [Organization](http://build.fhir.org/ig/HL7/US-Core-R4/StructureDefinition-us-core-organization.html)
* [Location](http://build.fhir.org/ig/HL7/US-Core-R4/StructureDefinition-us-core-location.html)

Additional information about the use of these artifacts can be found in the relevant specification.

**The artifacts are of four types**:

* 	**[Profiles](http://www.hl7.org/fhir/profiling.html)** that constrain FHIR resources to reflect PAO requirements.
* 	**[Extensions](http://www.hl7.org/fhir/extensibility.html)** that define additional data elements that can be conveyed as part of a resource.
* 	**[Code Systems](http://www.hl7.org/fhir/terminologies-systems.html)** that define PAO-specific terminologies to be used in one or more of the profiles.
* 	**[Value Sets](http://www.hl7.org/fhir/terminologies-valuesets.html)** that define the specific subsets of both PAO-defined and other code systems that can be (or are recommended to be) used within one or more profile elements.
* 	**[Operations](http:///www.hl7.org/fhir/operations.html)** that define the PAO-specific constraints on the [$processMessage](http://www.hl7.org/fhir/operation-messageheader-process-message.html) operation


[Next Page - Must Support and Missing Data](must_support_and_missing_data.html)