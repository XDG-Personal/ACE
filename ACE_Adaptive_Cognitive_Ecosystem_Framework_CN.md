# ACE：Adaptive Cognitive Ecosystem

## 自适应认知生态系统------完整框架构想

> 版本：Concept Draft v0.1\
> 日期：2026-09-10

## 1. 定义与目标

ACE 不是替代 LLM
的新模型，而是一种以**系统问题求解能力**为核心的开放式认知架构。LLM、小模型、算法、数据库、知识图谱、搜索、仿真器、工具、API、现实设备乃至人类，都可以成为系统中的异构认知资源。

核心假设：**智能不一定必须实例化在单一模型中；一般问题求解能力可能是异构认知资源在共享环境中持续组织、竞争、合作、行动、学习和演化后产生的系统属性。**

ACE 不首先追求"个体 Agent
有多聪明"，而关注系统能否解决问题、消耗多少资源、经验是否降低边际认知成本、新领域加入后旧能力是否保持，以及能否处理长期开放式任务。

``` text
J = V(solution) - λ1·C_compute - λ2·C_time - λ3·C_money - λ4·C_risk
Efficiency = Useful Problems Solved / Total Resource Cost
Experience ↑  ⇒  Marginal Cognitive Cost ↓
```

## 2. 从"大模型"到"大系统"

传统路线把知识、概念、推理和语言能力主要压缩进 Large Model θ。ACE
不否定这一路线，而是将 LLM 作为高价值的通用认知组件纳入更大的系统：

``` text
Problem / Goal
      ↓
Adaptive Cognitive Ecosystem
      ↓
Heterogeneous Cognitive Resources
      ↓
Competition + Cooperation + Action + Verification
      ↓
Hypothesis / Solution Emergence
      ↓
Persistent Knowledge + System Evolution
```

因此 `LLM ∈ ACE`，而不是 `ACE = LLM`。LLM
更适合成为高通用、高成本的认知器官、教师和新能力孵化器。

## 3. ACE 与 MoE / 普通 Agent 的区别

传统 MoE 是 `Input → Router → Top-K Neural Experts → Output`。ACE 的
Expert 可以是 LLM、Tiny LLM、小型神经网络、视觉模型、数学求解器、OpenCV
算法、数据库、搜索、知识图谱、规则系统、Fuzzy
System、物理仿真器、Python/C++ 程序、API、外部服务、现实设备或人类专家。

统一接口可抽象为：

``` text
Expert(Input, Context)
  → Claim / Action / Observation
  + Confidence + Membership
  + Estimated Cost + Evidence + Provenance
```

因此 `Expert ≠ LLM`、`Expert ≠ Agent`、`Expert ≠ Thread`。OpenClaw 一类
Agent Runtime 可以整体成为 ACE 中的高级 Thinker/Actor，而 ACE
上层仍存在认知市场、资源经济、知识沉淀和种群演化。

## 4. 理论定位：复杂适应系统

ACE 可受到混沌、生态、市场和社会系统启发，但更准确的理论定位是 **Complex
Adaptive System（复杂适应系统，CAS）**。

``` text
S(t+1) = F(S(t), Problem(t), Environment(t))
```

F 不是固定
Transformer，而是大量局部实体交互形成的宏观动力学。关键性质包括去中心化、异步、局部信息、通信延迟、竞争与合作、资源稀缺、生态位、出生/休眠/死亡、变异与组合、知识传承和宏观能力涌现。

## 5. 系统基本对象

``` text
ACE = (E, H, K, W, R, F, A, M)
```

-   **E --- Experts**：动态认知实体；
-   **H --- Hypotheses**：竞争、修正和组合的假设；
-   **K --- Knowledge**：独立于 Expert 生命周期的持久知识；
-   **W --- Workspace / World**：共享认知空间及外部环境；
-   **R --- Relations**：实体、概念、证据之间的关系；
-   **F --- Fitness Dynamics**：资源、信誉和长期适应度；
-   **A --- Actions**：对数字或现实环境的动作；
-   **M --- Memory**：经验、轨迹、事件和历史状态。

## 6. 动态角色

角色不是固定类型：`Role = f(Expert, Problem, Context)`。

**Thinker**：提出假设、分析、预测、规划、解释和跨领域组合，LLM
特别适合这一角色。\
**Actor**：调用
API、运行程序、查询数据库、控制设备、执行实验并取得真实反馈，形成
`Think → Act → Observe → Update`。\
**Critic**：寻找反例、验证证据、挑战假设、检查约束。\
**Archivist**：决定什么值得进入长期知识层，管理
provenance、版本和知识污染。

