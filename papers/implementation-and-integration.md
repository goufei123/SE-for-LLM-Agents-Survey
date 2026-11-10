# Implementation and Integration

实现与集成 · [Survey home](../README.md) · [Current manuscript](../paper/survey.pdf)

This reading guide follows the engineering problems, approaches, and representative studies in the current manuscript. A study can appear in more than one stage. Bibliographic metadata follows the manuscript snapshot.

## Topics discussed in the manuscript

- **From Specifications to Executable Integrations**: [Study, 2026](#washizaki2026swebok); [Wang et al., 2025](#wang2025openhandsplatform); [Li et al., 2025](#li2025encompass); [Amini et al., 2026](#amini2025agentspec); [Kuo et al., 2026](#kuo2026botender); [Bühler et al., 2026](#buehler2026agentbound); [Ouyang et al., 2026](#ouyang2026skcc); [Hasan et al., 2026](#hasan2026mcpsmells)
- **State and Data as Integration Artifacts**: [Study, 2026](#washizaki2026swebok); [Routray et al., 2026](#routray2026tieredchatbot); [Song et al., 2026](#song2026adp); [Park et al., 2025](#park2025workflowgraphs); [Jing et al., 2025](#jing2025mcip); [Cheng et al., 2026](#cheng2026agentgate); [Das et al., 2025](#das2025commandsans); [Xi et al., 2025](#xi2025agentgym)
- **Execution Efficiency and Representation Changes**: [Study, 2026](#washizaki2026swebok); [Zhang et al., 2025](#zhang2025apc); [Bai et al., 2026](#bai2026choreography); [Xiao et al., 2026](#xiao2026agentdiet); [Ye et al., 2025](#ye2025kvcomm); [Jeon et al., 2026](#jeon2026lragent); [Li et al., 2026](#li2026graphflow); [Xu et al., 2025](#xu2025nova); [Chung et al., 2026](#chung2026agentx); [Li et al., 2025](#li2025agentgit); [Ruan et al., 2026](#ruan2026cortex); [Zhong et al., 2026](#zhong2026dualspec); [Li et al., 2026](#li2026xgrammar2)
- **Enforcement, Recovery, and Integration Evidence**: [Study, 2026](#washizaki2026swebok); [Wan et al., 2026](#wan2026lco); [Ersoy et al., 2025](#ersoy2025darkpatterns); [Wen et al., 2026](#wen2026policyguard); [Nakash et al., 2025](#nakash2025craft); [Bühler et al., 2026](#buehler2026agentbound); [Perera et al., 2026](#perera2026rac); [Epperson et al., 2025](#epperson2025debugging); [Rafique et al., 2026](#rafique2026clawvm); [He et al., 2025](#he2025securityagents); [Xia et al., 2026](#xia2026tracefix); [Miao et al., 2026](#miao2026blindguard); [Nöther et al., 2026](#noether2026badacts); [Houde et al., 2025](#houde2025participation); [Wright et al., 2026](#wright2026altk); [Mayoral-Vilches et al., 2025](#mayoral2025caiinjection); [Jiang et al., 2026](#jiang2026chaincaps); [Oyelayo et al., 2026](#oyelayo2026mcpchallenges); [Lou et al., 2026](#lou2026autoharness); [Huang et al., 2026](#huang2026memoharness)

## Engineering problems and approaches

### Construction and integration

| Engineering problem | Approach | Key idea | Representative studies |
|---|---|---|---|
| Realizing executable behavior | Runtime construction | Build a session environment and expose shell, notebook, and browser actions through a runtime API. | [Wang et al., 2025](#wang2025openhandsplatform) |
| Realizing executable behavior | Programmable search abstraction | Compile workflow branchpoints into a search space while supplying search policy separately. | [Li et al., 2025](#li2025encompass) |
| Realizing executable behavior | Specification adapters | Instantiate a shared declarative Agent specification through framework-specific adapters. | [Amini et al., 2026](#amini2025agentspec) |
| Authoring deployable configurations | Participatory construction | Refine community proposals using interaction cases and deploy the resulting bot behavior. | [Kuo et al., 2026](#kuo2026botender) |
| Authoring deployable configurations | Typed skill compilation | Parse skill text into an intermediate representation, check it, and emit target-specific artifacts. | [Ouyang et al., 2026](#ouyang2026skcc) |
| Integrating state and data | Managed persistence and retrieval | Reconcile versioned facts and connect storage, retrieval, and context assembly to Agent execution. | [Routray et al., 2026](#routray2026tieredchatbot) |
| Integrating state and data | Schema-based data adaptation | Normalize source trajectories, convert them for target harnesses, and validate their structure. | [Song et al., 2026](#song2026adp) |
| Integrating state and data | Empirical integration analysis | Examine reference-server issues and linked fixes to identify recurring interface and implementation problems. | [Oyelayo et al., 2026](#oyelayo2026mcpchallenges) |

### Execution implementation

| Engineering problem | Approach | Key idea | Representative studies |
|---|---|---|---|
| Reducing repeated computation | Plan reuse | Retrieve successful plan templates and adapt cache hits to the current execution context. | [Zhang et al., 2025](#zhang2025apc) |
| Reducing repeated computation | Shared message encodings | Reuse global KV-cache representations through separate prefill and decode operations. | [Bai et al., 2026](#bai2026choreography) |
| Reducing repeated computation | Context-adjusted cache reuse | Estimate prefix-dependent offsets from online anchors, with dense-prefill fallback. | [Ye et al., 2025](#ye2025kvcomm) |
| Reducing repeated computation | Adapter-aware cache sharing | Share base caches and retain low-rank adapter contributions during attention computation. | [Jeon et al., 2026](#jeon2026lragent) |
| Reducing repeated computation | History compression | Shorten selected trajectory steps using an external reflection procedure. | [Xiao et al., 2026](#xiao2026agentdiet) |
| Making tool interactions conform | Grammar-constrained decoding | Dispatch and cache grammars to constrain dynamically selected tool-call formats. | [Li et al., 2026](#li2026xgrammar2) |
| Making tool interactions conform | Invocation middleware | Check calls before execution, process returned information, and detect silent failures. | [Wright et al., 2026](#wright2026altk) |
| Enforcing authorized execution | Learned policy interception | Classify policy–trajectory compliance and use the decision to intercept actions. | [Wen et al., 2026](#wen2026policyguard) |
| Enforcing authorized execution | Resource permissions | Convert reviewed capability manifests into external filesystem, network, and environment restrictions. | [Bühler et al., 2026](#buehler2026agentbound) |
| Enforcing authorized execution | Dataflow authority tracking | Propagate sink-specific authority with values and restrict composed tool calls. | [Jiang et al., 2026](#jiang2026chaincaps) |
| Recovering partial execution | Effect-aware recovery | Record tool effects and choose retries, alternatives, or compensating operations. | [Perera et al., 2026](#perera2026rac) |

## Discussed studies (45)

<a id="washizaki2026swebok"></a>

### Guide to the software engineering body of knowledge (SWEBOK guide)

Study, 2026 · IEEE Computer Society · [Paper](https://ieeecs-media.computer.org/media/education/swebok/swebok-v4.pdf)

**Discussion topics:** From Specifications to Executable Integrations; State and Data as Integration Artifacts; Execution Efficiency and Representation Changes; Enforcement, Recovery, and Integration Evidence.

<a id="oyelayo2026mcpchallenges"></a>

### Developer challenges in the adoption of model context protocol in AI agent development

Oyelayo et al., 2026 · Proceedings of the 2026 7th international workshop on bots and agents in software engineering · [Paper](https://doi.org/10.1145/3786161.3788462)

**Discussion topics:** Enforcement, Recovery, and Integration Evidence.

**Engineering approach:** Examine reference-server issues and linked fixes to identify recurring interface and implementation problems.

<a id="wang2025openhandsplatform"></a>

### OpenHands: An open platform for AI software developers as generalist agents

Wang et al., 2025 · The thirteenth international conference on learning representations · [Paper](https://openreview.net/forum?id=OJd3ayDDoF)

**Discussion topics:** From Specifications to Executable Integrations.

**Engineering approach:** Build a session environment and expose shell, notebook, and browser actions through a runtime API.

<a id="li2025encompass"></a>

### EnCompass: Enhancing agent programming with search over program execution paths

Li et al., 2025 · Advances in neural information processing systems · [Paper](https://doi.org/10.52202/085713-3533)

**Discussion topics:** From Specifications to Executable Integrations.

**Engineering approach:** Compile workflow branchpoints into a search space while supplying search policy separately.

<a id="amini2025agentspec"></a>

### Open agent specification: Enabling cross-framework comparison of AI agents

Amini et al., 2026 · Proceedings of the ACM conference on AI and agentic systems · [Paper](https://doi.org/10.1145/3786335.3813130)

**Discussion topics:** From Specifications to Executable Integrations.

**Engineering approach:** Instantiate a shared declarative Agent specification through framework-specific adapters.

<a id="kuo2026botender"></a>

### Botender: Supporting communities in collaboratively designing AI agents through case-based provocations

Kuo et al., 2026 · Proceedings of the 2026 CHI conference on human factors in computing systems · [Paper](https://doi.org/10.1145/3772318.3790500)

**Discussion topics:** From Specifications to Executable Integrations.

**Engineering approach:** Refine community proposals using interaction cases and deploy the resulting bot behavior.

<a id="buehler2026agentbound"></a>

### AgentBound: Securing execution boundaries of AI agents

Bühler et al., 2026 · Proceedings of the ACM on Software Engineering · [Paper](https://doi.org/10.1145/3808103)

**Discussion topics:** From Specifications to Executable Integrations; Enforcement, Recovery, and Integration Evidence.

**Engineering approach:** Convert reviewed capability manifests into external filesystem, network, and environment restrictions.

<a id="ouyang2026skcc"></a>

### SkCC: Portable and secure skill compilation for cross-framework LLM agents

Ouyang et al., 2026 · Preprint / author manuscript · [Paper](https://arxiv.org/abs/2605.03353)

**Discussion topics:** From Specifications to Executable Integrations.

**Engineering approach:** Parse skill text into an intermediate representation, check it, and emit target-specific artifacts.

<a id="hasan2026mcpsmells"></a>

### Model context protocol (MCP) tool descriptions are smelly! Towards improving AI agent efficiency with augmented MCP tool descriptions

Hasan et al., 2026 · Preprint / author manuscript · [Paper](https://doi.org/10.48550/arXiv.2602.14878)

**Discussion topics:** From Specifications to Executable Integrations.

<a id="routray2026tieredchatbot"></a>

### An advanced AI chatbot with tiered memory, retrieval-augmented generation, and model context protocol integration

Routray et al., 2026 · International Journal of Pharmacy with Medical Sciences · [Paper](https://doi.org/10.64751/ijpams.2026.v6.n2(1).174)

**Discussion topics:** State and Data as Integration Artifacts.

**Engineering approach:** Reconcile versioned facts and connect storage, retrieval, and context assembly to Agent execution.

<a id="song2026adp"></a>

### Agent data protocol: Unifying datasets for diverse, effective fine-tuning of LLM agents

Song et al., 2026 · The fourteenth international conference on learning representations · [Paper](https://openreview.net/forum?id=tG6301ORHd)

**Discussion topics:** State and Data as Integration Artifacts.

**Engineering approach:** Normalize source trajectories, convert them for target harnesses, and validate their structure.

<a id="park2025workflowgraphs"></a>

### A practical approach for building production-grade conversational agents with workflow graphs

Park et al., 2025 · Proceedings of the 63rd annual meeting of the association for computational linguistics (volume 6: Industry track) · [Paper](https://doi.org/10.18653/v1/2025.acl-industry.107)

**Discussion topics:** State and Data as Integration Artifacts.

<a id="jing2025mcip"></a>

### MCIP: Protecting MCP safety via model contextual integrity protocol

Jing et al., 2025 · Proceedings of the 2025 conference on empirical methods in natural language processing · [Paper](https://doi.org/10.18653/v1/2025.emnlp-main.62)

**Discussion topics:** State and Data as Integration Artifacts.

<a id="cheng2026agentgate"></a>

### AgentGate: A lightweight structured routing engine for the internet of agents

Cheng et al., 2026 · Preprint / author manuscript · [Paper](https://arxiv.org/abs/2604.06696v1)

**Discussion topics:** State and Data as Integration Artifacts.

<a id="das2025commandsans"></a>

### CommandSans: Securing AI agents with surgical precision prompt sanitization

Das et al., 2025 · Preprint / author manuscript · [Paper](https://doi.org/10.48550/arXiv.2510.08829)

**Discussion topics:** State and Data as Integration Artifacts.

<a id="xi2025agentgym"></a>

### AgentGym: Evaluating and training large language model-based agents across diverse environments

Xi et al., 2025 · Proceedings of the 63rd annual meeting of the association for computational linguistics (volume 1: Long papers) · [Paper](https://doi.org/10.18653/v1/2025.acl-long.1355)

**Discussion topics:** State and Data as Integration Artifacts.

<a id="zhang2025apc"></a>

### Agentic plan caching: Test-time memory for fast and cost-efficient LLM agents

Zhang et al., 2025 · Advances in neural information processing systems · [Paper](https://doi.org/10.52202/085713-3451)

**Discussion topics:** Execution Efficiency and Representation Changes.

**Engineering approach:** Retrieve successful plan templates and adapt cache hits to the current execution context.

<a id="bai2026choreography"></a>

### Accelerating language model workflows with prompt choreography

Bai et al., 2026 · Transactions of the Association for Computational Linguistics · [Paper](https://doi.org/10.1162/tacl.a.643)

**Discussion topics:** Execution Efficiency and Representation Changes.

**Engineering approach:** Reuse global KV-cache representations through separate prefill and decode operations.

<a id="xiao2026agentdiet"></a>

### Reducing cost of LLM agents with trajectory reduction

Xiao et al., 2026 · Proceedings of the ACM on Software Engineering · [Paper](https://doi.org/10.1145/3797084)

**Discussion topics:** Execution Efficiency and Representation Changes.

**Engineering approach:** Shorten selected trajectory steps using an external reflection procedure.

<a id="ye2025kvcomm"></a>

### KVCOMM: Online cross-context KV-cache communication for efficient LLM-based multi-agent systems

Ye et al., 2025 · Advances in neural information processing systems · [Paper](https://doi.org/10.52202/085713-0605)

**Discussion topics:** Execution Efficiency and Representation Changes.

**Engineering approach:** Estimate prefix-dependent offsets from online anchors, with dense-prefill fallback.

<a id="jeon2026lragent"></a>

### LRAgent: Efficient KV cache sharing for multi-LoRA LLM agents

Jeon et al., 2026 · Preprint / author manuscript · [Paper](https://arxiv.org/abs/2602.01053v2)

**Discussion topics:** Execution Efficiency and Representation Changes.

**Engineering approach:** Share base caches and retain low-rank adapter contributions during attention computation.

<a id="li2026graphflow"></a>

### GraphFlow: A graph-based workflow management for efficient LLM-agent serving

Li et al., 2026 · Preprint / author manuscript · [Paper](https://doi.org/10.48550/arXiv.2605.22566)

**Discussion topics:** Execution Efficiency and Representation Changes.

<a id="xu2025nova"></a>

### Nova: Real-time agentic vision-language model serving with adaptive cross-stage parallelization

Xu et al., 2025 · 2025 IEEE real-time systems symposium (RTSS) · [Paper](https://doi.org/10.1109/RTSS66672.2025.00038)

**Discussion topics:** Execution Efficiency and Representation Changes.

<a id="chung2026agentx"></a>

### Agent-X: Full pipeline acceleration of on-device AI agents

Chung et al., 2026 · Proceedings of the 24th annual international conference on mobile systems, applications and services · [Paper](https://doi.org/10.1145/3745756.3809195)

**Discussion topics:** Execution Efficiency and Representation Changes.

<a id="li2025agentgit"></a>

### AgentGit: A version control framework for reliable and scalable LLM-powered multi-agent systems

Li et al., 2025 · Preprint / author manuscript · [Paper](https://doi.org/10.48550/arXiv.2511.00628)

**Discussion topics:** Execution Efficiency and Representation Changes.

<a id="ruan2026cortex"></a>

### Cortex: Achieving low-latency, cost-efficient remote data access for LLM via semantic-aware knowledge caching

Ruan et al., 2026 · 23rd USENIX symposium on networked systems design and implementation (NSDI 26) · [Paper](https://www.usenix.org/conference/nsdi26/presentation/ruan-cortex)

**Discussion topics:** Execution Efficiency and Representation Changes.

<a id="zhong2026dualspec"></a>

### DualSpec: Accelerating deep research agents via dual-process action speculation

Zhong et al., 2026 · Preprint / author manuscript · [Paper](https://doi.org/10.48550/arXiv.2603.07416)

**Discussion topics:** Execution Efficiency and Representation Changes.

<a id="li2026xgrammar2"></a>

### XGrammar-2: Dynamic and efficient structured generation engine for agentic LLMs

Li et al., 2026 · Proceedings of the ACM conference on AI and agentic systems · [Paper](https://doi.org/10.1145/3786335.3813124)

**Discussion topics:** Execution Efficiency and Representation Changes.

**Engineering approach:** Dispatch and cache grammars to constrain dynamically selected tool-call formats.

<a id="wright2026altk"></a>

### Agent lifecycle toolkit (ALTK): Reusable middleware components for robust AI agents

Wright et al., 2026 · Proceedings of the ACM conference on AI and agentic systems · [Paper](https://doi.org/10.1145/3786335.3813206)

**Discussion topics:** Enforcement, Recovery, and Integration Evidence.

**Engineering approach:** Check calls before execution, process returned information, and detect silent failures.

<a id="wen2026policyguard"></a>

### Learning efficient guardrails for compliance

Wen et al., 2026 · Preprint / author manuscript · [Paper](https://arxiv.org/abs/2510.03485)

**Discussion topics:** Enforcement, Recovery, and Integration Evidence.

**Engineering approach:** Classify policy–trajectory compliance and use the decision to intercept actions.

<a id="jiang2026chaincaps"></a>

### ChainCaps: Composition-safe tool-using agents via monotonic capability attenuation

Jiang et al., 2026 · Preprint / author manuscript · [Paper](https://arxiv.org/abs/2605.26542v4)

**Discussion topics:** Enforcement, Recovery, and Integration Evidence.

**Engineering approach:** Propagate sink-specific authority with values and restrict composed tool calls.

<a id="perera2026rac"></a>

### Robust agent compensation (RAC): Teaching AI agents to compensate

Perera et al., 2026 · Proceedings of the ACM conference on AI and agentic systems · [Paper](https://doi.org/10.1145/3786335.3813141)

**Discussion topics:** Enforcement, Recovery, and Integration Evidence.

**Engineering approach:** Record tool effects and choose retries, alternatives, or compensating operations.

<a id="wan2026lco"></a>

### LCO: LLM-based constraint optimization for safer agentic LLMs in real-world tasks

Wan et al., 2026 · Findings of the association for computational linguistics: ACL 2026 · [Paper](https://doi.org/10.18653/v1/2026.findings-acl.1390)

**Discussion topics:** Enforcement, Recovery, and Integration Evidence.

<a id="ersoy2025darkpatterns"></a>

### Investigating the impact of dark patterns on LLM-based web agents

Ersoy et al., 2025 · Preprint / author manuscript · [Paper](https://arxiv.org/abs/2510.18113v1)

**Discussion topics:** Enforcement, Recovery, and Integration Evidence.

<a id="nakash2025craft"></a>

### Effective red-teaming of policy-adherent agents

Nakash et al., 2025 · Preprint / author manuscript · [Paper](https://arxiv.org/abs/2506.09600v3)

**Discussion topics:** Enforcement, Recovery, and Integration Evidence.

<a id="epperson2025debugging"></a>

### Interactive debugging and steering of multi-agent AI systems

Epperson et al., 2025 · Proceedings of the 2025 CHI conference on human factors in computing systems · [Paper](https://doi.org/10.1145/3706598.3713581)

**Discussion topics:** Enforcement, Recovery, and Integration Evidence.

<a id="rafique2026clawvm"></a>

### ClawVM: Harness-managed virtual memory for stateful tool-using LLM agents

Rafique et al., 2026 · Proceedings of the sixth european workshop on machine learning and systems · [Paper](https://doi.org/10.1145/3805621.3807648)

**Discussion topics:** Enforcement, Recovery, and Integration Evidence.

<a id="he2025securityagents"></a>

### Security of AI agents

He et al., 2025 · 2025 IEEE/ACM international workshop on responsible AI engineering (RAIE) · [Paper](https://doi.org/10.1109/RAIE66699.2025.00013)

**Discussion topics:** Enforcement, Recovery, and Integration Evidence.

<a id="xia2026tracefix"></a>

### TraceFix: Repairing agent coordination protocols with TLA+ counterexamples

Xia et al., 2026 · Proceedings of the ACM conference on AI and agentic systems · [Paper](https://doi.org/10.1145/3786335.3813159)

**Discussion topics:** Enforcement, Recovery, and Integration Evidence.

<a id="miao2026blindguard"></a>

### BlindGuard: Safeguarding LLM-based multi-agent systems under unknown attacks

Miao et al., 2026 · Preprint / author manuscript · [Paper](https://doi.org/10.48550/arXiv.2508.08127)

**Discussion topics:** Enforcement, Recovery, and Integration Evidence.

<a id="noether2026badacts"></a>

### Benchmarking the robustness of agentic systems to adversarially-induced harms

Nöther et al., 2026 · Preprint / author manuscript · [Paper](https://doi.org/10.48550/arXiv.2508.16481)

**Discussion topics:** Enforcement, Recovery, and Integration Evidence.

<a id="houde2025participation"></a>

### Controlling AI agent participation in group conversations: A human-centered approach

Houde et al., 2025 · Proceedings of the 30th international conference on intelligent user interfaces · [Paper](https://doi.org/10.1145/3708359.3712089)

**Discussion topics:** Enforcement, Recovery, and Integration Evidence.

<a id="mayoral2025caiinjection"></a>

### Cybersecurity AI: Hacking the AI hackers via prompt injection

Mayoral-Vilches et al., 2025 · Preprint / author manuscript · [Paper](https://doi.org/10.48550/arXiv.2508.21669)

**Discussion topics:** Enforcement, Recovery, and Integration Evidence.

<a id="lou2026autoharness"></a>

### AutoHarness: Improving LLM agents by automatically synthesizing a code harness

Lou et al., 2026 · Preprint / author manuscript · [Paper](https://arxiv.org/abs/2603.03329v1)

**Discussion topics:** Enforcement, Recovery, and Integration Evidence.

<a id="huang2026memoharness"></a>

### MemoHarness: Agent harnesses that learn from experience

Huang et al., 2026 · Preprint / author manuscript · [Paper](https://arxiv.org/abs/2607.14159v1)

**Discussion topics:** Enforcement, Recovery, and Integration Evidence.
