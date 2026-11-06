# Threat Model

## Purpose

A review is only relevant if its findings answer a real question: who could exploit this deployment, how, and what would they get? The threat model is the step that names those threats and ties each one to the control areas the review will test.

Without it, scope and severity rest on a generic checklist. With it, the reviewer can explain why one control area was tested in depth and another was left to an existing enterprise program.

## When it happens

The threat model is built during intake, from the deployment's data flow and trust boundaries, and confirmed with the accountable approver before evidence is requested. It sets review depth, so it comes before depth is agreed.

## What it contains

One page. Each threat in scope is one row:

| Field | What it records |
|---|---|
| ID | A short reference (T-1, T-2) used in findings and coverage |
| Who | The threat actor: an employee, a compromised account, a vendor, an external attacker, an operator making mistakes |
| What they want | The outcome that would harm the buyer |
| Way in | The entry point in this deployment: a user interface, a data source, a credential, an integration, an administrative path |
| Control areas tested | The gap categories the review tests against this threat |
| Result | The findings, or the controls verified, that answer the threat |

A starter table is in `../05-templates/threat-model-template.md`.

## Rules

1. **Derive threats from the deployment, not from a list.** Each threat must trace to a component, data flow or trust boundary in the review's own diagrams.
2. **Every threat in scope maps to control areas tested.** A threat with no tested control area is either out of scope or a gap in the review plan.
3. **Threats not tested are recorded, with the reason.** Mark them inherited (covered by another enterprise program the approver should confirm) or out of scope. A threat left off the page is invisible to the approver; a threat recorded as untested is a decision they can see.
4. **Severity uses the threat model.** How easily a named threat could exploit a weakness is one of the severity adjustments in `severity-model.md`.
5. **Keep it to one page.** The threat model scopes the review. It is not a separate assessment.

## Methods

The threat model does not require a named method. Where a buyer's program uses one, such as STRIDE or MITRE ATLAS, the same table can carry that method's categories in an extra column.

## Framework reference

The threat model applies the NIST AI RMF Map function: establishing the deployment's context, the actors involved, and the ways it could cause harm before risks are measured and managed. See `framework-alignment.md` for the broader methodology-to-framework mapping.
