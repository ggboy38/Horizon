---
layout: default
title: "Horizon Summary: 2026-05-09 (EN)"
date: 2026-05-09
lang: en
---

> From 39 items, 15 important content pieces were selected

---

1. [Triton 3.7.0: New ops, backend improvements for GPU kernels](#item-1) ⭐️ 9.0/10
2. [Google reCAPTCHA fails for de-googled Android users](#item-2) ⭐️ 8.0/10
3. [LLMs Degrade Document Quality by 25% in Delegation Workflows](#item-3) ⭐️ 8.0/10
4. [HTML as LLM Output: Unreasonable Effectiveness](#item-4) ⭐️ 8.0/10
5. [Mathematician's ChatGPT 5.5 Pro experience sparks AI debate](#item-5) ⭐️ 8.0/10
6. [OpenAI's WebRTC Problem: Article Proposes WebTransport Alternative](#item-6) ⭐️ 8.0/10
7. [AI accelerates breakdown of vulnerability disclosure cultures](#item-7) ⭐️ 8.0/10
8. [React2Shell: Critical RCE Vulnerability in React Server Components](#item-8) ⭐️ 8.0/10
9. [AWS North Virginia Outage Resolved, Highlights us-east-1 Fragility](#item-9) ⭐️ 8.0/10
10. [Anthropic's Teaching Claude Why Method Reduces AI Misalignment](#item-10) ⭐️ 8.0/10
11. [Mozilla Hardens Firefox with Claude Mythos Preview](#item-11) ⭐️ 8.0/10
12. [Anthropic seeks hundreds of billions, nears $1 trillion valuation](#item-12) ⭐️ 8.0/10
13. [US suspects Nvidia chips smuggled to China via Thailand](#item-13) ⭐️ 8.0/10
14. [DeepSeek eyes $45B valuation with state-led funding](#item-14) ⭐️ 8.0/10
15. [Baidu Releases ERNIE 5.1 with Efficient Pretraining, Claims Top Chinese Search Model](#item-15) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [Triton 3.7.0: New ops, backend improvements for GPU kernels](https://github.com/triton-lang/triton/releases/tag/v3.7.0) ⭐️ 9.0/10

Triton 3.7.0 has been released, introducing new operations such as tl.squeeze, tl.unsqueeze, scaled BMM, and FP8 constants, along with significant backend improvements for NVIDIA and AMD GPUs. This release enhances the expressiveness and performance of Triton, a widely-used GPU kernel compiler for AI/ML workloads, enabling more efficient and flexible kernel development. New features include support for FP8 constants, scaled batched matmul, and the ability to return constexpr from JIT-compiled code. Backend updates include LLVM bumps, improved 2CTA/multicast support, and enhanced AMD/HIP backend.

github · atalman · May 7, 22:19

**Background**: Triton is an open-source Python-like programming language and compiler developed by OpenAI for writing highly efficient GPU kernels. It abstracts low-level CUDA details, allowing researchers to write performant code with minimal expertise. This release continues Triton's evolution as a key tool in AI/ML infrastructure.

<details><summary>References</summary>
<ul>
<li><a href="https://openai.com/index/triton/">Introducing Triton: Open-source GPU programming for neural networks | OpenAI</a></li>
<li><a href="https://github.com/triton-lang/triton">GitHub - triton-lang/triton: Development repository for the Triton language and compiler · GitHub</a></li>
<li><a href="https://www.rightnowai.co/guides/frameworks/triton">Triton GPU Kernel Programming Guide: CUDA Alternative | RightNow AI | RightNow AI</a></li>

</ul>
</details>

**Tags**: `#triton`, `#gpu`, `#compiler`, `#machine learning`, `#release`

---

<a id="item-2"></a>
## [Google reCAPTCHA fails for de-googled Android users](https://reclaimthenet.org/google-broke-recaptcha-for-de-googled-android-users) ⭐️ 8.0/10

Google's new reCAPTCHA now requires Play Integrity API and remote attestation on Android, which breaks functionality for devices without Google Play Services, such as devices running custom ROMs or GrapheneOS. This change goes beyond previous CAPTCHA challenges by enforcing hardware-backed attestation, effectively excluding privacy-focused users and custom ROM communities from accessing websites that rely on reCAPTCHA. It raises concerns about vendor lock-in and the erosion of user choice in the Android ecosystem. The new reCAPTCHA uses Play Integrity API (formerly SafetyNet) and remote attestation to verify device integrity, reportedly tying the device identity to a static key (EK) that could be logged by Google servers. This is similar to the controversial Web Environment Integrity (WEI) proposal that was abandoned in 2023.

hackernews · anonymousiam · May 8, 18:45 · [Discussion](https://news.ycombinator.com/item?id=48067119)

**Background**: Play Integrity API is a set of services provided by Google Play Services that allows apps to verify the integrity of the device and app installation. Remote attestation is a trusted computing concept where a device proves its hardware and software state to a remote verifier using cryptographic keys. De-googled Android users run operating systems without Google Play Services, often for privacy reasons, and rely on alternatives like microG or sandboxed Play Services.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Play_Integrity_API">Play Integrity API - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/Remote_attestation">Remote attestation</a></li>
<li><a href="https://en.wikipedia.org/wiki/Web_Environment_Integrity">Web Environment Integrity - Wikipedia</a></li>

</ul>
</details>

**Discussion**: Commenters express strong disapproval, with many pointing out the privacy implications of remote attestation and comparing it to the abandoned WEI proposal. Some note that even users of GrapheneOS with sandboxed Play Services may be affected, and there is skepticism about Google's ability to avoid tracking users through this mechanism.

**Tags**: `#reCAPTCHA`, `#Android`, `#Google`, `#privacy`, `#attestation`

---

<a id="item-3"></a>
## [LLMs Degrade Document Quality by 25% in Delegation Workflows](https://arxiv.org/abs/2604.15597) ⭐️ 8.0/10

A new paper from Microsoft Research finds that large language models (LLMs) corrupt documents when used for delegation, with even frontier models like Gemini 3.1 Pro and GPT 5.4 degrading an average of 25% of content over 20 interaction cycles. This finding highlights a critical reliability issue for AI agents that automate document maintenance, as repeated LLM passes can silently erode accuracy and intent, potentially leading to costly errors in professional and scientific contexts. The study tested 19 LLMs on long workflows of up to 20 sequential interactions, measuring corruption via round-trip fidelity through invertible transformations. Even with tool use, degradation persisted, suggesting systemic issues beyond simple hallucination.

hackernews · rbanffy · May 9, 08:44 · [Discussion](https://news.ycombinator.com/item?id=48073246)

**Background**: LLMs are increasingly used to rephrase, summarize, or update documents, but each pass can introduce subtle changes that accumulate. This phenomenon, sometimes called 'semantic ablation,' mirrors the JPEG compression degradation meme. Prior work has noted model collapse when training on synthetic data, but this paper specifically examines intentional human-LLM delegation loops.

<details><summary>References</summary>
<ul>
<li><a href="https://arxiv.org/abs/2604.15597">[2604.15597] LLMs Corrupt Your Documents When You Delegate</a></li>
<li><a href="https://huggingface.co/papers/2604.15597">Paper page - LLMs Corrupt Your Documents When You Delegate</a></li>
<li><a href="https://cekrem.github.io/posts/llms-corrupt-your-documents/">LLMs Corrupt Your Documents (and the Theory Dies Twice) · cekrem.github.io</a></li>

</ul>
</details>

**Discussion**: Community comments express widespread agreement with the findings, with users comparing the effect to a 'JPEG meme' and coining terms like 'semantic ablation.' Some expressed suspicion about the tool-use results, noting that a basic agentic harness might not represent state-of-the-art systems. Others emphasize the need to minimize round trips to LLMs and use them as thin translation layers.

**Tags**: `#LLMs`, `#Document Quality`, `#Semantic Degradation`, `#AI Reliability`, `#Research`

---

<a id="item-4"></a>
## [HTML as LLM Output: Unreasonable Effectiveness](https://twitter.com/trq212/status/2052809885763747935) ⭐️ 8.0/10

A blog post and Twitter thread argue that using HTML as an output format for LLMs like Claude Code is surprisingly effective for creating rich, interactive documentation, challenging the default use of Markdown. This insight is significant because it prompts developers to reconsider the choice of output format for AI-assisted documentation, potentially leading to more interactive and visually appealing results without sacrificing the benefits of LLM generation. The post links to a live example page and references an article by Simon Willison on the same topic. Community discussion highlights trade-offs: HTML offers richer interactivity but makes it harder for humans to co-edit documents compared to Markdown.

hackernews · pretext · May 9, 04:53 · [Discussion](https://news.ycombinator.com/item?id=48071940)

**Background**: Claude Code is Anthropic's agentic coding tool for developers. Large language models (LLMs) typically output Markdown because of its simplicity and readability, but HTML allows for more complex layouts, interactivity, and embedded content. The debate centers on balancing richness with human editability.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Claude_Code">Claude Code</a></li>
<li><a href="https://claude.com/product/claude-code">Claude Code by Anthropic | AI Coding Agent, Terminal, IDE</a></li>

</ul>
</details>

**Discussion**: Some commenters worry that HTML output reduces the ability for humans to co-author documents, while others praise it for self-contained, shareable apps. Suggestions include using extended Markdown (e.g., with Mermaid) or MDX to blend formats. One critic dismisses the post as low quality.

**Tags**: `#LLM`, `#HTML`, `#Claude`, `#AI-assisted development`, `#documentation`

---

<a id="item-5"></a>
## [Mathematician's ChatGPT 5.5 Pro experience sparks AI debate](https://gowers.wordpress.com/2026/05/08/a-recent-experience-with-chatgpt-5-5-pro/) ⭐️ 8.0/10

Fields Medalist Tim Gowers published a blog post detailing his interactions with ChatGPT 5.5 Pro, highlighting its ability to generate novel mathematical ideas but also its limitations in conceptual accuracy. This discussion is significant because it reflects AI's growing role in academic research, particularly in mathematics, potentially altering how PhD students are trained and how ideas are valued. ChatGPT 5.5 Pro, released on April 23, 2026, is not available to free-tier users; the model demonstrated advanced reasoning but still made conceptual errors that required expert oversight.

hackernews · _alternator_ · May 9, 02:41 · [Discussion](https://news.ycombinator.com/item?id=48071262)

**Background**: ChatGPT 5.5 Pro is a large language model by OpenAI, codenamed "Spud". It represents an iterative improvement over GPT-5, with enhanced reasoning and multimodal capabilities. The model's performance in mathematical domains has sparked debate about AI's role in idea generation and the future of research.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/GPT-5.5">GPT - 5 . 5 - Wikipedia</a></li>

</ul>
</details>

**Discussion**: Community comments from a physics professor and other researchers highlight that while LLMs like ChatGPT 5.5 Pro are useful for catching errors and suggesting connections, they require expert knowledge to identify conceptual mistakes. There is discussion on whether the value of ideas lies in their scarcity or utility, and how AI might change the landscape of academic research.

**Tags**: `#AI`, `#ChatGPT`, `#mathematics`, `#research`, `#philosophy`

---

<a id="item-6"></a>
## [OpenAI's WebRTC Problem: Article Proposes WebTransport Alternative](https://moq.dev/blog/webrtc-is-the-problem/) ⭐️ 8.0/10

A blog post on moq.dev argues that WebRTC's architecture is fundamentally unsuitable for OpenAI's real-time API needs and proposes WebTransport as a superior alternative for low-latency AI interactions. This debate highlights potential shifts in real-time communication protocols for AI, affecting how developers build interactive AI services and the broader WebRTC ecosystem. The article criticizes WebRTC's mandatory STUN/DTLS handshake overhead and its lack of application-level buffering, while touting WebTransport's use of QUIC for reduced latency and improved client-server efficiency.

hackernews · atgctg · May 7, 17:11 · [Discussion](https://news.ycombinator.com/item?id=48051951)

**Background**: WebRTC (Web Real-Time Communication) is a widely-used protocol for video/audio/data communication in browsers, relying on RTP, STUN, and DTLS for peer-to-peer connections. WebTransport is a newer API leveraging QUIC and HTTP/3, designed for efficient client-server communication with lower overhead.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/WebRTC">WebRTC - Wikipedia</a></li>
<li><a href="https://developer.mozilla.org/en-US/docs/Web/API/WebRTC_API">WebRTC API - MDN Web Docs - Mozilla</a></li>
<li><a href="https://www.videosdk.live/developer-hub/webtransport/webrtc-vs-webtransport">WebRTC vs WebTransport: Comparison Guide - VideoSDK</a></li>

</ul>
</details>

**Discussion**: Comments on the article reflect a substantive debate: some criticize the author's characterization of WebRTC's design, others share alternative implementations (e.g., persistent connections like Alexa), and a few propose local processing of STT to reduce latency.

**Tags**: `#WebRTC`, `#OpenAI`, `#real-time AI`, `#WebTransport`, `#systems design`

---

<a id="item-7"></a>
## [AI accelerates breakdown of vulnerability disclosure cultures](https://www.jefftk.com/p/ai-is-breaking-two-vulnerability-cultures) ⭐️ 8.0/10

The article argues that AI, combined with increasing software transparency, is breaking down the two traditional vulnerability disclosure cultures—full disclosure and responsible disclosure—by making it easier to find and exploit vulnerabilities from publicly available patches and code. This shift could fundamentally change how vulnerabilities are managed, potentially leading to shorter embargo periods or even forced full disclosure, which may leave organizations with slower patching cycles at greater risk. The catalyst includes radical adoption of open-source software and improved reversing tools, not just LLMs. Community commenters note this trend predates AI, citing examples like Log4Shell where patches were exploited before CVE disclosure.

hackernews · speckx · May 8, 17:55 · [Discussion](https://news.ycombinator.com/item?id=48066524)

**Background**: Vulnerability disclosure cultures refer to the norms around how security flaws are disclosed: 'full disclosure' immediately publishes details, while 'responsible disclosure' coordinates with vendors before public release. Software transparency, driven by open source and better decompilation, has made it possible for attackers to infer vulnerabilities from patches even before an official disclosure.

<details><summary>References</summary>
<ul>
<li><a href="https://www.bugcrowd.com/blog/vulnerability-disclosure-policy-what-is-it-why-is-it-important/">Vulnerability Disclosure Policy: What is It & Why is it... | @Bugcrowd</a></li>
<li><a href="https://www.backslash.security/blog/the-sbom-revolution-mastering-software-transparency-in-the-age-of-cyber-resilience">The SBOM Revolution: Mastering Software Transparency ... - Backslash</a></li>

</ul>
</details>

**Discussion**: Commenters largely agree that the trend predates AI but acknowledge AI accelerates it. Some argue for private patching or shorter embargoes, while others note that organizations with fast patching are fine, and coordinated disclosure remains important despite cheaper exploit generation.

**Tags**: `#security`, `#vulnerability disclosure`, `#AI`, `#software transparency`, `#open source`

---

<a id="item-8"></a>
## [React2Shell: Critical RCE Vulnerability in React Server Components](https://lachlan.nz/blog/the-react2shell-story/) ⭐️ 8.0/10

A critical remote code execution vulnerability named React2Shell was discovered in React Server Components by security researcher Lachlan, who responsibly disclosed it and collaborated with Meta on remediation. This vulnerability could allow attackers to execute arbitrary code on servers running React Server Components, posing a severe security risk to many modern web applications. The responsible disclosure and collaboration with Meta highlight the critical need for security in the React ecosystem. The vulnerability involved a complex exploit chain described as a 'labyrinth', and the researcher participated in multiple calls with Meta to validate patches. The detailed writeup provides technical insights into the flaw.

hackernews · mufeedvh · May 8, 16:39 · [Discussion](https://news.ycombinator.com/item?id=48065511)

**Background**: React Server Components (RSC) are a feature in React that allow components to be rendered on the server, reducing client-side JavaScript and improving performance. Remote Code Execution (RCE) is a security vulnerability that enables an attacker to run arbitrary code on a target system from a remote location. The React2Shell vulnerability exposed a flaw in how RSC handles certain inputs, potentially leading to RCE.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/React_Server_Components">React Server Components</a></li>
<li><a href="https://www.linkedin.com/pulse/from-input-intrusion-how-remote-code-execution-work-paul-bamidele-mb8we">From Input to Intrusion: How Remote Code Execution Attacks Work</a></li>
<li><a href="https://medium.com/@QuantumCoder99/why-react-server-components-are-the-future-and-what-that-means-for-you-ca5a984760a0">Why React Server Components Are the Future (and What...) | Medium</a></li>

</ul>
</details>

**Discussion**: The community response was largely positive, with Guillermo Rauch praising Lachlan's responsible disclosure and collaboration. Some commenters expressed skepticism about React Server Components' complexity, while others valued the technical details shared in the writeup. Minor complaints about website design were also noted.

**Tags**: `#security`, `#react`, `#vulnerability`, `#RSC`

---

<a id="item-9"></a>
## [AWS North Virginia Outage Resolved, Highlights us-east-1 Fragility](https://www.cnbc.com/2026/05/08/aws-outage-data-center-fanduel-coinbase.html) ⭐️ 8.0/10

An outage at AWS's North Virginia data center (us-east-1) caused by overheating has been resolved, impacting services like FanDuel and Coinbase on May 8, 2026. This incident underscores the systemic risk of the us-east-1 region, which hosts a vast number of critical internet services, and reignites debates about cloud resilience and multi-region architecture. The outage was attributed to overheating due to cooling equipment failure, according to AWS; services including EC2 and RDS were impaired, and the incident lasted several hours before being fully resolved.

hackernews · christhecaribou · May 8, 03:31 · [Discussion](https://news.ycombinator.com/item?id=48058197)

**Background**: AWS us-east-1 is the company's oldest and busiest region, hosting a disproportionate share of internet traffic and many major services. AWS regions are composed of multiple Availability Zones (AZs) for redundancy, but a single AZ failure can still cause widespread impact if applications are not properly distributed.

<details><summary>References</summary>
<ul>
<li><a href="https://www.statuscake.com/blog/when-aws-us-east-1-fails-much-of-the-internet-fails-with-it/">When AWS us - east - 1 Fails, Much of the Internet Fails... - StatusCake</a></li>
<li><a href="https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/using-regions-availability-zones.html">Regions and Zones - Amazon Elastic Compute Cloud</a></li>
<li><a href="https://en.wikipedia.org/wiki/Amazon_Web_Services">Amazon Web Services - Wikipedia</a></li>

</ul>
</details>

**Discussion**: Comments highlight concerns about us-east-1's reliability, with users noting that it remains a single point of failure. Some discuss the potential for insider trading based on outage knowledge, while others question cooling capacity planning at AWS data centers.

**Tags**: `#AWS`, `#outage`, `#cloud computing`, `#reliability`, `#us-east-1`

---

<a id="item-10"></a>
## [Anthropic's Teaching Claude Why Method Reduces AI Misalignment](https://www.anthropic.com/research/teaching-claude-why) ⭐️ 8.0/10

Anthropic presented 'Teaching Claude Why,' a training method that teaches AI models to reason about values, achieving a significant reduction in misalignment using only 3 million tokens of data. This research tackles the critical AI alignment problem, aiming to ensure AI systems reliably follow human intentions. The efficiency of this approach suggests that value-based reasoning training could become a practical tool for improving AI safety across the industry. The misalignment reduction was achieved with only 3 million tokens of training data. The method also generalizes to open-weight models via Anthropic's Model Spec Midtraining, with fine-tuned versions released for Llama 3.1 8B, Qwen 2.5 32B, and Qwen 3 32B.

hackernews · pretext · May 8, 17:59 · [Discussion](https://news.ycombinator.com/item?id=48066592)

**Background**: AI alignment research focuses on ensuring that AI systems act in accordance with human values and goals. Traditional methods like reinforcement learning from human feedback often train models to mimic desired behaviors, but 'Teaching Claude Why' adds explicit reasoning about the underlying values, potentially leading to more robust alignment.

<details><summary>References</summary>
<ul>
<li><a href="https://www.anthropic.com/research/teaching-claude-why">Teaching Claude why \ Anthropic</a></li>

</ul>
</details>

**Discussion**: Commenters noted that the method generalizes to open models and praised the minimal data requirement, with some envisioning future personal alignment. However, others questioned the definition of alignment and its real-world implications, while skeptics pointed to existing powerful models without incidents.

**Tags**: `#ai-alignment`, `#value-learning`, `#anthropic`, `#ai-safety`, `#large-language-models`

---

<a id="item-11"></a>
## [Mozilla Hardens Firefox with Claude Mythos Preview](https://simonwillison.net/2026/May/7/firefox-claude-mythos/#atom-everything) ⭐️ 8.0/10

Mozilla used Anthropic's Claude Mythos preview to identify and patch hundreds of security vulnerabilities in Firefox, with the number of monthly security fixes jumping from ~20-30 to 423 in April 2026. This demonstrates a dramatic improvement in AI-assisted security auditing, shifting from generating 'unwanted slop' to producing actionable, high-signal bug reports that can significantly reduce project maintenance burden. The vulnerabilities found include a 20-year-old XSLT bug and a 15-year-old bug in the HTML <legend> element; many attempted exploits were blocked by Firefox's existing defense-in-depth measures, which is reassuring.

rss · Simon Willison · May 7, 17:56

**Background**: Claude Mythos is Anthropic's most advanced frontier model, released as a preview in April 2026 to select companies. It represents a new model class with state-of-the-art performance in cybersecurity. Mozilla improved their techniques for harnessing these models, steering, scaling, and stacking them to amplify signal and filter noise.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Claude_Mythos_Preview">Claude Mythos Preview</a></li>
<li><a href="https://grokipedia.com/page/Claude_Mythos_Preview">Claude Mythos Preview</a></li>

</ul>
</details>

**Tags**: `#firefox`, `#security`, `#AI`, `#vulnerability detection`, `#LLM`

---

<a id="item-12"></a>
## [Anthropic seeks hundreds of billions, nears $1 trillion valuation](https://www.ft.com/content/a40cafcc-0fa4-4e70-9e24-90d826aea56d) ⭐️ 8.0/10

Anthropic is reportedly planning a massive new funding round worth hundreds of billions of dollars this summer, which could push its valuation to nearly $1 trillion, surpassing OpenAI. This signals a major shift in AI industry leadership and investor sentiment, with Anthropic potentially becoming the most valuable AI company, impacting competition and resource allocation. The valuation is based on secondary market trading on platforms like Forge Global, where Anthropic's implied valuation has reached $1-1.2 trillion, compared to OpenAI's ~$880 billion. Anthropic raised $30 billion in February at a $380 billion valuation.

telegram · zaihuapd · May 8, 11:15

**Background**: Anthropic is an AI safety company and a key competitor to OpenAI. Private secondary markets enable trading of pre-IPO stakes, providing liquidity and price discovery for private companies. The surge reflects strong investor demand for AI infrastructure and enterprise adoption.

<details><summary>References</summary>
<ul>
<li><a href="https://forgeglobal.com/tandem_stock/">Invest and Sell Tandem Stock - Forge</a></li>
<li><a href="https://gadgetbond.com/anthropic-trillion-dollar-valuation-secondary-markets/">Investors chase Anthropic as its secondary value tops $1 trillion</a></li>
<li><a href="https://en.wikipedia.org/wiki/Private-equity_secondary_market">Private-equity secondary market</a></li>

</ul>
</details>

**Tags**: `#Anthropic`, `#AI funding`, `#valuation`, `#industry competition`, `#OpenAI`

---

<a id="item-13"></a>
## [US suspects Nvidia chips smuggled to China via Thailand](https://www.bloomberg.com/news/articles/2026-05-08/us-said-to-suspect-nvidia-chips-smuggled-to-alibaba-via-thailand) ⭐️ 8.0/10

US prosecutors suspect Thai company OBON Corp. smuggled Super Micro servers containing advanced Nvidia chips worth $2.5 billion to China, with Alibaba identified as one of the end customers. This case could escalate US-China tensions over semiconductor export controls and force a reassessment of chip restrictions on Thailand, potentially disrupting AI development in both countries. OBON was involved in creating Thailand's sovereign AI cloud Siam AI, which became an Nvidia partner. Alibaba denies any business relationship with Super Micro or OBON, and the former Siam AI CEO claims he left OBON and the company was not involved in smuggling.

telegram · zaihuapd · May 8, 13:23

**Background**: The US has imposed export controls to prevent advanced semiconductors from reaching China, especially Nvidia's high-end chips used for AI. Thailand has become a potential transshipment hub. This investigation highlights the challenges of enforcing these controls and the complex supply chains involved.

**Tags**: `#Nvidia`, `#chip export controls`, `#smuggling`, `#Alibaba`, `#geopolitics`

---

<a id="item-14"></a>
## [DeepSeek eyes $45B valuation with state-led funding](https://t.me/zaihuapd/41289) ⭐️ 8.0/10

DeepSeek is reportedly seeking a valuation of about $45 billion in its first major external funding round, with China's National Integrated Circuit Industry Investment Fund in talks to lead the investment. This funding round would mark deeper state involvement in China's AI sector, potentially accelerating DeepSeek's growth and intensifying geopolitical competition. It also signals strong confidence in DeepSeek's technology despite US export controls. The National Integrated Circuit Industry Investment Fund, also known as the 'Big Fund,' was established in 2014 to boost China's semiconductor self-sufficiency. If completed, this would be DeepSeek's first time raising external capital at such a high valuation.

telegram · zaihuapd · May 8, 14:59

**Background**: DeepSeek is a Chinese AI company known for developing cost-efficient and power-conscious large language models, competing with global players like OpenAI. The National Integrated Circuit Industry Investment Fund is a state-backed entity that invests in domestic semiconductor and related tech companies to reduce reliance on foreign technology. This potential investment shows the Chinese government's strategic interest in AI as a critical technology sector.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/DeepSeek">DeepSeek - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/China_Integrated_Circuit_Industry_Investment_Fund">China Integrated Circuit Industry Investment Fund - Wikipedia</a></li>
<li><a href="https://www.scmp.com/tech/enterprises/article/2145422/how-chinas-big-fund-helping-country-catch-global-semiconductor-race">How China ’s ‘Big Fund ’ is helping the country catch up in chip race</a></li>

</ul>
</details>

**Tags**: `#DeepSeek`, `#AI`, `#funding`, `#China`, `#industry investment`

---

<a id="item-15"></a>
## [Baidu Releases ERNIE 5.1 with Efficient Pretraining, Claims Top Chinese Search Model](https://mp.weixin.qq.com/s/_I9ziafHheXiJpA-QY2F7A) ⭐️ 8.0/10

Baidu has released ERNIE 5.1, a large language model that uses 'multi-dimensional elastic pretraining' to achieve leading performance at only 6% of typical pretraining cost, and it is now available on Qianfan and ERNIE Bot platforms. This release positions Baidu competitively in the Chinese AI landscape, claiming top scores on LMArena's search benchmark and surpassing DeepSeek-V4-Pro in agent capabilities, which could accelerate adoption of Baidu's AI services. ERNIE 5.1 scored 1223 on LMArena's search ranking, making it #1 in China and #4 globally, and its agent capabilities reportedly exceed DeepSeek-V4-Pro, while creative writing matches Gemini 3.1 Pro and reasoning approaches leading closed-source models.

telegram · zaihuapd · May 9, 07:45

**Background**: Large language model pretraining is typically computationally expensive, with costs often reaching millions of dollars. 'Multi-dimensional elastic pretraining' is a novel approach claimed to dynamically adjust resource usage during training, drastically reducing cost while maintaining or improving performance.

<details><summary>References</summary>
<ul>
<li><a href="https://arxiv.org/html/2510.06882v2">Multi - Dimensional Autoscaling of Stream Processing Services on...</a></li>
<li><a href="https://www.emergentmind.com/topics/elastic-training-paradigm">Elastic Training Paradigm</a></li>

</ul>
</details>

**Tags**: `#AI`, `#Large Language Model`, `#Baidu`, `#ERNIE`, `#NLP`

---