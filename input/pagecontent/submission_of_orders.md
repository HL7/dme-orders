[Previous Page - Workflow](workflow.html)

# Submission of Orders
Pushing orders to the rendering provider or intermediary (acts as a Rendering Provider) 
Intermediary System and MAY act as both a Sending System and Receiving System if it follows the PAO IG when sending to a Rendering Provider System)
1. When an event (e.g. creating an order that must be fulfilled by a third party) triggers a Post-Acute Order (PAO), the Sender creates a PAO Message Bundle and sends it to the recipients <code class="highlighter-rouge">$process-message</code> operation endpoint.
2. For this guide, there is an expectation that a PAO response message will be returned from the Recipient or Intermediary to the Sender. Therefore, the $process-message input parameters async and response-url are used.
3. There is an expectation that the data submitted represents all the data required by the Recipient/Intermediary to establish an order.  There is no expectation that the information to support payer billing is complete. The PAO Recipient/Intermediary can optionally fetch additional information from the patient’s medical record using FHIR RESTful searches or using the mechanisms defined in the CDex IG http://build.fhir.org/ig/HL7/davinci-ecdx/index.html.
4. When there is an Intermediary, once the PAO bundle is successfully received and processed, the Intermediary will distribute the order to the target Rendering Provider(s) to fulfill the order. The Intermediary **MAY** use FHIR messaging and the <code class="highlighter-rouge">$process-message</code> operation to do this or some other messaging protocol such as Direct or Secure File Transport Protocol (SFTP).  If the intended organization is specified in the Message Header, the intermediary **SHOULD** route the PAO to the intended recipient. When the order is not routed to the intended organization, the intermediary **SHOULD** inform the ordering provider. Note that the PAO Intermediary **MAY** customize the content based on: 
1) contractual requirements (e.g. coverage by a payer),
2) fulfillment capability (e.g. what is carried or in stock), and/or
3) patient preference (e.g. selecting a specific supplier or cost of service).

Usage

The $process-message operation is invoked by the Sender using the POST  syntax:

POST [base]$process-message

The body of the operation is the PAO Message Bundle containing:


The **MessageHeader** which is the first resource in the bundle and contains the message event code - that identifies the nature of the order bundle (initial order, update, cancel).
Additional resources (which may be in any order after the MessageHeader) include:
**Task** which defines the associated components of the order and its status. (Note: if task.focus is populated, it should point to the same request resources as task.basedOn
**Subscription** which contains the information necessary to receive a notification (or a completed updated Order Bundle) when the Task changes status.
**DeviceRequest**, **ServiceRequest** and/or a **MedicationRequest** which define the order.
The other resources in the bundle depend on the specific services requested and the nature of the documentation needed to perfect the order (e.g. may describe specific factors that will tailor the requested services to the specific patient need) and/or to meet payer documentation requirements for coverage/billing.
Note: All referenced resources **SHALL** be included in the bundle.

[Next Page - Message Bundles](message_bundles.html)