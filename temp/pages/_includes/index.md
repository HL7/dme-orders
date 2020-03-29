### Overview

# General
This is a FHIR R4 Implementation Guide to support the electronic exchange of post acute orders along with the exchange of supporting documentation between the ordering provider and the specific supplier.
* The initial version of the implementation guide (IG) will focus on orders and documentation for Durable Medical Equipment (DME) and Home Health Services.
* This specification is currently undergoing connectathon testing. It is expected to evolve, possibly significantly, as part of that process.

This implementation guide is the result of work sponsored by CMS's Center for Program Integrity, whose goal is to advance the ability for provider's to supply services that are medically necessary and appropriate to Medicare Beneficiaries. By enabling provider to communicate orders and supporting documentation in real-time to suppliers, beneficiaries can receive appropriate treatment more rapidly and reduce the burden on providers and suppliers to comply with documentation requirements.

# Feedback
Comments and suggestions are welcome on our Zulip stream...
or send a note to rdieterle@enablecare.us

# Change log
* **0.0.7b:** will update alpha with each subsequent test on 3-28-2020
* **0.0.7 (This version):** further updates that now include Code System, Value Set, US Core profile references in some PAO profiles
* **0.0.6:** Further changes to address publisher errors (not pushed to build)
* **0.0.5:** Update for tooling changes (not pushed to build)
* **0.0.4:** Cleanup versions, add known issues, and correct title 
* **0.0.3:** Working build on build.fhir.org
* **0.0.2:** Update to test build on build.fhir.org 
* **0.0.1:** Initial version published to the continuous build

# Known issues and to-dos
* Still working on complex extensions that will be part of a backbone element in the ServiceRequest and DeviceRequest
* Working with other members of the team to create appropriate examples
* Need to add full examples of message bundles
* Working on specific terminologies and value sets for post-acute orders



### Authors

<table>
<thead>
<tr>
<th>Name</th>
<th>Email</th>
</tr>
</thead>
<tbody>
<tr>
<td>HL7 International - Orders and Observations</td>
<td></td>
</tr>
</tbody>
</table>




[Next Page - Post-Acute Orders Home](Post-AcuteOrdersHome.html)