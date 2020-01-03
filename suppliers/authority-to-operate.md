---
expires: 2021-01-01
---
# Authority To Operate

## Purpose

All services or products supplied to or used by the Ministry of Justice must meet minimum security standards. Determining what standards apply, and whether they have been met, is carried out by an Assurance process.

Sometimes, it might be necessary to allow use of a service or product on a temporary (limited term) basis, until the Assurance process completes.
An example is where an existing Assurance has expired, and must be renewed.
Exceptionally, and rarely, it might be desirable for a new service or product where the initial Assurance process has not yet completed.

An "Authority to Operate" document (ATO) is not statement of Security Assurance.
It is a "statement of risk" for the service or product.
It provides a complete list of the high-level issues and risks that apply to the service or product.
These issues and risks prevent the Security Assurance process completing.
In order to allow the service or product to operate for an agreed, limited period of time, Information Asset Owner (IAO) acceptance of the issues and risks (known and unknown) is required.
An ATO provides a complete list of the actions that must be addressed.
It also provides the caveats, conditions or constraints on the use of the service or product that apply for the agreed, limited period of time during which the service or product may be used.

## Renewing an existing ATO

If an assurance process has not completed, or is not considered cost-effective owing to an expected 'sunsetting' of a service or product within the near future, it might be desirable to renew an existing ATO.

In such a case, a 'lightweight' ATO process applies:

- ensure that nothing [material has changed](#material-changes) involving the service or product, since the current ATO was issued. If there *has* been a material change, an ATO *cannot* be renewed.
- schedule and perform Penetration Tests and IT Health Checks (ITHCs) to take place as soon as possible, in order to validate the list of issues and risks in the current ATO
- 'cap' the duration of the renewed ATO at 50% of previous ATO - this is intentional, to make a formal Assurance process increasingly desirable. For example, a current ATO granted for 6 months would be renewed for a maximum of 3 months only.

### Material changes

A material or 'substantial' change to a service or product would include (but not be limited to) aspects such as:

- a change to the host operating system for the service or product
- a change to the functionality of the service or product, typically indicated by a change to the Version or Release identifier
- a change to resources used by the service or product, for example changing the database used by the service or product to store working information
- a migration from one container environment to another, for example from Microsoft Azure to Amazon AWS
- a change such that the service or product, or associated data, is relocated to or passes through a non-UK or non-EU environment
- a change to the licensing terms, support contract, or ownership of the service or product

The following would not normally be considered material or substantial changes to a service or product:

- a change to the hosting hardware or virtual machine
- modifications to capacity or performance of the service or product
- 'bug' fixes or patches

## Template

An ATO will normally contain the following sections.

### Statement scope

This describes:

- the service or product to which the ATO applies, in precise terms
- changes to the service or product which mean that the original Assurance is no longer valid
- the tests and evaluations performed, such as Penetration Tests or ITHCs, which resulted in the list of issues and risks that apply to the service or product

### Issues and risks

This provides a full list of the issues and risks, including:

- a unique issue or risk identifier, to facilitate unambiguous referencing
- a description of the issue or risk
- details of expected or required remediation actions to address the issue or risk
- the assessed risk level, described as an Impact indicator and a Likelihood indicator
- recommendations, providing additional information or guidance relevant to the issue or risk

### Resolved issues and risks

This provides a full list of the issues and risks that have been resolved.

### Conditions for continued operations

This provides a list of any caveats, conditions or constraints that apply to the use of the service or product.

Examples might include a requirement to repeat penetration tests or ITHCs at monthly intervals, or to have more frequent and faster escalating threat monitoring and incident reporting.

### Explicit statements of applicability

Include the following text:

    Acceptance of these risks and issues is necessary to allow the unassured
    system, service or product to continue operating until the risks and
    issues are remediated or safely decommissioned.

    The caveats, conditions and constraints apply to the system, service or
    product until the risks and issues are remediated or safely
    decommissioned.

    All the risks and issues should be managed at the Information Asset
    Owner (IAO) level, according to the assessed risk level.

### Formal Authority to Operate Authorisation

Start of Authority to Operate: \<START DATE><br/>
Expiry/Review of Authority to Operate: \<END DATE>

Assurer Name: \<ASSURER NAME><br/>
Assurer Signature or Email confirmation: \<ASSURER SIGNATURE><br/>
Date: \<DATE>

Information Asset Owner (IAO) Name: \<IAO NAME><br/>
IAO Signature or Email confirmation: \<IAO SIGNATURE><br/>
Date: \<DATE>
