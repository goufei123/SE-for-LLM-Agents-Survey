# Maintenance and Evolution

维护与演化 · [Survey home](../README.md) · [Current manuscript](../paper/survey.pdf)

This reading guide follows the engineering problems, approaches, and representative studies in the current manuscript. A study can appear in more than one stage. Bibliographic metadata follows the manuscript snapshot.

## Topics discussed in the manuscript

- **Making Executions Inspectable and Failures Localizable**: [Study, 2026](#washizaki2026swebok); [Zheng et al., 2025](#zheng2025agentsight); [Vu et al., 2026](#vu2026agentbehaviormining); [Desmond et al., 2025](#desmond2025trajectoryexplorer); [Sheng et al., 2026](#sheng2026dills); [Wang et al., 2026](#wang2026xagen); [Singh, 2026](#singh2026scapegoats); [George et al., 2025](#george2025cycledetection); [Ge et al., 2026](#ge2026famas); [Wang, 2026](#wang2026agenttracecausal); [Atreja, 2026](#atreja2026pathfinder); [Oyelayo et al., 2026](#oyelayo2026mcpchallenges); [Islam et al., 2026](#islam2026selfheal)
- **From Detection to Bounded Runtime Intervention**: [Study, 2026](#washizaki2026swebok); [Li et al., 2026](#li2026adr); [Advani, 2026](#advani2026falsesuccess); [Nanda et al., 2026](#nanda2026wink); [Liu et al., 2026](#liu2026processcentric); [He et al., 2026](#he2026atrust)
- **Revising Durable Artifacts and Refreshing Persistent State**: [Study, 2026](#washizaki2026swebok); [Qi et al., 2026](#qi2026llmascode); [Islam et al., 2026](#islam2026selfheal); [Liu et al., 2026](#liu2026skillforge); [Yang et al., 2026](#yang2026triage); [Xu et al., 2026](#xu2026hierarchicalmemory)
- **Governing Versions, Distribution, and Operational Feedback**: [Study, 2026](#washizaki2026swebok); [Wang et al., 2025](#wang2025openhandsplatform); [Dutta et al., 2026](#dutta2026agentriskbom); [Ponduru, 2026](#ponduru2026unifiedagents); [Rama et al., 2025](#rama2025cerebrum); [Pothukuchi, 2026](#pothukuchi2026enterprisecrm); [Gupta et al., 2026](#gupta2026customersupport); [Guo et al., 2026](#guo2026agentevaldag); [Choi et al., 2026](#choi2026policybank); [Wang et al., 2026](#wang2026harnesshandbook)

## Engineering problems and approaches

### Operational observation and diagnosis

| Engineering problem | Approach | Key idea | Representative studies |
|---|---|---|---|
| Collecting operational evidence | System-boundary instrumentation | Correlate LLM communication with process and operating-system events. | [Zheng et al., 2025](#zheng2025agentsight) |
| Collecting operational evidence | Event-model standardization | Represent calls, delegation, and costs for process and conformance analysis. | [Vu et al., 2026](#vu2026agentbehaviormining) |
| Collecting operational evidence | Step-level instrumentation | Persist structured events before and after runtime steps. | [Langay, 2026](#langay2026nexus) |
| Supporting maintainer inspection | Hierarchical summarization | Organize plans, actions, and operations into navigable diagnostic summaries. | [Sheng et al., 2026](#sheng2026dills) |
| Supporting maintainer inspection | Trace normalization | Align heterogeneous trajectories for visual inspection and feedback. | [Desmond et al., 2025](#desmond2025trajectoryexplorer) |
| Supporting maintainer inspection | Workflow-linked explanation | Connect logs and judge rationales to feedback and configuration editing. | [Wang et al., 2026](#wang2026xagen) |
| Recognizing anomalous behavior | Repetition analysis | Combine repeated calls and output similarity to identify harmful cycles. | [George et al., 2025](#george2025cycledetection) |
| Recognizing anomalous behavior | Message-boundary heuristics | Flag candidate unfaithful refusals from tool failures and response wording. | [Singh, 2026](#singh2026scapegoats) |
| Localizing faults | Replay-based attribution | Rank suspicious Agents and actions using replayed and abstracted trajectories. | [Ge et al., 2026](#ge2026famas) |
| Localizing faults | Dependency-graph analysis | Rank candidate causes using trace dependencies and positional features. | [Wang, 2026](#wang2026agenttracecausal) |
| Localizing faults | Query-based diagnosis | Generate executable trace queries to identify a deficiency and affected component. | [Atreja, 2026](#atreja2026pathfinder) |
| Characterizing recurring problems | Issue-to-change analysis | Relate reported integration problems to merged changes and code churn. | [Oyelayo et al., 2026](#oyelayo2026mcpchallenges) |

### Intervention and evolution

| Engineering problem | Approach | Key idea | Representative studies |
|---|---|---|---|
| Responding to execution problems | Staged detection and prevention | Escalate suspicious sessions for contextual analysis and block recognizable credential exposure. | [Li et al., 2026](#li2026adr) |
| Responding to execution problems | Calibrated failure triage | Prioritize apparently successful executions that may require investigation. | [Advani, 2026](#advani2026falsesuccess) |
| Responding to execution problems | Corrective guidance | Append targeted guidance after detecting misbehavior. | [Nanda et al., 2026](#nanda2026wink) |
| Responding to execution problems | Process-conditioned intervention | Suppress problematic steps or revise guidance using monitored process conditions. | [Liu et al., 2026](#liu2026processcentric) |
| Responding to execution problems | Trust-based participation control | Use timestamped trust estimates to filter messages or isolate Agents. | [He et al., 2026](#he2026atrust) |
| Revising durable artifacts | Defect-guided repair | Generate candidate code changes from defect patterns and API information, with critic feedback. | [Islam et al., 2026](#islam2026selfheal) |
| Revising durable artifacts | Test-gated replacement | Propose admitting a generated function only after caller-owned tests pass. | [Qi et al., 2026](#qi2026llmascode) |
| Revising durable artifacts | Instruction revision | Diagnose failures, edit skill documents, and commit the revised filesystem state. | [Liu et al., 2026](#liu2026skillforge) |
| Revising durable artifacts | Incremental index refresh | Update changed leaves and affected ancestor paths instead of rebuilding the full index. | [Xu et al., 2026](#xu2026hierarchicalmemory) |
| Governing versions and releases | Build identity | Use build-context hashes and version tags to control image reuse or rebuilding. | [Wang et al., 2025](#wang2025openhandsplatform) |
| Governing versions and releases | Authority-change review | Compare versioned descriptions of permissions, tools, memory access, and approval policies. | [Dutta et al., 2026](#dutta2026agentriskbom) |
| Governing versions and releases | Version-aware distribution | Package Agents with dependencies and preserve version history and integrity checks. | [Rama et al., 2025](#rama2025cerebrum) |
| Governing versions and releases | Evaluation-guided rollout | Combine versioned prompts, offline checks, progressive rollout, and operational feedback. | [Gupta et al., 2026](#gupta2026customersupport) |

## Discussed studies (32)

<a id="washizaki2026swebok"></a>

### Guide to the software engineering body of knowledge (SWEBOK guide)

Study, 2026 · IEEE Computer Society · [Paper](https://ieeecs-media.computer.org/media/education/swebok/swebok-v4.pdf)

**Discussion topics:** Making Executions Inspectable and Failures Localizable; From Detection to Bounded Runtime Intervention; Revising Durable Artifacts and Refreshing Persistent State; Governing Versions, Distribution, and Operational Feedback.

<a id="zheng2025agentsight"></a>

### AgentSight: System-level observability for AI agents using eBPF

Zheng et al., 2025 · Proceedings of the 4th workshop on practical adoption challenges of ML for systems · [Paper](https://doi.org/10.1145/3766882.3767169)

**Discussion topics:** Making Executions Inspectable and Failures Localizable.

**Engineering approach:** Correlate LLM communication with process and operating-system events.

<a id="vu2026agentbehaviormining"></a>

### Agent behavior mining: Generative AI agent governance in business processes

Vu et al., 2026 · Preprint / author manuscript · [Paper](https://arxiv.org/abs/2606.20669)

**Discussion topics:** Making Executions Inspectable and Failures Localizable.

**Engineering approach:** Represent calls, delegation, and costs for process and conformance analysis.

<a id="desmond2025trajectoryexplorer"></a>

### Agent trajectory explorer: Visualizing and providing feedback on agent trajectories

Desmond et al., 2025 · Proceedings of the AAAI Conference on Artificial Intelligence · [Paper](https://doi.org/10.1609/aaai.v39i28.35350)

**Discussion topics:** Making Executions Inspectable and Failures Localizable.

**Engineering approach:** Align heterogeneous trajectories for visual inspection and feedback.

<a id="sheng2026dills"></a>

### DiLLS: Interactive diagnosis of LLM-based multi-agent systems via layered summary of agent behaviors

Sheng et al., 2026 · Proceedings of the 2026 CHI conference on human factors in computing systems · [Paper](https://doi.org/10.1145/3772318.3790815)

**Discussion topics:** Making Executions Inspectable and Failures Localizable.

**Engineering approach:** Organize plans, actions, and operations into navigable diagnostic summaries.

<a id="wang2026xagen"></a>

### XAgen: An explainability tool for identifying and correcting failures in multi-agent workflows

Wang et al., 2026 · Proceedings of the extended abstracts of the 2026 CHI conference on human factors in computing systems · [Paper](https://doi.org/10.1145/3772363.3798531)

**Discussion topics:** Making Executions Inspectable and Failures Localizable.

**Engineering approach:** Connect logs and judge rationales to feedback and configuration editing.

<a id="langay2026nexus"></a>

### Design and implementation of a lightweight neural controller for LLM agent systems

Langay, 2026 · International Journal of Latest Technology in Engineering Management & Applied Science · [Paper](https://doi.org/10.51583/ijltemas.2026.150500172)

**Engineering approach:** Persist structured events before and after runtime steps.

<a id="george2025cycledetection"></a>

### Unsupervised cycle detection in agentic applications

George et al., 2025 · Preprint / author manuscript · [Paper](https://arxiv.org/abs/2511.10650v1)

**Discussion topics:** Making Executions Inspectable and Failures Localizable.

**Engineering approach:** Combine repeated calls and output similarity to identify harmful cycles.

<a id="singh2026scapegoats"></a>

### Guardrails as scapegoats: Auditing unfaithful safety refusals in tool-augmented LLM agents

Singh, 2026 · Preprint / author manuscript · [Paper](https://doi.org/10.48550/arXiv.2607.19449)

**Discussion topics:** Making Executions Inspectable and Failures Localizable.

**Engineering approach:** Flag candidate unfaithful refusals from tool failures and response wording.

<a id="ge2026famas"></a>

### Spectrum-based failure attribution for multi-agent systems

Ge et al., 2026 · Proceedings of the ACM on Software Engineering · [Paper](https://doi.org/10.1145/3797113)

**Discussion topics:** Making Executions Inspectable and Failures Localizable.

**Engineering approach:** Rank suspicious Agents and actions using replayed and abstracted trajectories.

<a id="wang2026agenttracecausal"></a>

### AgentTrace: Causal graph tracing for root cause analysis in deployed multi-agent systems

Wang, 2026 · Preprint / author manuscript · [Paper](https://arxiv.org/abs/2603.14688v2)

**Discussion topics:** Making Executions Inspectable and Failures Localizable.

**Engineering approach:** Rank candidate causes using trace dependencies and positional features.

<a id="atreja2026pathfinder"></a>

### Pathfinder: Self-improving agent trace analysis via adversarial self-play and code execution

Atreja, 2026 · Proceedings of the ACM conference on AI and agentic systems · [Paper](https://doi.org/10.1145/3786335.3813199)

**Discussion topics:** Making Executions Inspectable and Failures Localizable.

**Engineering approach:** Generate executable trace queries to identify a deficiency and affected component.

<a id="oyelayo2026mcpchallenges"></a>

### Developer challenges in the adoption of model context protocol in AI agent development

Oyelayo et al., 2026 · Proceedings of the 2026 7th international workshop on bots and agents in software engineering · [Paper](https://doi.org/10.1145/3786161.3788462)

**Discussion topics:** Making Executions Inspectable and Failures Localizable.

**Engineering approach:** Relate reported integration problems to merged changes and code churn.

<a id="islam2026selfheal"></a>

### SelfHeal: Empirical fix pattern analysis and bug repair in LLM agents

Islam et al., 2026 · Preprint / author manuscript · [Paper](https://arxiv.org/abs/2604.17699)

**Discussion topics:** Making Executions Inspectable and Failures Localizable; Revising Durable Artifacts and Refreshing Persistent State.

**Engineering approach:** Generate candidate code changes from defect patterns and API information, with critic feedback.

<a id="li2026adr"></a>

### ADR: An agentic detection system for enterprise agentic AI security

Li et al., 2026 · Preprint / author manuscript · [Paper](https://arxiv.org/abs/2605.17380)

**Discussion topics:** From Detection to Bounded Runtime Intervention.

**Engineering approach:** Escalate suspicious sessions for contextual analysis and block recognizable credential exposure.

<a id="advani2026falsesuccess"></a>

### From confident closing to silent failure: Characterizing false success in LLM agents

Advani, 2026 · Preprint / author manuscript · [Paper](https://arxiv.org/abs/2606.09863)

**Discussion topics:** From Detection to Bounded Runtime Intervention.

**Engineering approach:** Prioritize apparently successful executions that may require investigation.

<a id="nanda2026wink"></a>

### Wink: Recovering from misbehaviors in coding agents

Nanda et al., 2026 · Proceedings of the 3rd ACM international conference on AI-powered software · [Paper](https://doi.org/10.1145/3805760.3814911)

**Discussion topics:** From Detection to Bounded Runtime Intervention.

**Engineering approach:** Append targeted guidance after detecting misbehavior.

<a id="liu2026processcentric"></a>

### Process-centric analysis of agentic software systems

Liu et al., 2026 · Proceedings of the ACM on Programming Languages · [Paper](https://doi.org/10.1145/3798271)

**Discussion topics:** From Detection to Bounded Runtime Intervention.

**Engineering approach:** Suppress problematic steps or revise guidance using monitored process conditions.

<a id="he2026atrust"></a>

### To trust or not to trust: Attention-based trust management for LLM multi-agent systems

He et al., 2026 · Preprint / author manuscript · [Paper](https://arxiv.org/abs/2506.02546)

**Discussion topics:** From Detection to Bounded Runtime Intervention.

**Engineering approach:** Use timestamped trust estimates to filter messages or isolate Agents.

<a id="qi2026llmascode"></a>

### LLM-as-Code: Agentic programming for agent harness

Qi et al., 2026 · Preprint / author manuscript · [Paper](https://arxiv.org/abs/2606.15874v2)

**Discussion topics:** Revising Durable Artifacts and Refreshing Persistent State.

**Engineering approach:** Propose admitting a generated function only after caller-owned tests pass.

<a id="liu2026skillforge"></a>

### SkillForge: Forging domain-specific, self-evolving agent skills in cloud technical support

Liu et al., 2026 · Preprint / author manuscript · [Paper](https://arxiv.org/abs/2604.08618v2)

**Discussion topics:** Revising Durable Artifacts and Refreshing Persistent State.

**Engineering approach:** Diagnose failures, edit skill documents, and commit the revised filesystem state.

<a id="yang2026triage"></a>

### One recipe, many harnesses: What self-evolution encodes across languages and models

Yang et al., 2026 · Preprint / author manuscript · [Paper](https://arxiv.org/abs/2608.10178v1)

**Discussion topics:** Revising Durable Artifacts and Refreshing Persistent State.

<a id="xu2026hierarchicalmemory"></a>

### Hierarchical long-term semantic memory for LinkedIn’s hiring agent

Xu et al., 2026 · Proceedings of the 32nd ACM SIGKDD conference on knowledge discovery and data mining v.2 · [Paper](https://doi.org/10.1145/3770855.3818432)

**Discussion topics:** Revising Durable Artifacts and Refreshing Persistent State.

**Engineering approach:** Update changed leaves and affected ancestor paths instead of rebuilding the full index.

<a id="wang2025openhandsplatform"></a>

### OpenHands: An open platform for AI software developers as generalist agents

Wang et al., 2025 · The thirteenth international conference on learning representations · [Paper](https://openreview.net/forum?id=OJd3ayDDoF)

**Discussion topics:** Governing Versions, Distribution, and Operational Feedback.

**Engineering approach:** Use build-context hashes and version tags to control image reuse or rebuilding.

<a id="dutta2026agentriskbom"></a>

### AgentRiskBOM: A risk-scoping security bill of materials for agentic AI systems

Dutta et al., 2026 · Preprint / author manuscript · [Paper](https://doi.org/10.48550/arXiv.2606.21877)

**Discussion topics:** Governing Versions, Distribution, and Operational Feedback.

**Engineering approach:** Compare versioned descriptions of permissions, tools, memory access, and approval policies.

<a id="rama2025cerebrum"></a>

### Cerebrum (AIOS SDK): A platform for agent development, deployment, distribution, and discovery

Rama et al., 2025 · Proceedings of the 2025 conference of the nations of the americas chapter of the association for computational linguistics: Human language technologies (system demonstrations) · [Paper](https://doi.org/10.18653/v1/2025.naacl-demo.14)

**Discussion topics:** Governing Versions, Distribution, and Operational Feedback.

**Engineering approach:** Package Agents with dependencies and preserve version history and integrity checks.

<a id="gupta2026customersupport"></a>

### Building customer support AI agents at 100M-user scale: An evaluation-driven framework

Gupta et al., 2026 · Proceedings of the 32nd ACM SIGKDD conference on knowledge discovery and data mining v.2 · [Paper](https://doi.org/10.1145/3770855.3818332)

**Discussion topics:** Governing Versions, Distribution, and Operational Feedback.

**Engineering approach:** Combine versioned prompts, offline checks, progressive rollout, and operational feedback.

<a id="ponduru2026unifiedagents"></a>

### A unified framework for self-evolving and self-healing artificial intelligence agents

Ponduru, 2026 · Advanced International Journal of Multidisciplinary Research · [Paper](https://doi.org/10.62127/aijmr.2026.v04i04.1435)

**Discussion topics:** Governing Versions, Distribution, and Operational Feedback.

<a id="pothukuchi2026enterprisecrm"></a>

### Autonomous AI agents in enterprise CRM: Architecture, governance, and operational safety

Pothukuchi, 2026 · Journal of Information Systems Engineering and Management · [Paper](https://doi.org/10.52783/jisem.v11i2s.14537)

**Discussion topics:** Governing Versions, Distribution, and Operational Feedback.

<a id="guo2026agentevaldag"></a>

### AgentEval: DAG-structured step-level evaluation for agentic workflows with error propagation tracking

Guo et al., 2026 · Preprint / author manuscript · [Paper](https://arxiv.org/abs/2604.23581)

**Discussion topics:** Governing Versions, Distribution, and Operational Feedback.

<a id="choi2026policybank"></a>

### PolicyBank: Evolving policy understanding for LLM agents

Choi et al., 2026 · Preprint / author manuscript · [Paper](https://doi.org/10.48550/arXiv.2604.15505)

**Discussion topics:** Governing Versions, Distribution, and Operational Feedback.

<a id="wang2026harnesshandbook"></a>

### Harness Handbook: Making evolving agent harnesses readable, navigable, and editable

Wang et al., 2026 · Preprint / author manuscript · [Paper](https://arxiv.org/abs/2607.13285v1)

**Discussion topics:** Governing Versions, Distribution, and Operational Feedback.
