# Gap Categories

Core domains:
1. Vendor Assurance
2. Identity and Access
3. Network and Path Control
4. Data Protection Outbound
5. Data Protection Inbound / Output Validation
6. Admin / Endpoint / Operator Security
7. Supply Chain and Dependency Integrity
8. SDLC / Change Control
9. Governance / Acceptable Use
10. Monitoring / Audit / Response

Overlay-driven domains:
11. AI Governance / Model Controls
12. Agentic / Workflow Execution
13. Retrieval / Knowledge Security
14. Self-Hosted Infrastructure Control
15. Regulated Data Control
16. Output Liability / Public-Facing Safety
17. Integration / Connector Security

## Cross-references to established frameworks

Findings within these gap categories are typically cross-referenced to established frameworks during scoping and severity calibration. The mappings below describe the most common alignments. They are not exhaustive and individual findings may map to multiple framework references.

### NIST CSF 2.0 functions

| CSF Function | Gap Categories most commonly mapped |
|---|---|
| Govern | 1 Vendor Assurance, 9 Governance / Acceptable Use, 11 AI Governance / Model Controls, 15 Regulated Data Control |
| Identify | 4 Data Protection Outbound, 7 Supply Chain and Dependency Integrity, 13 Retrieval / Knowledge Security, 17 Integration / Connector Security |
| Protect | 2 Identity and Access, 3 Network and Path Control, 5 Data Protection Inbound / Output Validation, 6 Admin / Endpoint / Operator Security, 14 Self-Hosted Infrastructure Control |
| Detect | 10 Monitoring / Audit / Response, 12 Agentic / Workflow Execution, 13 Retrieval / Knowledge Security |
| Respond | 10 Monitoring / Audit / Response, 12 Agentic / Workflow Execution, 16 Output Liability / Public-Facing Safety |
| Recover | 8 SDLC / Change Control, 14 Self-Hosted Infrastructure Control |

The Recover function is a limited fit for the methodology. Mayhem Shield's review work focuses on prevention and detection. Recovery activities (rollback, remediation, infrastructure restoration) are noted where applicable but are not the primary review concern.

### OWASP Top 10 for LLM Applications (2026 edition)

| OWASP LLM ID | Description | Gap Categories most commonly mapped |
|---|---|---|
| LLM01 | Prompt Injection | 5 Output Validation, 12 Agentic / Workflow Execution, 13 Retrieval / Knowledge Security |
| LLM02 | Sensitive Information Disclosure | 4 Data Protection Outbound, 13 Retrieval / Knowledge Security, 15 Regulated Data Control, 17 Integration / Connector Security |
| LLM03 | Excessive Agency | 2 Identity and Access, 12 Agentic / Workflow Execution, 17 Integration / Connector Security |
| LLM04 | Supply Chain | 1 Vendor Assurance, 7 Supply Chain and Dependency Integrity, 8 SDLC / Change Control |
| LLM09 | Vector and Embedding Weaknesses | 13 Retrieval / Knowledge Security, 2 Identity and Access |
| LLM10 | Improper Output Handling | 5 Output Validation, 12 Agentic / Workflow Execution, 16 Output Liability / Public-Facing Safety |

OWASP LLM IDs not listed (LLM05, LLM06, LLM07, LLM08) may apply per engagement based on deployment specifics. Earlier editions numbered these entries differently; findings state the edition they cite.

### OWASP Top 10 for Agentic Applications

| ASI ID | Description | Gap Categories most commonly mapped |
|---|---|---|
| ASI01 | Agent Goal Hijack | 12 Agentic / Workflow Execution, 5 Output Validation, 13 Retrieval / Knowledge Security |
| ASI02 | Tool Misuse | 12 Agentic / Workflow Execution, 17 Integration / Connector Security |
| ASI03 | Identity & Privilege Abuse | 2 Identity and Access, 12 Agentic / Workflow Execution, 17 Integration / Connector Security |
| ASI04 | Agentic Supply Chain Vulnerabilities | 7 Supply Chain and Dependency Integrity, 1 Vendor Assurance, 17 Integration / Connector Security |
| ASI05 | Unexpected Code Execution | 12 Agentic / Workflow Execution, 6 Admin / Endpoint / Operator Security, 14 Self-Hosted Infrastructure Control |
| ASI06 | Memory & Context Poisoning | 13 Retrieval / Knowledge Security, 12 Agentic / Workflow Execution |
| ASI07 | Insecure Inter-Agent Communication | 12 Agentic / Workflow Execution, 3 Network and Path Control, 17 Integration / Connector Security |
| ASI08 | Cascading Failures | 12 Agentic / Workflow Execution, 10 Monitoring / Audit / Response |
| ASI09 | Human-Agent Trust Exploitation | 16 Output Liability / Public-Facing Safety, 9 Governance / Acceptable Use |
| ASI10 | Rogue Agents | 12 Agentic / Workflow Execution, 10 Monitoring / Audit / Response, 11 AI Governance / Model Controls |

### OWASP MCP Top 10 (beta)

The MCP list is in beta and its identifiers may change. Mappings below are cited as a draft reference.

| MCP ID | Description | Gap Categories most commonly mapped |
|---|---|---|
| MCP01:2025 | Token Mismanagement & Secret Exposure | 2 Identity and Access, 17 Integration / Connector Security |
| MCP02:2025 | Privilege Escalation via Scope Creep | 2 Identity and Access, 17 Integration / Connector Security |
| MCP03:2025 | Tool Poisoning | 7 Supply Chain and Dependency Integrity, 12 Agentic / Workflow Execution, 17 Integration / Connector Security |
| MCP04:2025 | Software Supply Chain Attacks & Dependency Tampering | 7 Supply Chain and Dependency Integrity |
| MCP05:2025 | Command Injection & Execution | 12 Agentic / Workflow Execution, 6 Admin / Endpoint / Operator Security |
| MCP06:2025 | Prompt Injection via Contextual Payloads | 5 Output Validation, 13 Retrieval / Knowledge Security |
| MCP07:2025 | Insufficient Authentication & Authorization | 2 Identity and Access, 17 Integration / Connector Security |
| MCP08:2025 | Lack of Audit and Telemetry | 10 Monitoring / Audit / Response |
| MCP09:2025 | Shadow MCP Servers | 17 Integration / Connector Security, 9 Governance / Acceptable Use |
| MCP10:2025 | Context Injection & Over-Sharing | 4 Data Protection Outbound, 13 Retrieval / Knowledge Security, 17 Integration / Connector Security |

For broader framework alignment beyond NIST CSF and the OWASP lists, see `framework-alignment.md`.
