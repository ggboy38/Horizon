---
layout: default
title: "Horizon Summary: 2026-05-16 (ZH)"
date: 2026-05-16
lang: zh
---

> From 38 items, 11 important content pieces were selected

---

1. [vllm 0.21.0 发布，支持 KV 卸载与推测解码](#item-1) ⭐️ 9.0/10
2. [Project Zero 披露 Pixel 10 零点击漏洞链](#item-2) ⭐️ 9.0/10
3. [古腾堡计划网站改进引发社区讨论](#item-3) ⭐️ 8.0/10
4. [盲目依赖 AI 是'AI 精神病'，Mitchell Hashimoto 警告](#item-4) ⭐️ 8.0/10
5. [Orthrus 实现 Qwen3 推理加速最高 7.8 倍，输出完全无损](#item-5) ⭐️ 8.0/10
6. [前沿 AI 打破了开放式 CTF 形式](#item-6) ⭐️ 8.0/10
7. [购买非苹果非谷歌智能手机：挑战重重](#item-7) ⭐️ 8.0/10
8. [Scott Alexander 用林迪定律探讨 AI 扩展极限](#item-8) ⭐️ 8.0/10
9. [苹果与 OpenAI 合作裂痕，OpenAI 或采取法律行动](#item-9) ⭐️ 8.0/10
10. [美国司法部要求苹果和谷歌提交 10 万多名汽车应用用户信息](#item-10) ⭐️ 8.0/10
11. [OpenAI 与马耳他合作，免费提供 ChatGPT Plus 并推广 AI 素养](#item-11) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [vllm 0.21.0 发布，支持 KV 卸载与推测解码](https://github.com/vllm-project/vllm/releases/tag/v0.21.0) ⭐️ 9.0/10

vllm 0.21.0 引入了基于混合内存分配器（HMA）的 KV 缓存卸载，以及支持思考预算的推测解码以用于推理模型，同时带来了弃用 Transformers v4 和需要 C++20 等重大变更。 这些改进通过将 KV 缓存卸载到 CPU 来减少 GPU 内存压力，并通过推测解码加速推理模型，从而提升了 LLM 推理效率，惠及大规模部署大型语言模型的人工智能/机器学习社区。 关键技术细节包括完全启用 HMA 进行 KV 卸载、调度端滑动窗口组支持，以及针对 Blackwell GPU 的新 TOKENSPEED_MLA 注意力后端。该版本还弃用了 Transformers v4（需要迁移至 v5），并要求使用兼容 C++20 的编译器。

github · khluu · May 15, 08:44

**背景**: KV 缓存是 LLM 推理中用于避免重复计算每个 token 的键值对的内存存储，但会消耗大量 GPU 内存。KV 卸载将部分缓存移至 CPU 内存以释放 GPU 资源。混合内存分配器（HMA）是 vllm 中一种新的内存管理架构，可高效处理异构内存（GPU/CPU）。推测解码使用较小的草稿模型提出 token 序列，再由大模型一次性验证，从而降低延迟并保持输出分布不变。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://vllm-project.github.io/2026/01/08/kv-offloading-connector.html">Inside vLLM's New KV Offloading Connector: Smarter Memory Transfer for ...</a></li>
<li><a href="https://en.wikipedia.org/wiki/Speculative_decoding">Speculative decoding</a></li>
<li><a href="https://www.youtube.com/watch?v=0cUFUtNW_S8">[ vLLM Office Hours #30] Hybrid Memory Allocator ... - YouTube</a></li>

</ul>
</details>

**标签**: `#vllm`, `#LLM inference`, `#breaking changes`, `#speculative decoding`, `#GPU optimization`

---

<a id="item-2"></a>
## [Project Zero 披露 Pixel 10 零点击漏洞链](https://projectzero.google/2026/05/pixel-10-exploit.html) ⭐️ 9.0/10

Google Project Zero 公布了针对 Pixel 10 的零点击漏洞链，展示了设备端 AI 解码消息带来的新攻击面。该漏洞无需用户交互即可实现远程代码执行。 这一发现表明，设备端 AI 功能虽然便利，但显著扩大了智能手机的攻击面。它凸显了对所有 Android 设备上 AI 驱动的消息处理进行安全审查的紧迫性。 该漏洞链结合了两个漏洞：Dolby 音频处理中的零点击漏洞（已于 2026 年 1 月修复）和一个自定义视频编解码器驱动漏洞。它实现了远程完全 root 权限，供应商在 90 天内完成了修复。

hackernews · happyhardcore · May 15, 13:39 · [社区讨论](https://news.ycombinator.com/item?id=48148460)

**背景**: 零点击漏洞无需受害者执行任何操作（如打开文件或点击链接），因此极其危险。设备端 AI 解码会在用户查看消息之前处理传入的短信或媒体，从而增加潜在攻击面。Project Zero 是谷歌的精英安全团队，通过公开披露漏洞来推动更快修复。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://projectzero.google/2026/05/pixel-10-exploit.html">A 0-click exploit chain for the Pixel 10: When a Door Closes, a Window Opens - Project Zero</a></li>
<li><a href="https://www.kaspersky.com/resource-center/definitions/what-is-zero-click-malware">Zero-Click Exploits</a></li>
<li><a href="https://netlas.io/blog/zero_click_exploits/">Zero-Click Exploits - Netlas Blog</a></li>

</ul>
</details>

**社区讨论**: 评论者担心设备端 AI 功能重复过去的错误，预处理消息创造了新的零点击风险。一些人欣慰于 Google 在 90 天内修复，但担忧其他 Android 厂商的响应速度。还有关于内核代码的技术讨论，以及认为漏洞披露变得更为频繁的观感。

**标签**: `#security`, `#zero-click exploit`, `#Android`, `#Project Zero`

---

<a id="item-3"></a>
## [古腾堡计划网站改进引发社区讨论](https://www.gutenberg.org/) ⭐️ 8.0/10

古腾堡计划的一位程序员宣布了正在进行的网站改进，包括界面焕新和即将推出的新功能。 古腾堡计划是基础性的开放获取数字图书馆，其持续改进使公共领域文学作品在全球范围内更易获取，鼓励阅读和学术使用。 改进工作持续数月，更多变化即将到来；但意大利用户报告因司法扣押令导致无法访问。

hackernews · JSeiko · May 15, 16:15 · [社区讨论](https://news.ycombinator.com/item?id=48150431)

**背景**: 古腾堡计划由迈克尔·S·哈特于 1971 年创立，是最古老的数字图书馆，提供超过 7 万本免费公共领域电子书。最初是利用 ARPANET 上大型主机的学生项目。该网站随着互联网发展而成长，至今仍是经典文学的重要资源。

**社区讨论**: 社区成员对更新表示赞赏，一位用户分享了古腾堡计划如何丰富其父亲阅读的个人故事。其他人讨论了与电子阅读器原生集成的可能性，而一位意大利用户报告了因法律扣押导致的地区访问限制。

**标签**: `#Project Gutenberg`, `#digital libraries`, `#open access`, `#ebooks`

---

<a id="item-4"></a>
## [盲目依赖 AI 是'AI 精神病'，Mitchell Hashimoto 警告](https://twitter.com/mitchellh/status/2055380239711457578) ⭐️ 8.0/10

Vagrant 创建者、HashiCorp 创始人 Mitchell Hashimoto 发布推文，批评公司盲目依赖 AI 而不进行批判性思考，并用'AI 精神病'这一术语来描述这一现象。 这一评论在科技界引起强烈共鸣，因为许多组织正在大力投资 AI 却缺乏适当评估，可能导致错误决策并助长行业炒作。 该推文在 Hacker News 上以 1641 分和 861 条评论获得 8.0/10 的高分，显示出高度的社区参与。讨论揭示了关于在利用 AI 作为工具与维护人类批判性思维之间平衡的细致辩论。

hackernews · reasonableklout · May 15, 20:26 · [社区讨论](https://news.ycombinator.com/item?id=48153379)

**背景**: 'AI 精神病'是指对 AI 工具的非理性过度依赖，决策仅仅因为'AI 这么说的'而做出，当 AI 输出不正确或有偏见时，往往导致不良结果。该术语反映了技术专家对软件工程和业务流程中不加批判地采用 AI 的日益担忧，尤其是在公司急于整合 AI 而不验证其价值的情况下。

**社区讨论**: 评论者大多同意 Mitchell 的观点，分享了管理推动 AI 使用但没有明确收益的个人经历。有些人区分了将 AI 作为生产力工具和盲目信任 AI，另一些人对炒作和采用 AI 的压力表示沮丧。少数人指出，AI 可能有帮助，但不应取代人类推理。

**标签**: `#AI`, `#software engineering`, `#critical thinking`, `#industry trends`, `#hype`

---

<a id="item-5"></a>
## [Orthrus 实现 Qwen3 推理加速最高 7.8 倍，输出完全无损](https://github.com/chiennv2000/orthrus) ⭐️ 8.0/10

Orthrus 提出了一种双架构框架，在 Qwen3 推理中实现了每前向传播最多 7.8 倍的令牌加速，并且可证明地保持了原自回归模型的精确输出分布。 这一突破在不牺牲质量的情况下大幅降低了 LLM 推理延迟，使大型模型在本地部署和实时应用中更加实用。同时，它为结合自回归模型和扩散模型的优势开辟了新方向。 Orthrus 通过双视角扩散解码方法实现加速：并行运行一个小型扩散模型生成多个令牌，同时自回归的 Qwen3 验证输出以确保保真度。该系统包含一个学习到的草稿模型和一个验证步骤，以确保输出分布完全相同。

hackernews · FranckDernoncou · May 15, 22:38 · [社区讨论](https://news.ycombinator.com/item?id=48154865)

**背景**: 自回归 LLM 逐个生成令牌，处理长序列时可能较慢。而扩散模型可以并行生成多个令牌，但通常会产生不同的输出分布。Orthrus 借鉴推测解码的思路，采用双架构方法，将扩散模型的速度与自回归模型的保真度结合起来，从而弥合了这一差距。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/chiennv2000/orthrus">GitHub - chiennv2000/orthrus: Fast, lossless LLM inference ...</a></li>
<li><a href="https://arxiv.org/html/2605.12825v1">Orthrus: Memory-Efficient Parallel Token Generation via Dual ...</a></li>

</ul>
</details>

**社区讨论**: 社区成员对这种新颖方法表示热情，有人指出此前竟然没有人尝试过这种做法。大家提出了关于计算量缩减权衡的问题，以及将其与 GGUF/量化模型集成的潜力，并和完全扩散变压器进行了比较。总体情绪积极且充满好奇。

**标签**: `#efficient inference`, `#Qwen3`, `#LLM optimization`, `#transformer acceleration`

---

<a id="item-6"></a>
## [前沿 AI 打破了开放式 CTF 形式](https://kabir.au/blog/the-ctf-scene-is-dead) ⭐️ 8.0/10

一篇文章指出，先进的 AI 模型已经使传统的夺旗赛（CTF）变得不再困难，可能终结开放式 CTF 形式。 这威胁到了网络安全教育和竞争性黑客的核心，迫使人们重新思考当 AI 能瞬间解决挑战时，如何测试人类技能。 文章作者声称，前沿 AI 可以在无需人类干预的情况下解决大多数 CTF 挑战，降低了竞赛对技能评估的价值。

hackernews · frays · May 16, 07:01 · [社区讨论](https://news.ycombinator.com/item?id=48157559)

**背景**: 夺旗赛（CTF）是一种网络安全竞赛，参赛者通过解决挑战来寻找隐藏的“旗帜”。传统上，CTF 测试密码学、逆向工程和利用等方面的动手技能。像 GPT-4 和专门代理这样的 AI 模型最近展示了自主解决此类任务的能力，引发了对这些竞赛未来的质疑。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Capture_the_flag_(cybersecurity)">Capture the flag (cybersecurity) - Wikipedia</a></li>
<li><a href="https://www.huntress.com/cybersecurity-education/cybersecurity-awareness/capture-the-flag">Cybersecurity Capture the Flag | Hands-On CTF by Huntress | Huntress</a></li>
<li><a href="https://www.hackthebox.com/hacker/ctf">Capture The Flag Competitions For Hackers | Hack The Box CTFs</a></li>

</ul>
</details>

**社区讨论**: 评论者反应不一：有人指出与 AI 对教育影响的相似之处，有人尝试改进混淆器以对抗 AI 反混淆，还有人建议线下比赛作为解决方案。还有讨论关于文章标题变化导致的困惑。

**标签**: `#AI`, `#CTF`, `#cybersecurity`, `#LLMs`, `#education`

---

<a id="item-7"></a>
## [购买非苹果非谷歌智能手机：挑战重重](https://www.theregister.com/on-prem/2026/05/01/where-to-buy-a-non-apple-non-google-smartphone/5219681) ⭐️ 8.0/10

一篇《The Register》的文章及其社区讨论探讨了购买和使用不运行 iOS 或带有谷歌服务的 Android 智能手机的实际困难，强调了生态系统锁定和关键应用的依赖问题。 对于寻求苹果和谷歌替代品的注重隐私的用户来说，缺乏支持银行、政府和交通等关键应用的可行选项使切换变得极为困难，从而巩固了双头垄断的市场控制。 社区评论指出，即使是像 GrapheneOS 这样的非谷歌 Android 分支，某些应用仍需依赖沙盒化的谷歌服务，而华为的 HarmonyOS 等设备也面临类似的谷歌应用兼容性问题。

hackernews · _____k · May 16, 08:34 · [社区讨论](https://news.ycombinator.com/item?id=48158130)

**背景**: 中国以外的大多数智能手机依赖苹果的 iOS 或带有谷歌移动服务（GMS）的 Android。虽然存在像 GrapheneOS（针对 Pixel 设备的注重隐私的 Android 分支）这样的替代方案，但许多关键应用——尤其是银行和身份验证应用——需要 GMS 或 iOS 的 API，从而形成了难以摆脱的生态系统锁定。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/GrapheneOS">GrapheneOS</a></li>
<li><a href="https://grapheneos.org/">GrapheneOS: the private and secure mobile OS</a></li>
<li><a href="https://smartphones.gadgethacks.com/news/families-ditch-apps-for-apple-ecosystem-lock-in/">Families Ditch Apps for Apple Ecosystem Lock-In << Smartphones :: Gadget Hacks</a></li>

</ul>
</details>

**社区讨论**: 评论者指出了现实中的痛点：银行和政府应用在非标准 Android 系统上经常无法使用，一些用户被迫携带第二台设备或使用远程访问工具。Pixel 手机上的 GrapheneOS 被赞为当前最佳选择，但缺乏多样化的硬件（例如支持美国频段的基础功能手机）仍然令人沮丧。

**标签**: `#Smartphones`, `#Privacy`, `#Android alternatives`, `#GrapheneOS`, `#Community discussion`

---

<a id="item-8"></a>
## [Scott Alexander 用林迪定律探讨 AI 扩展极限](https://www.astralcodexten.com/p/the-sigmoids-wont-save-you) ⭐️ 8.0/10

Scott Alexander 的文章《sigmoids 救不了你》认为 AI 进展不可预测，可能不会延续当前的扩展趋势，并运用林迪定律质疑指数级持续改进的假设。 这一观点挑战了广泛持有的信念，即 AI 性能将随算力和数据的增加而持续扩展，这对于做出长期决策的研究人员、投资者和政策制定者至关重要。它促使社区考虑 AI 发展的更多可能性。 文章运用林迪定律（认为非易耗品的未来预期寿命与其当前年龄成正比）指出，如果 AI 扩展至今是线性的，那么它可能继续线性增长，而不是像 sigmoid 曲线预测的那样达到平台期。但作者也指出这类预测存在固有不确定性。

hackernews · Tomte · May 15, 10:51 · [社区讨论](https://news.ycombinator.com/item?id=48147021)

**背景**: 在机器学习中，sigmoid 函数是一条 S 形曲线，用于模拟会饱和的增长，常被用作神经网络的激活函数。林迪定律由纳西姆·塔勒布推广，认为非易耗技术或思想存在的时间越长，它可能持续的时间就越长。Scott Alexander 是一位知名的理性主义博主，经常撰写关于 AI 和预测的文章。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Sigmoid_function">Sigmoid function - Wikipedia</a></li>

</ul>
</details>

**社区讨论**: 评论者就林迪定律在 AI 趋势中的适用性展开辩论，有人指出作者个人认为进步将持续。其他人指出 AI 扩展可能衡量的是与智能无关的能力，而不确定性意味着任何模型都无法自信地预测未来。

**标签**: `#AI`, `#deep learning`, `#scaling`, `#Lindy's Law`, `#machine learning`

---

<a id="item-9"></a>
## [苹果与 OpenAI 合作裂痕，OpenAI 或采取法律行动](https://www.bloomberg.com/news/articles/2026-05-14/openai-apple-partnership-frays-setting-up-possible-legal-fight) ⭐️ 8.0/10

苹果与 OpenAI 的合作关系正在恶化，OpenAI 正考虑对苹果采取法律行动，指控其未充分推广 ChatGPT 集成，导致订阅转化远不及预期。苹果计划在 2026 年 WWDC 上向 Claude、Gemini 等第三方模型开放 Siri，进一步削弱 OpenAI 的独家地位。 这一裂痕可能重塑消费设备中的 AI 集成格局，或促使苹果建立更开放的生态系统，与多个 AI 合作伙伴合作。两大科技巨头之间的法律行动可能为 AI 合作合同和收入分成树立先例。 ChatGPT 在苹果系统中的集成被指入口隐蔽、功能受限，多数用户仍直接使用独立 App。同时，苹果对 OpenAI 的隐私标准、硬件业务以及挖角行为感到不满。

telegram · zaihuapd · May 15, 12:59

**背景**: 苹果与 OpenAI 于 2024 年宣布合作，将 ChatGPT 集成到 Siri 中，旨在增强 Siri 的生成式 AI 能力。ChatGPT 是 OpenAI 开发的大型语言模型，能够生成类似人类的文本、代码等。同样，Anthropic 的 Claude 和 Google 的 Gemini 是竞争性 AI 模型，苹果现在可能允许它们接入 Siri。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Claude_AI">Claude AI</a></li>
<li><a href="https://en.wikipedia.org/wiki/Gemini_AI">Gemini AI</a></li>

</ul>
</details>

**标签**: `#AI`, `#OpenAI`, `#Apple`, `#partnership`, `#legal`

---

<a id="item-10"></a>
## [美国司法部要求苹果和谷歌提交 10 万多名汽车应用用户信息](https://9to5mac.com/2026/05/15/doj-reportedly-demands-apple-and-google-identify-over-100000-users-of-car-app/) ⭐️ 8.0/10

美国司法部已向苹果、谷歌和亚马逊发出传票，要求提供超过 10 万名 EZ Lynk 汽车改装应用用户的身份、住址和购买记录，作为调查可能违反《清洁空气法》的一部分。 司法部的大规模数据请求引发了重大的隐私和法律问题，可能为政府通过技术平台获取用户数据开创先例。这也凸显了对售后排放作弊装置的持续打击。 传票于今年 3 月和 4 月发出，据报道苹果和谷歌准备挑战这一请求，认为其范围过宽，与调查目的不相称。EZ Lynk 否认其产品主要用于绕过排放控制。

telegram · zaihuapd · May 16, 05:34

**背景**: EZ Lynk 是一款基于云的车辆诊断和调校平台，允许用户修改发动机控制单元（ECU）参数，可能禁用或绕过排放控制。此类改装在《清洁空气法》下被视为“作弊装置”，司法部一直在调查制造和销售这些设备的公司。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://ezlynk.com/">EZ LYNK®: The Future of Vehicle Diagnostics & Control</a></li>
<li><a href="https://en.wikipedia.org/wiki/Defeat_device">Defeat device - Wikipedia</a></li>

</ul>
</details>

**标签**: `#privacy`, `#legal`, `#apple`, `#google`, `#data request`

---

<a id="item-11"></a>
## [OpenAI 与马耳他合作，免费提供 ChatGPT Plus 并推广 AI 素养](https://openai.com/index/malta-chatgpt-plus-partnership/) ⭐️ 8.0/10

OpenAI 与马耳他政府宣布了一项首个国家级合作，所有马耳他公民在完成马耳他大学开发的 AI 素养课程后，可获得一年免费 ChatGPT Plus 访问权限。 这一举措标志着 AI 普及的重要里程碑，将免费使用先进 AI 工具与强制性责任教育相结合，为全球国家 AI 政策树立了先例。 该计划名为“AI for All”，将于 5 月启动，由马耳他数字创新局管理，并逐步扩展至海外马耳他公民。

telegram · zaihuapd · May 16, 10:40

**背景**: ChatGPT Plus 是 OpenAI ChatGPT 的订阅版本，提供优先访问、更快响应和额外功能。AI 素养课程旨在教育公众了解 AI 能力和伦理考量，确保明智且负责任的使用。

**标签**: `#OpenAI`, `#ChatGPT`, `#Malta`, `#AI literacy`, `#government partnership`

---