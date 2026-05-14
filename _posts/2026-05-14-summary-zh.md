---
layout: default
title: "Horizon Summary: 2026-05-14 (ZH)"
date: 2026-05-14
lang: zh
---

> From 38 items, 8 important content pieces were selected

---

1. [NGINX 暴露 18 年潜伏严重 RCE 漏洞](#item-1) ⭐️ 10.0/10
2. [DeepSeek 对话系统漏洞：未闭合<think>标签泄露他人聊天记录](#item-2) ⭐️ 9.0/10
3. [RTX 5090 外接显卡搭配 M4 MacBook Air：游戏与大语言模型的惊喜](#item-3) ⭐️ 8.0/10
4. [MIT 报告研究生新生入学人数下降 20%](#item-4) ⭐️ 8.0/10
5. [Claude AI 暴力破解密码恢复 40 万美元比特币钱包](#item-5) ⭐️ 8.0/10
6. [Anthropic 与 SpaceX 合作提升 Claude AI 算力限制](#item-6) ⭐️ 8.0/10
7. [美国放行 H200 对华销售，英伟达寻求在华突破](#item-7) ⭐️ 8.0/10
8. [京东开设 AI 硬件自营专区，上架受制裁 NVIDIA GPU](#item-8) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [NGINX 暴露 18 年潜伏严重 RCE 漏洞](https://depthfirst.com/research/nginx-rift-achieving-nginx-rce-via-an-18-year-old-vulnerability) ⭐️ 10.0/10

2026 年 5 月 13 日，披露了一个严重的远程代码执行漏洞 CVE-2026-42945，CVSS v4.0 评分 9.2，影响 NGINX 从 0.6.27 到 1.30.0 的所有版本，根源是 ngx_http_rewrite_module 中的堆缓冲区溢出。 NGINX 在全球数亿台服务器上部署，包括 Kubernetes Ingress 和 API 网关等关键云原生环境，此漏洞构成巨大安全风险，远程攻击者可在无需身份验证的情况下执行任意代码。 该漏洞源于脚本引擎两遍执行流程中的状态不一致：当 rewrite 替换字符串含有问号时，模块错误计算缓冲区大小，导致第二遍时堆溢出。修复版本为 NGINX 1.31.0/1.30.1 和 NGINX Plus R36 P4/R32 P6；临时缓解方法是将未命名捕获组（$1、$2）替换为命名捕获组。

telegram · zaihuapd · May 14, 02:41

**背景**: 堆缓冲区溢出是指程序向堆分配的内存区域写入超出容量的数据，可能覆盖相邻内存并导致任意代码执行。ngx_http_rewrite_module 模块默认编译到 NGINX 中，用于使用 PCRE 正则表达式进行 URL 重写。CVSS v4.0 是通用漏洞评分系统的最新版本，相比之前版本提供了更精细和上下文感知的严重性评分。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://nginx.org/en/docs/http/ngx_http_rewrite_module.html">Module ngx_http_rewrite_module</a></li>
<li><a href="https://owasp.org/www-community/attacks/Buffer_overflow_attack">Buffer Overflow Attack | OWASP Foundation</a></li>
<li><a href="https://www.first.org/cvss/specification-document">CVSS v4.0 Specification Document</a></li>

</ul>
</details>

**标签**: `#NGINX`, `#security`, `#vulnerability`, `#RCE`, `#CVE`

---

<a id="item-2"></a>
## [DeepSeek 对话系统漏洞：未闭合<think>标签泄露他人聊天记录](https://github.com/deepseek-ai/DeepSeek-R1/issues/840) ⭐️ 9.0/10

2026 年 5 月 11 日，DeepSeek 的网络和 API 对话系统中发现了一个漏洞。攻击者可以在全新的空对话中发送未闭合的 '<think' 字符串，导致模型返回其他用户的对话历史片段，可能包含代码、密钥和隐私信息等敏感数据。 这一漏洞至关重要，因为 DeepSeek 被广泛使用，攻击者无需身份验证即可远程获取其他用户的私人数据，这削弱了人们对 AI 系统的信任，并带来严重的隐私风险。 该漏洞影响 DeepSeek 网络和 API 服务。报告者负责任地披露了漏洞，并未加以利用，该问题已在 GitHub 上公开。

telegram · zaihuapd · May 14, 13:15

**背景**: 像 DeepSeek-R1 这样的推理模型使用特殊标记如'<think>'和'</think>'来划分思维链推理。未闭合的'<think>'标签可能导致模型误解输入边界，从而引发跨用户数据泄露。会话隔离是多租户 LLM 应用中防止用户之间上下文污染的关键安全机制。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://huggingface.co/deepseek-ai/DeepSeek-R1-Distill-Qwen-32B/discussions/37">deepseek -ai/ DeepSeek -R1-Distill-Qwen-32B · [RESOLVED] Model is...</a></li>
<li><a href="https://redteams.ai/topics/walkthroughs/defense/session-isolation-patterns">Session Isolation Patterns | redteams.ai</a></li>
<li><a href="https://www.spaceo.ai/case-study/think-tag-mystery-ai-reasoning-debugging/">The Think Tag Mystery: When AI Started Showing Its Homework</a></li>

</ul>
</details>

**社区讨论**: 社区评论指出，第三方部署也出现了这种问题，一些人将其归因于模型幻觉而非纯粹的会话隔离缺陷。讨论表明，这个问题在推理模型实现中可能普遍存在。

**标签**: `#security`, `#vulnerability`, `#AI-safety`, `#DeepSeek`, `#LLM`

---

<a id="item-3"></a>
## [RTX 5090 外接显卡搭配 M4 MacBook Air：游戏与大语言模型的惊喜](https://scottjg.com/posts/2026-05-05-egpu-mac-gaming/) ⭐️ 8.0/10

一篇文章展示了如何将 RTX 5090 外接显卡用于 M4 MacBook Air，进行游戏和大语言模型推理，并在提示词处理速度上取得了惊人的提升。 这挑战了 eGPU 与 Apple Silicon Mac 不兼容的普遍认知，可能使 Mac 用户能够获得强大的 GPU 加速用于游戏和 AI 工作负载。大语言模型提示词处理速度的大幅提升，让 Mac 在本地模型推理方面更具可行性。 该设置可能依赖 Thunderbolt 连接和自定义驱动程序，因为苹果官方仅支持 Intel Mac 上的 AMD eGPU。RTX 5090 是 NVIDIA 显卡，因此克服驱动限制是一项显著成就。

hackernews · allenleee · May 14, 15:47 · [社区讨论](https://news.ycombinator.com/item?id=48137145)

**背景**: eGPU（外置显卡）是一种包含桌面级显卡的外部扩展坞，通过 Thunderbolt 连接笔记本电脑以提升图形性能。Apple Silicon Mac 采用统一内存架构，且官方不支持 eGPU（尤其是 NVIDIA 显卡），原因在于驱动和架构差异。大语言模型的提示词处理（prefill）是一个计算密集型阶段，Mac 由于内存带宽限制通常在此环节表现较慢。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.hp.com/us-en/shop/tech-takes/external-gpu-laptop-egpu-guide">Do External Graphics Cards Work for Laptops E GP Us Explained</a></li>
<li><a href="https://www.dignited.com/75312/egpu-explained/">What Is an eGPU Used For? - Dignited</a></li>
<li><a href="https://www.adaline.ai/blog/how-prompts-are-processed-in-llms-and-how-llms-reason-using-prompts">How Prompts Are Processed in LLMs and How LLMs Reason Using ...</a></li>

</ul>
</details>

**社区讨论**: 评论者表达了兴奋之情，一些人强调了这对大语言模型工作的实用价值，以及长期以来对 Apple Silicon 上虚拟机 GPU 直通的需求。有用户指出，eGPU 兼容性此前被苹果官方认为是不可能的事情。

**标签**: `#eGPU`, `#Apple Silicon`, `#gaming`, `#LLM`, `#M4 MacBook`

---

<a id="item-4"></a>
## [MIT 报告研究生新生入学人数下降 20%](https://president.mit.edu/writing-speeches/video-transcript-message-president-kornbluth-about-funding-and-talent-pipeline) ⭐️ 8.0/10

MIT 校长 Sally Kornbluth 宣布研究生新生人数减少了 20%，并将这一下降归因于资金短缺和学术界更广泛的幻灭情绪。 这一下降信号表明美国研究生教育可能存在系统性问题，包括研究资金不稳定和学术生涯吸引力下降，可能影响未来的创新和人才输送。 下降归因于资金减少导致带资助的录取名额减少，以及潜在学生对学术职业道路越来越幻灭。MIT 研究生中 41%为国际学生，因此移民政策也是一个额外因素。

hackernews · dmayo · May 14, 14:51 · [社区讨论](https://news.ycombinator.com/item?id=48136262)

**背景**: 研究生教育，尤其是 STEM 领域，通常依赖联邦拨款和大学资金来支持学生。研究资金的持续减少，加上博士完成时间长（中位数 6 年）和学术界的就业前景不佳，导致许多人质疑攻读研究生学位的价值。在 MIT 这样的顶尖机构出现的下降可能预示美国大学更广泛的趋势。

**社区讨论**: 社区评论者表达了不同观点：一些人将下降归因于研究资金减少和移民障碍，而另一些人则指出对学术界艰苦条件及糟糕就业前景的普遍幻灭。少数评论者暗示顶尖人才可能正在转向中国机构，这些机构在科学和工程领域越来越有竞争力。

**标签**: `#academia`, `#graduate-education`, `#research-funding`, `#MIT`, `#higher-education-trends`

---

<a id="item-5"></a>
## [Claude AI 暴力破解密码恢复 40 万美元比特币钱包](https://www.tomshardware.com/tech-industry/cryptocurrency/bitcoin-trader-recovers-usd400-000-using-claude-ai-after-losing-wallet-password-11-years-ago-bot-tried-3-5-trillion-passwords-before-decrypting-an-old-wallet-backup) ⭐️ 8.0/10

一位比特币交易者使用 Anthropic 的 Claude AI 恢复了一个包含 40 万美元比特币的钱包，此前他在 11 年前丢失了密码，AI 尝试了 3.5 万亿种密码组合后才成功。 这展示了 AI 在密码恢复任务中的实用价值，可能帮助其他丢失加密货币钱包访问权限的人，并凸显了 AI 在高效解决复杂暴力破解问题上的能力。 恢复成功是因为用户在一本大学笔记本中找到了旧的助记词种子短语，大大缩小了密码搜索范围；Claude AI 被用来通过自定义脚本自动化暴力破解过程。

hackernews · cednore · May 14, 14:49 · [社区讨论](https://news.ycombinator.com/item?id=48136240)

**背景**: 暴力破解密码恢复涉及尝试每一种可能的组合直到找到正确的。对于加密货币钱包，密码保护着私钥；如果密码丢失，恢复可能极其困难。像 Claude 这样的 AI 模型可以通过基于提示或模式智能生成候选密码来加速这一过程。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.coindesk.com/tech/2026/05/14/claude-helps-recover-usd395-000-in-bitcoin-trapped-on-a-computer-for-years">Did Claude just 'crack' a bitcoin wallet? AI tool helps find ...</a></li>
<li><a href="https://pywallet.org/">PyWallet – Bitcoin Wallet Recovery</a></li>
<li><a href="https://www.anthropic.com/claude/opus">Claude Opus 4.7 \ Anthropic</a></li>

</ul>
</details>

**社区讨论**: 社区成员分享了类似的使用 Claude 的成功经历，例如纠正 IRS 审计和从损坏的 SD 卡中恢复变形的图像。一些人指出真正的突破是找到了种子短语，但也承认 Claude 在暴力破解过程中的作用。

**标签**: `#AI`, `#Cryptocurrency`, `#Wallet Recovery`, `#Claude`, `#Security`

---

<a id="item-6"></a>
## [Anthropic 与 SpaceX 合作提升 Claude AI 算力限制](https://t.me/zaihuapd/41371) ⭐️ 8.0/10

Anthropic 与 SpaceX 达成合作，使用 Colossus 1 数据中心全部算力，一个月内新增超过 300 兆瓦容量和 22 万块 NVIDIA GPU，并立即将 Claude Code 和 Claude API 的速率限制翻倍。 此次合作大幅缓解了 Anthropic 的算力瓶颈，支持更快的模型训练和推理，并直接让使用 Claude Code 和 API 的开发者和企业受益，获得更高的吞吐量和更少的限制。 该协议让 Anthropic 独家使用 Colossus 1 的全部 22 万块 GPU 和 300 兆瓦电力。Claude Code 所有付费方案的速率限制翻倍，Pro/Max 用户的高峰期限制被取消；Claude Opus 的 API 速率限制也显著提高。

telegram · zaihuapd · May 14, 00:57

**背景**: Colossus 1 是由 xAI（SpaceX 旗下）在田纳西州孟菲斯建造的 AI 超级计算机，目前是全世界最大的 AI 超级计算机。Anthropic 开发了 Claude 系列大语言模型，用于聊天机器人和 AI 辅助软件开发。此次合作为 Anthropic 提供了海量计算资源，以应对日益增长的需求。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Colossus_(supercomputer)">Colossus (supercomputer) - Wikipedia</a></li>
<li><a href="https://www.datacenterdynamics.com/en/news/anthropic-to-use-all-of-spacex-xais-colossus-1-data-center-compute/">Anthropic to use all of SpaceX-xAI's Colossus 1 data center ...</a></li>

</ul>
</details>

**标签**: `#Anthropic`, `#Claude`, `#AI Infrastructure`, `#GPU`, `#Spaceship`

---

<a id="item-7"></a>
## [美国放行 H200 对华销售，英伟达寻求在华突破](https://www.reuters.com/business/retail-consumer/us-clears-h200-chip-sales-10-china-firms-nvidia-ceo-looks-breakthrough-2026-05-14/) ⭐️ 8.0/10

美国商务部已批准约 10 家中国企业（包括阿里巴巴、腾讯、字节跳动、京东）购买英伟达 H200 芯片，但尚未有交付完成，黄仁勋访华推动交易。 这一进展凸显了中美科技竞争的持续，以及中国在进口高端 AI 芯片与发展国产芯片之间的权衡，影响多家中国科技巨头和 AI 产业。 联想和富士康等分销商也获得许可，单一客户最多可购买 7.5 万颗芯片，但部分中国企业在北京方面的指导下转趋谨慎。

telegram · zaihuapd · May 14, 08:57

**背景**: 英伟达 H200 是一款面向 AI 和高性能计算工作负载的高性能 GPU，采用先进内存技术。美国对华出口先进 AI 芯片实施管制以防止军事用途，导致中国企业一边寻求进口高端芯片，一边投资国产替代方案。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.nvidia.com/en-us/data-center/h200/">H 200 GPU | NVIDIA</a></li>
<li><a href="https://en.wikipedia.org/wiki/Nvidia">Nvidia - Wikipedia</a></li>

</ul>
</details>

**标签**: `#中美科技竞争`, `#英伟达`, `#AI芯片`, `#H200`, `#出口管制`

---

<a id="item-8"></a>
## [京东开设 AI 硬件自营专区，上架受制裁 NVIDIA GPU](https://t.me/zaihuapd/41386) ⭐️ 8.0/10

京东上线了“AI 硬件京东自营专区”，首批上架了 NVIDIA GeForce RTX 5090 32G 涡轮版、RTX PRO 6000 Blackwell 服务器版以及 H100 等此前受美国出口制裁限制的硬件。 此举可能使中国 AI 开发者和公司恢复获取顶级 NVIDIA GPU，绕开美国出口管制，并对全球 AI 硬件供应链产生影响。 RTX 5090 涡轮版列为全球统一规格无阉割版本，而 H100 此前已被禁止对华出口。该专区由京东自营，暗示官方分销渠道。

telegram · zaihuapd · May 14, 16:22

**背景**: 近年来，美国政府以国家安全为由，对向中国出口高端 NVIDIA GPU 实施了限制。这催生了活跃的灰色市场和走私活动。NVIDIA 的 Blackwell 架构（如 RTX 5090、RTX PRO 6000）代表了最新一代 AI 性能显著提升的产品。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Blackwell_(microarchitecture)">Blackwell (microarchitecture) - Wikipedia</a></li>
<li><a href="https://www.tomshardware.com/pc-components/gpus/despite-us-sanctions-researchers-in-china-can-still-access-high-end-nvidia-gpus-for-ai">Despite U.S. sanctions, researchers in China can still access ...</a></li>
<li><a href="https://www.cnbc.com/2025/12/09/us-attorneys-office-southern-district-of-texas-prosecutors-nvidia-chips-h200-h100-smuggle-china.html">Nvidia chips: Plots to send GPUs to China expose $160 ... - CNBC</a></li>

</ul>
</details>

**标签**: `#AI hardware`, `#NVIDIA`, `#sanctions`, `#GPU`, `#JD.com`

---