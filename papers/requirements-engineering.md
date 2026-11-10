# Requirements Engineering

需求工程 · [Survey home](../README.md) · [Current manuscript](../paper/survey.pdf)

This reading guide follows the engineering problems, approaches, and representative studies in the current manuscript. A study can appear in more than one stage. Bibliographic metadata follows the manuscript snapshot.

## Topics discussed in the manuscript

- **Acquiring and Revising Requirements**: [Axetorn et al., 2026](#axetorn2026trustrequirements); [Neves et al., 2025](#neves2025yuma); [Galster et al., 2026](#galster2026configuring); [Wen, 2026](#wen2026skillspec); [Dhanorkar et al., 2026](#dhanorkar2026oversight); [Sheng et al., 2026](#sheng2026dills); [Wang et al., 2026](#wang2026xagen)
- **Specifying Safety and Authority**: [Ojewale et al., 2026](#ojewale2026doubt); [Doshi et al., 2026](#doshi2026safetooluse); [Alamdari et al., 2026](#alamdari2026formal); [Axetorn et al., 2026](#axetorn2026trustrequirements)
- **Operationalizing Delegation and Governance**: [Hagar et al., 2026](#hagar2026runtimeconfiguration); [Mok et al., 2026](#mok2026actioncentric)

## Engineering problems and approaches

### Needs, safety, authority, and delegation

| Engineering problem | Approach | Key idea | Representative studies |
|---|---|---|---|
| Identifying needs and making them explicit | Stakeholder elicitation | Code interview accounts into trust themes, refine them with experts, and map explicit requirements to design. | [Axetorn et al., 2026](#axetorn2026trustrequirements) |
| Identifying needs and making them explicit | Interactive goal refinement | Clarify goals and constraints through dialogue, then use the textual specification to propose a design for user approval. | [Neves et al., 2025](#neves2025yuma) |
| Identifying needs and making them explicit | Configuration analysis (observational) | Characterize existing configuration mechanisms and specification cues; identify what artifacts expose or omit. | [Galster et al., 2026](#galster2026configuring); [Wen, 2026](#wen2026skillspec) |
| Specifying acceptable and authorized behavior | Action preconditions | State required information and authority, with clarification or escalation when conditions are unmet. | [Ojewale et al., 2026](#ojewale2026doubt) |
| Specifying acceptable and authorized behavior | Hazard-based derivation | Trace stakeholder values through potential losses and unsafe behavior to safety requirements. | [Doshi et al., 2026](#doshi2026safetooluse) |
| Specifying acceptable and authorized behavior | Temporal specification | Encode supplied obligations in LTL and map observed events to propositions for compliance checking. | [Alamdari et al., 2026](#alamdari2026formal) |
| Expressing delegation and governance requirements | Situated configuration | Encode professional commitments as persistent instructions, evidence requirements, and escalation rules. | [Hagar et al., 2026](#hagar2026runtimeconfiguration) |
| Expressing delegation and governance requirements | Threat-to-control mapping | Translate threats into control objectives, security functions, and organizational assessment criteria. | [Mok et al., 2026](#mok2026actioncentric) |

## Discussed studies (16)

<a id="axetorn2026trustrequirements"></a>

### Addressing trust requirements in the design of an open-source multi-agent LLM-based domain-specific chatbot

Axetorn et al., 2026 · Requirements Engineering · [Paper](https://doi.org/10.1007/s00766-026-00457-w)

**Discussion topics:** Acquiring and Revising Requirements; Specifying Safety and Authority.

**Engineering approach:** Code interview accounts into trust themes, refine them with experts, and map explicit requirements to design.

<a id="neves2025yuma"></a>

### Yuma: Geração de workflows multiagentes a partir de linguagem natural

Neves et al., 2025 · Anais estendidos do XXXI simpósio brasileiro de sistemas multimídia e web · [Paper](https://doi.org/10.5753/webmedia_estendido.2025.16421)

**Discussion topics:** Acquiring and Revising Requirements.

**Engineering approach:** Clarify goals and constraints through dialogue, then use the textual specification to propose a design for user approval.

<a id="galster2026configuring"></a>

### Configuring agentic AI coding tools: An exploratory study

Galster et al., 2026 · Proceedings of the 3rd ACM international conference on AI-powered software · [Paper](https://doi.org/10.1145/3805760.3814887)

**Discussion topics:** Acquiring and Revising Requirements.

**Engineering approach:** Characterize existing configuration mechanisms and specification cues; identify what artifacts expose or omit.

<a id="wen2026skillspec"></a>

### Toward user comprehension supports for LLM agent skill specifications

Wen, 2026 · Preprint / author manuscript · [Paper](https://arxiv.org/abs/2605.19362)

**Discussion topics:** Acquiring and Revising Requirements.

**Engineering approach:** Characterize existing configuration mechanisms and specification cues; identify what artifacts expose or omit.

<a id="dhanorkar2026oversight"></a>

### Human oversight of agentic systems in practice: Examining the oversight work, challenges, and heuristics of developers using software agents

Dhanorkar et al., 2026 · Proceedings of the 2026 ACM conference on fairness, accountability, and transparency · [Paper](https://doi.org/10.1145/3805689.3812402)

**Discussion topics:** Acquiring and Revising Requirements.

<a id="sheng2026dills"></a>

### DiLLS: Interactive diagnosis of LLM-based multi-agent systems via layered summary of agent behaviors

Sheng et al., 2026 · Proceedings of the 2026 CHI conference on human factors in computing systems · [Paper](https://doi.org/10.1145/3772318.3790815)

**Discussion topics:** Acquiring and Revising Requirements.

<a id="wang2026xagen"></a>

### XAgen: An explainability tool for identifying and correcting failures in multi-agent workflows

Wang et al., 2026 · Proceedings of the extended abstracts of the 2026 CHI conference on human factors in computing systems · [Paper](https://doi.org/10.1145/3772363.3798531)

**Discussion topics:** Acquiring and Revising Requirements.

<a id="ojewale2026doubt"></a>

### Designing for doubt: The case for informed abstention in autonomous agents

Ojewale et al., 2026 · Preprint / author manuscript · [Paper](https://doi.org/10.48550/arXiv.2606.02965)

**Discussion topics:** Specifying Safety and Authority.

**Engineering approach:** State required information and authority, with clarification or escalation when conditions are unmet.

<a id="doshi2026safetooluse"></a>

### Towards verifiably safe tool use for LLM agents

Doshi et al., 2026 · Proceedings of the IEEE/ACM 48th international conference on software engineering · [Paper](https://doi.org/10.1145/3786582.3786839)

**Discussion topics:** Specifying Safety and Authority.

**Engineering approach:** Trace stakeholder values through potential losses and unsafe behavior to safety requirements.

<a id="alamdari2026formal"></a>

### Formal methods meet LLMs: Auditing, monitoring, and intervention for compliance of advanced AI systems

Alamdari et al., 2026 · Proceedings of the 2026 ACM conference on fairness, accountability, and transparency · [Paper](https://doi.org/10.1145/3805689.3812339)

**Discussion topics:** Specifying Safety and Authority.

**Engineering approach:** Encode supplied obligations in LTL and map observed events to propositions for compliance checking.

<a id="hagar2026runtimeconfiguration"></a>

### Runtime configuration for situated governance of AI agents: A case study in investigative journalism

Hagar et al., 2026 · AI and Ethics · [Paper](https://doi.org/10.1007/s43681-026-01298-7)

**Discussion topics:** Operationalizing Delegation and Governance.

**Engineering approach:** Encode professional commitments as persistent instructions, evidence requirements, and escalation rules.

<a id="mok2026actioncentric"></a>

### An action-centric zero trust maturity model for agentic AI environments

Mok et al., 2026 · Sensors · [Paper](https://doi.org/10.3390/s26165205)

**Discussion topics:** Operationalizing Delegation and Governance.

**Engineering approach:** Translate threats into control objectives, security functions, and organizational assessment criteria.

<a id="zheng2026persona"></a>

### Persona-based requirements engineering for explainable multi-agent educational systems: A scenario simulator for clinical reasoning training

Zheng et al., 2026 · Preprint / author manuscript · [Paper](https://arxiv.org/abs/2604.17186)

<a id="david2026alignmentcontracts"></a>

### Alignment contracts for agentic security systems

David et al., 2026 · Preprint / author manuscript · [Paper](https://doi.org/10.48550/arXiv.2605.00081)

<a id="shin2026agentbuild"></a>

### Fantastic scientific agents and how to build them: AgentBuild for rietveld refinement

Shin et al., 2026 · Preprint / author manuscript · [Paper](https://arxiv.org/abs/2606.12834v1)

<a id="ghalebikesabi2024contextual"></a>

### Operationalizing contextual integrity in privacy-conscious assistants

Ghalebikesabi et al., 2024 · Preprint / author manuscript · [Paper](https://arxiv.org/abs/2408.02373v2)

## SE background references

- [Requirements engineering: A roadmap](https://doi.org/10.1145/336512.336523) (2000).
- [Goal-oriented requirements engineering: A guided tour](https://doi.org/10.1109/ISRE.2001.948567) (2001).
- [Modeling security requirements through ownership, permission and delegation](https://doi.org/10.1109/RE.2005.43) (2005).
