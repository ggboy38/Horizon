---
layout: default
title: "Horizon Summary: 2026-05-09 (ZH)"
date: 2026-05-09
lang: zh
---

> From 39 items, 15 important content pieces were selected

---

1. [Triton 3.7.0 发布：新增操作与后端改进](#item-1) ⭐️ 9.0/10
2. [Google reCAPTCHA 对去谷歌化的 Android 用户失效](#item-2) ⭐️ 8.0/10
3. [LLM 在委托工作流中使文档质量下降 25%](#item-3) ⭐️ 8.0/10
4. [HTML 作为 LLM 输出：惊人的有效性](#item-4) ⭐️ 8.0/10
5. [数学家使用 ChatGPT 5.5 Pro 引发 AI 研究讨论](#item-5) ⭐️ 8.0/10
6. [OpenAI 的 WebRTC 问题：文章提议 WebTransport 替代方案](#item-6) ⭐️ 8.0/10
7. [AI 加速漏洞披露文化的崩溃](#item-7) ⭐️ 8.0/10
8. [React2Shell：React 服务器组件中的严重 RCE 漏洞](#item-8) ⭐️ 8.0/10
9. [AWS 弗吉尼亚北部宕机解决，凸显 us-east-1 脆弱性](#item-9) ⭐️ 8.0/10
10. [Anthropic 的 'Teaching Claude Why' 方法减少 AI 误对齐](#item-10) ⭐️ 8.0/10
11. [Mozilla 借助 Claude Mythos 预览版加固 Firefox](#item-11) ⭐️ 8.0/10
12. [Anthropic 拟融资数百亿美元，估值逼近万亿美元](#item-12) ⭐️ 8.0/10
13. [美国怀疑英伟达芯片经泰国走私至中国](#item-13) ⭐️ 8.0/10
14. [DeepSeek 估值目标 450 亿美元，国家基金领投](#item-14) ⭐️ 8.0/10
15. [百度发布文心大模型 5.1，宣称高效预训练，中国搜索排名第一](#item-15) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [Triton 3.7.0 发布：新增操作与后端改进](https://github.com/triton-lang/triton/releases/tag/v3.7.0) ⭐️ 9.0/10

Triton 3.7.0 已发布，新增了 tl.squeeze、tl.unsqueeze、缩放批量矩阵乘法（scaled BMM）和 FP8 常量等操作，并对 NVIDIA 和 AMD GPU 的后端进行了重大改进。 此次发布增强了 Triton（AI/ML 工作负载中广泛使用的 GPU 内核编译器）的表现力和性能，使得内核开发更加高效和灵活。 新功能包括 FP8 常量支持、缩放批量矩阵乘法以及从 JIT 编译代码返回 constexpr 的能力。后端更新包括 LLVM 升级、改进的 2CTA/多播支持以及增强的 AMD/HIP 后端。

github · atalman · May 7, 22:19

**背景**: Triton 是 OpenAI 开发的一种开源的类 Python 编程语言和编译器，用于编写高效的 GPU 内核。它抽象了底层的 CUDA 细节，使研究人员无需深厚的 CUDA 经验就能编写高性能代码。此次发布延续了 Triton 作为 AI/ML 基础设施关键工具的演进。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://openai.com/index/triton/">Introducing Triton: Open-source GPU programming for neural networks | OpenAI</a></li>
<li><a href="https://github.com/triton-lang/triton">GitHub - triton-lang/triton: Development repository for the Triton language and compiler · GitHub</a></li>
<li><a href="https://www.rightnowai.co/guides/frameworks/triton">Triton GPU Kernel Programming Guide: CUDA Alternative | RightNow AI | RightNow AI</a></li>

</ul>
</details>

**标签**: `#triton`, `#gpu`, `#compiler`, `#machine learning`, `#release`

---

<a id="item-2"></a>
## [Google reCAPTCHA 对去谷歌化的 Android 用户失效](https://reclaimthenet.org/google-broke-recaptcha-for-de-googled-android-users) ⭐️ 8.0/10

Google 的新版 reCAPTCHA 现在要求 Android 设备使用 Play Integrity API 和远程证明，这导致没有 Google Play 服务的设备（如运行自定义 ROM 或 GrapheneOS 的设备）无法正常使用。 这一变化超越了以往的 CAPTCHA 验证，强制要求硬件级别的证明，实际上将注重隐私的用户和自定义 ROM 社区排除在依赖 reCAPTCHA 的网站之外。这引发了关于供应商锁定以及 Android 生态系统中用户选择权被侵蚀的担忧。 新版 reCAPTCHA 使用 Play Integrity API（前身为 SafetyNet）和远程证明来验证设备完整性，据报道会将设备身份绑定到一个静态密钥（EK），该密钥可能被 Google 服务器记录。这与 2023 年被放弃的争议性 Web Environment Integrity（WEI）提案类似。

hackernews · anonymousiam · May 8, 18:45 · [社区讨论](https://news.ycombinator.com/item?id=48067119)

**背景**: Play Integrity API 是 Google Play Services 提供的一组服务，允许应用验证设备和应用安装的完整性。远程证明是一种可信计算概念，设备通过加密密钥向远程验证者证明其硬件和软件状态。去谷歌化的 Android 用户出于隐私考虑运行没有 Google Play Services 的操作系统，并依赖 microG 或沙盒化的 Play Services 等替代方案。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Play_Integrity_API">Play Integrity API - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/Remote_attestation">Remote attestation</a></li>
<li><a href="https://en.wikipedia.org/wiki/Web_Environment_Integrity">Web Environment Integrity - Wikipedia</a></li>

</ul>
</details>

**社区讨论**: 评论者表达了强烈的反对意见，许多人指出了远程证明的隐私隐患，并将其与已放弃的 WEI 提案进行比较。一些评论提到，即使是使用带有沙盒 Play Services 的 GrapheneOS 用户也可能受到影响，并且对 Google 能否通过此机制避免追踪用户表示怀疑。

**标签**: `#reCAPTCHA`, `#Android`, `#Google`, `#privacy`, `#attestation`

---

<a id="item-3"></a>
## [LLM 在委托工作流中使文档质量下降 25%](https://arxiv.org/abs/2604.15597) ⭐️ 8.0/10

微软研究院的一篇新论文发现，大型语言模型（LLM）在被用于委托任务时会破坏文档，即使是 Gemini 3.1 Pro 和 GPT 5.4 等前沿模型在 20 个交互周期后平均也会使 25%的内容退化。 这一发现凸显了自动化文档维护的 AI 智能体存在关键可靠性问题，因为重复的 LLM 处理会悄然侵蚀准确性和意图，可能在专业和科学领域导致代价高昂的错误。 该研究测试了 19 个 LLM 在长达 20 个连续交互的工作流上的表现，通过可逆变换的往返保真度来测量退化。即使使用了工具，退化仍然存在，表明存在超出简单幻觉的系统性问题。

hackernews · rbanffy · May 9, 08:44 · [社区讨论](https://news.ycombinator.com/item?id=48073246)

**背景**: LLM 越来越多地被用于改写、总结或更新文档，但每次处理都可能引入微小的变化并逐渐累积。这种现象有时被称为“语义消融”，类似于 JPEG 压缩退化的梗。先前的研究注意到了在合成数据上训练时的模型崩溃，但这篇论文专门考察了有意识的人机 LLM 委托循环。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arxiv.org/abs/2604.15597">[2604.15597] LLMs Corrupt Your Documents When You Delegate</a></li>
<li><a href="https://huggingface.co/papers/2604.15597">Paper page - LLMs Corrupt Your Documents When You Delegate</a></li>
<li><a href="https://cekrem.github.io/posts/llms-corrupt-your-documents/">LLMs Corrupt Your Documents (and the Theory Dies Twice) · cekrem.github.io</a></li>

</ul>
</details>

**社区讨论**: 社区评论普遍赞同这一发现，用户将这种效应比作“JPEG 梗”，并创造了“语义消融”等术语。一些人对工具使用的结果表示怀疑，指出基本的智能体框架可能不代表最先进的系统。其他人强调需要最小化 LLM 的往返次数，并将它们用作薄翻译层。

**标签**: `#LLMs`, `#Document Quality`, `#Semantic Degradation`, `#AI Reliability`, `#Research`

---

<a id="item-4"></a>
## [HTML 作为 LLM 输出：惊人的有效性](https://twitter.com/trq212/status/2052809885763747935) ⭐️ 8.0/10

一篇博客文章和推特帖子主张，使用 HTML 作为像 Claude Code 这样的 LLM 的输出格式，在创建丰富、可交互的文档方面出奇地有效，挑战了默认使用 Markdown 的做法。 这一见解意义重大，因为它促使开发者重新考虑 AI 辅助文档的输出格式选择，有望在不牺牲 LLM 生成优势的前提下，获得更互动、更美观的结果。 该帖子链接到一个在线示例页面，并引用了 Simon Willison 关于同一主题的文章。社区讨论突出了权衡：HTML 提供更丰富的交互性，但与 Markdown 相比，人类共同编辑文档的难度增加。

hackernews · pretext · May 9, 04:53 · [社区讨论](https://news.ycombinator.com/item?id=48071940)

**背景**: Claude Code 是 Anthropic 面向开发者的代理式编码工具。大型语言模型（LLM）通常输出 Markdown，因为它简单易读，但 HTML 允许更复杂的布局、交互性和嵌入内容。争论的核心在于平衡丰富性与人类可编辑性。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Claude_Code">Claude Code</a></li>
<li><a href="https://claude.com/product/claude-code">Claude Code by Anthropic | AI Coding Agent, Terminal, IDE</a></li>

</ul>
</details>

**社区讨论**: 一些评论者担心 HTML 输出会降低人类共同编写文档的能力，而另一些人则称赞它可以生成自包含、可共享的应用。建议包括使用扩展 Markdown（例如带有 Mermaid）或 MDX 来混合格式。一位批评者认为该帖子质量低下。

**标签**: `#LLM`, `#HTML`, `#Claude`, `#AI-assisted development`, `#documentation`

---

<a id="item-5"></a>
## [数学家使用 ChatGPT 5.5 Pro 引发 AI 研究讨论](https://gowers.wordpress.com/2026/05/08/a-recent-experience-with-chatgpt-5-5-pro/) ⭐️ 8.0/10

菲尔兹奖得主蒂莫西·高尔斯发布博客文章，详细描述了他与 ChatGPT 5.5 Pro 的互动，突出了其生成新颖数学想法的能力，但也指出了其概念准确性上的局限性。 这一讨论意义重大，因为它反映了 AI 在学术研究中日益增长的作用，尤其是在数学领域，可能改变博士生的培养方式和思想的评估方式。 ChatGPT 5.5 Pro 于 2026 年 4 月 23 日发布，不向免费用户开放；该模型展示了高级推理能力，但仍会犯概念性错误，需要专家监督。

hackernews · _alternator_ · May 9, 02:41 · [社区讨论](https://news.ycombinator.com/item?id=48071262)

**背景**: ChatGPT 5.5 Pro 是 OpenAI 的大型语言模型，代号"Spud"。它是对 GPT-5 的迭代改进，具有更强的推理和多模态能力。该模型在数学领域的表现引发了关于 AI 在思想生成中的作用以及研究未来的讨论。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/GPT-5.5">GPT - 5 . 5 - Wikipedia</a></li>

</ul>
</details>

**社区讨论**: 来自一位物理学教授和其他研究人员的社区评论强调，虽然像 ChatGPT 5.5 Pro 这样的 LLM 在捕捉错误和提示联系方面很有用，但需要专家知识来识别概念性错误。讨论涉及思想的价值在于其稀缺性还是实用性，以及 AI 可能如何改变学术研究的格局。

**标签**: `#AI`, `#ChatGPT`, `#mathematics`, `#research`, `#philosophy`

---

<a id="item-6"></a>
## [OpenAI 的 WebRTC 问题：文章提议 WebTransport 替代方案](https://moq.dev/blog/webrtc-is-the-problem/) ⭐️ 8.0/10

moq.dev 上的一篇博文认为，WebRTC 的架构从根本上不适合 OpenAI 实时 API 的需求，并提出 WebTransport 作为低延迟 AI 交互的更好替代方案。 这场辩论凸显了 AI 实时通信协议可能发生的转变，影响开发者构建交互式 AI 服务的方式以及更广泛的 WebRTC 生态系统。 该文章批评 WebRTC 强制性的 STUN/DTLS 握手开销以及缺乏应用层缓冲，同时推崇 WebTransport 使用 QUIC 来减少延迟并提高客户端-服务器效率。

hackernews · atgctg · May 7, 17:11 · [社区讨论](https://news.ycombinator.com/item?id=48051951)

**背景**: WebRTC（Web 实时通信）是一种广泛使用的浏览器视频/音频/数据通信协议，依赖 RTP、STUN 和 DTLS 进行点对点连接。WebTransport 是一种较新的 API，利用 QUIC 和 HTTP/3，专为低开销的高效客户端-服务器通信而设计。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/WebRTC">WebRTC - Wikipedia</a></li>
<li><a href="https://developer.mozilla.org/en-US/docs/Web/API/WebRTC_API">WebRTC API - MDN Web Docs - Mozilla</a></li>
<li><a href="https://www.videosdk.live/developer-hub/webtransport/webrtc-vs-webtransport">WebRTC vs WebTransport: Comparison Guide - VideoSDK</a></li>

</ul>
</details>

**社区讨论**: 文章的评论反映了激烈的辩论：一些人批评作者对 WebRTC 设计的描述，其他人分享替代实现（例如类似 Alexa 的持久连接），还有一些人提议本地处理语音转文本以减少延迟。

**标签**: `#WebRTC`, `#OpenAI`, `#real-time AI`, `#WebTransport`, `#systems design`

---

<a id="item-7"></a>
## [AI 加速漏洞披露文化的崩溃](https://www.jefftk.com/p/ai-is-breaking-two-vulnerability-cultures) ⭐️ 8.0/10

这种转变可能从根本上改变漏洞管理方式，可能导致更短的禁运期甚至强制完全披露，从而让补丁周期较慢的组织面临更大风险。 催化剂包括开源软件的大量采用和逆向工具的改进，而不仅仅是 LLM。社区评论者指出这一趋势早于 AI，并以 Log4Shell 为例，补丁在 CVE 披露前就被利用了。

hackernews · speckx · May 8, 17:55 · [社区讨论](https://news.ycombinator.com/item?id=48066524)

**背景**: 漏洞披露文化是指围绕安全漏洞如何披露的规范：'完全披露'当即发布细节，而'负责任披露'则在公开发布前与供应商协调。由开源和更好的反编译工具推动的软件透明度，使得攻击者即使在官方披露之前也能从补丁中推断出漏洞。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.bugcrowd.com/blog/vulnerability-disclosure-policy-what-is-it-why-is-it-important/">Vulnerability Disclosure Policy: What is It & Why is it... | @Bugcrowd</a></li>
<li><a href="https://www.backslash.security/blog/the-sbom-revolution-mastering-software-transparency-in-the-age-of-cyber-resilience">The SBOM Revolution: Mastering Software Transparency ... - Backslash</a></li>

</ul>
</details>

**社区讨论**: 评论者大多同意这一趋势早于 AI，但承认 AI 加速了它。有人主张私有补丁或更短的禁运期，而另一些人指出快速补丁的组织没问题，即使利用生成更便宜，协调披露仍然重要。

**标签**: `#security`, `#vulnerability disclosure`, `#AI`, `#software transparency`, `#open source`

---

<a id="item-8"></a>
## [React2Shell：React 服务器组件中的严重 RCE 漏洞](https://lachlan.nz/blog/the-react2shell-story/) ⭐️ 8.0/10

安全研究员 Lachlan 在 React 服务器组件中发现了一个名为 React2Shell 的严重远程代码执行漏洞，他负责任地进行了披露，并与 Meta 合作进行了修复。 该漏洞可能允许攻击者在运行 React 服务器组件的服务器上执行任意代码，对许多现代 Web 应用构成严重安全风险。负责任地披露和与 Meta 的合作凸显了 React 生态系统中安全性的关键需求。 该漏洞涉及一个被描述为“迷宫”的复杂利用链，研究人员多次与 Meta 通话以验证补丁。详细的文章提供了对该漏洞的技术见解。

hackernews · mufeedvh · May 8, 16:39 · [社区讨论](https://news.ycombinator.com/item?id=48065511)

**背景**: React 服务器组件 (RSC) 是 React 的一项功能，允许在服务器上渲染组件，减少客户端 JavaScript 并提高性能。远程代码执行 (RCE) 是一种安全漏洞，使攻击者能够从远程位置在目标系统上运行任意代码。React2Shell 漏洞暴露了 RSC 处理某些输入时的缺陷，可能导致 RCE。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/React_Server_Components">React Server Components</a></li>
<li><a href="https://www.linkedin.com/pulse/from-input-intrusion-how-remote-code-execution-work-paul-bamidele-mb8we">From Input to Intrusion: How Remote Code Execution Attacks Work</a></li>
<li><a href="https://medium.com/@QuantumCoder99/why-react-server-components-are-the-future-and-what-that-means-for-you-ca5a984760a0">Why React Server Components Are the Future (and What...) | Medium</a></li>

</ul>
</details>

**社区讨论**: 社区反应总体积极，Guillermo Rauch 赞扬了 Lachlan 的负责任披露和合作。一些评论者对 React 服务器组件的复杂性表示怀疑，而另一些则重视文章中分享的技术细节。也有人对网站设计提出了小抱怨。

**标签**: `#security`, `#react`, `#vulnerability`, `#RSC`

---

<a id="item-9"></a>
## [AWS 弗吉尼亚北部宕机解决，凸显 us-east-1 脆弱性](https://www.cnbc.com/2026/05/08/aws-outage-data-center-fanduel-coinbase.html) ⭐️ 8.0/10

2026 年 5 月 8 日，AWS 弗吉尼亚北部数据中心（us-east-1）因过热导致宕机，影响 FanDuel 和 Coinbase 等服务，现已修复。 该事件凸显了 us-east-1 区域存在的系统性风险，该区域承载大量关键互联网服务，再次引发关于云可靠性和多区域架构的讨论。 据 AWS 称，此次宕机由冷却设备故障导致的过热引起；EC2 和 RDS 等服务受损，故障持续数小时后完全恢复。

hackernews · christhecaribou · May 8, 03:31 · [社区讨论](https://news.ycombinator.com/item?id=48058197)

**背景**: AWS us-east-1 是该公司的首个且最繁忙的区域，承载着不成比例的互联网流量和众多主要服务。AWS 区域由多个可用区（AZ）组成以实现冗余，但如果应用程序未正确分布，单个可用区的故障仍可能造成广泛影响。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.statuscake.com/blog/when-aws-us-east-1-fails-much-of-the-internet-fails-with-it/">When AWS us - east - 1 Fails, Much of the Internet Fails... - StatusCake</a></li>
<li><a href="https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/using-regions-availability-zones.html">Regions and Zones - Amazon Elastic Compute Cloud</a></li>
<li><a href="https://en.wikipedia.org/wiki/Amazon_Web_Services">Amazon Web Services - Wikipedia</a></li>

</ul>
</details>

**社区讨论**: 评论表达了对 us-east-1 可靠性的担忧，用户指出它仍然是单点故障。一些讨论涉及基于宕机信息进行内幕交易的可能性，其他人则质疑 AWS 数据中心的冷却容量规划。

**标签**: `#AWS`, `#outage`, `#cloud computing`, `#reliability`, `#us-east-1`

---

<a id="item-10"></a>
## [Anthropic 的 'Teaching Claude Why' 方法减少 AI 误对齐](https://www.anthropic.com/research/teaching-claude-why) ⭐️ 8.0/10

Anthropic 发布了 'Teaching Claude Why' 方法，通过训练模型推理价值观，仅用 300 万 token 的数据就大幅降低了误对齐率。 这项研究解决了关键的 AI 对齐问题，旨在确保 AI 系统可靠地遵循人类意图。该方法的效率表明，基于价值观的推理训练可能成为提升 AI 安全性的实用工具。 该方法仅用 300 万 token 的训练数据就实现了误对齐降低。该技术还通过 Anthropic 的 Model Spec Midtraining 推广到开放权重模型，并已发布针对 Llama 3.1 8B、Qwen 2.5 32B 和 Qwen 3 32B 的微调版本。

hackernews · pretext · May 8, 17:59 · [社区讨论](https://news.ycombinator.com/item?id=48066592)

**背景**: AI 对齐研究旨在确保 AI 系统按照人类价值观和目标行动。传统方法如基于人类反馈的强化学习通常训练模型模仿期望行为，而 'Teaching Claude Why' 增加了对潜在价值观的明确推理，可能实现更稳健的对齐。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.anthropic.com/research/teaching-claude-why">Teaching Claude why \ Anthropic</a></li>

</ul>
</details>

**社区讨论**: 评论者指出该方法可推广到开放模型，并赞赏其极少的数据需求，有人甚至设想未来可实现个人定制对齐。但也有人质疑对齐的定义及其现实影响，怀疑者则指出已有强大模型并未引发事故。

**标签**: `#ai-alignment`, `#value-learning`, `#anthropic`, `#ai-safety`, `#large-language-models`

---

<a id="item-11"></a>
## [Mozilla 借助 Claude Mythos 预览版加固 Firefox](https://simonwillison.net/2026/May/7/firefox-claude-mythos/#atom-everything) ⭐️ 8.0/10

Mozilla 利用 Anthropic 的 Claude Mythos 预览版发现并修复了 Firefox 中的数百个安全漏洞，每月安全修复数量从约 20-30 个跃升至 2026 年 4 月的 423 个。 这展示了 AI 辅助安全审计的巨大进步，从生成“不受欢迎的垃圾信息”转变为产生可操作、高信噪比的漏洞报告，显著减轻了项目维护负担。 发现的漏洞包括一个存在 20 年的 XSLT 漏洞和一个存在 15 年的 HTML <legend> 元素漏洞；许多尝试的攻击被 Firefox 现有的纵深防御措施阻止，这令人安心。

rss · Simon Willison · May 7, 17:56

**背景**: Claude Mythos 是 Anthropic 最先进的前沿模型，于 2026 年 4 月以预览版形式向特定公司发布。它代表了网络安全领域具有最先进性能的新模型类别。Mozilla 改进了利用这些模型的技术，包括引导、扩展和堆叠它们，以放大信号并过滤噪声。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Claude_Mythos_Preview">Claude Mythos Preview</a></li>
<li><a href="https://grokipedia.com/page/Claude_Mythos_Preview">Claude Mythos Preview</a></li>

</ul>
</details>

**标签**: `#firefox`, `#security`, `#AI`, `#vulnerability detection`, `#LLM`

---

<a id="item-12"></a>
## [Anthropic 拟融资数百亿美元，估值逼近万亿美元](https://www.ft.com/content/a40cafcc-0fa4-4e70-9e24-90d826aea56d) ⭐️ 8.0/10

据报道，Anthropic 正计划在今年夏天进行一轮高达数百亿美元的新融资，有望将其估值推至近 1 万亿美元，超过 OpenAI。 这标志着 AI 行业领导地位和投资者情绪的重大转变，Anthropic 可能成为估值最高的 AI 公司，影响行业竞争和资源分配。 该估值基于 Forge Global 等平台的二级市场交易数据，Anthropic 的隐含估值已达到 1 至 1.2 万亿美元，而 OpenAI 约为 8800 亿美元。Anthropic 在 2 月份刚完成 300 亿美元融资，估值为 3800 亿美元。

telegram · zaihuapd · May 8, 11:15

**背景**: Anthropic 是一家 AI 安全公司，也是 OpenAI 的主要竞争对手。私募二级市场允许交易上市前股份，为私营公司提供流动性和价格发现。估值飙升反映了投资者对 AI 基础设施和企业级应用的强劲需求。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://forgeglobal.com/tandem_stock/">Invest and Sell Tandem Stock - Forge</a></li>
<li><a href="https://gadgetbond.com/anthropic-trillion-dollar-valuation-secondary-markets/">Investors chase Anthropic as its secondary value tops $1 trillion</a></li>
<li><a href="https://en.wikipedia.org/wiki/Private-equity_secondary_market">Private-equity secondary market</a></li>

</ul>
</details>

**标签**: `#Anthropic`, `#AI funding`, `#valuation`, `#industry competition`, `#OpenAI`

---

<a id="item-13"></a>
## [美国怀疑英伟达芯片经泰国走私至中国](https://www.bloomberg.com/news/articles/2026-05-08/us-said-to-suspect-nvidia-chips-smuggled-to-alibaba-via-thailand) ⭐️ 8.0/10

美国检方怀疑泰国公司 OBON Corp.将装有先进英伟达芯片、价值 25 亿美元的 Super Micro 服务器走私至中国，阿里巴巴被列为终端客户之一。 此案可能加剧美中半导体出口管制紧张局势，并促使美国重新评估对泰国的芯片限制，可能影响两国的人工智能发展。 OBON 曾参与创建泰国主权 AI 云 Siam AI，后者获得了英伟达合作伙伴地位。阿里巴巴否认与 Super Micro 或 OBON 有任何业务关系，前 Siam AI 首席执行官声称已离开 OBON，且公司未涉及走私。

telegram · zaihuapd · May 8, 13:23

**背景**: 美国已实施出口管制以阻止先进半导体流入中国，尤其是用于人工智能的英伟达高端芯片。泰国已成为潜在的转运枢纽。此次调查凸显了执行这些管制以及涉及复杂供应链的挑战。

**标签**: `#Nvidia`, `#chip export controls`, `#smuggling`, `#Alibaba`, `#geopolitics`

---

<a id="item-14"></a>
## [DeepSeek 估值目标 450 亿美元，国家基金领投](https://t.me/zaihuapd/41289) ⭐️ 8.0/10

据称 DeepSeek 正寻求约 450 亿美元估值的首轮大规模外部融资，中国国家集成电路产业投资基金正洽谈领投。 此轮融资将标志着国资更深介入中国 AI 领域，可能加速 DeepSeek 的发展并加剧地缘政治竞争。同时，在美方出口管制背景下，这也体现了对 DeepSeek 技术的强烈信心。 国家集成电路产业投资基金（又称“大基金”）成立于 2014 年，旨在推动中国半导体自主可控。若融资完成，这将是 DeepSeek 首次以如此高估值进行外部融资。

telegram · zaihuapd · May 8, 14:59

**背景**: DeepSeek 是一家中国 AI 公司，以开发高效节能的大语言模型而闻名，与 OpenAI 等全球企业竞争。国家集成电路产业投资基金是国资背景的投资实体，专注于投资国内半导体及相关科技公司，以减少对外国技术的依赖。此次潜在投资显示了中国政府对 AI 作为关键科技领域的战略重视。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/DeepSeek">DeepSeek - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/China_Integrated_Circuit_Industry_Investment_Fund">China Integrated Circuit Industry Investment Fund - Wikipedia</a></li>
<li><a href="https://www.scmp.com/tech/enterprises/article/2145422/how-chinas-big-fund-helping-country-catch-global-semiconductor-race">How China ’s ‘Big Fund ’ is helping the country catch up in chip race</a></li>

</ul>
</details>

**标签**: `#DeepSeek`, `#AI`, `#funding`, `#China`, `#industry investment`

---

<a id="item-15"></a>
## [百度发布文心大模型 5.1，宣称高效预训练，中国搜索排名第一](https://mp.weixin.qq.com/s/_I9ziafHheXiJpA-QY2F7A) ⭐️ 8.0/10

百度发布了文心大模型 5.1，该模型采用“多维弹性预训练”，以业界同规模模型约 6%的预训练成本实现领先性能，现已上线千帆模型广场和文心一言。 此次发布使百度在中国 AI 领域占据竞争地位，声称在 LMArena 搜索基准测试中得分最高，并且 Agent 能力超越 DeepSeek-V4-Pro，可能加速百度 AI 服务的采用。 文心 5.1 在 LMArena 搜索榜以 1223 分位列国内第一、全球第四；其 Agent 能力超越 DeepSeek-V4-Pro，创意写作与 Gemini 3.1 Pro 相当，推理能力接近业界领先的闭源模型。

telegram · zaihuapd · May 9, 07:45

**背景**: 大型语言模型的预训练通常计算成本高昂，费用常达数百万美元。“多维弹性预训练”是一种创新方法，据称可在训练过程中动态调整资源使用，大幅降低成本的同时保持或提升性能。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arxiv.org/html/2510.06882v2">Multi - Dimensional Autoscaling of Stream Processing Services on...</a></li>
<li><a href="https://www.emergentmind.com/topics/elastic-training-paradigm">Elastic Training Paradigm</a></li>

</ul>
</details>

**标签**: `#AI`, `#Large Language Model`, `#Baidu`, `#ERNIE`, `#NLP`

---