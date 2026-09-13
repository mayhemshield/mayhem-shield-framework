# Mayhem Shield Framework (Public)

## Enterprise AI implementation assurance

[Mayhem Shield](https://mayhemshield.com) provides buyer-side assurance for enterprise AI deployments. The firm assesses whether security controls actually hold for a specific deployment, covering data paths, identities, integrations, workflows, and go-live conditions, and documents the results for approvers as findings, evidence requests, and conditions for each approval gate. It does not resell or implement the products it reviews.

This repository is the public version of the Mayhem Shield framework. It provides the method, classification model, and public-safe templates used to scope and assess enterprise AI implementations.

## What Mayhem Shield does
- Evaluates implementation-level risk in AI-enabled systems, as deployed in the buyer's environment.
- Maps expected controls to concrete architecture and workflow patterns.
- Uses evidence-based review phases and approval gates.
- Highlights control gaps and readiness concerns before pilot expansion or production.

Engagements: [mayhemshield.com/services](https://mayhemshield.com/services). Contact: info@mayhemshield.com. LinkedIn: [Mayhem Shield](https://www.linkedin.com/company/mayhem-shield/)

## What this framework is
- A structured assurance model for enterprise AI implementations.
- A way to classify deployments by primary implementation category.
- An overlay model for capability patterns that materially change risk.
- A practical starting point for internal review and external due diligence conversations.

## Who this is for
- **Security, risk, and compliance teams** scoping AI assurance and control expectations.
- **Architecture and platform owners** aligning design choices with review structure and evidence needs.
- **Product and engineering leaders** preparing for governance, procurement, or customer due diligence on AI features.
- **Anyone** who needs a clear, repeatable way to talk about *how* an AI system is implemented, not only *what* vendor documentation claims.

## Six implementation categories
Every review starts with one primary implementation category:
1. Pure AI Services
2. AI-Native SaaS
3. Traditional SaaS with AI Features
4. SaaS with AI Enhancement
5. Infrastructure with AI
6. AI-Native Content Generation

## Capability overlays
Overlays are additive modifiers applied on top of the primary category when relevant:
- RAG
- Agentic Workflow Execution
- Self-Hosted / Private Deployment
- Regulated Data
- Integration / Connector Exposure
- Output Liability / Public-Facing Use

## Framework alignment
Mayhem Shield's methodology references established standards including NIST AI RMF 1.0, ISO/IEC 42001:2023, EU AI Act, OWASP Top 10 for LLM Applications, NIST CSF 2.0, and SR 11-7. See `00-core-framework/framework-alignment.md` for where each standard appears in the methodology. Alignment refers to methodology reference, not certification. Mayhem Shield is not a NIST-recognized assessor.

### Mapping to NIST AI RMF 1.0
Review outputs reference the four AI RMF 1.0 functions. Each finding in a deliverable is tagged with the function it most directly addresses.

| AI RMF 1.0 function | Where it appears in this framework |
|---|---|
| Govern | Review of organizational accountability for the deployment; gate conditions and approver documentation (`00-core-framework/methodology.md`, `00-core-framework/framework-alignment.md`) |
| Map | Intake classification by implementation category and capability overlays; architecture and data-flow diagrams with control points (`01-implementation-categories/`, `02-capability-overlays/`, `05-templates/`) |
| Measure | Evidence rules and the findings register; gap categories and templates (`00-core-framework/evidence-model.md`, `00-core-framework/gap-categories.md`) |
| Manage | Severity calibration and gate conditions for POC, pilot, and production (`00-core-framework/severity-model.md`) |

Reports state the framework version used (AI RMF 1.0) so the mapping can be checked against the published document.

## Citing this framework
[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.22732175.svg)](https://doi.org/10.5281/zenodo.22732175)

A `CITATION.cff` file is included. GitHub renders it under "Cite this repository". The DOI above resolves to the latest archived release on Zenodo; each release also has its own version DOI on the Zenodo record.

## How to use this in 30 minutes
1. Skim `00-core-framework/methodology.md` for the review model and phases (about 10 minutes).
2. Open `03-guides/category-selection-guide.md` and pick **one** primary implementation category for your deployment (about 5 minutes).
3. Open `03-guides/overlay-selection-guide.md` and note **all** overlays that apply (about 5 minutes).
4. Read the matching files under `01-implementation-categories/` and `02-capability-overlays/` for definitions you selected (about 10 minutes).

You will leave with a labeled scope (category plus overlays) and vocabulary aligned with the rest of the framework. Deeper work lives under `00-core-framework/` (evidence, severity, gates) and `05-templates/` when you are ready to document architecture and flows.

## How to navigate this repository
- `00-core-framework/` - Core methodology, evidence model, claim verification, severity model, and review structure.
- `01-implementation-categories/` - Definitions and distinctions for the six primary categories.
- `02-capability-overlays/` - Overlay definitions and control-impact context.
- `03-guides/` - Public-safe guidance for category and overlay selection.
- `05-templates/` - Public-safe starter templates for diagrams and review artifacts.

Recommended path:
1. `00-core-framework/methodology.md`
2. `00-core-framework/claim-verification.md`
3. `01-implementation-categories/README.md`
4. `02-capability-overlays/README.md`
5. `03-guides/category-selection-guide.md`
6. `03-guides/overlay-selection-guide.md`
7. `00-core-framework/framework-alignment.md`

## What is intentionally not included in this public version
This repository intentionally excludes proprietary internal delivery artifacts. It is designed for framework transparency and public education, not for complete internal engagement execution.
