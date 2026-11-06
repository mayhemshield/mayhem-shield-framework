# Severity Model

Default severity is a starting point, not the final answer.

Severity should be adjusted based on:
- how easily a threat named in the threat model could exploit the weakness (see `threat-model.md`)
- deployment scope
- production exposure
- data sensitivity
- public-facing use
- action-taking capability
- compensating controls

## Framework reference

Severity calibration draws on the NIST AI RMF Manage function. Where a finding affects production risk, regulatory exposure, or public-facing output, severity is adjusted upward to reflect Manage-function expectations around residual risk treatment. See `framework-alignment.md` for the broader methodology-to-framework mapping.
