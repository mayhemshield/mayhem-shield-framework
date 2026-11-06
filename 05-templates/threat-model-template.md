# Threat Model Template

Public-safe starter for the one-page threat model described in `../00-core-framework/threat-model.md`. Replace the example rows with threats derived from the deployment's own data flow and trust boundaries.

## Threats in scope

| ID | Who | What they want | Way in | Control areas tested | Result |
|---|---|---|---|---|---|
| T-1 | Signed-in user acting outside their role | Data they are not entitled to see | Normal use of the AI feature | Identity and Access; Retrieval / Knowledge Security | |
| T-2 | Anyone who can edit a source the AI reads | To change what the AI tells other users | Editable content in an indexed source | Retrieval / Knowledge Security; Output Validation | |
| T-3 | Holder of a leaked integration credential | Broad access to connected systems | Service account or API key | Integration / Connector Security; Identity and Access | |
| T-4 | The AI vendor, or an attacker who breaches it | Prompts, outputs or stored data | Vendor API or hosted workspace | Vendor Assurance; Data Protection Outbound | |
| T-5 | Operator making unreviewed changes | Changed behavior with no record | Configuration or prompt settings | SDLC / Change Control; Monitoring / Audit / Response | |

## Threats not tested

| ID | Who | Why not tested | What the approver should rely on |
|---|---|---|---|
| T-6 | | Inherited / Out of scope | |

## Notes

- Confirmed with: (approver role), on (date).
- Method used, if any: (none, STRIDE, MITRE ATLAS, other).
