This specification uses the abbreviation PAO for Post-Acute Orders.

Rendering provider in this specification means the individual or organization that is responsible for providing the services, devices, and/or medications specified in the order.

# Content and Organization of this Implementation Guide
The implementation guide is organized into the following sections:
* 	**Home** this page – describes the overall organization of the Implementation Guide.
* 	**[Background](http://build.fhir.org/ig/HL7/dme-orders/background.html)** describes current environment and the intent of the implementation guide.  It also covers items that are: 1) in scope, 2) out of scope, 3) business requirements, and 4) clinical requirements.
* 	**[Workflow](http://build.fhir.org/ig/HL7/dme-orders/workflow.html)** defines the overall exchange of information between the ordering provider and the rendering provider.  Flows are defined both with and without an intermediary.
* 	*[*Submission of Orders](http://build.fhir.org/ig/HL7/dme-orders/submission_of_orders.html)** defines the order submission process using messaging.
* 	**[Message Bundles](http://build.fhir.org/ig/HL7/dme-orders/message_bundles.html)** defines the content of the message bundles defined in this implementation guide.
* 	**[Technical Background](http://build.fhir.org/ig/HL7/dme-orders/technical_background.html)** describes the different specifications this implementation guide relies on and indicates what developers should read and understand prior to implementing this specification.
* 	**[FHIR Artifacts Overview](http://build.fhir.org/ig/HL7/dme-orders/fhir_artifacts_overview.html)** covers the type of FHIR artifacts that are included in this implementation guide.
* 	**[Must Support and Missing Data](http://build.fhir.org/ig/HL7/dme-orders/must_support_and_missing_data.html)** describes the required treatment of elements with a Must Support flag and how to handle Missing Data .
* 	**[Artifact Summary](http://build.fhir.org/ig/HL7/dme-orders/artifacts.html)** The Artifacts section introduce and provides links to the FHIR R4 profiles, extensions, code systems, value sets, and other FHIR artifacts used in this implementation guide.

# Dependencies
This implementation guide relies on the following other specifications:
* 	**[FHIR R 4.0.1](http://hl7.org/fhir/)** - The current official version of FHIR as of the time this implementation guide was published. See the background page for key pieces of this specification implementers should be familiar with.
* 	**[US Core STU 3.1.0](http://build.fhir.org/ig/HL7/US-Core-R4/)** - The current official version of US Core based on [FHIR R4](http://hl7.org/fhir//). 


[Next Page - Background](background.html)