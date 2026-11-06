# Threat Model

## Purpose

A review is only relevant if its findings answer a real question: who could exploit this deployment, how, and what would they get? The threat model is the step that names those threats and ties each one to the control areas the review will test.

Without it, scope and severity rest on a generic checklist. With it, the reviewer can explain why one control area was tested in depth and another was left to an existing enterprise program.

## When it happens

The threat model is built during intake, from the deployment's data flow and trust boundaries, and confirmed with the accountable approver before evidence is requested. It sets review depth, so it comes before depth is agreed.

At intake the threat model records the control areas planned for each threat. Results are filled in after evidence validation.

The threat model is revalidated against the architecture actually deployed. When fieldwork finds a component, trust boundary, data flow or attack path that the intake diagrams did not show, the threat model is updated, and the change to review depth is agreed with the approver before the review continues.

## What it contains

One page. Each threat in scope is one row:

| Field | What it records |
|---|---|
| ID | A short reference (T-1, T-2) used in findings and coverage |
| Who | The threat actor or failure source: an employee, a compromised account, a vendor, an external attacker, an operator making mistakes |
| Objective or harmful outcome | What the actor is after, or the harm an accidental failure would cause |
| Way in | The entry point in this deployment: a user interface, a data source, a credential, an integration, an administrative path |
| Control areas | At intake, the gap categories planned for testing; after fieldwork, the ones actually tested |
| Result | Filled in after evidence validation: the findings or verified controls that answer the threat, each with its evidence class |

A starter table is in `../05-templates/threat-model-template.md`.

## Rules

1. **Derive threats from the deployment, not from a list.** Each threat must trace to a component, data flow or trust boundary in the review's own diagrams.
2. **Every threat in scope maps to control areas tested.** A threat with no tested control area is either out of scope or a gap in the review plan.
3. **Threats not tested are recorded, with the reason.** A threat left off the page is invisible to the approver; a threat recorded as untested is a decision they can see. Each untested threat, and each control it depends on, takes one of three statuses:
   - **Inherited, evidenced:** an existing enterprise program provides current assurance that applies to this deployment, and the assurance record is referenced.
   - **Inherited, unconfirmed:** an enterprise control is expected to apply, but its applicability or effectiveness for this deployment has not been established. This is not a verified control.
   - **Excluded:** the review will not assess it, and the approver sees the limitation.

   For each inherited item, the control test record names an owner and the assurance reference where one exists. That detail stays out of the one-page threat model.
4. **Keep scenarios with different attack paths apart.** A stolen password and a stolen session token, or a vendor's permitted use of data and a breach of the vendor, are separate threats because different controls answer them.
5. **Severity uses the threat model.** How easily a named threat could exploit a weakness is one of the severity adjustments in `severity-model.md`.
6. **Keep it to one page.** The threat model scopes the review. It is not a separate assessment.

## Methods

The threat model does not require a named method. Where a buyer's program uses one, such as STRIDE or MITRE ATLAS, the same table can carry that method's categories in an extra column.

## Framework reference

The threat model applies the NIST AI RMF Map function: establishing the deployment's context, the actors involved, and the ways it could cause harm before risks are measured and managed. See `framework-alignment.md` for the broader methodology-to-framework mapping.