## 7. Hypothesis Population

ACE 中真正竞争的不只是 Expert，也包括 Hypothesis。Expert
可以支持、反驳、修正、组合假设，或请求 Actor
实验。最终答案通过证据、验证、成本和竞争逐渐形成 dominant hypothesis /
attractor，而不是简单投票。

``` text
H1 ───┐
      ├── H7 ──┐
H2 ───┘        ├── H12
H3 ─── H8 ─────┘
```

## 8. Cognitive Marketplace：认知市场

问题被发布为 `P={goal, context, constraints, reward, risk}`。候选 Expert
根据 Interest、Capability、Confidence、Cost、Risk、Reputation、Reward 和
Energy 决定是否参与。

``` text
Central Router → Expert
```

转变为：

``` text
Problem Publication → Cheap Candidate Discovery
                    → Distributed Competition / Cooperation
                    → Resource Allocation
```

可将其理解为 `Attention ≈ Resource Allocation`。ANN/HNSW
等只负责廉价候选发现，相当于"电话簿"，而不是中央智能 Router。

## 9. Energy、Reputation 与 Fitness

简单"生命倒计时"可发展为三层机制。

### Energy：短期代谢资源

``` text
Energy(t+1) = Energy(t) - Metabolism - ComputeCost
            - CommunicationCost - ActionCost + Reward
```

Energy 可直接映射 GPU/CPU 时间、API
成本、等待时间和现实行动成本。对所有问题都调用昂贵 Frontier LLM
的个体会快速耗尽资源。

### Reputation：上下文相关可信度

``` text
Reliability(E | LowLight) = .32
Reliability(E | Daylight) = .96
```

### Fitness：长期进化适应度

决定 Expert 是否获得资源、繁殖、休眠或淘汰：

``` text
Energy     → short-term viability
Reputation → credibility
Fitness    → long-term survival
```

低频高价值 Expert 应允许 Dormant，代谢成本接近零。

## 10. 信息延迟与局部认知

ACE
不要求全局同步：`State_i(t) ≠ State_j(t)`。延迟和局部信息可能促进独立探索、多样性和专业化，但也可能导致信息垄断、串谋和延迟套利。因此系统需要区分
Public Knowledge 与 Private/Local Knowledge，并奖励高价值信息共享。

## 11. 模糊数学与证据表达

ACE 不是"模糊系统"，但模糊数学适合作为实体之间的部分交流语言：

``` text
μ_E(P)   Expert 对问题的适配程度
μ_E(H)   Expert 对假设的支持程度
μ_C(E)   Expert 属于某生态位/概念的程度
```

一个 Expert 可同时 `μ_Vision=.80`、`μ_Physics=.50`，比固定
`ExpertType=Vision` 更适合动态生态。证据融合还可结合 Bayesian
inference、Possibility Theory、Evidence Theory、Prediction Market 和
Causal Attribution。

## 12. 专业化与生态位涌现

ACE 不希望人工定义所有领域。长期竞争可能形成
Perception、Geometry、Motion、Physics、Programming、Verification 等
Cluster。理想目标是：

``` text
Domain = Emergent Expert Cluster
```

而不是 `Domain = Programmer-defined Category`。

## 13. Expert 的出生、组合、变异与死亡

当系统发现重复未解决问题或反复出现的昂贵推理模式时：

``` text
Repeated / Novel Pattern
      ↓
Collect Successful Trajectories
      ↓
Generate Candidate Expert
      ↓
Training / Distillation / Compilation
      ↓
Validation → Register
```

同领域组合用于提高适应度；跨领域组合可能形成新能力，例如
`Motion × Geometry → Trajectory`、`Vision × Thermal Physics → Thermal Vision`。

Expert Genome 可包括
Architecture、BaseModel、Adapter、Tools、Rules、Prompt、KnowledgeRefs、Hyperparameters。Mutation
修改其中一部分，再由环境选择。

Expert 可以死亡，但：

``` text
Expert → temporary
Knowledge → persistent
```

## 14. Knowledge Sedimentation：知识沉淀

ACE 必须把"谁知道"与"系统知道什么"分开：

``` text
Experts / Hypotheses / Problems
          ↓
   Knowledge Sediment
          ↓
Facts + Relations + Procedures
+ Experience + Evidence + Provenance
```

核心原则：**Agent is disposable; validated knowledge and system
capability are persistent.** 替换 LLM 版本不应造成系统失忆。

## 15. Cognitive Compilation：认知编译

这是 ACE 最关键的资源效率机制之一：

