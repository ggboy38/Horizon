---
layout: default
title: "Horizon Summary: 2026-05-14 (EN)"
date: 2026-05-14
lang: en
---

> From 38 items, 8 important content pieces were selected

---

1. [NGINX Critical RCE Vulnerability After 18 Years](#item-1) ⭐️ 10.0/10
2. [DeepSeek dialogue system vulnerability: unclosed <think> leaks other users' chat history](#item-2) ⭐️ 9.0/10
3. [RTX 5090 eGPU on M4 MacBook Air: Gaming and LLM Surprise](#item-3) ⭐️ 8.0/10
4. [MIT reports 20% drop in incoming graduate students](#item-4) ⭐️ 8.0/10
5. [Claude AI recovers $400K Bitcoin wallet by brute-forcing password](#item-5) ⭐️ 8.0/10
6. [Anthropic partners with SpaceX to boost Claude AI compute limits](#item-6) ⭐️ 8.0/10
7. [US Clears H200 Sales to 10 Chinese Firms, NVIDIA Eyes Breakthrough](#item-7) ⭐️ 8.0/10
8. [JD.com Opens AI Hardware Store, Lists Sanctioned NVIDIA GPUs](#item-8) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [NGINX Critical RCE Vulnerability After 18 Years](https://depthfirst.com/research/nginx-rift-achieving-nginx-rce-via-an-18-year-old-vulnerability) ⭐️ 10.0/10

A critical remote code execution vulnerability, CVE-2026-42945 with a CVSS v4.0 score of 9.2, was disclosed in NGINX on May 13, 2026, affecting all versions from 0.6.27 to 1.30.0 due to a heap buffer overflow in the ngx_http_rewrite_module. NGINX is deployed on hundreds of millions of servers globally, including critical cloud-native environments like Kubernetes ingress and API gateways, making this vulnerability a massive security risk that could enable remote attackers to execute arbitrary code without authentication. The vulnerability stems from state inconsistency in the script engine's two-pass execution: the rewrite module miscalculates buffer size when a rewrite replacement string contains a question mark, leading to heap overflow during the second pass. Patches are available in NGINX 1.31.0/1.30.1 and NGINX Plus R36 P4/R32 P6; a workaround is to replace unnamed capture groups ($1, $2) with named captures.

telegram · zaihuapd · May 14, 02:41

**Background**: A heap buffer overflow occurs when a program writes more data to a heap-allocated memory region than it can hold, potentially overwriting adjacent memory and enabling arbitrary code execution. The ngx_http_rewrite_module handles URL rewriting using PCRE regular expressions and is compiled into NGINX by default. CVSS v4.0 is the latest version of the Common Vulnerability Scoring System, providing more granular and context-aware severity scoring than previous versions.

<details><summary>References</summary>
<ul>
<li><a href="https://nginx.org/en/docs/http/ngx_http_rewrite_module.html">Module ngx_http_rewrite_module</a></li>
<li><a href="https://owasp.org/www-community/attacks/Buffer_overflow_attack">Buffer Overflow Attack | OWASP Foundation</a></li>
<li><a href="https://www.first.org/cvss/specification-document">CVSS v4.0 Specification Document</a></li>

</ul>
</details>

**Tags**: `#NGINX`, `#security`, `#vulnerability`, `#RCE`, `#CVE`

---

<a id="item-2"></a>
## [DeepSeek dialogue system vulnerability: unclosed <think> leaks other users' chat history](https://github.com/deepseek-ai/DeepSeek-R1/issues/840) ⭐️ 9.0/10

A vulnerability was discovered on May 11, 2026 in DeepSeek's Web and API dialogue system. An attacker can send an unclosed '<think' string in a new empty conversation, causing the model to return fragments of other users' chat history, potentially including sensitive information such as code, keys, and private data. This is critical because DeepSeek is widely used, and the vulnerability allows remote attackers to access other users' private data without authentication, undermining trust in AI systems and posing severe privacy risks. The vulnerability affects both DeepSeek Web and API services. The reporter disclosed it responsibly without exploiting it, and the issue is publicly known on GitHub.

telegram · zaihuapd · May 14, 13:15

**Background**: Reasoning models like DeepSeek-R1 use special tokens such as '<think>' and '</think>' to delimit chain-of-thought reasoning. An unclosed '<think>' tag can cause the model to misinterpret input boundaries, leading to cross-user data leakage. Session isolation is a critical security mechanism in multi-tenant LLM applications to prevent context contamination between users.

<details><summary>References</summary>
<ul>
<li><a href="https://huggingface.co/deepseek-ai/DeepSeek-R1-Distill-Qwen-32B/discussions/37">deepseek -ai/ DeepSeek -R1-Distill-Qwen-32B · [RESOLVED] Model is...</a></li>
<li><a href="https://redteams.ai/topics/walkthroughs/defense/session-isolation-patterns">Session Isolation Patterns | redteams.ai</a></li>
<li><a href="https://www.spaceo.ai/case-study/think-tag-mystery-ai-reasoning-debugging/">The Think Tag Mystery: When AI Started Showing Its Homework</a></li>

</ul>
</details>

**Discussion**: Community comments indicate that third-party deployments also exhibit this behavior, and some attribute it to model hallucination rather than a pure session isolation flaw. The discussion suggests the issue may be widespread in reasoning model implementations.

**Tags**: `#security`, `#vulnerability`, `#AI-safety`, `#DeepSeek`, `#LLM`

---

<a id="item-3"></a>
## [RTX 5090 eGPU on M4 MacBook Air: Gaming and LLM Surprise](https://scottjg.com/posts/2026-05-05-egpu-mac-gaming/) ⭐️ 8.0/10

An article demonstrates that an RTX 5090 eGPU can be used with an M4 MacBook Air for gaming and LLM inference, revealing surprising improvements in prompt processing speed. This challenges the common belief that eGPUs are incompatible with Apple Silicon Macs, potentially enabling Mac users to access powerful GPU acceleration for gaming and AI workloads. The significant boost in LLM prompt processing could make Macs more viable for local model inference. The setup likely requires a Thunderbolt connection and custom drivers, as Apple officially only supports AMD eGPUs on Intel Macs. The RTX 5090 is an NVIDIA card, so overcoming driver limitations is a notable achievement.

hackernews · allenleee · May 14, 15:47 · [Discussion](https://news.ycombinator.com/item?id=48137145)

**Background**: An eGPU (external GPU) is an external enclosure containing a desktop graphics card that connects to a laptop via Thunderbolt to boost graphical performance. Apple Silicon Macs use unified memory and do not officially support eGPUs, especially from NVIDIA, due to driver and architecture differences. LLM prompt processing (prefill) is a compute-intensive phase where the model processes input text, and Macs are often slow at this due to memory bandwidth constraints.

<details><summary>References</summary>
<ul>
<li><a href="https://www.hp.com/us-en/shop/tech-takes/external-gpu-laptop-egpu-guide">Do External Graphics Cards Work for Laptops E GP Us Explained</a></li>
<li><a href="https://www.dignited.com/75312/egpu-explained/">What Is an eGPU Used For? - Dignited</a></li>
<li><a href="https://www.adaline.ai/blog/how-prompts-are-processed-in-llms-and-how-llms-reason-using-prompts">How Prompts Are Processed in LLMs and How LLMs Reason Using ...</a></li>

</ul>
</details>

**Discussion**: Commenters expressed excitement, with some highlighting the practical value for LLM work and long-standing requests for VM GPU passthrough on Apple Silicon. One user noted that eGPU compatibility was previously considered impossible by Apple itself.

**Tags**: `#eGPU`, `#Apple Silicon`, `#gaming`, `#LLM`, `#M4 MacBook`

---

<a id="item-4"></a>
## [MIT reports 20% drop in incoming graduate students](https://president.mit.edu/writing-speeches/video-transcript-message-president-kornbluth-about-funding-and-talent-pipeline) ⭐️ 8.0/10

MIT President Sally Kornbluth announced a 20% reduction in the number of incoming graduate students, attributing the decline to funding shortfalls and a broader disillusionment with academia. This decline signals potential systemic issues in U.S. graduate education, including research funding instability and waning appeal of academic careers, which could impact future innovation and the talent pipeline. The drop is attributed to both funding declines that reduce the number of funded offers and a growing disillusionment among prospective students with the academic career path. MIT's graduate student body is 41% international, making immigration policies an additional factor.

hackernews · dmayo · May 14, 14:51 · [Discussion](https://news.ycombinator.com/item?id=48136262)

**Background**: Graduate education, especially in STEM fields, often relies on federal grants and university funding to support students. A sustained decline in research funding, combined with long PhD completion times (median 6 years) and poor job prospects in academia, has led many to question the value of pursuing a graduate degree. The drop at a top institution like MIT may foreshadow broader trends across U.S. universities.

**Discussion**: Community commenters expressed varied views: some attributed the drop to declining research funding and immigration hurdles, while others pointed to a broader disillusionment with academia's grueling conditions and poor job prospects. A few commenters suggested that top talent may be shifting to institutions in China, which are increasingly competitive in science and engineering.

**Tags**: `#academia`, `#graduate-education`, `#research-funding`, `#MIT`, `#higher-education-trends`

---

<a id="item-5"></a>
## [Claude AI recovers $400K Bitcoin wallet by brute-forcing password](https://www.tomshardware.com/tech-industry/cryptocurrency/bitcoin-trader-recovers-usd400-000-using-claude-ai-after-losing-wallet-password-11-years-ago-bot-tried-3-5-trillion-passwords-before-decrypting-an-old-wallet-backup) ⭐️ 8.0/10

A Bitcoin trader used Anthropic's Claude AI to recover a wallet containing $400,000 worth of Bitcoin after losing the password 11 years ago, with the AI trying 3.5 trillion password combinations before succeeding. This demonstrates AI's practical utility in cryptographic recovery tasks, potentially helping others who have lost access to cryptocurrency wallets, and highlights the power of AI in solving complex brute-force problems efficiently. The recovery was possible because the user found an old mnemonic seed phrase in a college notebook, significantly narrowing the password search space; Claude AI was used to automate the brute-force process with custom scripts.

hackernews · cednore · May 14, 14:49 · [Discussion](https://news.ycombinator.com/item?id=48136240)

**Background**: Brute-force password recovery involves trying every possible combination until the correct one is found. For cryptocurrency wallets, the password protects the private key; if the password is lost, recovery can be extremely difficult. AI models like Claude can assist by intelligently generating candidate passwords based on hints or patterns, speeding up the process.

<details><summary>References</summary>
<ul>
<li><a href="https://www.coindesk.com/tech/2026/05/14/claude-helps-recover-usd395-000-in-bitcoin-trapped-on-a-computer-for-years">Did Claude just 'crack' a bitcoin wallet? AI tool helps find ...</a></li>
<li><a href="https://pywallet.org/">PyWallet – Bitcoin Wallet Recovery</a></li>
<li><a href="https://www.anthropic.com/claude/opus">Claude Opus 4.7 \ Anthropic</a></li>

</ul>
</details>

**Discussion**: Community members shared similar success stories with Claude, such as correcting an IRS audit and recovering malformed images from a bad SD card. Some noted that the real breakthrough was finding the seed phrase, but acknowledged Claude's role in the brute-force effort.

**Tags**: `#AI`, `#Cryptocurrency`, `#Wallet Recovery`, `#Claude`, `#Security`

---

<a id="item-6"></a>
## [Anthropic partners with SpaceX to boost Claude AI compute limits](https://t.me/zaihuapd/41371) ⭐️ 8.0/10

Anthropic has partnered with SpaceX to use all compute capacity of the Colossus 1 datacenter, adding over 300 MW and 220,000 NVIDIA GPUs within a month, and immediately doubled rate limits for Claude Code and Claude API. This partnership significantly alleviates compute bottlenecks for Anthropic, enabling faster model training and inference, and directly benefits developers and enterprises using Claude Code and API with higher throughput and fewer restrictions. The deal grants Anthropic exclusive access to all 220,000 GPUs and 300 MW of power at Colossus 1. Rate limits for Claude Code have been doubled for all paid tiers, and peak-hour restrictions are removed for Pro/Max users; Claude Opus API limits are also significantly increased.

telegram · zaihuapd · May 14, 00:57

**Background**: Colossus 1 is an AI supercomputer built by xAI (owned by SpaceX) in Memphis, Tennessee, and is currently the world's largest AI supercomputer. Anthropic develops the Claude series of large language models, which are used for chatbots and AI-assisted software development. The partnership provides Anthropic with massive computing resources to meet growing demand.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Colossus_(supercomputer)">Colossus (supercomputer) - Wikipedia</a></li>
<li><a href="https://www.datacenterdynamics.com/en/news/anthropic-to-use-all-of-spacex-xais-colossus-1-data-center-compute/">Anthropic to use all of SpaceX-xAI's Colossus 1 data center ...</a></li>

</ul>
</details>

**Tags**: `#Anthropic`, `#Claude`, `#AI Infrastructure`, `#GPU`, `#Spaceship`

---

<a id="item-7"></a>
## [US Clears H200 Sales to 10 Chinese Firms, NVIDIA Eyes Breakthrough](https://www.reuters.com/business/retail-consumer/us-clears-h200-chip-sales-10-china-firms-nvidia-ceo-looks-breakthrough-2026-05-14/) ⭐️ 8.0/10

The US Commerce Department has approved approximately 10 Chinese companies, including Alibaba, Tencent, ByteDance, and JD.com, to purchase NVIDIA's H200 chips, though no deliveries have been completed yet and Jensen Huang is visiting China to facilitate the transactions. This development highlights the ongoing US-China tech competition and the delicate balance between importing advanced AI chips and developing domestic alternatives, affecting major Chinese tech firms and the broader AI industry. Distributors like Lenovo and Foxconn have also received licenses, with individual customers allowed to purchase up to 75,000 chips, but some Chinese companies are cautious due to guidance from Beijing.

telegram · zaihuapd · May 14, 08:57

**Background**: The NVIDIA H200 is a high-performance GPU designed for AI and high-performance computing workloads, featuring advanced memory technology. The US has imposed export controls on advanced AI chips to China to prevent military use, leading to a complex landscape where Chinese firms seek access while also investing in domestic alternatives.

<details><summary>References</summary>
<ul>
<li><a href="https://www.nvidia.com/en-us/data-center/h200/">H 200 GPU | NVIDIA</a></li>
<li><a href="https://en.wikipedia.org/wiki/Nvidia">Nvidia - Wikipedia</a></li>

</ul>
</details>

**Tags**: `#中美科技竞争`, `#英伟达`, `#AI芯片`, `#H200`, `#出口管制`

---

<a id="item-8"></a>
## [JD.com Opens AI Hardware Store, Lists Sanctioned NVIDIA GPUs](https://t.me/zaihuapd/41386) ⭐️ 8.0/10

JD.com has launched an 'AI Hardware JD Self-operated' store, initially listing NVIDIA GeForce RTX 5090 32GB Turbo Edition, RTX PRO 6000 Blackwell server GPU, and H100, all previously restricted by US export sanctions. This move potentially enables Chinese AI developers and companies to regain access to top-tier NVIDIA GPUs, circumventing US export controls and impacting the global AI hardware supply chain. The RTX 5090 Turbo Edition is listed as a global unmodified version, while the H100 was previously banned for export to China. The store appears to be operated directly by JD.com, suggesting official distribution.

telegram · zaihuapd · May 14, 16:22

**Background**: In recent years, the US government imposed export restrictions on high-end NVIDIA GPUs to China, citing national security concerns. This has led to a thriving grey market and smuggling operations. NVIDIA's Blackwell architecture (e.g., RTX 5090, RTX PRO 6000) represents the latest generation with significant AI performance gains.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Blackwell_(microarchitecture)">Blackwell (microarchitecture) - Wikipedia</a></li>
<li><a href="https://www.tomshardware.com/pc-components/gpus/despite-us-sanctions-researchers-in-china-can-still-access-high-end-nvidia-gpus-for-ai">Despite U.S. sanctions, researchers in China can still access ...</a></li>
<li><a href="https://www.cnbc.com/2025/12/09/us-attorneys-office-southern-district-of-texas-prosecutors-nvidia-chips-h200-h100-smuggle-china.html">Nvidia chips: Plots to send GPUs to China expose $160 ... - CNBC</a></li>

</ul>
</details>

**Tags**: `#AI hardware`, `#NVIDIA`, `#sanctions`, `#GPU`, `#JD.com`

---