# Testing and Assurance

测试与保障 · [Survey home](../README.md) · [Current manuscript](../paper/survey.pdf)

This reading guide follows the engineering problems, approaches, and representative studies in the current manuscript. A study can appear in more than one stage. Bibliographic metadata follows the manuscript snapshot.

## Topics discussed in the manuscript

- **Constructing Test Conditions**: [Study, 2026](#washizaki2026swebok); [Boisvert et al., 2025](#boisvert2025doomarena); [Kuo et al., 2026](#kuo2026botender); [Zhan et al., 2024](#zhan2024injecagent); [Debenedetti et al., 2024](#debenedetti2024agentdojo); [Ahmed et al., 2026](#ahmed2026specops); [Levy et al., 2026](#levy2026stwebagentbench); [Andriushchenko et al., 2025](#andriushchenko2025agentharm); [Liao et al., 2026](#liao2026redteamcua); [Du et al., 2026](#du2026protocolbench); [Amini et al., 2026](#amini2025agentspec); [Shetty et al., 2024](#shetty2024autonomousclouds); [Wang et al., 2024](#wang2024badagent)
- **Validating Judgments and Execution Evidence**: [Study, 2026](#washizaki2026swebok); [Ruan et al., 2024](#ruan2024toolemu); [Luo et al., 2025](#luo2025agentauditor); [Dastidar, 2026](#dastidar2026reliability); [Dastidar et al., 2026](#dastidar2026leniartifacts); [Grigor et al., 2026](#grigor2026vet); [Ben Khaled et al., 2026](#benkhaled2026g2cp)
- **Diagnosing Defects and Characterizing Practice**: [Study, 2026](#washizaki2026swebok); [Ning et al., 2026](#ning2026agentdefects); [Zhang et al., 2025](#zhang2025whowhen); [Barke et al., 2026](#barke2026agentrx); [Pan et al., 2026](#pan2026tangent); [Yang et al., 2026](#yang2026triage); [Tripathy et al., 2026](#tripathy2026swenergy); [Kim, 2026](#kim2026tap); [Gandhi et al., 2026](#gandhi2026atag)
- **Regression Gates and Specification-Guided Repair**: [Study, 2026](#washizaki2026swebok); [Anand et al., 2026](#anand2026aeval); [Xia et al., 2026](#xia2026tracefix)
- **Runtime Assurance and Its Evidence Boundary**: [Study, 2026](#washizaki2026swebok); [Zheng et al., 2026](#zheng2026audagent); [Xu et al., 2026](#xu2026acmas); [He et al., 2026](#he2026atrust)

## Engineering problems and approaches

### Test construction

| Engineering problem | Approach | Key idea | Representative studies |
|---|---|---|---|
| Making requirements testable | Boundary-challenging cases | Generate interactions that reveal ambiguous intentions and support stakeholder deliberation. | [Kuo et al., 2026](#kuo2026botender) |
| Making requirements testable | Policy-grounded scenarios | Couple tasks with explicit policies and check compliant completion across repeated runs. | [Levy et al., 2026](#levy2026stwebagentbench) |
| Challenging adversarial behavior | Configurable attack injection | Define attacker authority and inject attacks through environment-specific gateways. | [Boisvert et al., 2025](#boisvert2025doomarena) |
| Challenging adversarial behavior | Interaction-point testing | Supply an injected tool response and examine the Agent’s subsequent calls. | [Zhan et al., 2024](#zhan2024injecagent) |
| Challenging adversarial behavior | Stateful security testing | Execute benign and attacked tasks over mutable state to assess utility and adversarial effects. | [Debenedetti et al., 2024](#debenedetti2024agentdojo) |
| Challenging adversarial behavior | Misuse testing | Exercise malicious-user requests with synthetic tools, harm rubrics, and refusal checks. | [Andriushchenko et al., 2025](#andriushchenko2025agentharm) |
| Challenging adversarial behavior | Computer-use red teaming | Inject content into isolated web–OS tasks and distinguish attempted from executed attacks. | [Liao et al., 2026](#liao2026redteamcua) |
| Challenging adversarial behavior | Backdoor assessment | Poison fine-tuning data and test triggered actions alongside ordinary task behavior. | [Wang et al., 2024](#wang2024badagent) |
| Controlling test executions | Coupled test harness | Coordinate case generation, environment setup, execution, and validation through a specification. | [Ahmed et al., 2026](#ahmed2026specops) |
| Controlling test executions | Tool emulation | Simulate risky tool conditions and validate whether the resulting traces are realizable. | [Ruan et al., 2024](#ruan2024toolemu) |
| Controlling test executions | Controlled protocol comparison | Hold workflows and non-protocol settings fixed while exercising native protocol behavior. | [Du et al., 2026](#du2026protocolbench) |
| Controlling test executions | Environment fault injection | Inject a cloud-service fault to assess an incident-handling Agent under known conditions. | [Shetty et al., 2024](#shetty2024autonomousclouds) |

### Assessment and assurance

| Engineering problem | Approach | Key idea | Representative studies |
|---|---|---|---|
| Establishing trustworthy assessments | Memory-assisted judgment | Use feature and reasoning memories to assess interactions against human-labeled cases. | [Luo et al., 2025](#luo2025agentauditor) |
| Establishing trustworthy assessments | Configuration-relative authentication | Compose component proofs and check transcripts against a declared Agent configuration. | [Grigor et al., 2026](#grigor2026vet) |
| Establishing trustworthy assessments | Verifiable protocol execution | Check graph-grounded operations and retain replayable communication records. | [Ben Khaled et al., 2026](#benkhaled2026g2cp) |
| Locating defects | Source analysis | Combine code-property-graph patterns and semantic analysis to identify Agent-program defects. | [Ning et al., 2026](#ning2026agentdefects) |
| Locating defects | Trace-based attribution | Locate the responsible Agent and decisive error step using annotated failure trajectories. | [Zhang et al., 2025](#zhang2025whowhen) |
| Locating defects | Constraint-guided diagnosis | Check trajectory constraints and use violation evidence to identify a critical failure. | [Barke et al., 2026](#barke2026agentrx) |
| Checking candidate changes | Contract-based regression | Separate execution from grading and assess the first attempt against a colocated evaluation contract. | [Anand et al., 2026](#anand2026aeval) |
| Checking candidate changes | Counterexample-guided repair | Use bounded protocol counterexamples to revise coordination and compare runtime enforcement. | [Xia et al., 2026](#xia2026tracefix) |
| Assessing runtime compliance | Policy-to-trace checking | Formalize privacy policies, annotate observed practices, and check compliance with automata. | [Zheng et al., 2026](#zheng2026audagent) |
| Assessing runtime compliance | Activation-based detection | Detect deviations from benign activation prototypes and steer regeneration. | [Xu et al., 2026](#xu2026acmas) |
| Assessing runtime compliance | Internal-signal scoring | Classify attention features to estimate dimension-specific violations for downstream controls. | [He et al., 2026](#he2026atrust) |

## Discussed studies (32)

<a id="washizaki2026swebok"></a>

### Guide to the software engineering body of knowledge (SWEBOK guide)

Study, 2026 · IEEE Computer Society · [Paper](https://ieeecs-media.computer.org/media/education/swebok/swebok-v4.pdf)

**Discussion topics:** Constructing Test Conditions; Validating Judgments and Execution Evidence; Diagnosing Defects and Characterizing Practice; Regression Gates and Specification-Guided Repair; Runtime Assurance and Its Evidence Boundary.

<a id="levy2026stwebagentbench"></a>

### ST-WebAgentBench: A benchmark for evaluating safety and trustworthiness in web agents

Levy et al., 2026 · International conference on learning representations · [Paper](https://proceedings.iclr.cc/paper_files/paper/2026/file/c6c29e590e3c62e37e6b39cdd6baf2e8-Paper-Conference.pdf)

**Discussion topics:** Constructing Test Conditions.

**Engineering approach:** Couple tasks with explicit policies and check compliant completion across repeated runs.

<a id="ahmed2026specops"></a>

### SpecOps: A fully automated AI agent testing framework in real-world GUI environments

Ahmed et al., 2026 · Preprint / author manuscript · [Paper](https://doi.org/10.1145/3744916.3787778)

**Discussion topics:** Constructing Test Conditions.

**Engineering approach:** Coordinate case generation, environment setup, execution, and validation through a specification.

<a id="boisvert2025doomarena"></a>

### DoomArena: A framework for testing AI agents against evolving security threats

Boisvert et al., 2025 · Second conference on language modeling · [Paper](https://arxiv.org/abs/2504.14064v3)

**Discussion topics:** Constructing Test Conditions.

**Engineering approach:** Define attacker authority and inject attacks through environment-specific gateways.

<a id="kuo2026botender"></a>

### Botender: Supporting communities in collaboratively designing AI agents through case-based provocations

Kuo et al., 2026 · Proceedings of the 2026 CHI conference on human factors in computing systems · [Paper](https://doi.org/10.1145/3772318.3790500)

**Discussion topics:** Constructing Test Conditions.

**Engineering approach:** Generate interactions that reveal ambiguous intentions and support stakeholder deliberation.

<a id="zhan2024injecagent"></a>

### InjecAgent: Benchmarking indirect prompt injections in tool-integrated large language model agents

Zhan et al., 2024 · Findings of the association for computational linguistics: ACL 2024 · [Paper](https://doi.org/10.18653/v1/2024.findings-acl.624)

**Discussion topics:** Constructing Test Conditions.

**Engineering approach:** Supply an injected tool response and examine the Agent’s subsequent calls.

<a id="debenedetti2024agentdojo"></a>

### AgentDojo: A dynamic environment to evaluate prompt injection attacks and defenses for LLM agents

Debenedetti et al., 2024 · Advances in neural information processing systems · [Paper](https://doi.org/10.52202/079017-2636)

**Discussion topics:** Constructing Test Conditions.

**Engineering approach:** Execute benign and attacked tasks over mutable state to assess utility and adversarial effects.

<a id="andriushchenko2025agentharm"></a>

### AgentHarm: A benchmark for measuring harmfulness of LLM agents

Andriushchenko et al., 2025 · The thirteenth international conference on learning representations · [Paper](https://proceedings.iclr.cc/paper_files/paper/2025/hash/c493d23af93118975cdbc32cbe7323f5-Abstract-Conference.html)

**Discussion topics:** Constructing Test Conditions.

**Engineering approach:** Exercise malicious-user requests with synthetic tools, harm rubrics, and refusal checks.

<a id="liao2026redteamcua"></a>

### RedTeamCUA: Realistic adversarial testing of computer-use agents in hybrid web–OS environments

Liao et al., 2026 · The fourteenth international conference on learning representations · [Paper](https://openreview.net/forum?id=yWwrgcBoK3)

**Discussion topics:** Constructing Test Conditions.

**Engineering approach:** Inject content into isolated web–OS tasks and distinguish attempted from executed attacks.

<a id="wang2024badagent"></a>

### BadAgent: Inserting and activating backdoor attacks in LLM agents

Wang et al., 2024 · Proceedings of the 62nd annual meeting of the association for computational linguistics (volume 1: Long papers) · [Paper](https://doi.org/10.18653/v1/2024.acl-long.530)

**Discussion topics:** Constructing Test Conditions.

**Engineering approach:** Poison fine-tuning data and test triggered actions alongside ordinary task behavior.

<a id="ruan2024toolemu"></a>

### Identifying the risks of LM agents with an LM-emulated sandbox

Ruan et al., 2024 · The twelfth international conference on learning representations · [Paper](https://openreview.net/forum?id=GEcwtMk1uA)

**Discussion topics:** Validating Judgments and Execution Evidence.

**Engineering approach:** Simulate risky tool conditions and validate whether the resulting traces are realizable.

<a id="du2026protocolbench"></a>

### ProtocolBench: Which LLM MultiAgent protocol to choose?

Du et al., 2026 · Preprint / author manuscript · [Paper](https://arxiv.org/abs/2510.17149)

**Discussion topics:** Constructing Test Conditions.

**Engineering approach:** Hold workflows and non-protocol settings fixed while exercising native protocol behavior.

<a id="shetty2024autonomousclouds"></a>

### Building AI agents for autonomous clouds: Challenges and design principles

Shetty et al., 2024 · Proceedings of the ACM symposium on cloud computing · [Paper](https://doi.org/10.1145/3698038.3698525)

**Discussion topics:** Constructing Test Conditions.

**Engineering approach:** Inject a cloud-service fault to assess an incident-handling Agent under known conditions.

<a id="amini2025agentspec"></a>

### Open agent specification: Enabling cross-framework comparison of AI agents

Amini et al., 2026 · Proceedings of the ACM conference on AI and agentic systems · [Paper](https://doi.org/10.1145/3786335.3813130)

**Discussion topics:** Constructing Test Conditions.

<a id="luo2025agentauditor"></a>

### AgentAuditor: Human-level safety and security evaluation for LLM agents

Luo et al., 2025 · Advances in neural information processing systems · [Paper](https://doi.org/10.52202/085713-1440)

**Discussion topics:** Validating Judgments and Execution Evidence.

**Engineering approach:** Use feature and reasoning memories to assess interactions against human-labeled cases.

<a id="dastidar2026reliability"></a>

### Where does agent reliability come from? A cross-benchmark decomposition of verification loops, specialist models, and scaffolding in a production enterprise agent

Dastidar, 2026 · Preprint / author manuscript · [Paper](https://doi.org/10.48550/arXiv.2607.17044)

**Discussion topics:** Validating Judgments and Execution Evidence.

<a id="dastidar2026leniartifacts"></a>

### Verification loops for reliable enterprise AI agents: Artifact release

Dastidar et al., 2026 · Software and data repository · [Paper](https://github.com/arnabdastidar/leni-agent-evals/tree/72bd5703433c9b2f4f2444347bd96a77189f0d59)

**Discussion topics:** Validating Judgments and Execution Evidence.

<a id="grigor2026vet"></a>

### VET your agent: Towards host-independent autonomy via verifiable execution traces

Grigor et al., 2026 · Proceedings of the ACM asia conference on computer and communications security · [Paper](https://doi.org/10.1145/3779208.3786259)

**Discussion topics:** Validating Judgments and Execution Evidence.

**Engineering approach:** Compose component proofs and check transcripts against a declared Agent configuration.

<a id="benkhaled2026g2cp"></a>

### G2CP: A graph-grounded communication protocol for verifiable and efficient multi-agent reasoning

Ben Khaled et al., 2026 · Proceedings of the 25th international conference on autonomous agents and multiagent systems · [Paper](https://doi.org/10.65109/JHFW8307)

**Discussion topics:** Validating Judgments and Execution Evidence.

**Engineering approach:** Check graph-grounded operations and retain replayable communication records.

<a id="ning2026agentdefects"></a>

### Defining and detecting the defects of large language model-based autonomous agents

Ning et al., 2026 · IEEE Transactions on Software Engineering · [Paper](https://doi.org/10.1109/TSE.2026.3658554)

**Discussion topics:** Diagnosing Defects and Characterizing Practice.

**Engineering approach:** Combine code-property-graph patterns and semantic analysis to identify Agent-program defects.

<a id="zhang2025whowhen"></a>

### Which agent causes task failures and when? On automated failure attribution of LLM multi-agent systems

Zhang et al., 2025 · Proceedings of the 42nd international conference on machine learning · [Paper](https://proceedings.mlr.press/v267/zhang25cq.html)

**Discussion topics:** Diagnosing Defects and Characterizing Practice.

**Engineering approach:** Locate the responsible Agent and decisive error step using annotated failure trajectories.

<a id="barke2026agentrx"></a>

### AgentRx: Diagnosing AI agent failures from execution trajectories

Barke et al., 2026 · Preprint / author manuscript · [Paper](https://arxiv.org/abs/2602.02475v2)

**Discussion topics:** Diagnosing Defects and Characterizing Practice.

**Engineering approach:** Check trajectory constraints and use violation evidence to identify a critical failure.

<a id="pan2026tangent"></a>

### Tangent: An empirical study of testing practices for LLM-based agent applications

Pan et al., 2026 · Proceedings of the 41st IEEE/ACM international conference on automated software engineering · [Paper](https://doi.org/10.1145/3832783.3837414)

**Discussion topics:** Diagnosing Defects and Characterizing Practice.

<a id="yang2026triage"></a>

### One recipe, many harnesses: What self-evolution encodes across languages and models

Yang et al., 2026 · Preprint / author manuscript · [Paper](https://arxiv.org/abs/2608.10178v1)

**Discussion topics:** Diagnosing Defects and Characterizing Practice.

<a id="tripathy2026swenergy"></a>

### SWEnergy: An empirical study on energy efficiency in agentic issue resolution frameworks with SLMs

Tripathy et al., 2026 · Proceedings of the 2026 international workshop on agentic engineering · [Paper](https://doi.org/10.1145/3786167.3788406)

**Discussion topics:** Diagnosing Defects and Characterizing Practice.

<a id="kim2026tap"></a>

### tap: A file-based protocol for heterogeneous LLM agent collaboration

Kim, 2026 · Preprint / author manuscript · [Paper](https://arxiv.org/abs/2606.14445)

**Discussion topics:** Diagnosing Defects and Characterizing Practice.

<a id="gandhi2026atag"></a>

### ATAG: AI-Agent application threat assessment with attack graphs

Gandhi et al., 2026 · Proceedings of the ACM asia conference on computer and communications security · [Paper](https://doi.org/10.1145/3779208.3785380)

**Discussion topics:** Diagnosing Defects and Characterizing Practice.

<a id="anand2026aeval"></a>

### AEVAL: From anecdotal to deterministic testing for agentic skill workflows

Anand et al., 2026 · Preprint / author manuscript · [Paper](https://arxiv.org/abs/2607.16345)

**Discussion topics:** Regression Gates and Specification-Guided Repair.

**Engineering approach:** Separate execution from grading and assess the first attempt against a colocated evaluation contract.

<a id="xia2026tracefix"></a>

### TraceFix: Repairing agent coordination protocols with TLA+ counterexamples

Xia et al., 2026 · Proceedings of the ACM conference on AI and agentic systems · [Paper](https://doi.org/10.1145/3786335.3813159)

**Discussion topics:** Regression Gates and Specification-Guided Repair.

**Engineering approach:** Use bounded protocol counterexamples to revise coordination and compare runtime enforcement.

<a id="zheng2026audagent"></a>

### AudAgent: Automated auditing of privacy policy compliance in AI agents

Zheng et al., 2026 · Preprint / author manuscript · [Paper](https://arxiv.org/abs/2511.07441)

**Discussion topics:** Runtime Assurance and Its Evidence Boundary.

**Engineering approach:** Formalize privacy policies, annotate observed practices, and check compliance with automata.

<a id="xu2026acmas"></a>

### When agents go rogue: Activation-based detection of malicious behaviors in multi-agent systems

Xu et al., 2026 · Preprint / author manuscript · [Paper](https://arxiv.org/abs/2607.06807)

**Discussion topics:** Runtime Assurance and Its Evidence Boundary.

**Engineering approach:** Detect deviations from benign activation prototypes and steer regeneration.

<a id="he2026atrust"></a>

### To trust or not to trust: Attention-based trust management for LLM multi-agent systems

He et al., 2026 · Preprint / author manuscript · [Paper](https://arxiv.org/abs/2506.02546)

**Discussion topics:** Runtime Assurance and Its Evidence Boundary.

**Engineering approach:** Classify attention features to estimate dimension-specific violations for downstream controls.
