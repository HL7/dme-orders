[Previous Page - Workflow](Workflow.html)

# Submission of Orders
Pushing Unsolicited Orders to the Performing Provider, Supplier, or Intermediary
1. When an event (e.g. creating an order that must be fulfilled by a third party) triggers a Post-Acute Order (PAO), the Sender creates a PAO Message Bundle and sends it to the recipients <code class="highlighter-rouge">$process-message</code> operation endpoint.
2. For this guide, there is an expectation that a PAO response message will be returned from the Recipient or Intermediary to the Sender. Therefore, the $process-message input parameters async and response-url are used.
3. There is an expectation that the data submitted represents all the data required by the Recipient/Intermediary to establish an order.  There is not an expectation that the data to support medical necessity is complete. The PAO Recipient/Intermediary can optionally fetch additional information from the patients medical record using FHIR RESTful searches or using the mechanisms defined in the CDex IG.
4. When there is an Intermediary, once the PAO bundle is successfully received and processed, the Intermediary will distribute the order to the target Service Provider(s) or DME(s) to fulfill the order. The Intermediary **MAY** use FHIR messaging and the <code class="highlighter-rouge">$process-message</code> operation to do this or some other messaging protocol such as Direct or SFTP.  If the intended organization is specified in the Message Header, the intermediary **SHOULD** route the PAO to the intended recipient. Note that the PAO Intermediary **MAY** customize the content based on the end user (for example, sending only the part of an order to a supplier based on their fulfillment capability).


Usage

The $process-message operation is invoked by the Sender using the POST  syntax:

POST [base]$process-message

The body of the operation is the PAO Message Bundle containing:


The **MessageHeader** which is the first resource in the bundle and contains the message event code - that identifies the nature of the order bundle (initial order, update, cancel).
The **MessageDefinition** which is the second resource in the bundle and contains the message content definition.
The **Task** which is the third resource in the bundle and defines the associated components of the order and its status.
The **Subscription** which is the fourth resource in the bundle and contains the information necessary to receive a notification (or a completed updated Order Bundle) when the Task changes status.
The **DeviceRequest**, **ServiceRequest** and/or a **MedicationRequest** defines the order.
The other resources in the bundle depend on the nature of the required documentation needed to perfect the order and/or document medical necessity based on the service or device that is the basis for the order.
Note: all referenced resources **SHALL** be included in the bundle.

We will create a Home Oxygen scenario Example Transaction as an example of using the <code class="highlighter-rouge">$process-message</code> operation to send/receive a POA Message Bundle.

[Next Page - Message Bundles](MessageBundles.html)