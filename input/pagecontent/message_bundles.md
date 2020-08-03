[Previous Page - Submission of Orders](submission_of_orders.html)

### The Post-Acute Order Message Bundle

<p>For every PAO, the object that is exchanged is a <a href="http://hl7.org/fhir/R4/bundle.html#message">FHIR message Bundle</a>. It consists of a Bundle identified by the type message, with the first resource in the bundle being a <a href="http://hl7.org/fhir/R4/messagehead### The Post-Acute Order Message Bundle

<p>For every PAO, the object that is exchanged is a <a href="http://hl7.org/fhir/R4/bundle.html#message">FHIR message Bundle</a>. It consists of a Bundle identified by the type message, with the first resource in the bundle being a <a href="http://hl7.org/fhir/R4/messageheader.html">MessageHeader</a> resource. The MessageHeader resource has a code - the message event - that identifies the reason for the exchange (e.g. initial order, update, and cancel).  The MessageHeader also carries additional PAO  metadata. The other resources in the bundle depend on the message event and the order scenario and form a network through their relationships with each other - either through a direct reference to another resource or through a chain of intermediate references.</p>

<p><strong>Each Bundle must have:</strong></p>

<ol>
  <li><em>MessageHeader/MessageDefinition</em></li>
  <li><em>Task</em></li>
  <li><em>Subscription</em></li>
  <li><em>DeviceRequest/ServiceRequest/MedicationRequest (Medication)</em></li>
	<li><em>Included Resources</em></li>
</ol>

<table><tr><td><img src="MessageBundleContentDrawing6.jpg" /></td></tr></table>
er.html">MessageHeader</a> resource. The MessageHeader resource has a code - the message event - that identifies the reason for the exchange (e.g. initial order, update, cancel)  The MessageHeader also carries additional PAO  metadata. The other resources in the bundle depend on the message event and the order scenario and form a network through their relationships with each other - either through a direct reference to another resource or through a chain of intermediate references.</p>

<p><strong>Each Bundle must have:</strong></p>

<ol>
  <li><em>MessageHeader/MessageDefinition</em></li>
  <li><em>Task</em></li>
  <li><em>Subscription</em></li>
  <li><em>DeviceRequest/ServiceRequest/MedicationRequest(Medication)</em></li>
	<li><em>Included Resouces</em></li>
</ol>

<table><tr><td><img src="MessageBundleContentDrawing6.jpg" /></td></tr></table>

[Next Page - Technical Background](technical_background.html)