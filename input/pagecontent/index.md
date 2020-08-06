This specification uses the abbreviation PAO for Post-Acute Orders.

Rendering provider in this specification means the individual or organization that is responsible for providing the services, devices, and/or medications specified in the order.

# Content and Organization of this Implementation Guide
The implementation guide is organized into the following sections:
* 	**Index** this page – describes the overall organization of the Implementation Guide.
* 	**[Background](http://build.fhir.org/ig/HL7/dme-orders/background.html)** describes current environment and the intent of the implementation guide.  It also covers items that are: 1) in scope, 2) out of scope, 3) business requirements, and 4) clinical requirements.
* 	**[Security and Privacy](http://build.fhir.org/ig/HL7/dme-orders/security_and_privacy.html)**  – describes the security and privacy guidelines for use of this implementation guide.
* 	**[RESTful FHIR exchanges](http://build.fhir.org/ig/HL7/dme-orders/restful_fhir_exchanges.html)**  – describes the RESTful method of exchanging orders, updates and status.
* 	**[FHIR Messaging exchanges](http://build.fhir.org/ig/HL7/dme-orders/fhir_messaging_exchanges.html)**  – describes the use of FHIR messaging to exchanging orders, updates and status.
* 	**[Mixed Intermediary exchanges](http://build.fhir.org/ig/HL7/dme-orders/mixed_intermediary_exchange_model.html)**  – describes the use of both RESTful FHIR and FHIR messaging exchanges with an Intermediary.
* 	**[Technical Background](http://build.fhir.org/ig/HL7/dme-orders/technical_background.html)** describes the different specifications this implementation guide relies on and indicates what developers should read and understand prior to implementing this specification.
* 	**[FHIR Artifacts Overview](http://build.fhir.org/ig/HL7/dme-orders/fhir_artifacts_overview.html)** covers the type of FHIR artifacts that are included in this implementation guide.
* 	**[Must Support and Missing Data](http://build.fhir.org/ig/HL7/dme-orders/must_support_and_missing_data.html)** describes the required treatment of elements with a Must Support flag and how to handle Missing Data .
* 	**[Artifact Summary](http://build.fhir.org/ig/HL7/dme-orders/artifacts.html)** The Artifacts section introduce and provides links to the FHIR R4 profiles, extensions, code systems, value sets, and other FHIR artifacts used in this implementation guide.

# Dependencies
This implementation guide relies on the following other specifications:
* 	**[FHIR R 4.0.1](http://hl7.org/fhir/)** - The current official version of FHIR as of the time this implementation guide was published. See the background page for key pieces of this specification implementers should be familiar with.
* 	**[US Core STU 3.1.0](http://build.fhir.org/ig/HL7/US-Core-R4/)** - The current official version of US Core based on [FHIR R4](http://hl7.org/fhir//). 

# Credits
This work was sponsored by the Centers for Medicare and Medicaid Services (CMS) as part of a contract with ScopeInfotech to support the EMDI Project.
This IG was developed under the auspices of the [Orders and Observations](http://www.hl7.org/Special/committees/orders/leadership.cfm) work group. Current work group co-chairs are:

* 	**Hans Juitendijk** – Cerner Corportation
* 	**Ulrike Merrick** – Vernetzt, LLC
* 	**Lorraine Constable** – HL7 Canada
* 	**Raf Herzog** – Roche Diagnostics
* 	**John David Nolal, MD** – Children’s Mercy Hospitals and Clinics
* 	**David Burgess** – Laboratory Corporation of Americal
* 	**Robert Hausam, MD** – Hausem Consulting, LLC
	
The EMDI Project coordination is managed by:

* 	**Pallavi Talekar** – ScopeInfotech
* 	**Nandini Ganguly** – ScopeInfoTech
* 	**Briana Barnes** – ScopeInfotech
* 	**Ray Wilkerson** – ScopeInfotech

Development of this IG was performed by **Robert Dieterle** – EnableCare, LLC

Special thanks go to the numerous EMDI members who have participated on conference calls and reviews over the last two years and those who participated in the previous ballot of this IG, as well as those who are participating in this one!

If you are interested in participating in the Post-Acute orders project: information about our calls, minutes of past discussions, and other information can be found here on our HL7 Confluence page.


[Next Page - Background](background.html)