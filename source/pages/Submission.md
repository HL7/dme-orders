---
title: Submission
layout: default
active: Submission
---

[Previous Page](MustSupport_and_Missing_Data.html)

Pushing Unsolicited Notifications to the Performing Provider, Suppler, or Intermediary
<p>As shown in Figure 4, When an event triggers a Post-Acute Order (PAO), the Sender creates a PAO Message Bundle and sends it to the recipients <code class="highlighter-rouge">$process-message</code> operation endpoint.</p>
 <ol>
 <li>For this guide there is an expectation that  for a PAO response message to be returned from the Recipient or Intermediary to the Sender. Therefore, the $process-message input parameters async and response-url are used.</li>
  <li>There is an expectation that the data submitted represents all the data required by the Recipient/Intermediary to establish an order.  There is not expectation that the data to support medical necessity is complete. The PAO Recipient/Intermediary can optionally fetch additional information from the patients medical record using FHIR RESTful searches or using the mechanisms defined in the CDex IG.  The endpoint for this search may be known or supplied via the <code class="highlighter-rouge">$process-message</code> operation payload.</li>
  <li>Not shown in figure 4, after the Intermediary successfully receives the PAO, processes it and redistributes the data the Service Provider(s) or DME(s) to fulfill the order. The Intermediary <strong>MAY</strong> use FHIR messaging and the <code class="highlighter-rouge">$process-message</code> operation to do this or some other messaging protocol such as Direct, SMS or V2 messaging.  If the intended organization is specified in the Message Header, the intermediary <strong>SHOULD</strong> route the PAO to the intended recipient. Note that the PAO Intermediary <strong>MAY</strong> customize the content based on the end user (for example, sending only the part of an order to a supplier the suppler can fulfill).</li>
</ol>

Usage
<p>The $process-message operation is invoked by the Sender using the POST  syntax:</p>
<p>POST [base]$process-message</code></p>
<p>The body of the operation is the PAO Message Bundle containing:</p>

<ol>
  <li>The <strong>MessageHeader</strong> which is the first resource in the bundle and contains the message event code - that identifies the nature of the order bundle (initial order, update, cancel).</li>
  <li>The <strong>MessageDefinition</strong>  which is the second resource in the bundle and contains the message content definition.
  <li>The <strong>Task</strong> which is the third resource in the bundle and defines the associated components of the order and its status.</li>
  <li>The <strong>Subscription</strong> which is the fourth resource in the bundle and contains the information necessary to receive a notification (or a completed updated Order Bundle) when the Task changes status.</li>
  <li>The <strong>ServiceRequest</strong> and/or a <strong>DeviceRequest</strong> which defines the components of the order. Note: all of the referenced resources in ServiceRequest or Device Request <strong>SHALL</strong> be included in the bundle.</li>
  <li>The <strong>Organization</strong> and <strong>Location</strong> for the intended Service Provider, DME Supplier or Intermediary.</li>

  <li>The other resources in the bundle depend on the nature of the required documentation needed to perfect the order and/or document medical necessity based on the service or device that is the basis for the order.</li>
</ol>
<p>An HTTP Status success code is returned on successful submission.</p>
	
<p>See the Home Oxygen scenario Example Transaction</a> for an example of using the <code class="highlighter-rouge">$process-message</code> operation to send a POA Message Bundle.</p>
</ol>
<h3 id="reliable-delivery">Reliable Delivery</h3>
<p>Upon receiving a message, the Receiver/Intermediary may return one of several status codes which is documented in <a href="http://hl7.org/fhir/R4/messageheader-operation-process-message.html"><code class="highlighter-rouge">$process-message</code></a> definition.</p>
note-to-balloters
  <p>We are actively seeking input on whether additional guidance should be documented in this guide on FHIR-related errors (in addition to normal HTTP errors related to security, header and content type negotiation issues). For example, whether to define a minimum set of error response code, such as those listed <a href="http://hl7.org/fhir/R4/http.html#rejecting-updates">here</a>. Additionally, what additional guidance to specify how the Sender can provide a more reliable delivery of notifications to the intended recipient(s).  For example, defining what actions the Sender must take when it receives a particular error response code.</p>

[Next Page](Message_Bundles.html)