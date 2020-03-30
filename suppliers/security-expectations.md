---
expires: 2020-01-01
---
# Security Controls for `OFFICIAL`

The baseline requirements for IT services that support or process `OFFICIAL` information can be found [here](https://www.gov.uk/guidance/official-sensitive-data-and-it).

This document provides supplementary detail and clarification about MoJ requirements and expectations for handling MoJ information.

## Suppliers

All suppliers *must* have [ISO27001](https://www.iso.org/isoiec-27001-information-security.html) and [CyberEssentials Plus](https://www.cyberessentials.ncsc.gov.uk/), at a minimum.

It is *highly recommended* that suppliers have [NCSC Commercial Product Assurance (CPA)](https://www.ncsc.gov.uk/information/commercial-product-assurance-cpa) for their products or services.

## Procedures

All suppliers *must* have procedures addressing the following aspects.

The procedures *must* be in place and followed at all times.

### User Management

A full, documented Joiner/Mover/Leaver (JML) procedure *must* be place for all staff utilised by the Supplier in providing a service to the MoJ. This includes contractors or other temporary staff.

System administrators for each Supplier *must* be able to manage their own users. It *must* be easy for administrators to remove user access, *and* to expire user accounts forcibly after a certain period of time. All accounts *must* expire automatically after an agreed period of time. There *must* be a means for administrators to:

- validate new user requests to make sure they are approved
- obtain a list of users who have moved on
- apply a list of moved on users to perform a bulk removal of access permissions
- obtain a list of users who are about to auto-expire

### Separation of duties

It *must not* be possible for any user to carry out an export of a full copy of data without approval from another party.

### Personnel

All Supplier staff and contractors with access to MoJ information *must* have a minimum of [Government Baseline Personnel Security Standard (BPSS)](https://www.gov.uk/government/publications/government-baseline-personnel-security-standard) clearance.

Privileged user actions *must* be carried out *only* from accounts specifically designed for this purpose. Privileged user accounts *must* be separate from any accounts users have for non-privileged actions.

The risk of unauthorised users gaining administrator access *must* be minimised.

## Technical

The following basic technical requirements are considered mandatory, unless otherwise discussed, agreed and documented:

- ensure unique per-user accounts
- enforce [Multi-factor authentication (MFA)](https://en.wikipedia.org/wiki/Multi-factor_authentication) access controls
- restrict the permitted rate of login attempts
- restrict access to HTTPS only, if web based access is available
- apply the principle of least privilege for all data access. This means restrict by data content, and restrict to read-only rather than read-write wherever possible and appropriate
- users working with data *must not* be able to see the data of other users or organisations, other than as part of their role or remit
- data *must* be encrypted at rest and in transit
- All actions on data, such as viewing, editing and deleting, must be logged and audited at the individual user level
- penetration tests and IT Health Checks *must* be performed *and* satisfactorily passed *before* a service goes live. The tests and checks *must* also be run again, *and* satisfactorily passed:
   - at intervals of not more than 12 calendar months since the last successful tests
   - before any major change to infrastructure goes live, including but not limited to modifications to functional capability, implementation, or hosting
- any issues identified during Penetration tests or IT Health Check as a result of service changes *must* be mitigated or accepted before the service changes go live
- user submitted data *must* be validated to prevent web threats such as injection attacks and cross site scripting
- an 'idle' timeout *must* be enforced, to detect and close inactive sessions
- 'Best of breed' mechanisms *must* be in place at all times to detect malicious attacks on the Service
- logs and other auditable material *must* be stored remotely to ensure forensic diagnosis capability following incident
- service provision *must* be resilient to denial of service attacks, and scalable to spikes in usage
- live/production/real data *must not* be stored, processed, or transmitted on or through development or test environments
- infrastructure *must* be patched and hardened without delay
- networks *must* be segmented as appropriate to ensure maximum possible Confidentiality, Integrity, and Availability
- cached or 'past expiry' data *must* be purged as soon as possible, unless subject to a Retention Order
