---
layout: default
title: "Horizon Summary: 2026-05-07 (EN)"
date: 2026-05-07
lang: en
---

> From 36 items, 12 important content pieces were selected

---

1. [SQLite Recommended by Library of Congress for Digital Preservation](#item-1) ⭐️ 9.0/10
2. [NVIDIA, OpenAI, Microsoft Release MRC Protocol for AI Clusters](#item-2) ⭐️ 9.0/10
3. [Moonshot AI Raises $700M+ at $10B+ Valuation as Kimi Revenue Skyrockets](#item-3) ⭐️ 9.0/10
4. [SGLang v0.5.11: CUDA 13, Torch 2.11, Spec Decode V2](#item-4) ⭐️ 8.0/10
5. [Vibe coding and agentic engineering converge, raising concerns](#item-5) ⭐️ 8.0/10
6. [Developer Migrates Auth: Supabase → Clerk → Better Auth](#item-6) ⭐️ 8.0/10
7. [Mathematical Theory Proposes Analytic Jump in Deep Learning Training](#item-7) ⭐️ 8.0/10
8. [Google Chrome Silent 4GB AI Model Download Sparks Privacy, Legal Outcry](#item-8) ⭐️ 8.0/10
9. [EU Proposes Mandatory Removal of Huawei, ZTE Equipment](#item-9) ⭐️ 8.0/10
10. [Anthropic Partners with SpaceX to Boost Claude Compute Limits](#item-10) ⭐️ 8.0/10
11. [Apple's R&D spending exceeds 10% of revenue for first time in 30 years, accelerating AI push](#item-11) ⭐️ 8.0/10
12. [Xiaomi Open-Sources OmniVoice: 646-Language Voice Cloning TTS](#item-12) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [SQLite Recommended by Library of Congress for Digital Preservation](https://sqlite.org/locrsf.html) ⭐️ 9.0/10

The Library of Congress has officially recommended SQLite as a preferred format for digital content storage, recognizing its suitability for long-term preservation. This endorsement from a major cultural institution validates SQLite's robustness and reliability, potentially driving broader adoption in archival and preservation systems worldwide. The recommendation is part of the Library of Congress's sustainability of digital formats initiative, and while initially made in 2018, it remains relevant as of 2026.

hackernews · whatisabcdefgh · May 6, 21:58 · [Discussion](https://news.ycombinator.com/item?id=48042434)

**Background**: SQLite is a self-contained, serverless, zero-configuration SQL database engine that stores data in a single disk file. It is widely used in applications, embedded systems, and increasingly for data interchange. The Library of Congress evaluates digital formats for their longevity, openness, and adoption to guide preservation efforts.

**Discussion**: Community comments highlight diverse perspectives: some praise SQLite's reliability and simplicity for most apps, while others note it may be overkill for simple tasks or pose security risks when PII is easily copied. One user also pointed out that the recommendation is nearly eight years old.

**Tags**: `#SQLite`, `#Library of Congress`, `#data storage`, `#digital preservation`, `#database`

---

<a id="item-2"></a>
## [NVIDIA, OpenAI, Microsoft Release MRC Protocol for AI Clusters](https://blogs.nvidia.com/blog/spectrum-x-ethernet-mrc/) ⭐️ 9.0/10

NVIDIA, OpenAI, and Microsoft jointly released the Multipath Reliable Connection (MRC) protocol, an open RDMA standard that uses packet spraying for multi-path data transmission and microsecond-level failover, aimed at reducing network congestion in AI supercomputing clusters. This collaboration addresses a critical bottleneck in large-scale AI training — GPU idle time due to network congestion — and is already deployed in production clusters training GPT-5.5, promising to accelerate future AI infrastructure such as Project Stargate. MRC is designed for RoCEv2 (RDMA over Converged Ethernet) and enables a single RDMA connection to distribute traffic across multiple network paths simultaneously, improving throughput and load balancing. It is already integrated into NVIDIA's Spectrum-X platform and Blackwell architecture, powering Microsoft's Fairwater and Oracle's OCI Abilene clusters.

telegram · zaihuapd · May 6, 14:39

**Background**: Remote Direct Memory Access (RDMA) is a technology that allows data transfer between servers' memory without CPU involvement, reducing latency and overhead. Traditional RDMA connections are single-path, leading to congestion in large AI clusters. MRC extends this by enabling multi-path communication, using packet spraying to balance load and reroute around failures in microseconds.

<details><summary>References</summary>
<ul>
<li><a href="https://www.servethehome.com/nvidia-spectrum-x-mrc-is-the-custom-rdma-transport-protocol-for-gigascale-ai/">NVIDIA Spectrum-X MRC is the Custom RDMA Transport Protocol for Gigascale AI - ServeTheHome</a></li>
<li><a href="https://en.wikipedia.org/wiki/Remote_direct_memory_access">Remote direct memory access - Wikipedia</a></li>
<li><a href="https://4sysops.com/archives/multipath-reliable-connection-mrc-a-new-open-networking-protocol-for-ai-supercomputers/">Multipath Reliable Connection (MRC): a new, open networking protocol for AI supercomputers – 4sysops</a></li>

</ul>
</details>

**Tags**: `#AI Infrastructure`, `#Networking`, `#NVIDIA`, `#OpenAI`, `#RDMA`

---

<a id="item-3"></a>
## [Moonshot AI Raises $700M+ at $10B+ Valuation as Kimi Revenue Skyrockets](https://t.me/zaihuapd/41251) ⭐️ 9.0/10

Chinese AI startup Moonshot AI has completed a new funding round of over $700 million, led by Alibaba, Tencent, and others, pushing its valuation past $10 billion. In just 20 days, revenue from its Kimi assistant has exceeded its total 2025 revenue, driven by global paid users and API calls. This funding marks one of the largest AI investments in China, highlighting the rapid growth and market demand for domestic large language models. The revenue surge indicates strong product-market fit, potentially positioning Kimi as a leading competitor to global AI assistants. The round includes investments from Alibaba, Tencent, Wu Capital, and Jiuan, with total funding exceeding $1.2 billion. Moonshot AI achieved the $10B valuation in just over two years, the fastest for a Chinese startup to reach 'deci-unicorn' status. Its K2.5 model is an open-source multimodal AI model released in January 2026, and is available on the OpenRouter platform.

telegram · zaihuapd · May 7, 00:30

**Background**: Moonshot AI is a Beijing-based startup founded in 2023, focused on developing large language models and AI assistants. Kimi is their flagship AI assistant product supporting text, code, and visual understanding. The company's rapid valuation growth reflects the intense investment race in China's AI sector, especially after the rise of models like DeepSeek and others.

<details><summary>References</summary>
<ul>
<li><a href="https://www.kimi.com/ai-models/kimi-k2-5">Kimi K2.5 | Open Visual Agentic Model for Real Work</a></li>
<li><a href="https://openrouter.ai/">OpenRouter</a></li>
<li><a href="https://build.nvidia.com/moonshotai/kimi-k2.5/modelcard">kimi-k2.5 Model by Moonshotai | NVIDIA NIM</a></li>

</ul>
</details>

**Tags**: `#AI`, `#funding`, `#startup`, `#large language model`, `#China`

---

<a id="item-4"></a>
## [SGLang v0.5.11: CUDA 13, Torch 2.11, Spec Decode V2](https://github.com/sgl-project/sglang/releases/tag/v0.5.11) ⭐️ 8.0/10

SGLang v0.5.11 has been released, upgrading the default CUDA version to 13.0, PyTorch to 2.11, and enabling speculative decoding V2 by default. It also introduces a decode radix cache for prefill/decode disaggregation and adds support for numerous new models including Gemma 4, GLM-5.1, Qwen3.6, MiMo-V2.5, Ling-2.6-Flash, Mistral Medium 3.5, and Kimi-K2.6. These upgrades significantly improve LLM inference performance: speculative decoding V2 reduces CPU overhead per step, the decode radix cache recovers time-to-first-token (TTFT) savings in disaggregated deployments, and the new model support broadens SGLang's applicability. This release marks a major step forward for the LLM serving ecosystem. Key technical changes include: default CUDA version upgraded to 13.0 and PyTorch to 2.11; speculative decoding V2 enabled by default with overlap scheduling to hide CPU overhead; decode radix cache for PD disaggregation; LoRA support for DeepSeek-V3 and Kimi-K2; community-contributed FA3 kernels; and context parallelism enhancements with all-reduce and RMSNorm fusion.

github · Kangyan-Zhou · May 5, 21:28

**Background**: SGLang is a high-performance inference engine for large language models (LLMs). Speculative decoding accelerates LLM inference by predicting and verifying multiple tokens simultaneously, reducing latency while preserving output quality. Prefill/decode (PD) disaggregation decouples the two stages of inference to improve interactivity. Radix cache is a technique used in SGLang for automatic KV cache reuse through a radix tree structure, exploiting shared prefixes across requests.

<details><summary>References</summary>
<ul>
<li><a href="https://developer.nvidia.com/blog/an-introduction-to-speculative-decoding-for-reducing-latency-in-ai-inference/">An Introduction to Speculative Decoding for Reducing Latency in AI Inference | NVIDIA Technical Blog</a></li>
<li><a href="https://www.bentoml.com/llm/inference-optimization/prefill-decode-disaggregation">Prefill - decode disaggregation | LLM Inference Handbook</a></li>
<li><a href="https://www.lmsys.org/blog/2024-01-17-sglang/">Fast and Expressive LLM Inference with RadixAttention and SGLang - LMSYS Blog | LMSYS Org</a></li>

</ul>
</details>

**Tags**: `#SGLang`, `#LLM serving`, `#CUDA`, `#speculative decoding`, `#release notes`

---

<a id="item-5"></a>
## [Vibe coding and agentic engineering converge, raising concerns](https://simonwillison.net/2026/May/6/vibe-coding-and-agentic-engineering/#atom-everything) ⭐️ 8.0/10

In a podcast, Simon Willison realized that his once-clear distinction between vibe coding (using AI without reviewing code) and agentic engineering (professional oversight) is blurring, as he now sometimes trusts AI agents for production code without reviewing every line. This convergence challenges responsible AI use in software development, potentially lowering code quality and increasing security risks if even experienced engineers skip review. It highlights the need for updated best practices as AI tools become more reliable. Willison noted that for routine tasks like building a JSON API endpoint, Claude Code is so reliable he doesn't review the code, yet he feels guilt about not reviewing production code. He compares this to trusting code from other teams in larger organizations.

rss · Simon Willison · May 6, 14:24 · [Discussion](https://news.ycombinator.com/item?id=48037128)

**Background**: Vibe coding refers to using AI to generate code without understanding it, often by non-programmers relying on 'vibes' and minimal review. Agentic engineering, in contrast, involves professional engineers orchestrating AI agents while maintaining architectural control and code review. These terms emerged from the proliferation of AI coding tools like GitHub Copilot and Claude Code.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Vibe_coding">Vibe coding - Wikipedia</a></li>
<li><a href="https://cloud.google.com/discover/what-is-agentic-coding">What is agentic coding? How it works and use cases | Google Cloud</a></li>
<li><a href="https://addyosmani.com/blog/agentic-engineering/">AddyOsmani.com - Agentic Engineering</a></li>

</ul>
</details>

**Discussion**: Commenters expressed mixed views: u8 noted that vibe coding is fine for personal projects given AI's jagged frontier, while etothet argued that undisciplined engineering existed before AI. jwpapi questioned the reliability claim, pointing out many design decisions still need human judgment, and zarzavat warned that AI errors are becoming more subtle.

**Tags**: `#AI coding`, `#vibe coding`, `#agentic engineering`, `#software development`, `#LLMs`

---

<a id="item-6"></a>
## [Developer Migrates Auth: Supabase → Clerk → Better Auth](https://blog.val.town/better-auth) ⭐️ 8.0/10

A developer documented their journey migrating authentication from Supabase to Clerk and finally to Better Auth, sharing practical insights and trade-offs. The post sparks high-engagement debate on self-hosted vs third-party authentication, offering real-world migration lessons that help developers make informed decisions. The move involved migrating from Supabase Auth (tightly coupled with Postgres) to Clerk (a third-party service) and then to Better Auth (a self-hosted, TypeScript-first library).

hackernews · stevekrouse · May 6, 17:19 · [Discussion](https://news.ycombinator.com/item?id=48038827)

**Background**: Supabase is an open-source Firebase alternative that includes built-in auth. Clerk is a third-party authentication service offering full-stack user management. Better Auth is a lightweight, extensible authentication library for TypeScript that avoids vendor lock-in. The debate centers on whether to offload auth to a third party or maintain full control with self-hosted solutions.

<details><summary>References</summary>
<ul>
<li><a href="https://clerk.com/">Clerk | Authentication and User Management</a></li>
<li><a href="https://www.contentful.com/blog/clerk-authentication/">Clerk auth: What it is and how to add it to your Next.js project | Contentful</a></li>
<li><a href="https://www.telerik.com/blogs/simplified-authentication-better-auth">Simplified Authentication with Better Auth | Telerik Blogs</a></li>

</ul>
</details>

**Discussion**: Comments show varied perspectives: one user questioned the need for third-party auth at all, while another (Bereket from Better Auth) expressed joy that the library solved the problem. Another developer defended rolling their own auth for customizability, and a technical comment highlighted how availability compounds in complex systems.

**Tags**: `#authentication`, `#supabase`, `#clerk`, `#better-auth`, `#web-development`

---

<a id="item-7"></a>
## [Mathematical Theory Proposes Analytic Jump in Deep Learning Training](https://elonlit.com/scrivings/a-theory-of-deep-learning/) ⭐️ 8.0/10

A new article proposes a mathematical theory that characterizes deep learning training dynamics using locally linear differential equations and kernel eigenmodes, suggesting a method to analytically jump to the final network state without iterative optimization. This work offers a potential path to drastically accelerate deep learning training by bypassing the slow, step-by-step optimization process, and provides a new mathematical lens for understanding how neural networks learn. The theory shows that in output space, dominant eigenmodes of the evolving kernel equilibrate exponentially fast, making iterative gradient descent inefficient. The paper also draws connections to control theory, identifying the 'Cumulative Dissipation Gramian' as equivalent to the Observability Gramian.

hackernews · elonlit · May 5, 19:38 · [Discussion](https://news.ycombinator.com/item?id=48027455)

**Background**: Deep learning training typically relies on iterative optimization algorithms like gradient descent, which update network parameters step by step. The new theory leverages concepts from kernel methods and dynamical systems to explain training dynamics, suggesting that many optimization steps are unnecessary because the kernel's dominant eigenmodes converge rapidly.

<details><summary>References</summary>
<ul>
<li><a href="https://elonlit.com/scrivings/a-theory-of-deep-learning/">A Theory of Deep Learning | Elements of a Vector Space</a></li>
<li><a href="https://en.wikipedia.org/wiki/Kernel_method">Kernel method - Wikipedia</a></li>

</ul>
</details>

**Discussion**: Comments express strong interest, with references to related papers such as 'Deep Learning is Not So Mysterious or Different' and 'A Theory of Generalization in Deep Learning'. Some discussants question the computational cost of the proposed analytic jump, while one commenter cautions that the title may overreach, comparing the field's current state to the era of Kepler rather than Newton.

**Tags**: `#deep learning`, `#theory`, `#mathematical framework`, `#training dynamics`

---

<a id="item-8"></a>
## [Google Chrome Silent 4GB AI Model Download Sparks Privacy, Legal Outcry](https://www.tomshardware.com/tech-industry/cyber-security/google-chrome-silently-downloads-4gb-ai-model-to-your-device-without-permission-report-claims-researcher-says-practice-may-violate-eu-law-waste-thousands-of-kilowatts-of-energy) ⭐️ 8.0/10

Security researcher Alexander Hanff reported that Google Chrome silently downloads a 4 GB Gemini Nano AI model file (weights.bin) to eligible devices without user consent, and the file reappears even after manual deletion. This practice potentially violates EU GDPR and other privacy laws, raises significant environmental concerns due to massive energy consumption for distribution, and imposes bandwidth costs on users with data caps, affecting millions globally. The downloaded file is weights.bin, containing the model parameters for Gemini Nano. The researcher estimates that if deployed to 1 billion users, the resulting carbon emissions could reach 60,000 tons.

telegram · zaihuapd · May 6, 11:15

**Background**: Gemini Nano is Google's on-device AI model designed for tasks like smart reply and summarization, running locally via Android's AICore. 'weights.bin' stores the neural network parameters (weights) that define the model's behavior. Silently downloading large files without explicit consent contravenes principles of user control and transparency under laws like GDPR.

<details><summary>References</summary>
<ul>
<li><a href="https://www.androidauthority.com/google-chrome-weights-bin-ai-model-download-explained-3664043/">The truth behind Chrome's 4GB 'weights.bin' Gemini Nano file</a></li>
<li><a href="https://www.zdnet.com/article/google-may-have-downloaded-a-4gb-chrome-file-to-your-pc-heres-why/">Why Chrome may have quietly downloaded a 4GB file to ... - ZDNET</a></li>
<li><a href="https://www.thewindowsclub.com/what-is-weights-bin-file-in-chrome-can-i-delete-it">What is weights.bin file in Chrome? Can I delete it?</a></li>

</ul>
</details>

**Tags**: `#Privacy`, `#Google Chrome`, `#AI`, `#GDPR`, `#Environment`

---

<a id="item-9"></a>
## [EU Proposes Mandatory Removal of Huawei, ZTE Equipment](https://t.me/zaihuapd/41247) ⭐️ 8.0/10

The European Commission is considering new regulations that would require all EU member states to phase out equipment from Huawei and ZTE in their telecom and broadband infrastructure, upgrading previous non-binding recommendations to legally binding rules with economic penalties for non-compliance. This marks a significant policy shift from voluntary guidelines to mandatory enforcement, potentially reshaping Europe's 5G supply chain and escalating tensions with China, while impacting global telecom vendors' market access and trade relations. The EU also plans to restrict external infrastructure funding, stopping project loans to non-EU countries that use Huawei or ZTE equipment. The move is justified by EU officials as protecting cybersecurity and technological sovereignty, while China strongly condemns the designation of Chinese firms as high-risk without factual basis.

telegram · zaihuapd · May 6, 14:00

**Background**: Since 2020, the EU has issued non-binding recommendations to restrict 'high-risk suppliers' in 5G networks, but implementation varied across member states. The proposed regulation seeks to harmonize and enforce these restrictions. The EU's Global Gateway initiative, a €300 billion infrastructure investment program, may also tighten eligibility criteria. These steps reflect broader concerns about vendor risk and supply chain security in critical telecom infrastructure.

<details><summary>References</summary>
<ul>
<li><a href="https://www.institutmontaigne.org/en/expressions/europeans-struggle-mitigate-5g-risks">Europeans Struggle to Mitigate 5G Risks | Institut Montaigne</a></li>
<li><a href="https://www.rosalux.de/en/news/id/51019/the-global-gateway-deception">The “ Global Gateway ” Deception - Rosa-Luxemburg-Stiftung</a></li>

</ul>
</details>

**Tags**: `#Huawei`, `#ZTE`, `#EU regulation`, `#telecom`, `#cybersecurity`

---

<a id="item-10"></a>
## [Anthropic Partners with SpaceX to Boost Claude Compute Limits](https://www.anthropic.com/news/higher-limits-spacex) ⭐️ 8.0/10

Anthropic has signed a partnership with SpaceX to gain exclusive access to the entire Colossus 1 data center in Memphis, Tennessee, adding over 300 megawatts of compute capacity with more than 220,000 NVIDIA GPUs. Effective immediately, Claude Code rate limits are doubled for all paid plans and peak-hour restrictions are removed for Pro and Max users, while Claude Opus API rate limits have been significantly increased. This partnership significantly alleviates compute bottlenecks for Anthropic, enabling faster iteration and larger-scale deployments of Claude, directly benefiting developers and enterprises that rely on Claude Code and Claude API. It also highlights the strategic importance of dedicated AI data centers and the growing collaboration between AI labs and infrastructure providers like SpaceX. Colossus 1 is one of the world's largest AI data centers, equipped with H100, H200, and next-generation GB200 accelerators from NVIDIA. Anthropic expressed interest in collaborating with SpaceX on space-based computing gigawatts in the future.

telegram · zaihuapd · May 6, 16:35

**Background**: Claude Code is Anthropic's agentic coding tool that integrates into the terminal for tasks like understanding codebases, editing files, and running commands. The partnership with SpaceX provides Anthropic with dedicated access to massive compute capacity, addressing the high resource demands of training and running large language models like Claude.

<details><summary>References</summary>
<ul>
<li><a href="https://www.nbcnews.com/tech/tech-news/anthropic-spacex-partnership-compute-power-rcna343902">Anthropic and SpaceX announce major partnership as AI arms races...</a></li>
<li><a href="https://www.theneurondaily.com/p/anthropic-spacex-data-center-deal">Anthropic- SpaceX Memphis Deal Doubles Claude Code Limits</a></li>
<li><a href="https://claude.com/product/claude-code">Claude Code by Anthropic | AI Coding Agent, Terminal, IDE</a></li>

</ul>
</details>

**Tags**: `#Anthropic`, `#Claude`, `#SpaceX`, `#AI compute`, `#GPU`

---

<a id="item-11"></a>
## [Apple's R&D spending exceeds 10% of revenue for first time in 30 years, accelerating AI push](https://www.cnbc.com/2026/05/06/apples-rd-spending-climbs-to-10percent-of-revenue-on-ai-investments.html) ⭐️ 8.0/10

Apple's R&D spending reached 10.3% of revenue in the March 2026 quarter, the first time it has exceeded 10% in three decades, with a 34% year-over-year increase in R&D investment. This milestone signals Apple's strategic urgency in AI, as it invests in on-device AI, custom chips, and private cloud computing to reshape its hardware platform, potentially impacting the entire consumer electronics ecosystem. Apple is reportedly developing AI glasses and AirPods with cameras, alongside Siri upgrades and its first foldable iPhone, aiming to deeply integrate AI into its hardware ecosystem. CEO Tim Cook is set to hand over in September 2026.

telegram · zaihuapd · May 7, 01:00

**Background**: On-device AI refers to artificial intelligence processing performed directly on a user's device rather than in the cloud, enhancing privacy and speed. Private cloud computing is a cloud environment dedicated to a single organization, offering controlled access and data security. Apple's strategic focus on these areas aligns with its broader push to integrate AI into its product lineup while maintaining user privacy.

<details><summary>References</summary>
<ul>
<li><a href="https://www.anquanke.com/post/id/297252">苹 果 推出“ 私 有 云 计 算 ”和 Apple Intelligence AI-安全KER - 安全资讯平台</a></li>

</ul>
</details>

**Tags**: `#苹果`, `#AI`, `#研发`, `#硬件平台`

---

<a id="item-12"></a>
## [Xiaomi Open-Sources OmniVoice: 646-Language Voice Cloning TTS](https://mp.weixin.qq.com/s/TCS_Sd10g_rvf1cszw673A) ⭐️ 8.0/10

Xiaomi has open-sourced OmniVoice, a multi-language voice cloning text-to-speech (TTS) model based on a minimal bidirectional Transformer architecture. It achieves training speeds of 100,000 hours per day and PyTorch inference at 40x real-time, with synthesis quality surpassing mainstream commercial systems. OmniVoice's support for 646 languages and cross-language cloning capabilities can significantly broaden the accessibility of high-quality TTS for low-resource languages. Its open-source release allows researchers and developers to build upon the model, potentially accelerating innovation in voice synthesis and voice cloning. The model uses full-codebook random masking and large language model pre-training parameters to improve efficiency and intelligibility. It is trained on a dataset of 580,000 hours across 646 languages built from 50 open-source datasets, and in 24-language tests it outperforms commercial systems while approaching real human speech in 102-language evaluations.

telegram · zaihuapd · May 7, 10:06

**Background**: Text-to-speech (TTS) technology converts written text into spoken audio. Voice cloning is a specialized TTS technique that mimics a specific person's voice from a short audio sample. Traditional TTS models often struggle with multilingual support and require large amounts of data per language, making OmniVoice's efficient architecture and extensive language coverage noteworthy.

<details><summary>References</summary>
<ul>
<li><a href="https://omnivoice.app/">OmniVoice : Free AI Voice Generator & Voice Cloning</a></li>

</ul>
</details>

**Tags**: `#语音克隆`, `#TTS`, `#多语言`, `#开源`, `#小米`

---