---
layout: default
title: "Horizon Summary: 2026-05-07 (ZH)"
date: 2026-05-07
lang: zh
---

> From 36 items, 12 important content pieces were selected

---

1. [美国国会图书馆推荐 SQLite 用于数字保存](#item-1) ⭐️ 9.0/10
2. [英伟达、OpenAI、微软联合发布 MRC 协议提升 AI 集群效率](#item-2) ⭐️ 9.0/10
3. [月之暗面融资超 7 亿美元，估值破百亿，Kimi 收入飙升](#item-3) ⭐️ 9.0/10
4. [SGLang v0.5.11: 升级 CUDA 13、Torch 2.11、默认推测解码 V2](#item-4) ⭐️ 8.0/10
5. [Vibe coding 与 agentic engineering 趋同，引发担忧](#item-5) ⭐️ 8.0/10
6. [开发者认证迁移：Supabase → Clerk → Better Auth](#item-6) ⭐️ 8.0/10
7. [深度学习数学理论提出训练动态的解析跳跃](#item-7) ⭐️ 8.0/10
8. [Google Chrome 静默下载 4GB AI 模型引发隐私与法律争议](#item-8) ⭐️ 8.0/10
9. [欧盟拟强制移除华为中兴设备](#item-9) ⭐️ 8.0/10
10. [Anthropic 与 SpaceX 合作提升 Claude 算力](#item-10) ⭐️ 8.0/10
11. [苹果研发支出占比突破 10%，加速 AI 布局](#item-11) ⭐️ 8.0/10
12. [小米开源 OmniVoice：支持 646 种语言的语音克隆 TTS](#item-12) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [美国国会图书馆推荐 SQLite 用于数字保存](https://sqlite.org/locrsf.html) ⭐️ 9.0/10

美国国会图书馆正式推荐 SQLite 作为数字内容存储的首选格式，认可其适合长期保存。 这一来自重要文化机构的认可验证了 SQLite 的健壮性和可靠性，可能推动其在全球档案和保存系统中更广泛地采用。 该推荐属于美国国会图书馆数字格式可持续性计划的一部分，虽然最初发布于 2018 年，但截至 2026 年仍然有效。

hackernews · whatisabcdefgh · May 6, 21:58 · [社区讨论](https://news.ycombinator.com/item?id=48042434)

**背景**: SQLite 是一个自包含、无服务器、零配置的 SQL 数据库引擎，将数据存储在单个磁盘文件中。它广泛应用于应用程序、嵌入式系统，并越来越多地用于数据交换。美国国会图书馆评估数字格式的长期性、开放性和采用情况，以指导保存工作。

**社区讨论**: 社区评论展现了多元视角：有人称赞 SQLite 对大多数应用的可靠性和简洁性，也有人指出它对于简单任务可能过于复杂，或当个人身份信息容易被复制时存在安全风险。还有用户指出该推荐已有近八年历史。

**标签**: `#SQLite`, `#Library of Congress`, `#data storage`, `#digital preservation`, `#database`

---

<a id="item-2"></a>
## [英伟达、OpenAI、微软联合发布 MRC 协议提升 AI 集群效率](https://blogs.nvidia.com/blog/spectrum-x-ethernet-mrc/) ⭐️ 9.0/10

英伟达、OpenAI 和微软联合发布了多路径可靠连接（MRC）协议，这是一项开放的 RDMA 标准，采用数据包喷射技术实现多路径并发传输和微秒级故障重路由，旨在减少 AI 超算集群的网络拥塞。 这一合作解决了大规模 AI 训练中的关键瓶颈——因网络拥塞导致的 GPU 闲置，并已部署于训练 GPT-5.5 的生产集群中，有望加速如 Stargate 项目等未来 AI 基础设施建设。 MRC 专为 RoCEv2（融合以太网上的 RDMA）设计，允许单个 RDMA 连接同时在多条网络路径上分发流量，从而提升吞吐量和负载均衡。它已集成到英伟达的 Spectrum-X 平台和 Blackwell 架构中，支撑着微软 Fairwater 和甲骨文 OCI Abilene 等集群。

telegram · zaihuapd · May 6, 14:39

**背景**: 远程直接内存访问（RDMA）是一种允许服务器间内存直接数据传输、绕过 CPU 以减少延迟和开销的技术。传统 RDMA 连接是单路径的，在大型 AI 集群中容易导致拥塞。MRC 通过启用多路径通信，利用数据包喷射平衡负载并在微秒内绕过故障重路由，扩展了 RDMA 的能力。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.servethehome.com/nvidia-spectrum-x-mrc-is-the-custom-rdma-transport-protocol-for-gigascale-ai/">NVIDIA Spectrum-X MRC is the Custom RDMA Transport Protocol for Gigascale AI - ServeTheHome</a></li>
<li><a href="https://en.wikipedia.org/wiki/Remote_direct_memory_access">Remote direct memory access - Wikipedia</a></li>
<li><a href="https://4sysops.com/archives/multipath-reliable-connection-mrc-a-new-open-networking-protocol-for-ai-supercomputers/">Multipath Reliable Connection (MRC): a new, open networking protocol for AI supercomputers – 4sysops</a></li>

</ul>
</details>

**标签**: `#AI Infrastructure`, `#Networking`, `#NVIDIA`, `#OpenAI`, `#RDMA`

---

<a id="item-3"></a>
## [月之暗面融资超 7 亿美元，估值破百亿，Kimi 收入飙升](https://t.me/zaihuapd/41251) ⭐️ 9.0/10

中国 AI 初创公司月之暗面完成新一轮超 7 亿美元融资，由阿里、腾讯等领投，估值突破 100 亿美元。其 Kimi 助手近 20 天累计收入已超过 2025 年全年总额，全球付费用户和 API 调用量激增。 这笔融资是近年来中国 AI 领域最大的投资之一，凸显了国内大语言模型的快速增长和市场需求。收入激增表明产品与市场高度契合，Kimi 有望成为全球 AI 助手的领先竞争者。 本轮融资包括阿里、腾讯、五源资本和九安等投资方，累计融资额超 12 亿美元。月之暗面仅用两年多时间估值突破百亿美元，刷新国内企业晋级‘十角兽’的最快速度。其 K2.5 模型是 2026 年 1 月发布的开源多模态 AI 模型，已在 OpenRouter 平台上线。

telegram · zaihuapd · May 7, 00:30

**背景**: 月之暗面是一家 2023 年成立的北京 AI 初创公司，专注于大语言模型和 AI 助手开发。Kimi 是其旗舰 AI 助手产品，支持文本、代码和视觉理解。该公司估值快速增长反映了中国 AI 领域的投资热潮，尤其是在 DeepSeek 等模型崛起之后。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.kimi.com/ai-models/kimi-k2-5">Kimi K2.5 | Open Visual Agentic Model for Real Work</a></li>
<li><a href="https://openrouter.ai/">OpenRouter</a></li>
<li><a href="https://build.nvidia.com/moonshotai/kimi-k2.5/modelcard">kimi-k2.5 Model by Moonshotai | NVIDIA NIM</a></li>

</ul>
</details>

**标签**: `#AI`, `#funding`, `#startup`, `#large language model`, `#China`

---

<a id="item-4"></a>
## [SGLang v0.5.11: 升级 CUDA 13、Torch 2.11、默认推测解码 V2](https://github.com/sgl-project/sglang/releases/tag/v0.5.11) ⭐️ 8.0/10

SGLang v0.5.11 版本发布，将默认 CUDA 版本升级至 13.0，PyTorch 升级至 2.11，默认启用推测解码 V2（通过重叠调度减少 CPU 开销），新增解码侧 radix 缓存以支持预填充/解码分离部署中长公共前缀的缓存命中率恢复，并新增对 Gemma 4、GLM-5.1、Qwen3.6、MiMo-V2.5、Ling-2.6-Flash、Mistral Medium 3.5、Kimi-K2.6 等模型的支持。 这些更新大幅提升了大型语言模型推理服务的性能：默认推测解码 V2 可减少每步 CPU 开销，解码侧 radix 缓存恢复预填充/解码分离部署中的首词延迟（TTFT）节省，同时新增多款流行模型的支持，扩展了 SGLang 的适用性，对 LLM 服务社区具有重要意义。 关键技术变化包括：默认 CUDA 版本升级至 13.0，PyTorch 从 2.9 升至 2.11；推测解码 V2 通过重叠调度隐藏 CPU 开销成为默认模式；新增解码侧 radix 缓存恢复预填充/解码分离下的缓存命中率；支持 DeepSeek-V3 和 Kimi-K2 的 LoRA 微调；集成社区贡献的 FA3 内核；上下文并行方面融合了 All-reduce 和 RMSNorm 以加速端到端推理。

github · Kangyan-Zhou · May 5, 21:28

**背景**: SGLang 是一个专为大型语言模型（LLM）推理设计的高性能推理引擎。推测解码（Speculative Decoding）是一种加速技术，通过同时预测和验证多个 token 来减少延迟，同时保持输出质量。预填充/解码分离（PD Disaggregation）将推理过程分为两个独立阶段，可降低解码阶段的延迟并提高交互性。Radix 缓存是 SGLang 中采用的一种自动 KV 缓存复用技术，通过基数树（radix tree）结构跨请求共享前缀，提升缓存命中率。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://developer.nvidia.com/blog/an-introduction-to-speculative-decoding-for-reducing-latency-in-ai-inference/">An Introduction to Speculative Decoding for Reducing Latency in AI Inference | NVIDIA Technical Blog</a></li>
<li><a href="https://www.bentoml.com/llm/inference-optimization/prefill-decode-disaggregation">Prefill - decode disaggregation | LLM Inference Handbook</a></li>
<li><a href="https://www.lmsys.org/blog/2024-01-17-sglang/">Fast and Expressive LLM Inference with RadixAttention and SGLang - LMSYS Blog | LMSYS Org</a></li>

</ul>
</details>

**标签**: `#SGLang`, `#LLM serving`, `#CUDA`, `#speculative decoding`, `#release notes`

---

<a id="item-5"></a>
## [Vibe coding 与 agentic engineering 趋同，引发担忧](https://simonwillison.net/2026/May/6/vibe-coding-and-agentic-engineering/#atom-everything) ⭐️ 8.0/10

在一次播客中，Simon Willison 意识到他曾经清晰的区分——vibe coding（使用 AI 而不审查代码）与 agentic engineering（专业工程师的监督）——正在模糊，因为他现在有时会信任 AI 代理来生成生产代码，而不审查每一行。 这种趋同挑战了 AI 在软件开发中的负责任使用，如果连有经验的工程师都跳过代码审查，可能会降低代码质量并增加安全风险。它突显了随着 AI 工具变得更加可靠，需要更新最佳实践。 Willison 指出，对于像构建 JSON API 端点这样的常规任务，Claude Code 非常可靠，以至于他不审查代码，但他对没有审查生产代码感到内疚。他将此比作在大型组织中信任其他团队提供的代码。

rss · Simon Willison · May 6, 14:24 · [社区讨论](https://news.ycombinator.com/item?id=48037128)

**背景**: Vibe coding 指使用 AI 生成代码而不理解代码，通常是非程序员依赖“感觉”和最小程度审查。而 agentic engineering 则指专业工程师编排 AI 代理，同时保持架构控制和代码审查。这些术语源于 GitHub Copilot 和 Claude Code 等 AI 编码工具的普及。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Vibe_coding">Vibe coding - Wikipedia</a></li>
<li><a href="https://cloud.google.com/discover/what-is-agentic-coding">What is agentic coding? How it works and use cases | Google Cloud</a></li>
<li><a href="https://addyosmani.com/blog/agentic-engineering/">AddyOsmani.com - Agentic Engineering</a></li>

</ul>
</details>

**社区讨论**: 评论者表达了不同观点：u8 指出，鉴于 AI 的锯齿状前沿，vibe coding 对个人项目没问题；etothet 认为不规范的工程早在 AI 出现前就存在；jwpapi 质疑可靠性说法，指出许多设计决策仍需人类判断；zarzavat 警告 AI 错误变得更加微妙。

**标签**: `#AI coding`, `#vibe coding`, `#agentic engineering`, `#software development`, `#LLMs`

---

<a id="item-6"></a>
## [开发者认证迁移：Supabase → Clerk → Better Auth](https://blog.val.town/better-auth) ⭐️ 8.0/10

一位开发者记录了他们从 Supabase 迁移到 Clerk 再迁移到 Better Auth 的认证之旅，分享了实践中的见解和权衡。 该文章引发了关于自托管与第三方认证的高参与度讨论，提供了实际的迁移经验，帮助开发者做出明智决策。 迁移过程涉及从 Supabase Auth（与 Postgres 紧密耦合）到 Clerk（第三方服务）再到 Better Auth（自托管、TypeScript 优先的库）的转变。

hackernews · stevekrouse · May 6, 17:19 · [社区讨论](https://news.ycombinator.com/item?id=48038827)

**背景**: Supabase 是一个开源的 Firebase 替代品，包含内置认证。Clerk 是一个第三方认证服务，提供全栈用户管理。Better Auth 是一个轻量级、可扩展的 TypeScript 认证库，避免了供应商锁定。争论的核心在于是否将认证外包给第三方，还是通过自托管解决方案保持完全控制。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://clerk.com/">Clerk | Authentication and User Management</a></li>
<li><a href="https://www.contentful.com/blog/clerk-authentication/">Clerk auth: What it is and how to add it to your Next.js project | Contentful</a></li>
<li><a href="https://www.telerik.com/blogs/simplified-authentication-better-auth">Simplified Authentication with Better Auth | Telerik Blogs</a></li>

</ul>
</details>

**社区讨论**: 评论显示了不同的观点：一位用户质疑第三方认证的必要性，而另一位（Better Auth 的 Bereket）表示很高兴该库解决了问题。另一位开发者为自己编写认证以支持定制化辩护，还有一条技术评论强调了复杂系统中可用性的叠加效应。

**标签**: `#authentication`, `#supabase`, `#clerk`, `#better-auth`, `#web-development`

---

<a id="item-7"></a>
## [深度学习数学理论提出训练动态的解析跳跃](https://elonlit.com/scrivings/a-theory-of-deep-learning/) ⭐️ 8.0/10

一篇新文章提出了一种数学理论，利用局部线性微分方程和核特征模态来刻画深度学习训练动态，并提出了一种无需迭代优化即可解析跳跃到最终网络状态的方法。 这项工作为通过绕过缓慢的逐步优化过程来大幅加速深度学习训练提供了潜在路径，并为理解神经网络如何学习提供了新的数学视角。 该理论表明，在输出空间中，演化核的主要特征模态以指数速度快速平衡，使得迭代梯度下降效率低下。论文还联系了控制理论，指出“累积耗散格兰姆矩阵”与可观测性格兰姆矩阵等价。

hackernews · elonlit · May 5, 19:38 · [社区讨论](https://news.ycombinator.com/item?id=48027455)

**背景**: 深度学习训练通常依赖于梯度下降等迭代优化算法，逐步更新网络参数。新理论利用核方法和动力系统的概念来解释训练动态，表明由于核的主要特征模态快速收敛，许多优化步骤是不必要的。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://elonlit.com/scrivings/a-theory-of-deep-learning/">A Theory of Deep Learning | Elements of a Vector Space</a></li>
<li><a href="https://en.wikipedia.org/wiki/Kernel_method">Kernel method - Wikipedia</a></li>

</ul>
</details>

**社区讨论**: 评论表达了浓厚的兴趣，并引用了相关论文，如《深度学习并不神秘或不同》和《深度学习泛化理论》。一些讨论者质疑所提议解析跳跃的计算成本，而一位评论者提醒标题可能有些夸大，将该领域当前状态比作开普勒时代而非牛顿时代。

**标签**: `#deep learning`, `#theory`, `#mathematical framework`, `#training dynamics`

---

<a id="item-8"></a>
## [Google Chrome 静默下载 4GB AI 模型引发隐私与法律争议](https://www.tomshardware.com/tech-industry/cyber-security/google-chrome-silently-downloads-4gb-ai-model-to-your-device-without-permission-report-claims-researcher-says-practice-may-violate-eu-law-waste-thousands-of-kilowatts-of-energy) ⭐️ 8.0/10

安全研究员 Alexander Hanff 报告称，Google Chrome 在未获用户同意的情况下向符合条件的设备静默下载约 4 GB 的 Gemini Nano AI 模型文件（weights.bin），即便手动删除也会自动重下。 该行为可能违反欧盟 GDPR 等隐私法律，因大规模分发消耗大量能源而引发严重的环境担忧，并对流量受限用户造成带宽成本，影响全球数百万用户。 下载的文件是 weights.bin，包含 Gemini Nano 的模型参数。研究员估算，若部署至 10 亿用户，产生的碳排放可能达 6 万吨。

telegram · zaihuapd · May 6, 11:15

**背景**: Gemini Nano 是 Google 的端侧 AI 模型，用于智能回复、摘要等功能，通过 Android 的 AICore 在本地运行。'weights.bin' 存储定义模型行为的神经网络参数（权重）。未经明确同意静默下载大文件违反了 GDPR 等法律中用户控制和透明度的原则。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.androidauthority.com/google-chrome-weights-bin-ai-model-download-explained-3664043/">The truth behind Chrome's 4GB 'weights.bin' Gemini Nano file</a></li>
<li><a href="https://www.zdnet.com/article/google-may-have-downloaded-a-4gb-chrome-file-to-your-pc-heres-why/">Why Chrome may have quietly downloaded a 4GB file to ... - ZDNET</a></li>
<li><a href="https://www.thewindowsclub.com/what-is-weights-bin-file-in-chrome-can-i-delete-it">What is weights.bin file in Chrome? Can I delete it?</a></li>

</ul>
</details>

**标签**: `#Privacy`, `#Google Chrome`, `#AI`, `#GDPR`, `#Environment`

---

<a id="item-9"></a>
## [欧盟拟强制移除华为中兴设备](https://t.me/zaihuapd/41247) ⭐️ 8.0/10

欧盟委员会正考虑出台新规，强制要求所有成员国在其电信和宽带基础设施中淘汰华为和中兴通讯的设备，将此前非约束性建议升级为具有法律效力的强制性规定，违规者将面临经济处罚。 这标志着从自愿指南向强制执行的重大政策转变，可能重塑欧洲 5G 供应链，加剧与中国的关系紧张，并影响全球电信供应商的市场准入和贸易关系。 欧盟还计划收紧对外基础设施资金池，停止向使用华为或中兴设备的非欧盟国家提供项目贷款。欧盟官员称此举意在维护网络安全和技术自主权，而中方强烈谴责将中企定性为高风险缺乏事实依据。

telegram · zaihuapd · May 6, 14:00

**背景**: 自 2020 年以来，欧盟发布了非约束性建议，限制 5G 网络中的“高风险供应商”，但各成员国执行情况不一。拟议法规旨在统一并强制执行这些限制。欧盟的“全球门户”计划（3000 亿欧元基础设施投资计划）也可能收紧资格标准。这些举措反映了对关键电信基础设施中供应商风险和供应链安全的广泛担忧。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.institutmontaigne.org/en/expressions/europeans-struggle-mitigate-5g-risks">Europeans Struggle to Mitigate 5G Risks | Institut Montaigne</a></li>
<li><a href="https://www.rosalux.de/en/news/id/51019/the-global-gateway-deception">The “ Global Gateway ” Deception - Rosa-Luxemburg-Stiftung</a></li>

</ul>
</details>

**标签**: `#Huawei`, `#ZTE`, `#EU regulation`, `#telecom`, `#cybersecurity`

---

<a id="item-10"></a>
## [Anthropic 与 SpaceX 合作提升 Claude 算力](https://www.anthropic.com/news/higher-limits-spacex) ⭐️ 8.0/10

Anthropic 与 SpaceX 签署合作协议，获得位于孟菲斯的 Colossus 1 数据中心的全部算力使用权，新增超过 300 兆瓦的计算容量，包含逾 22 万块 NVIDIA GPU。即日起，Claude Code 所有付费方案的速率限制翻倍，Pro 和 Max 用户的高峰期限制被取消，Claude Opus 的 API 速率限制也大幅提升。 此次合作大幅缓解了 Anthropic 的计算瓶颈，使 Claude 能够更快迭代和大规模部署，直接惠及依赖 Claude Code 和 Claude API 的开发者与企业。这也凸显了专用 AI 数据中心的重要性，以及 AI 实验室与 SpaceX 等基础设施提供商之间日益增长的协作趋势。 Colossus 1 是世界上最庞大的 AI 数据中心之一，配备了 NVIDIA H100、H200 以及下一代 GB200 加速器。Anthropic 还表示有兴趣与 SpaceX 未来在空间计算（千瓦级）方面展开合作。

telegram · zaihuapd · May 6, 16:35

**背景**: Claude Code 是 Anthropic 推出的智能编码工具，集成在终端中，可用于理解代码库、编辑文件和运行命令等任务。与 SpaceX 的合作使 Anthropic 获得了专用的海量算力，满足了训练和运行 Claude 等大语言模型对资源的极高需求。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.nbcnews.com/tech/tech-news/anthropic-spacex-partnership-compute-power-rcna343902">Anthropic and SpaceX announce major partnership as AI arms races...</a></li>
<li><a href="https://www.theneurondaily.com/p/anthropic-spacex-data-center-deal">Anthropic- SpaceX Memphis Deal Doubles Claude Code Limits</a></li>
<li><a href="https://claude.com/product/claude-code">Claude Code by Anthropic | AI Coding Agent, Terminal, IDE</a></li>

</ul>
</details>

**标签**: `#Anthropic`, `#Claude`, `#SpaceX`, `#AI compute`, `#GPU`

---

<a id="item-11"></a>
## [苹果研发支出占比突破 10%，加速 AI 布局](https://www.cnbc.com/2026/05/06/apples-rd-spending-climbs-to-10percent-of-revenue-on-ai-investments.html) ⭐️ 8.0/10

2026 年 3 月财季，苹果研发支出占营收比例升至 10.3%，为 30 年来首次突破 10%，研发投入增速高达 34%。 这一里程碑表明苹果在 AI 领域的战略紧迫性，正投入端侧 AI、自研芯片及私有云计算以重塑硬件平台，可能影响整个消费电子生态系统。 据报苹果正在研发 AI 眼镜和带摄像头的 AirPods，同时推进 Siri 升级和首款折叠屏 iPhone，旨在将 AI 深度整合进硬件生态。现任 CEO 库克将于 2026 年 9 月交棒。

telegram · zaihuapd · May 7, 01:00

**背景**: 端侧 AI 是指在用户设备上直接进行的人工智能处理，而非在云端，能提升隐私和速度。私有云计算是专为单一组织提供的云环境，具备可控访问和数据安全。苹果在这些领域的战略重点符合其将 AI 整合进产品线同时维护用户隐私的整体方向。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.anquanke.com/post/id/297252">苹 果 推出“ 私 有 云 计 算 ”和 Apple Intelligence AI-安全KER - 安全资讯平台</a></li>

</ul>
</details>

**标签**: `#苹果`, `#AI`, `#研发`, `#硬件平台`

---

<a id="item-12"></a>
## [小米开源 OmniVoice：支持 646 种语言的语音克隆 TTS](https://mp.weixin.qq.com/s/TCS_Sd10g_rvf1cszw673A) ⭐️ 8.0/10

OmniVoice 支持 646 种语言和跨语言克隆，能够显著扩大高质量 TTS 对低资源语言的可及性。其开源发布允许研究人员和开发者在此基础上进一步开发，可能加速语音合成和语音克隆领域的创新。 该模型使用全码本随机掩蔽和大语言模型预训练参数来提升效率和可懂度。它在从 50 个开源数据集构建的 58 万小时、646 种语言的训练集上训练，在 24 种语言的测试中优于商用系统，在 102 种语言的评估中接近真实人声。

telegram · zaihuapd · May 7, 10:06

**背景**: 文本转语音（TTS）技术将书面文字转换为口语音频。语音克隆是一种专门的 TTS 技术，能从短音频样本中模仿特定人的声音。传统的 TTS 模型在多语言支持方面往往存在困难，且每种语言需要大量数据，因此 OmniVoice 的高效架构和广泛语言覆盖显得尤为重要。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://omnivoice.app/">OmniVoice : Free AI Voice Generator & Voice Cloning</a></li>

</ul>
</details>

**标签**: `#语音克隆`, `#TTS`, `#多语言`, `#开源`, `#小米`

---