# Architecture and Design

架构与设计 · [Survey home](../README.md) · [Current manuscript](../paper/survey.pdf)

This reading guide follows the engineering problems, approaches, and representative studies in the current manuscript. A study can appear in more than one stage. Bibliographic metadata follows the manuscript snapshot.

## Topics discussed in the manuscript

- **Describing and Realizing Coordination**: [Study, 2026](#washizaki2026swebok); [Mei et al., 2025](#mei2025aios); [Rausch et al., 2026](#rausch2026agenticc4); [Lu et al., 2026](#lu2026agentarceval); [Yang et al., 2026](#yang2026bamas); [Yuan et al., 2025](#yuan2025composer); [Wang et al., 2025](#wang2025openhandsplatform); [Bollig et al., 2026](#bollig2026coordination); [Yu et al., 2026](#yu2026dyntaskmas); [Caldeira et al., 2025](#caldeira2025control); [Alsheich et al., 2026](#alsheich2026linguistic); [Yang et al., 2025](#yang2025agentnet); [Bala et al., 2026](#bala2026pm4aa); [Eger et al., 2026](#eger2026architecture); [Hu et al., 2026](#hu2026evomas); [Yue et al., 2026](#yue2026autoras)
- **Discovering Services and Selecting Protocols**: [Study, 2026](#washizaki2026swebok); [Aminiranjbar et al., 2025](#aminiranjbar2025dawn); [Du et al., 2026](#du2026protocolbench)
- **Locating Control and Recovery Boundaries**: [Study, 2026](#washizaki2026swebok); [Bagdasarian et al., 2024](#bagdasarian2024airgapagent); [Yu et al., 2026](#yu2026minim); [Odersky et al., 2026](#odersky2026tracked); [Wu et al., 2025](#wu2024isolategpt); [Joshi et al., 2026](#joshi2026deontic); [Shlomov et al., 2026](#shlomov2026governance); [Zhou et al., 2026](#zhou2026confirmation); [Zhuang et al., 2026](#zhuang2026agentclick); [Jing et al., 2025](#jing2025mcip); [Tang et al., 2025](#tang2025riskknowledge); [Lin et al., 2026](#lin2026supervisoragent); [Yu et al., 2026](#yu2026operationalhallucination); [Qi et al., 2026](#qi2026llmascode); [Ben Khaled et al., 2026](#benkhaled2026g2cp); [Mao et al., 2025](#mao2025semap); [Chang et al., 2025](#chang2025sagallm); [Zheng et al., 2026](#zheng2026acrfence)
- **Designing State and Resource Substrates**: [Study, 2026](#washizaki2026swebok); [Wang et al., 2026](#wang2026openhands); [Xu et al., 2026](#xu2026hierarchicalmemory); [Wu et al., 2026](#wu2026dualpath); [Xu et al., 2026](#xu2026toolarchitecture)

## Engineering problems and approaches

### Structural design

| Engineering problem | Approach | Key idea | Representative studies |
|---|---|---|---|
| Assigning and assessing responsibilities | Shared runtime services | Separate Agent applications from kernel-managed resources through explicit interfaces. | [Mei et al., 2025](#mei2025aios) |
| Assigning and assessing responsibilities | Scenario-based assessment | Relate stakeholder goals and quality scenarios to design risks and recommendations. | [Lu et al., 2026](#lu2026agentarceval) |
| Assigning and assessing responsibilities | Controlled interface comparison | Vary interface abstractions while keeping capabilities similar to expose design trade-offs. | [Xu et al., 2026](#xu2026toolarchitecture) |
| Selecting and coordinating participants | Budgeted composition | Select model or tool inventories using supplied rankings or local component tests. | [Yang et al., 2026](#yang2026bamas); [Yuan et al., 2025](#yuan2025composer) |
| Selecting and coordinating participants | Specification and projection | Check a global communication specification and project it into local Agent programs. | [Bollig et al., 2026](#bollig2026coordination) |
| Selecting and coordinating participants | Dependency-aware scheduling | Maintain a subtask graph and dispatch ready work as dependencies change. | [Yu et al., 2026](#yu2026dyntaskmas) |
| Selecting and coordinating participants | Template or executor selection | Choose a predefined collaboration pattern or a behavior-calibrated executor for a query. | [Yang et al., 2026](#yang2026bamas); [Alsheich et al., 2026](#alsheich2026linguistic) |
| Selecting and coordinating participants | Decentralized coordination | Route work locally and update collaboration links from interaction outcomes. | [Yang et al., 2025](#yang2025agentnet) |
| Selecting and coordinating participants | Process-derived design | Map historical process traces to prescribed roles and role-specific process specifications. | [Bala et al., 2026](#bala2026pm4aa) |
| Selecting and coordinating participants | Configuration search | Mutate and recombine roles, models, prompts, tools, and communication links using execution feedback. | [Hu et al., 2026](#hu2026evomas) |
| Connecting distributed services | Discovery and composition | Separate orchestration from resource registration, discovery, and execution. | [Aminiranjbar et al., 2025](#aminiranjbar2025dawn) |
| Connecting distributed services | Requirement-guided protocol choice | Select per-module protocols and bridge their interfaces under explicit requirements. | [Du et al., 2026](#du2026protocolbench) |
| Organizing state and resources | State separation and scoping | Separate specifications from recoverable execution state, or align memory access with ownership. | [Wang et al., 2026](#wang2026openhands); [Xu et al., 2026](#xu2026hierarchicalmemory) |
| Organizing state and resources | Resource-path design | Split cache-loading paths and schedule transfers to manage serving bottlenecks. | [Wu et al., 2026](#wu2026dualpath) |

### Architectural control and recovery

| Engineering problem | Approach | Key idea | Representative studies |
|---|---|---|---|
| Bounding disclosure and propagation | Data minimization | Restrict third-party interaction to a task-relevant data subset behind a one-way boundary. | [Bagdasarian et al., 2024](#bagdasarian2024airgapagent) |
| Bounding disclosure and propagation | Mediated isolation | Separate applications and mediate their exchanges through trusted operators and permissions. | [Wu et al., 2025](#wu2024isolategpt) |
| Governing authority | External policy decisions | Evaluate typed invocations against explicit permissions and obligations outside the acting model. | [Joshi et al., 2026](#joshi2026deontic) |
| Governing authority | Policy-triggered checkpoints | Place blocking, approval, and advisory policies at explicit interaction points. | [Shlomov et al., 2026](#shlomov2026governance) |
| Recognizing risky execution | Information-flow supervision | Structure execution trajectories so a trained Guardian can identify and categorize risk. | [Jing et al., 2025](#jing2025mcip) |
| Recognizing risky execution | Proposal–critique control | Abstract a proposed action and its context, critique risk, and request revision. | [Tang et al., 2025](#tang2025riskknowledge) |
| Recognizing risky execution | Selective supervision | Use lightweight triggers to request context-dependent correction or verification. | [Lin et al., 2026](#lin2026supervisoragent) |
| Preserving execution consistency | Protocol contracts | Combine typed messages, behavioral contracts, and checked task-state transitions. | [Mao et al., 2025](#mao2025semap) |
| Preserving execution consistency | Compensation design | Preserve dependencies, validate before commitment, and associate effects with recovery actions. | [Chang et al., 2025](#chang2025sagallm) |
| Preserving execution consistency | Effect-aware restoration | Use a proposed effect log and semantic comparison to distinguish replay from an explicit fork. | [Zheng et al., 2026](#zheng2026acrfence) |

## Discussed studies (39)

<a id="washizaki2026swebok"></a>

### Guide to the software engineering body of knowledge (SWEBOK guide)

Study, 2026 · IEEE Computer Society · [Paper](https://ieeecs-media.computer.org/media/education/swebok/swebok-v4.pdf)

**Discussion topics:** Describing and Realizing Coordination; Discovering Services and Selecting Protocols; Locating Control and Recovery Boundaries; Designing State and Resource Substrates.

<a id="xu2026toolarchitecture"></a>

### The devil is in the interface: Evaluating how tool architecture shapes coding agent behavior

Xu et al., 2026 · Preprint / author manuscript · [Paper](https://arxiv.org/abs/2608.11386)

**Discussion topics:** Designing State and Resource Substrates.

**Engineering approach:** Vary interface abstractions while keeping capabilities similar to expose design trade-offs.

<a id="mei2025aios"></a>

### AIOS: LLM agent operating system

Mei et al., 2025 · Second conference on language modeling · [Paper](https://openreview.net/forum?id=L4HHkCDz2x)

**Discussion topics:** Describing and Realizing Coordination.

**Engineering approach:** Separate Agent applications from kernel-managed resources through explicit interfaces.

<a id="rausch2026agenticc4"></a>

### Describing agentic AI systems with C4: Lessons from industry projects

Rausch et al., 2026 · 2026 IEEE 23rd international conference on software architecture companion (ICSA-c) · [Paper](https://doi.org/10.1109/ICSA-C68850.2026.00092)

**Discussion topics:** Describing and Realizing Coordination.

<a id="lu2026agentarceval"></a>

### AgentArcEval: An architecture evaluation method for foundation model based agents

Lu et al., 2026 · Journal of Systems and Software · [Paper](https://doi.org/10.1016/j.jss.2025.112656)

**Discussion topics:** Describing and Realizing Coordination.

**Engineering approach:** Relate stakeholder goals and quality scenarios to design risks and recommendations.

<a id="yang2026bamas"></a>

### BAMAS: Structuring budget-aware multi-agent systems

Yang et al., 2026 · Proceedings of the AAAI Conference on Artificial Intelligence · [Paper](https://doi.org/10.1609/aaai.v40i35.40226)

**Discussion topics:** Describing and Realizing Coordination.

**Engineering approach:** Select model or tool inventories using supplied rankings or local component tests.

**Engineering approach:** Choose a predefined collaboration pattern or a behavior-calibrated executor for a query.

<a id="yuan2025composer"></a>

### Automated composition of agents: A knapsack approach for agentic component selection

Yuan et al., 2025 · Advances in neural information processing systems · [Paper](https://doi.org/10.52202/085713-1355)

**Discussion topics:** Describing and Realizing Coordination.

**Engineering approach:** Select model or tool inventories using supplied rankings or local component tests.

<a id="wang2025openhandsplatform"></a>

### OpenHands: An open platform for AI software developers as generalist agents

Wang et al., 2025 · The thirteenth international conference on learning representations · [Paper](https://openreview.net/forum?id=OJd3ayDDoF)

**Discussion topics:** Describing and Realizing Coordination.

<a id="bollig2026coordination"></a>

### Provable coordination for LLM agents via message sequence charts

Bollig et al., 2026 · Preprint / author manuscript · [Paper](https://arxiv.org/abs/2604.17612)

**Discussion topics:** Describing and Realizing Coordination.

**Engineering approach:** Check a global communication specification and project it into local Agent programs.

<a id="yu2026dyntaskmas"></a>

### Toward scalable LLM-based multi-agent collaboration: A dynamic task graph approach with asynchronous parallel execution

Yu et al., 2026 · Electronics · [Paper](https://doi.org/10.3390/electronics15112475)

**Discussion topics:** Describing and Realizing Coordination.

**Engineering approach:** Maintain a subtask graph and dispatch ready work as dependencies change.

<a id="caldeira2025control"></a>

### Where should control reside in multi-agent language-model systems?

Caldeira et al., 2025 · Proceedings of the international conference on AI research · [Paper](https://doi.org/10.34190/icair.5.1.4157)

**Discussion topics:** Describing and Realizing Coordination.

<a id="alsheich2026linguistic"></a>

### Linguistic firewall: Geometry as defense in multi-agent systems routing

Alsheich et al., 2026 · Preprint / author manuscript · [Paper](https://doi.org/10.48550/arXiv.2606.30555)

**Discussion topics:** Describing and Realizing Coordination.

**Engineering approach:** Choose a predefined collaboration pattern or a behavior-calibrated executor for a query.

<a id="yang2025agentnet"></a>

### AgentNet: Decentralized evolutionary coordination for LLM-based multi-agent systems

Yang et al., 2025 · Preprint / author manuscript · [Paper](https://arxiv.org/abs/2504.00587v2)

**Discussion topics:** Describing and Realizing Coordination.

**Engineering approach:** Route work locally and update collaboration links from interaction outcomes.

<a id="bala2026pm4aa"></a>

### Using process mining to generate AI agents from software engineering process records

Bala et al., 2026 · Preprint / author manuscript · [Paper](https://doi.org/10.48550/arXiv.2607.04948)

**Discussion topics:** Describing and Realizing Coordination.

**Engineering approach:** Map historical process traces to prescribed roles and role-specific process specifications.

<a id="eger2026architecture"></a>

### Gestaltung agentischer KI-systeme für die digitale versorgungssteuerung: Ein design-science-research-ansatz

Eger et al., 2026 · HMD Praxis der Wirtschaftsinformatik · [Paper](https://doi.org/10.1365/s40702-026-01301-z)

**Discussion topics:** Describing and Realizing Coordination.

<a id="hu2026evomas"></a>

### EvoMAS: Evolutionary generation of multi-agent systems

Hu et al., 2026 · Preprint / author manuscript · [Paper](https://arxiv.org/abs/2602.06511)

**Discussion topics:** Describing and Realizing Coordination.

**Engineering approach:** Mutate and recombine roles, models, prompts, tools, and communication links using execution feedback.

<a id="yue2026autoras"></a>

### AutoRAS: Learning robust agentic systems with primitive representations

Yue et al., 2026 · Preprint / author manuscript · [Paper](https://doi.org/10.48550/arXiv.2606.21445)

**Discussion topics:** Describing and Realizing Coordination.

<a id="aminiranjbar2025dawn"></a>

### DAWN: Designing distributed agents in a worldwide network

Aminiranjbar et al., 2025 · IEEE Access · [Paper](https://doi.org/10.1109/ACCESS.2025.3588425)

**Discussion topics:** Discovering Services and Selecting Protocols.

**Engineering approach:** Separate orchestration from resource registration, discovery, and execution.

<a id="du2026protocolbench"></a>

### ProtocolBench: Which LLM MultiAgent protocol to choose?

Du et al., 2026 · Preprint / author manuscript · [Paper](https://arxiv.org/abs/2510.17149)

**Discussion topics:** Discovering Services and Selecting Protocols.

**Engineering approach:** Select per-module protocols and bridge their interfaces under explicit requirements.

<a id="wang2026openhands"></a>

### The OpenHands software agent SDK: A composable and extensible foundation for production agents

Wang et al., 2026 · Proceedings of machine learning and systems · [Paper](https://proceedings.mlsys.org/paper_files/paper/2026/hash/8ae9cf363ea625161f885b798c1f1f78-Abstract-Conference.html)

**Discussion topics:** Designing State and Resource Substrates.

**Engineering approach:** Separate specifications from recoverable execution state, or align memory access with ownership.

<a id="xu2026hierarchicalmemory"></a>

### Hierarchical long-term semantic memory for LinkedIn’s hiring agent

Xu et al., 2026 · Proceedings of the 32nd ACM SIGKDD conference on knowledge discovery and data mining v.2 · [Paper](https://doi.org/10.1145/3770855.3818432)

**Discussion topics:** Designing State and Resource Substrates.

**Engineering approach:** Separate specifications from recoverable execution state, or align memory access with ownership.

<a id="wu2026dualpath"></a>

### DualPath: Accelerating agentic LLM inference by harvesting disaggregated KV-cache storage I/O

Wu et al., 2026 · Proceedings of the ACM SIGCOMM 2026 conference · [Paper](https://doi.org/10.1145/3789240.3829159)

**Discussion topics:** Designing State and Resource Substrates.

**Engineering approach:** Split cache-loading paths and schedule transfers to manage serving bottlenecks.

<a id="bagdasarian2024airgapagent"></a>

### AirGapAgent: Protecting privacy-conscious conversational agents

Bagdasarian et al., 2024 · Proceedings of the 2024 ACM SIGSAC conference on computer and communications security · [Paper](https://doi.org/10.1145/3658644.3690350)

**Discussion topics:** Locating Control and Recovery Boundaries.

**Engineering approach:** Restrict third-party interaction to a task-relevant data subset behind a one-way boundary.

<a id="yu2026minim"></a>

### Minim: Privacy-aware minimal view for agents via trusted local sanitization

Yu et al., 2026 · Preprint / author manuscript · [Paper](https://arxiv.org/abs/2606.13949)

**Discussion topics:** Locating Control and Recovery Boundaries.

<a id="odersky2026tracked"></a>

### Securing agents with tracked capabilities

Odersky et al., 2026 · Proceedings of the ACM conference on AI and agentic systems · [Paper](https://doi.org/10.1145/3786335.3813127)

**Discussion topics:** Locating Control and Recovery Boundaries.

<a id="wu2024isolategpt"></a>

### IsolateGPT: An execution isolation architecture for LLM-based agentic systems

Wu et al., 2025 · Proceedings of the network and distributed system security symposium · [Paper](https://doi.org/10.14722/ndss.2025.241131)

**Discussion topics:** Locating Control and Recovery Boundaries.

**Engineering approach:** Separate applications and mediate their exchanges through trusted operators and permissions.

<a id="joshi2026deontic"></a>

### Deontic policies for runtime governance of agentic AI systems

Joshi et al., 2026 · Preprint / author manuscript · [Paper](https://arxiv.org/abs/2606.19464)

**Discussion topics:** Locating Control and Recovery Boundaries.

**Engineering approach:** Evaluate typed invocations against explicit permissions and obligations outside the acting model.

<a id="shlomov2026governance"></a>

### Governance by construction for generalist agents

Shlomov et al., 2026 · Proceedings of the ACM conference on AI and agentic systems · [Paper](https://doi.org/10.1145/3786335.3813192)

**Discussion topics:** Locating Control and Recovery Boundaries.

**Engineering approach:** Place blocking, approval, and advisory policies at explicit interaction points.

<a id="zhou2026confirmation"></a>

### When should users check? Modeling confirmation frequency in multi-step agentic AI tasks

Zhou et al., 2026 · Proceedings of the 2026 CHI conference on human factors in computing systems · [Paper](https://doi.org/10.1145/3772318.3790655)

**Discussion topics:** Locating Control and Recovery Boundaries.

<a id="zhuang2026agentclick"></a>

### AgentClick: A skill-based human-in-the-loop review layer for terminal AI agents

Zhuang et al., 2026 · Proceedings of the ACM conference on AI and agentic systems · [Paper](https://doi.org/10.1145/3786335.3813232)

**Discussion topics:** Locating Control and Recovery Boundaries.

<a id="jing2025mcip"></a>

### MCIP: Protecting MCP safety via model contextual integrity protocol

Jing et al., 2025 · Proceedings of the 2025 conference on empirical methods in natural language processing · [Paper](https://doi.org/10.18653/v1/2025.emnlp-main.62)

**Discussion topics:** Locating Control and Recovery Boundaries.

**Engineering approach:** Structure execution trajectories so a trained Guardian can identify and categorize risk.

<a id="tang2025riskknowledge"></a>

### LM agents may fail to act on their own risk knowledge

Tang et al., 2025 · Second conference on language modeling · [Paper](https://openreview.net/forum?id=OeYdS51k8F)

**Discussion topics:** Locating Control and Recovery Boundaries.

**Engineering approach:** Abstract a proposed action and its context, critique risk, and request revision.

<a id="lin2026supervisoragent"></a>

### Stop wasting your tokens: Towards efficient runtime multi-agent systems

Lin et al., 2026 · International Conference on Learning Representations · [Paper](https://openreview.net/pdf/aed934fd020d5d5137d1923e25b3393ee85fe1ca.pdf)

**Discussion topics:** Locating Control and Recovery Boundaries.

**Engineering approach:** Use lightweight triggers to request context-dependent correction or verification.

<a id="yu2026operationalhallucination"></a>

### Operational hallucination and safety drift in AI agents

Yu et al., 2026 · Preprint / author manuscript · [Paper](https://doi.org/10.48550/arXiv.2607.18366)

**Discussion topics:** Locating Control and Recovery Boundaries.

<a id="qi2026llmascode"></a>

### LLM-as-Code: Agentic programming for agent harness

Qi et al., 2026 · Preprint / author manuscript · [Paper](https://arxiv.org/abs/2606.15874v2)

**Discussion topics:** Locating Control and Recovery Boundaries.

<a id="benkhaled2026g2cp"></a>

### G2CP: A graph-grounded communication protocol for verifiable and efficient multi-agent reasoning

Ben Khaled et al., 2026 · Proceedings of the 25th international conference on autonomous agents and multiagent systems · [Paper](https://doi.org/10.65109/JHFW8307)

**Discussion topics:** Locating Control and Recovery Boundaries.

<a id="mao2025semap"></a>

### Towards engineering multi-agent LLMs: A protocol-driven approach

Mao et al., 2025 · Preprint / author manuscript · [Paper](https://doi.org/10.48550/arXiv.2510.12120)

**Discussion topics:** Locating Control and Recovery Boundaries.

**Engineering approach:** Combine typed messages, behavioral contracts, and checked task-state transitions.

<a id="chang2025sagallm"></a>

### SagaLLM: Context management, validation, and transaction guarantees for multi-agent LLM planning

Chang et al., 2025 · Proceedings of the VLDB Endowment · [Paper](https://doi.org/10.14778/3750601.3750611)

**Discussion topics:** Locating Control and Recovery Boundaries.

**Engineering approach:** Preserve dependencies, validate before commitment, and associate effects with recovery actions.

<a id="zheng2026acrfence"></a>

### ACRFence: Preventing semantic rollback attacks in agent checkpoint-restore

Zheng et al., 2026 · Preprint / author manuscript · [Paper](https://doi.org/10.48550/arXiv.2603.20625)

**Discussion topics:** Locating Control and Recovery Boundaries.

**Engineering approach:** Use a proposed effect log and semantic comparison to distinguish replay from an explicit fork.