``` text
Expensive LLM Reasoning
        ↓
Repeated Successful Pattern
        ↓
Distillation / Compilation
        ↓
Small Expert
        ↓
Rule / Algorithm / Cache
```

理想成本曲线：

``` text
1st       Frontier LLM      cost 1000
10th      General LLM       cost 200
100th     Small Expert      cost 10
1000th    Algorithm/Cache   cost 0.1
```

即 `Reasoning → Experience → Knowledge → Skill → Cheap Expert`。LLM
因而成为 Teacher / Bootstrapping Engine / Capability Incubator。

## 16. Cognitive Escalation：最小充分认知

``` text
Tier 0  Cache / deterministic rule
Tier 1  Algorithmic Expert
Tier 2  Small NN / Tiny Model
Tier 3  Specialist Small LLM
Tier 4  General LLM
Tier 5  Frontier LLM / Multi-agent / Real-world Experiment
```

核心原则：**Minimum Sufficient
Cognition------只使用完成任务所需的最低充分认知资源。**

## 17. Credit Assignment

这是 ACE 最关键的问题之一：

``` text
Problem → Thinker A → Hypothesis → Thinker B → Planner C
        → Actor D → Sensor E → Outcome
```

最终成功后，奖励如何分配将直接决定生态演化方向。因此需要 Provenance
Graph，并研究 delayed reward、causal contribution、counterfactual
evaluation、Shapley-like attribution、prediction market 和 outcome-based
settlement。奖励应针对实际因果贡献，而不是"参与过"。

## 18. 防止奖励投机与生态退化

只要存在奖励，就可能出现 reward
hacking、只做简单任务、迎合多数意见、串谋、信息垄断、free
rider、reputation manipulation 和 resource
hoarding。因此不能使用单一"生命值"作为最终目标。

系统需要多来源评价、独立
Critic、真实环境反馈、风险成本、延迟结算、反事实验证、资源上限、多样性保护和休眠机制。

> 进化只能保证"适应规则"，不能保证自动产生真理或智能。因此**生态规则本身就是
> ACE 的核心算法**。

## 19. World Model 与 Concept Formation

如果 ACE 要走向更一般的问题求解能力，至少需要：

**World Model**：学习 `P(S_{t+1}|S_t,A_t)`，即"如果做
X，会发生什么"，而不仅是 `P(answer|question)`。

**Automatic Concept Formation**：

``` text
Observation → Novelty / Compression Opportunity
            → Concept Formation
            → New Expert / Relation / Skill
```

否则系统仍依赖人工 ontology。这可能是 ACE
最困难、也最有研究价值的方向之一。

## 20. 三个时间尺度

``` text
Fast   Thinking:  Experts ↔ Hypotheses ↔ Actions
Medium Learning:  Expert/Knowledge/Reputation/Relation update
Slow   Evolution: Population_t → Selection/Reproduction/Mutation → Population_t+1
```

即：`Thinking ⊂ Learning ⊂ Evolution`。

## 21. 当前硬件上的实现原则

ACE 的可扩展性依赖**稀疏、事件驱动、按需激活**，而不是让所有 Expert
常驻运行：

``` text
100,000 registered experts
        ↓
100 candidates
        ↓
10 bids
        ↓
3–10 active experts
        ↓
0–1 expensive LLM call
```

Expert Registry 只保存
ID、Capabilities、Cost、Reliability、Embedding、Dependencies、State、Location
等元数据。

``` text
100,000 logical entities
        ↓
event queue
        ↓
8–32 workers
```

因此 `Agent ≠ Thread`。第一版不需要 Kubernetes；单进程 Runtime + Event
Bus + Worker Pool 即可验证核心机制。

## 22. 推荐运行时结构

``` text
┌─────────────────────────────────────┐
│              ACE Runtime            │
│  Problem / Goal Interface           │
│  Cognitive Marketplace              │
│  Event Bus / Shared Workspace       │
│  Expert Registry                    │
│  Hypothesis Store                   │
│  Knowledge / Memory Store           │
│  Reputation / Energy / Fitness      │
│  Credit Assignment                  │
│  Evolution Manager                  │
│  Cognitive Compiler                 │
│                                     │
│  Experts:                           │
│   Algorithms / Small Models / LLMs  │
│   Agent Runtime (e.g. OpenClaw)     │
│   Tools / APIs / DB / Search        │
│   Simulators / Physical Actors      │
└─────────────────────────────────────┘
```

## 23. 最小可行实验（MVP）

第一阶段不应依赖大量 LLM，建议先用几十到几百个简单实体测试动力学。

