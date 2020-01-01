---
title: Message Bundles
layout: default
active: Message Bundles
---

[Previous Page](Submission.html)

### The Post-Acute Order Message Bundle

<p>For every PAO, the object that is exchanged is a <a href="http://hl7.org/fhir/R4/bundle.html#message">FHIR message Bundle</a>. It consists of a Bundle identified by the type message, with the first resource in the bundle being a <a href="http://hl7.org/fhir/R4/messageheader.html">MessageHeader</a> resource. The MessageHeader resource has a code - the message event - that identifies the reason for the exchange (e.g. initial order, update, cancel)  The MessageHeader also carries additional PAO  metadata. The other resources in the bundle depend on the message event and the order scenario and form a network through their relationships with each other - either through a direct reference to another resource or through a chain of intermediate references.</p>

<p><strong>Each Bundle must have:</strong></p>

<ol>
  <li><em>MessageHeader</em></li>
  <li><em>List of other resources</em></li>
</ol>null