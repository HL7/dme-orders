[Previous Page - Technical Background](technical_background.html)

Complying with this implementation guide means complying with a number of profiles, extensions, value sets and custom search parameters. This page provides an overview of where this information can be found.
The FHIR artifacts used by Post-acute Orders are organized, in this section, according to whether the content developed as part of the US Core implementation guides or is specific to this implementation guide.

# Artifact Lists

Post-acute Order specific Artifacts (do not have US Core R4 profiles)
* [Bundle](http://hl7.org/fhir/us/dme-orders/StructureDefinition/PAOX-bundle)
* MessageHeader
* MessageDefinition
* Task
* Subscription
* DeviceRequest
* ServiceRequest
* Coverage

US Core (3.0.0 - R4 based) profiles
* MedicationRequest
* Medication
* Provenance

US Core (3.0.0 - R4 based) profiles referenced by the above resources
* Patient
* Practitioner
* PractitionerRole
* Organization
* Location

Additional information about the use of these artifacts can be found in the main specification.
The artifacts are of four types:
* 	**Profiles** (http://hl7.org/fhir/R4/profiling.html) constrain FHIR resources to reflect PAO requirements
* 	**Extensions** define additional data elements that can be conveyed as part of a resource
* 	**Code Systems** define PAO-specific terminologies to be used in one or more of those profiles
* 	**Value Sets** define the specific subsets of both PAO-defined and other code systems that can be (or are recommended to be) used within one or more profile elements
* 	**Operations** of which there is only one which defines the PAO-specific constraints on the $processMessage operation


[Next Page - Must Support and Missing Data](must_support_and_missing_data.html)