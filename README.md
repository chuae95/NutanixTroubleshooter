Project Nix is a prototype, alert-driven troubleshooting assistant for Nutanix environments. It combines structured infrastructure evidence, retrieval-augmented generation (RAG), and a small locally deployable language model to produce grounded root-cause hypotheses and recommended diagnostic checks.
Nix is not intended to replace Prism monitoring or automatically execute remediation. Prism detects and raises the initial alert; Nix gathers the surrounding evidence, retrieves relevant operational knowledge, and helps an engineer determine what most likely happened.

Given a Nutanix alert, Nix should:
1. Identify the affected entity and incident time window.
2. Collect relevant metrics, events, topology information, and selected logs.
3. Convert the collected telemetry into compact, structured evidence.
4. Retrieve applicable Nutanix and infrastructure documentation.
5. Generate a ranked diagnosis supported by evidence and documentation.
6. Recommend safe next checks while abstaining when evidence is insufficient.

Proposed phases:
Phase 1: Research and scope defiinition
- EviRCA and evidence-card extraction
- RAG for operational documentation
- Small-model RCA performance
- Available Nutanix APIs, alerts, metrics and logs

Phase 2: Nutanix playground
- Nutanix test environment
- Prism access
- Metric and event collection
- Check if possible to trigger certain metrics

Phase 3: Nutanix RAG
- Authorized Nutanix documentation collection
- Nutanix Knowledege based articles
- Approved networking, Linux, Kubernetes and SQL references
- Reviewed Incident reports (Pipeline for our side to input)

References:
EviRCA: Decoupling Evidence Extraction from Reasoning for Microservice Root-Cause Analysis
https://arxiv.org/pdf/2609.19825
Root Cause Analysis Method Based on Large Language Models with Residual Connection Structures
https://arxiv.org/pdf/2602.08804
LogReasoner: Empowering LLMs with Expert-like Coarse-to-Fine Reasoning for Automated Log Analysis
https://arxiv.org/pdf/2509.20798