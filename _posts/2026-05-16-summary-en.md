---
layout: default
title: "Horizon Summary: 2026-05-16 (EN)"
date: 2026-05-16
lang: en
---

> From 38 items, 11 important content pieces were selected

---

1. [vllm 0.21.0 Released with KV Offload and Speculative Decoding](#item-1) ⭐️ 9.0/10
2. [Project Zero discloses 0-click exploit for Pixel 10](#item-2) ⭐️ 9.0/10
3. [Project Gutenberg site improvements spark community discussion](#item-3) ⭐️ 8.0/10
4. [Blind AI reliance is 'AI psychosis,' warns Mitchell Hashimoto](#item-4) ⭐️ 8.0/10
5. [Orthrus speeds up Qwen3 inference up to 7.8x with lossless output](#item-5) ⭐️ 8.0/10
6. [Frontier AI breaks open CTF format](#item-6) ⭐️ 8.0/10
7. [Buying non-Apple, non-Google smartphones: a challenge](#item-7) ⭐️ 8.0/10
8. [Scott Alexander Explores AI Scaling Limits with Lindy's Law](#item-8) ⭐️ 8.0/10
9. [Apple and OpenAI Partnership Fractures, OpenAI Considers Legal Action](#item-9) ⭐️ 8.0/10
10. [US DOJ demands Apple, Google identify 100,000+ car app users](#item-10) ⭐️ 8.0/10
11. [OpenAI and Malta Partner for Free ChatGPT Plus with AI Literacy](#item-11) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [vllm 0.21.0 Released with KV Offload and Speculative Decoding](https://github.com/vllm-project/vllm/releases/tag/v0.21.0) ⭐️ 9.0/10

vllm 0.21.0 introduces KV cache offloading with Hybrid Memory Allocator (HMA) and speculative decoding with thinking budget for reasoning models, along with breaking changes like deprecating Transformers v4 and requiring C++20. These improvements enhance LLM inference efficiency by reducing GPU memory pressure via CPU offloading and accelerating reasoning models via speculative decoding, benefiting the AI/ML community deploying large language models at scale. Key technical details include the full enablement of HMA for KV offloading, scheduling-side sliding window group support, and the new TOKENSPEED_MLA attention backend for Blackwell GPUs. The release also deprecates Transformers v4 (migration to v5 required) and mandates a C++20-compatible compiler.

github · khluu · May 15, 08:44

**Background**: KV cache is a memory store used during LLM inference to avoid recomputing key-value pairs for each token, but it consumes significant GPU memory. KV offloading moves part of this cache to CPU memory to free GPU resources. Hybrid Memory Allocator (HMA) is a new memory management architecture in vllm that efficiently handles heterogeneous memory (GPU/CPU). Speculative decoding uses a smaller draft model to propose token sequences, which the larger model verifies in one pass, reducing latency while preserving output distribution.

<details><summary>References</summary>
<ul>
<li><a href="https://vllm-project.github.io/2026/01/08/kv-offloading-connector.html">Inside vLLM's New KV Offloading Connector: Smarter Memory Transfer for ...</a></li>
<li><a href="https://en.wikipedia.org/wiki/Speculative_decoding">Speculative decoding</a></li>
<li><a href="https://www.youtube.com/watch?v=0cUFUtNW_S8">[ vLLM Office Hours #30] Hybrid Memory Allocator ... - YouTube</a></li>

</ul>
</details>

**Tags**: `#vllm`, `#LLM inference`, `#breaking changes`, `#speculative decoding`, `#GPU optimization`

---

<a id="item-2"></a>
## [Project Zero discloses 0-click exploit for Pixel 10](https://projectzero.google/2026/05/pixel-10-exploit.html) ⭐️ 9.0/10

Google Project Zero published a 0-click exploit chain for the Pixel 10, demonstrating how on-device AI decoding of messages introduces new attack surfaces. The exploit allows remote code execution without any user interaction. This discovery highlights that on-device AI features, while convenient, significantly expand the attack surface of smartphones. It underscores the urgent need for security reviews of AI-powered message processing across all Android devices. The exploit chain combines two bugs: a zero-click vulnerability in Dolby audio processing (patched January 2026) and a custom video codec driver bug. It achieves full root access remotely, and the vendor patched within 90 days.

hackernews · happyhardcore · May 15, 13:39 · [Discussion](https://news.ycombinator.com/item?id=48148460)

**Background**: Zero-click exploits require no action from the victim, such as opening a file or clicking a link, making them extremely dangerous. On-device AI decoding processes incoming messages (e.g., SMS or media) before the user even views them, increasing the potential attack surface. Project Zero is Google's elite security team that publicly discloses vulnerabilities to drive faster fixes.

<details><summary>References</summary>
<ul>
<li><a href="https://projectzero.google/2026/05/pixel-10-exploit.html">A 0-click exploit chain for the Pixel 10: When a Door Closes, a Window Opens - Project Zero</a></li>
<li><a href="https://www.kaspersky.com/resource-center/definitions/what-is-zero-click-malware">Zero-Click Exploits</a></li>
<li><a href="https://netlas.io/blog/zero_click_exploits/">Zero-Click Exploits - Netlas Blog</a></li>

</ul>
</details>

**Discussion**: Commenters expressed concern that on-device AI features repeat past mistakes by pre-processing messages, creating new zero-click risks. Some were relieved that Google patched within 90 days, but worried about other Android vendors' response times. There was also technical discussion about kernel code and a sense that exploit disclosures have become more frequent.

**Tags**: `#security`, `#zero-click exploit`, `#Android`, `#Project Zero`

---

<a id="item-3"></a>
## [Project Gutenberg site improvements spark community discussion](https://www.gutenberg.org/) ⭐️ 8.0/10

A programmer at Project Gutenberg announced ongoing site improvements, including a revamped interface and upcoming features. Project Gutenberg is a foundational open-access digital library, and its continuous improvement makes public-domain literature more accessible worldwide, encouraging reading and scholarly use. The improvements involve months of work with more changes coming; however, access issues were reported by a user in Italy due to a judicial seizure order.

hackernews · JSeiko · May 15, 16:15 · [Discussion](https://news.ycombinator.com/item?id=48150431)

**Background**: Project Gutenberg, founded in 1971 by Michael S. Hart, is the oldest digital library, offering over 70,000 free eBooks in the public domain. It was initially a student project using a mainframe computer on ARPANET. The site has grown alongside the internet and remains a vital resource for classic literature.

**Discussion**: Community members expressed appreciation for the updates, with one user sharing a personal story of how Project Gutenberg enriched their father's reading. Others discussed the potential for native integration with e-book readers, while a user from Italy reported a regional access block due to legal seizure.

**Tags**: `#Project Gutenberg`, `#digital libraries`, `#open access`, `#ebooks`

---

<a id="item-4"></a>
## [Blind AI reliance is 'AI psychosis,' warns Mitchell Hashimoto](https://twitter.com/mitchellh/status/2055380239711457578) ⭐️ 8.0/10

Mitchell Hashimoto, creator of Vagrant and founder of HashiCorp, posted a tweet criticizing companies for blindly relying on AI without critical thinking, coining the term 'AI psychosis' to describe this phenomenon. This commentary resonates deeply in the tech community, as many organizations are heavily investing in AI without proper evaluation, potentially leading to flawed decision-making and reinforcing industry hype. The tweet achieved a high score of 8.0/10 on Hacker News with 1641 points and 861 comments, indicating strong engagement. The discussion highlights a nuanced debate about the balance between leveraging AI as a tool and preserving human critical thinking.

hackernews · reasonableklout · May 15, 20:26 · [Discussion](https://news.ycombinator.com/item?id=48153379)

**Background**: 'AI psychosis' refers to an irrational over-reliance on AI tools, where decisions are made simply because 'AI said so,' often leading to poor outcomes when AI outputs are incorrect or biased. The term reflects a growing concern among technologists about the uncritical adoption of AI in software engineering and business processes, especially as companies rush to integrate AI without verifying its value.

**Discussion**: Commenters largely agree with Mitchell, sharing personal experiences of management pushing AI usage without clear benefits. Some distinguish between using AI as a productivity tool and blindly trusting it, while others express frustration with the hype and pressure to adopt AI. A few note that AI can be useful but should not replace human reasoning.

**Tags**: `#AI`, `#software engineering`, `#critical thinking`, `#industry trends`, `#hype`

---

<a id="item-5"></a>
## [Orthrus speeds up Qwen3 inference up to 7.8x with lossless output](https://github.com/chiennv2000/orthrus) ⭐️ 8.0/10

Orthrus introduces a dual-architecture framework that accelerates Qwen3 inference by up to 7.8× tokens per forward pass while provably preserving the exact output distribution of the original autoregressive model. This breakthrough significantly reduces inference latency for LLMs without sacrificing quality, making large models more practical for local deployment and real-time applications. It also opens a new direction for combining autoregressive and diffusion model strengths. Orthrus achieves this speedup by using a dual-view diffusion decoding method that runs a small diffusion model in parallel to generate multiple tokens, while the autoregressive Qwen3 validates outputs to ensure fidelity. The system includes a learned draft model and a verification step to guarantee identical output distribution.

hackernews · FranckDernoncou · May 15, 22:38 · [Discussion](https://news.ycombinator.com/item?id=48154865)

**Background**: Autoregressive LLMs generate tokens sequentially, which can be slow for long sequences. Diffusion models, on the other hand, can generate multiple tokens in parallel but often produce different output distributions. Orthrus bridges this gap by using a dual-architecture approach that combines the speed of diffusion with the fidelity of autoregressive models, inspired by speculative decoding techniques.

<details><summary>References</summary>
<ul>
<li><a href="https://github.com/chiennv2000/orthrus">GitHub - chiennv2000/orthrus: Fast, lossless LLM inference ...</a></li>
<li><a href="https://arxiv.org/html/2605.12825v1">Orthrus: Memory-Efficient Parallel Token Generation via Dual ...</a></li>

</ul>
</details>

**Discussion**: Community members expressed enthusiasm about the novel approach, with some noting that it is surprising it had not been tried before. Questions about compute reduction trade-offs and the potential for integration with GGUF/quantized models were raised, alongside comparisons to full diffusion transformers. Overall sentiment is positive and curious.

**Tags**: `#efficient inference`, `#Qwen3`, `#LLM optimization`, `#transformer acceleration`

---

<a id="item-6"></a>
## [Frontier AI breaks open CTF format](https://kabir.au/blog/the-ctf-scene-is-dead) ⭐️ 8.0/10

An article argues that advanced AI models have made traditional Capture The Flag (CTF) contests trivial, potentially ending the open CTF format. This threatens the core of cybersecurity education and competitive hacking, forcing a rethink of how to test human skills when AI can solve challenges instantly. The article's author claims that frontier AI can solve most CTF challenges without human intervention, reducing the competition's value for skill assessment.

hackernews · frays · May 16, 07:01 · [Discussion](https://news.ycombinator.com/item?id=48157559)

**Background**: Capture The Flag (CTF) is a cybersecurity competition where participants solve challenges to find hidden 'flags.' Traditionally, CTFs test hands-on skills in areas like cryptography, reverse engineering, and exploitation. AI models like GPT-4 and specialized agents have recently shown ability to solve such tasks autonomously, raising questions about the future of these competitions.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Capture_the_flag_(cybersecurity)">Capture the flag (cybersecurity) - Wikipedia</a></li>
<li><a href="https://www.huntress.com/cybersecurity-education/cybersecurity-awareness/capture-the-flag">Cybersecurity Capture the Flag | Hands-On CTF by Huntress | Huntress</a></li>
<li><a href="https://www.hackthebox.com/hacker/ctf">Capture The Flag Competitions For Hackers | Hack The Box CTFs</a></li>

</ul>
</details>

**Discussion**: Commenters shared mixed reactions: some noted parallels with AI's impact on education, others experimented with improving obfuscators against AI deobfuscation, and a few suggested offline competitions as a solution. There was also a discussion about the article's title change causing confusion.

**Tags**: `#AI`, `#CTF`, `#cybersecurity`, `#LLMs`, `#education`

---

<a id="item-7"></a>
## [Buying non-Apple, non-Google smartphones: a challenge](https://www.theregister.com/on-prem/2026/05/01/where-to-buy-a-non-apple-non-google-smartphone/5219681) ⭐️ 8.0/10

A Register article and community discussion explore the practical difficulties of purchasing and using smartphones that don't run iOS or Android with Google services, highlighting ecosystem lock-in and critical app dependencies. For privacy-conscious users seeking alternatives to Apple and Google, the lack of viable options for essential apps (banking, government, transit) makes switching extremely challenging, reinforcing the duopoly's market grip. Community comments note that even non-Google Android forks like GrapheneOS still rely on sandboxed Google services for some apps, and that devices like Huawei's HarmonyOS face similar issues with Google app compatibility.

hackernews · _____k · May 16, 08:34 · [Discussion](https://news.ycombinator.com/item?id=48158130)

**Background**: Most smartphones shipped outside of China rely on either Apple's iOS or Google's Android with Google Mobile Services (GMS). Alternatives like GrapheneOS (a privacy-focused Android fork for Pixel devices) exist, but many critical apps—especially banking and authentication—require GMS or iOS APIs, creating an ecosystem lock-in that is difficult to escape.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/GrapheneOS">GrapheneOS</a></li>
<li><a href="https://grapheneos.org/">GrapheneOS: the private and secure mobile OS</a></li>
<li><a href="https://smartphones.gadgethacks.com/news/families-ditch-apps-for-apple-ecosystem-lock-in/">Families Ditch Apps for Apple Ecosystem Lock-In << Smartphones :: Gadget Hacks</a></li>

</ul>
</details>

**Discussion**: Commenters highlight real-world pain points: banking and government apps often break on non-standard Android builds, and some users resort to carrying a second device or using remote access tools. GrapheneOS on Pixel phones is praised as the best current option, but the lack of diverse hardware (e.g., minimal feature phones with proper US band support) remains a frustration.

**Tags**: `#Smartphones`, `#Privacy`, `#Android alternatives`, `#GrapheneOS`, `#Community discussion`

---

<a id="item-8"></a>
## [Scott Alexander Explores AI Scaling Limits with Lindy's Law](https://www.astralcodexten.com/p/the-sigmoids-wont-save-you) ⭐️ 8.0/10

Scott Alexander's article 'The sigmoids won't save you' argues that AI progress is unpredictable and may not follow current scaling trends, applying Lindy's Law to question the assumption of continued exponential improvement. This perspective challenges the widely held belief that AI performance will keep scaling with compute and data, which is crucial for researchers, investors, and policymakers making long-term decisions. It encourages the community to consider a wider range of possible futures for AI development. The article uses Lindy's Law, which states that the future life expectancy of a non-perishable item is proportional to its current age, to argue that if AI scaling has been linear so far, it may continue linearly rather than plateauing as a sigmoid curve would predict. However, the author also notes the inherent uncertainty in such predictions.

hackernews · Tomte · May 15, 10:51 · [Discussion](https://news.ycombinator.com/item?id=48147021)

**Background**: In machine learning, a sigmoid function is an S-shaped curve that models growth that saturates, often used as an activation function in neural networks. Lindy's Law, popularized by Nassim Taleb, suggests that the longer a non-perishable technology or idea has existed, the longer it is likely to persist. Scott Alexander is a well-known rationalist blogger who frequently writes about AI and forecasting.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Sigmoid_function">Sigmoid function - Wikipedia</a></li>

</ul>
</details>

**Discussion**: Commenters debate the applicability of Lindy's Law to AI trends, with some noting that the author has a personal stake in predicting continued progress. Others point out that AI scaling may be measuring capabilities unrelated to intelligence, and that uncertainty means no model can predict the future with confidence.

**Tags**: `#AI`, `#deep learning`, `#scaling`, `#Lindy's Law`, `#machine learning`

---

<a id="item-9"></a>
## [Apple and OpenAI Partnership Fractures, OpenAI Considers Legal Action](https://www.bloomberg.com/news/articles/2026-05-14/openai-apple-partnership-frays-setting-up-possible-legal-fight) ⭐️ 8.0/10

Apple and OpenAI's partnership is deteriorating, with OpenAI considering legal action against Apple for allegedly not adequately promoting the ChatGPT integration, leading to subscription conversions far below expectations. Apple plans to open Siri to third-party AI models like Claude and Gemini at WWDC 2026, further diluting OpenAI's exclusive position. This rift could reshape the AI integration landscape in consumer devices, potentially leading to a more open ecosystem where Apple leverages multiple AI partners. Legal action between two tech giants may set precedents for AI partnership contracts and revenue sharing. ChatGPT integration in Apple systems is reportedly hidden and feature-limited, with most users still using the standalone ChatGPT app. Apple is also unhappy with OpenAI's privacy standards, hardware business, and poaching of Apple engineers.

telegram · zaihuapd · May 15, 12:59

**Background**: Apple and OpenAI announced a partnership in 2024 to integrate ChatGPT into Siri, aiming to enhance Siri's capabilities with generative AI. ChatGPT is a large language model developed by OpenAI that can generate human-like text, code, and more. Similarly, Claude (by Anthropic) and Gemini (by Google) are competing AI models that Apple may now allow on Siri.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Claude_AI">Claude AI</a></li>
<li><a href="https://en.wikipedia.org/wiki/Gemini_AI">Gemini AI</a></li>

</ul>
</details>

**Tags**: `#AI`, `#OpenAI`, `#Apple`, `#partnership`, `#legal`

---

<a id="item-10"></a>
## [US DOJ demands Apple, Google identify 100,000+ car app users](https://9to5mac.com/2026/05/15/doj-reportedly-demands-apple-and-google-identify-over-100000-users-of-car-app/) ⭐️ 8.0/10

The US Department of Justice has issued subpoenas to Apple, Google, and Amazon demanding they provide the identities, addresses, and purchase records of over 100,000 users of the EZ Lynk car modification app, as part of an investigation into potential Clean Air Act violations. This mass data request from the DOJ raises significant privacy and legal concerns, as it could set a precedent for government access to user data via tech platforms. It also highlights the ongoing crackdown on aftermarket emission defeat devices. The subpoenas were issued in March and April of the current year, and Apple and Google are reportedly preparing to challenge the request as overly broad and not narrowly tailored to the investigation. EZ Lynk denies its products are primarily used to bypass emissions controls.

telegram · zaihuapd · May 16, 05:34

**Background**: EZ Lynk is a cloud-based vehicle diagnostics and tuning platform that allows users to modify engine control unit (ECU) parameters, which can potentially disable or bypass emissions controls. Such modifications are considered 'defeat devices' under the Clean Air Act, and the DOJ has been investigating companies that manufacture and sell them.

<details><summary>References</summary>
<ul>
<li><a href="https://ezlynk.com/">EZ LYNK®: The Future of Vehicle Diagnostics & Control</a></li>
<li><a href="https://en.wikipedia.org/wiki/Defeat_device">Defeat device - Wikipedia</a></li>

</ul>
</details>

**Tags**: `#privacy`, `#legal`, `#apple`, `#google`, `#data request`

---

<a id="item-11"></a>
## [OpenAI and Malta Partner for Free ChatGPT Plus with AI Literacy](https://openai.com/index/malta-chatgpt-plus-partnership/) ⭐️ 8.0/10

OpenAI and the Maltese government announced a first-of-its-kind national partnership, offering all Maltese citizens one year of free ChatGPT Plus upon completing an AI literacy course developed by the University of Malta. This initiative marks a significant milestone in AI democratization, combining free access to advanced AI tools with mandatory education on responsible use, setting a precedent for national AI policy worldwide. The program, called 'AI for All,' will launch in May, managed by the Malta Digital Innovation Authority, and will gradually extend to Maltese citizens abroad.

telegram · zaihuapd · May 16, 10:40

**Background**: ChatGPT Plus is a subscription tier of OpenAI's ChatGPT that provides priority access, faster responses, and additional features. AI literacy courses aim to educate the public on AI capabilities and ethical considerations, ensuring informed and responsible usage.

**Tags**: `#OpenAI`, `#ChatGPT`, `#Malta`, `#AI literacy`, `#government partnership`

---