1.  **Sparse Activation**：注册大量
    Expert，验证单任务激活数保持很小，延迟不随总数线性增长。
2.  **Resource Efficiency**：与普通 LLM Agent 比较 Tokens/problem、GPU
    seconds/problem、Wall time/problem、Money/problem、Success rate。
3.  **Experience Amortization**：验证 `Cost(P,t) ↓ as Experience(t) ↑`。
4.  **Continual Capability**：持续加入新领域，观察旧领域性能是否保持。
5.  **Emergent Specialization**：不预定义 Math/Vision
    等固定类型，观察是否自行形成稳定生态位。
6.  **Think--Act--Learn**：在可验证模拟环境中观察 Actor
    反馈是否能更新知识、信誉和策略。
7.  **Cognitive Compilation**：验证昂贵 LLM 轨迹能否被蒸馏/编译成廉价
    Expert。
8.  **Ecological
    Stability**：观察是否出现垄断、串谋、投机、生态崩溃及恢复机制。

## 24. 与当前 LLM Agent 的核心对照实验

给传统 LLM Agent 和 ACE
**相同模型、工具和总资源预算**，运行重复、多领域和长期任务。

关注：

``` text
Success rate
Total compute
Total tokens
Wall-clock time
Cost per solved problem
Old-task retention
New-domain acquisition cost
Cost reduction with experience
```

ACE 最关键的成功信号不是第一次比大型 LLM 更聪明，而是：

``` text
Experience ↑
Capability ↑
Cost / Problem ↓
```

## 25. AGI 的位置

AGI 可以作为远期目标，但不应成为近期验证标准。

ACE 更基础的研究假设是：

> **AGI need not be instantiated in a single model.**

更进一步：

``` text
General Intelligence = Emergent Property(
  Diverse Specialists,
  Shared World,
  Competition,
  Cooperation,
  Action,
  Memory,
  Knowledge,
  Evolution
)
```

即一般智能可能存在于系统动力学中，而不是任何一个个体模型中。

## 26. 当前最重要的开放问题

1.  **Credit Assignment**：怎样正确奖励真正产生因果贡献的实体？
2.  **Concept Formation**：系统如何自行发现值得形成的新概念？
3.  **World Model**：怎样形成跨 Expert 的统一因果世界模型？
4.  **Knowledge Validation**：什么知识可以沉淀，如何处理冲突与版本？
5.  **Cognitive Compilation**：何时把昂贵推理编译成廉价技能？
6.  **Ecological Stability**：怎样防止垄断、串谋、寄生和奖励投机？
7.  **Diversity vs Convergence**：如何既收敛到答案又保持探索多样性？
8.  **Expert Discovery**：怎样在海量 Expert 中廉价发现候选？
9.  **Open-ended Evolution**：如何让系统长期成长而不是陷入局部最优？
10. **Safety / Governance**：当 Actor
    能影响现实环境时，哪些动作必须受系统外约束？

## 27. ACE 的工程原则

-   **System over Agent**：评价系统，不迷信个体智能。
-   **Sparse over Dense**：总能力可以巨大，单次激活必须稀疏。
-   **Explicit Knowledge over Repeated
    Reasoning**：能沉淀的知识不重复支付推理成本。
-   **Action and Verification over Verbal
    Consensus**：现实反馈优先于语言自洽。
-   **Local Adaptation over Global
    Retraining**：尽量局部更新，不整体重训。
-   **Minimum Sufficient Cognition**：使用最低充分认知资源。
-   **Knowledge Survives Agents**：个体可替换，知识和系统能力持续存在。
-   **Evolution with
    Governance**：允许演化，但生态规则和现实动作必须受约束。

## 28. 一句话定义

> **ACE
> 是一个以问题求解效率为目标、由异构认知实体组成的复杂适应系统；实体通过竞争、合作、行动、验证、资源经济、知识沉淀和持续演化，使系统能力在长期运行中增长，并尝试让单位问题的边际认知成本随经验持续下降。**

## 29. 最核心的可证伪命题

ACE 是否值得继续研究，最终可以归结为一个非常具体的问题：

``` text
在相同或更低的长期资源预算下，
一个允许知识沉淀、技能编译、异构专家竞争合作和结构演化的系统，
能否比固定 LLM / 传统 Agent 系统解决更多、更长期、更开放的问题？
```

如果答案是否定的，ACE 只是复杂的调度系统；如果答案是肯定的，并且出现：

``` text
Experience ↑  ⇒  Capability ↑ and Cost/problem ↓
```

那么它就代表一种不同于单纯参数 Scaling 的认知系统扩展路径。
