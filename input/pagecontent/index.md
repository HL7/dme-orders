This specification uses the abbreviation PAO for Post-Acute Orders.
Rendering provider in this specification means the individual or organization that is responsible for providing the services, devices, and/or medications specified in the order.
 This specification is currently undergoing connectathon testing. It is expected to evolve, possibly significantly, as part of that process. 
Feedback is welcome and may be submitted as a Jira ticket indicating PAO as the specification. 
This implementation guide is dependent on other specifications. Please submit any comments you have on these base specifications as follows: 
* 	Feedback on the FHIR core specification should be submitted as a Jira ticket with "FHIR Core" as the specification.
* 	Feedback on the US core profiles should be submitted as a Jira ticket with "US Core" as the specification.

# Content and Organization of this Implementation Guide
The implementation guide is organized into the following sections:
* 	**Home** this page – describes the overall organization of the Implementation Guide
* 	**Background** describes current environment and the intent of the implementation guide.  It also covers items that are: 1) in scope, 2) out of scope, 3) business requirements, and 4) clinical requirements
* 	**Workflow** defines the overall exchange of information between the ordering provider and the rendering provider.  Flows are defined both with and without an intermediary
* 	**Submission of Orders** defines the order submission process using messaging
* 	**Message Bundles** defines the content of the message bundles defined in this implementation guide.
* 	**Technical Background** describes the different specifications this implementation guide relies on and indicates what developers should read and understand prior to implementing this specification
* 	**FHIR Artifacts Overview** covers the type of FHIR artifacts that are included in this implementation guide
* 	**Must Support and Missing Data** describes the required treatment of elements with a Must Support flag and how to handle Missing Data 
* 	**Artifacts** The Artifacts section introduce and provides links to the FHIR R4 profiles, extension, code systems, value sets and other FHIR artifacts used in this implementation guide

# Dependencies
This implementation guide relies on the following other specifications:
* 	**FHIR R4** - The current official version of FHIR as of the time this implementation guide was published. See the background page for key pieces of this specification implementers should be familiar with.
* 	**US Core STU3** - The current official version of US Core based on FHIR R4.


[Next Page - Background](background.html)