This specification is designed as a foundational IG for the exchange of FHIR Orders outside of the acute care setting. It provides specific methods for the exchange of orders and their accompanying documenation between the ordering and renering provider.  It also defines workflow that accomodates the role of an intermediary that may perfect the order and decide, based on a number of factors (e.g., insurance coverage, availability, capability, preferences) the appropriate rendering provider to excute the order.

The actors in this specification include:
* 1) Ordering Provider -- creates the order for a service, device, medication, referral
* 2) Rendering Provider -- performs the service, provides the item(s) or medications indicated in the order, and the
* 3) Intermediary -- responsible for directing the FHIR orders between the Ordering and Rendering providers.

To accomodate both synchronous workflows and asynchronous workflows, this implemenation guide supports RESTful exchanges based on the exchange of the FHIR Task resource and exchanges based on FHIR messaging.  These exchange methods can be used in any combination between the actors.


# Content and Organization of this Implementation Guide
The implementation guide is organized into the following sections:
* 	[Index ](http://build.fhir.org/ig/HL7/dme-orders/index.html)describes the overall organization of the implementation guide.
* 	[Background](http://build.fhir.org/ig/HL7/dme-orders/background.html) describes current environment and the intent of the implementation guide.  It also covers items that are: 1) in scope, 2) out of scope, 3) business requirements, and 4) clinical requirements.
* 	[Security and Privacy](http://build.fhir.org/ig/HL7/dme-orders/security_and_privacy.html) describes the security and privacy guidelines for use of this implementation guide.
* 	[RESTful FHIR exchanges](http://build.fhir.org/ig/HL7/dme-orders/restful_fhir_exchanges.html)  describes the RESTful method of exchanging orders, updates and status.
* 	[FHIR Messaging exchanges](http://build.fhir.org/ig/HL7/dme-orders/fhir_messaging_exchanges.html) describes the use of FHIR messaging to exchanging orders, updates and status.
* 	[Mixed Intermediary exchanges](http://build.fhir.org/ig/HL7/dme-orders/mixed_intermediary_exchange_model.html)  describes the use of both RESTful FHIR and FHIR messaging exchanges with an Intermediary.
* 	[Technical Background](http://build.fhir.org/ig/HL7/dme-orders/technical_background.html) describes the different specifications this implementation guide relies on and indicates what developers should read and understand prior to implementing this specification.
* 	[FHIR Artifacts Overview](http://build.fhir.org/ig/HL7/dme-orders/fhir_artifacts_overview.html) covers the type of FHIR artifacts that are included in this implementation guide.
* 	[Must Support and Missing Data](http://build.fhir.org/ig/HL7/dme-orders/must_support_and_missing_data.html) describes the required treatment of elements with a Must Support flag and how to handle Missing Data.
* 	[Artifact Summary](http://build.fhir.org/ig/HL7/dme-orders/artifacts.html) introduces and provides links to the FHIR R4 profiles, extensions, code systems, value sets, and other FHIR artifacts used in this implementation guide.

# Dependencies
This implementation guide relies on the following other specifications:
* 	[FHIR R 4.0.1](http://hl7.org/fhir/) - The current official version of FHIR as of the time this implementation guide was published. See the background page for key pieces of this specification implementers should be familiar with.
* 	[US Core STU 3.1.1](http://build.fhir.org/ig/HL7/US-Core-R4/) - The current official version of US Core based on [FHIR R4](http://hl7.org/fhir//). 

# Credits
This work was sponsored by the Centers for Medicare and Medicaid Services (CMS) as part of a contract with Scope Infotech Inc. to support the EMDI Project.
This IG was developed under the auspices of the [Orders and Observations](http://www.hl7.org/Special/committees/orders/leadership.cfm) work group. Current work group co-chairs are:

* 	**Hans Buitendijk** – Cerner Corportation
* 	**Ulrike Merrick** – Vernetzt, LLC
* 	**Lorraine Constable** – HL7 Canada
* 	**Raf Herzog** – Roche Diagnostics
* 	**John David Nolal, MD** – Children’s Mercy Hospitals and Clinics
* 	**David Burgess** – Laboratory Corporation of Americal
* 	**Robert Hausam, MD** – Hausem Consulting, LLC

The Electronic Medical Documentation Interoperability (EMDI) project coordination is managed by:

* 	**Pallavi Talekar** – Scope Infotech Inc.
* 	**Nandini Ganguly** – Scope InfoTech Inc.
* 	**Briana Barnes** – Scope Infotech Inc.
* 	**Kishan Patel** - Scope Infotech Inc.
* 	**Ray Wilkerson** – Scope Infotech INnc.

Development of this IG was performed by **Robert Dieterle** – EnableCare, LLC

Special thanks to the numerous EMDI participants who have contributed to conference calls, provided feedback over the last two years, and those who participated in the previous ballot of this IG, as well as those who are participating in this one!

In particular, ordering workflow diagrams were provided, in part, by:

* **Vassil Peytchev** - Epic 

If you are interested in participating in the Post-Acute orders project: information about our calls, minutes of past discussions, and other information can be found [here](https://confluence.hl7.org/pages/viewpage.action?pageId=44499186) on our HL7 Confluence page.

# Change log
* **0.2.2a* :**updates from 11/14/2021
* **0.2.2b* :**updates from 5/23/2022
* **0.2.2c* :**updates from 6/19/2023
* **0.2.2d* :**updates from 6/22/2023
* **0.2.2.e* :**updates from 6/25/2023 

End of home page