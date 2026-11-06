# Threat Model Template

Public-safe starter for the one-page threat model described in `../00-core-framework/threat-model.md`. Replace the example rows with threats derived from the deployment's own data flow and trust boundaries. At intake, fill in the planned control areas and leave Result blank. Fill in Result, with the evidence class for each item, after evidence validation. Update the table if fieldwork finds components or paths the intake diagrams did not show.

## Threats in scope

| ID | Who | Objective or harmful outcome | Way in | Control areas | Result (after fieldwork) |
|---|---|---|---|---|---|
| T-1 | Signed-in user acting outside their role | Data they are not entitled to see | Normal use of the AI feature | Identity and Access; Retrieval / Knowledge Security | |
| T-2 | Anyone who can edit a source the AI reads | To change what the AI tells other users | Editable content in an indexed source | Retrieval / Knowledge Security; Output Validation | |
| T-3 | Holder of a leaked integration credential | Broad access to connected systems | Service account or API key | Integration / Connector Security; Identity and Access | |
| T-4 | The AI vendor, using data as its terms permit | Prompts, outputs or stored data retained or used beyond what the buyer intended | Vendor API or hosted workspace | Vendor Assurance; Data Protection Outbound | |
| T-5 | Operator making unreviewed changes, by mistake or intent | Changed behavior with no record | Configuration or prompt settings | SDLC / Change Control; Monitoring / Audit / Response | |

## Threats not tested

| ID | Who | Status | Owner | Assurance reference |
|---|---|---|---|---|
| T-6 | An attacker who breaches the AI vendor | Inherited, evidenced / Inherited, unconfirmed / Excluded | | |

## Notes

- Confirmed with: (approver role), on (date).
- Method used, if any: (none, STRIDE, MITRE ATLAS, other).
