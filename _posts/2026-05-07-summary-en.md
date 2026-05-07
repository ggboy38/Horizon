---
layout: default
title: "Horizon Summary: 2026-05-07 (EN)"
date: 2026-05-07
lang: en
---

> From 34 items, 10 important content pieces were selected

---

1. [Anthropic Partners with SpaceX for Massive GPU Compute](#item-1) ⭐️ 9.0/10
2. [SGLang v0.5.11: CUDA 13, Torch 2.11, Spec Decode V2, New Models](#item-2) ⭐️ 8.0/10
3. [School Programs Cut Child Marriages in Nigeria](#item-3) ⭐️ 8.0/10
4. [SQLite Named Library of Congress Recommended Storage Format](#item-4) ⭐️ 8.0/10
5. [AI creates illusion of productivity with verbose artifacts](#item-5) ⭐️ 8.0/10
6. [Vibe coding and agentic engineering converge in practice](#item-6) ⭐️ 8.0/10
7. [Moonshot AI Valuation Hits $10B After $700M+ Funding Round](#item-7) ⭐️ 8.0/10
8. [Apple R&D spending surpasses 10% of revenue for first time in 30 years](#item-8) ⭐️ 8.0/10
9. [Tencent Hy3 Preview Hits 10x Token Volume vs Hy2 in 2 Weeks](#item-9) ⭐️ 8.0/10
10. [Xiaomi Open-Sources OmniVoice: 646-Language Voice Cloning TTS](#item-10) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [Anthropic Partners with SpaceX for Massive GPU Compute](https://www.anthropic.com/news/higher-limits-spacex) ⭐️ 9.0/10

Anthropic announced a deal with SpaceX to use the entire compute capacity of the Colossus 1 data center, gaining access to over 220,000 Nvidia GPUs and 300 megawatts of power. Immediately, Claude Code's rate limits for all paid plans are doubled, and peak-hour restrictions for Pro/Max users are removed, with significant increases to Claude Opus API limits. This partnership dramatically expands Anthropic's computing resources, enabling faster model training and higher service capacity for Claude. It underscores the critical role of massive-scale GPU clusters in the competitive AI landscape and represents a strategic alliance between two major tech players. The Colossus 1 data center in Memphis, Tennessee, provides over 300 megawatts of power and more than 220,000 Nvidia GPUs. Claude Code's 5-hour rate limit is doubled for all paid tiers, and Pro/Max users no longer face peak-hour restrictions; Claude Opus API rate limits are also substantially increased.

telegram · zaihuapd · May 6, 16:35

**Background**: Anthropic is the developer of Claude, a leading AI assistant and family of large language models. Claude Code is a recently released agentic coding tool that integrates with the user's codebase to perform software development tasks. The Colossus 1 data center, originally built by xAI (also owned by Elon Musk), is one of the largest AI supercomputers in the world.

<details><summary>References</summary>
<ul>
<li><a href="https://www.cnbc.com/2026/05/06/anthropic-spacex-data-center-capacity.html">Anthropic, SpaceX announce compute deal, includes space ...</a></li>
<li><a href="https://www.msn.com/en-us/news/other/anthropic-secures-full-use-of-spacexs-colossus-1-data-center/gm-GML9F02A91">Anthropic secures full use of SpaceX's Colossus 1 data center</a></li>

</ul>
</details>

**Tags**: `#AI`, `#算力合作`, `#Claude`, `#Anthropic`, `#SpaceX`

---

<a id="item-2"></a>
## [SGLang v0.5.11: CUDA 13, Torch 2.11, Spec Decode V2, New Models](https://github.com/sgl-project/sglang/releases/tag/v0.5.11) ⭐️ 8.0/10

SGLang v0.5.11 upgrades default CUDA to 13 and PyTorch to 2.11, makes speculative decoding V2 the default, introduces decode radix cache for PD disaggregation, and adds support for models like Gemma 4, GLM-5.1, Qwen3.6, and Kimi-K2.6. This release significantly modernizes the SGLang inference stack with latest CUDA and PyTorch versions, and improves inference performance through default speculative decoding V2 and enhanced caching for disaggregated deployments. These updates are critical for developers deploying large language models at scale, offering both speed and flexibility. Speculative decoding V2 uses overlap scheduling to hide CPU overhead, reducing per-step CPU cost for EAGLE/MTP/DFLASH paths. The new decode radix cache recovers prefix cache hit rates under prefill/decode disaggregation, saving TTFT for long shared prefixes.

github · Kangyan-Zhou · May 5, 21:28

**Background**: SGLang is a high-performance serving framework for large language models and multimodal models, known for its RadixAttention mechanism. Speculative decoding is a technique that uses a small draft model to propose tokens and a target model to verify them in parallel, speeding up inference. PD (prefill-decode) disaggregation separates the prefill and decode phases across different workers to optimize resource utilization.

<details><summary>References</summary>
<ul>
<li><a href="https://github.com/sgl-project/sglang">GitHub - sgl-project/ sglang : SGLang is a high-performance serving...</a></li>
<li><a href="https://newreleases.io/project/github/sgl-project/sglang/release/v0.5.11">sgl-project/ sglang v0.5.11 on GitHub</a></li>
<li><a href="https://github.com/sgl-project/sglang/issues/3554">[Feature] Proposal for adding PD - Disaggregation Feature to SGLang...</a></li>

</ul>
</details>

**Tags**: `#SGLang`, `#LLM inference`, `#CUDA`, `#PyTorch`, `#speculative decoding`

---

<a id="item-3"></a>
## [School Programs Cut Child Marriages in Nigeria](https://www.nature.com/articles/d41586-026-00796-2) ⭐️ 8.0/10

A new study finds that targeted school programs, which address the reasons girls drop out, significantly reduce child marriages in Nigeria. This research highlights a scalable intervention that can improve girls' lives and reduce a harmful practice, informing policy in Nigeria and other developing regions. The study is observational, and commenters note that the reduction may stem from the support system and safe environment provided, not just school attendance per se.

hackernews · surprisetalk · May 7, 13:30 · [Discussion](https://news.ycombinator.com/item?id=48049208)

**Background**: Child marriage remains prevalent in Nigeria, with many girls forced into marriage early due to poverty, cultural norms, and lack of educational opportunities. Keeping girls in school is often proposed as a protective factor, but evidence on effective programs is limited.

**Discussion**: Commenters debate whether the effect is due to schooling or the program's broader support; some suggest other factors like factory jobs also help reduce child marriage. Others recommend reading the full policy brief for more context.

**Tags**: `#education`, `#child marriage`, `#Nigeria`, `#social development`, `#policy`

---

<a id="item-4"></a>
## [SQLite Named Library of Congress Recommended Storage Format](https://sqlite.org/locrsf.html) ⭐️ 8.0/10

The Library of Congress has officially recommended SQLite as a storage format for digital preservation, highlighting its reliability and durability. This endorsement from a major cultural institution validates SQLite as a trusted format for long-term data storage, potentially boosting its adoption in archiving and other sectors. The recommendation is based on SQLite's proven stability and widespread use; however, community comments note that this recognition dates back to 2018, making it several years old.

hackernews · whatisabcdefgh · May 6, 21:58 · [Discussion](https://news.ycombinator.com/item?id=48042434)

**Background**: SQLite is a self-contained, serverless database engine widely used in applications for local data storage. The Library of Congress maintains a list of recommended formats for sustaining digital content, and its inclusion signals that SQLite meets high standards for preservation.

**Discussion**: Community comments show mixed views: some praise SQLite's reliability, while others note it may be overkill for simple use cases and point out the announcement's age. One commenter created a lighter alternative, and another highlights corporate bans due to data portability risks.

**Tags**: `#SQLite`, `#data storage`, `#Library of Congress`, `#file formats`, `#digital preservation`

---

<a id="item-5"></a>
## [AI creates illusion of productivity with verbose artifacts](https://nooneshappy.com/article/appearing-productive-in-the-workplace/) ⭐️ 8.0/10

An article critiques how AI is used to generate lengthy, superficial work artifacts (e.g., requirements documents, status updates) that create an illusion of productivity while diluting expert judgment and elongating workplace communications. This matters because it highlights a growing trend where AI-generated content undermines genuine productivity and expertise, leading to bloated workflows and erosion of critical thinking in professional settings. The article identifies three forms of this problem: novices producing work resembling seniors', people generating artifacts in untrained disciplines, and experts whose judgment and taste are diluted by AI reliance.

hackernews · diebillionaires · May 6, 16:18 · [Discussion](https://news.ycombinator.com/item?id=48038001)

**Background**: The article is a critique of a phenomenon where AI tools like large language models are used to generate verbose, seemingly professional documents. This creates an illusion of productivity but actually wastes time and dilutes true expertise. The author observes that workplace communications are becoming elongated and less meaningful.

**Discussion**: Comments resonate deeply with the article's observations, with users sharing real-world examples of managers using AI to appear competent, leading to over-engineered designs and personal attacks when challenged. One commenter notes that LLMs have automated sucking up to management.

**Tags**: `#AI`, `#workplace productivity`, `#software engineering`, `#management`, `#critique`

---

<a id="item-6"></a>
## [Vibe coding and agentic engineering converge in practice](https://simonwillison.net/2026/May/6/vibe-coding-and-agentic-engineering/#atom-everything) ⭐️ 8.0/10

Simon Willison, an experienced software engineer, reveals that vibe coding and agentic engineering are blurring in his own work, as AI coding tools become more reliable and he finds himself reviewing less of the generated code, even for production systems. This convergence challenges the earlier distinction between irresponsible vibe coding for personal projects and responsible agentic engineering, raising questions about code trustworthiness and engineering standards as AI tools become more autonomous. Willison notes that for routine tasks like creating a JSON API endpoint with SQL, he trusts Claude Code to produce correct code without review, but feels guilt about not checking every line, comparing it to relying on code from other teams in large organizations.

rss · Simon Willison · May 6, 14:24 · [Discussion](https://news.ycombinator.com/item?id=48037128)

**Background**: Vibe coding is an AI-assisted practice where developers describe what they want and let an LLM generate code, often without scrutinizing the output. Agentic engineering involves using AI tools as an assistant while maintaining full oversight and engineering rigor. The distinction has been widely discussed since Andrej Karpathy coined 'vibe coding' in early 2025.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Vibe_coding">Vibe coding - Wikipedia</a></li>
<li><a href="https://www.ibm.com/think/topics/agentic-engineering">What is agentic engineering? - IBM</a></li>
<li><a href="https://mitsloan.mit.edu/ideas-made-to-matter/agentic-ai-explained">Agentic AI, explained - MIT Sloan</a></li>

</ul>
</details>

**Discussion**: Commenters express skepticism about AI reliability, with one noting that errors become more subtle and harder to catch. Another points out that undisciplined engineering practices existed before AI but are now accelerated. A third questions the assumption that AI always gets routine tasks right, citing missing architectural decisions.

**Tags**: `#AI coding`, `#vibe coding`, `#agentic engineering`, `#software engineering`, `#LLM tools`

---

<a id="item-7"></a>
## [Moonshot AI Valuation Hits $10B After $700M+ Funding Round](https://t.me/zaihuapd/41251) ⭐️ 8.0/10

Moonshot AI, the Chinese AI startup behind the Kimi assistant, has completed a new funding round of over $700 million led by Alibaba and Tencent, pushing its valuation past $10 billion. In the past 20 days, Kimi's cumulative revenue has already surpassed its total for the entire year of 2025, driven by global paid users and API calls, with overseas revenue now exceeding domestic. This milestone underscores the rapid growth and valuation escalation of Chinese AI startups, challenging U.S. dominance in the large language model space. The revenue surge indicates strong product-market fit and global adoption, positioning Moonshot AI as a key player alongside leading international models. The cumulative funding for Moonshot AI now exceeds $1.2 billion. Its latest model, the open-source K2.5, is a multimodal agentic model built on 15 trillion tokens and is available on platforms like OpenRouter.

telegram · zaihuapd · May 7, 00:30

**Background**: Moonshot AI is a Chinese startup founded in 2023, known for developing the Kimi large language model and assistant. The company has gained attention for its open-source K2 series, with K2.5 being its most powerful model, integrating vision, language, and agentic capabilities. OpenRouter is a unified API platform providing access to various AI models.

<details><summary>References</summary>
<ul>
<li><a href="https://www.kimi.com/ai-models/kimi-k2-5">Kimi K2.5 | Open Visual Agentic Model for Real Work</a></li>
<li><a href="https://github.com/MoonshotAI/Kimi-K2.5">GitHub - MoonshotAI/Kimi-K2.5: Moonshot's most powerful model</a></li>
<li><a href="https://openrouter.ai/models">Models | OpenRouter</a></li>

</ul>
</details>

**Tags**: `#AI`, `#Funding`, `#Startup`, `#Large Language Model`

---

<a id="item-8"></a>
## [Apple R&D spending surpasses 10% of revenue for first time in 30 years](https://www.cnbc.com/2026/05/06/apples-rd-spending-climbs-to-10percent-of-revenue-on-ai-investments.html) ⭐️ 8.0/10

Apple's R&D spending reached 10.3% of revenue in the March 2026 fiscal quarter, the first time it has exceeded 10% in 30 years, with R&D investment growing 34% year-over-year despite 17% revenue growth. This marks a strategic pivot for Apple, as it aggressively invests in on-device AI, custom chips, and private cloud computing to reshape its hardware platform, similar to the iPod-era transformation. The move signals Apple's urgency to catch up in AI and could define its post-iPhone product lineup. Apple is reportedly developing AI glasses and AirPods with cameras, alongside a foldable iPhone and Siri upgrades. CEO Tim Cook is set to step down in September 2026, and the company is focusing on on-device AI and private cloud computing to power Apple Intelligence.

telegram · zaihuapd · May 7, 01:00

**Background**: On-device AI runs AI models directly on devices like phones and tablets without constant cloud connectivity, enabling faster responses and better privacy. Apple's 'Private Cloud Compute' is a server infrastructure that handles complex AI tasks securely. Apple's R&D spending ratios had been below 10% for decades, and this increase reflects a major strategic bet.

<details><summary>References</summary>
<ul>
<li><a href="https://zhuanlan.zhihu.com/p/1931281139416404545">终于有人把端侧大模型说清楚了 - 知乎</a></li>
<li><a href="https://stock.10jqka.com.cn/usstock/20260218/c674837048.shtml">消息称 苹 果 AI 私 有 云 端 算 力大跃进：跳过 M3 和 M4，直接部署 M5 芯片</a></li>
<li><a href="https://www.163.com/dy/article/KRODH2L40511B8LM.html">苹 果 AI 眼 镜 曝光：内置2颗摄像头、支持Siri交互、可手势控制</a></li>

</ul>
</details>

**Tags**: `#Apple`, `#AI`, `#R&D`, `#hardware`, `#strategy`

---

<a id="item-9"></a>
## [Tencent Hy3 Preview Hits 10x Token Volume vs Hy2 in 2 Weeks](https://finance.sina.com.cn/tech/shenji/2026-05-07/doc-inhwzrtp8521239.shtml) ⭐️ 8.0/10

Tencent's Hy3 preview model achieved over ten times the token call volume of its predecessor Hy2 within two weeks of launch and ranked first on OpenRouter's weekly leaderboard overall and in market share. This rapid adoption signals strong market validation for Tencent's latest open-source LLM, which could accelerate competition among major AI providers and drive further innovation in agent and coding scenarios. The Hy3 preview is a 295B-parameter Mixture-of-Experts (MoE) model with 21B active parameters and a 256K token context window, showing particular strength in coding and tool-use tasks with over 16.5x growth in related applications.

telegram · zaihuapd · May 7, 05:34

**Background**: Tencent Hunyuan (Hy) is a series of large language models developed by Tencent. The Hy3 preview is the latest open-source MoE model, which activates only a subset of parameters per token for efficiency. OpenRouter is a unified API platform that aggregates models from multiple providers, allowing users to compare and access them easily.

<details><summary>References</summary>
<ul>
<li><a href="https://hy3ai.com/">Hy3 Preview — Tencent Hunyuan 3 Open-Source Model</a></li>
<li><a href="https://www.tencent.com/en-us/articles/2202320.html">Tencent Unveils Hy3 preview; Model Enhances Agent ...</a></li>
<li><a href="https://huggingface.co/tencent/Hy3-preview">tencent/Hy3-preview · Hugging Face</a></li>

</ul>
</details>

**Tags**: `#AI models`, `#Tencent`, `#OpenRouter`, `#LLM`, `#model benchmark`

---

<a id="item-10"></a>
## [Xiaomi Open-Sources OmniVoice: 646-Language Voice Cloning TTS](https://mp.weixin.qq.com/s/TCS_Sd10g_rvf1cszw673A) ⭐️ 8.0/10

Xiaomi has open-sourced OmniVoice, a massively multilingual zero-shot text-to-speech (TTS) model that supports over 600 languages, including voice cloning. The model achieves a training speed of 100,000 hours per day and a PyTorch inference speed of 40x real-time, outperforming mainstream commercial systems in synthesis quality. This release democratizes high-quality multilingual TTS, enabling applications in accessibility, education, and global communication. Its zero-shot voice cloning capability allows users to clone voices in hundreds of languages without fine-tuning, significantly reducing the barrier to personalized speech synthesis. OmniVoice uses a diffusion language model-style discrete non-autoregressive architecture with full-codebook random masking. It was trained on 580,000 hours of speech data across 646 languages from 50 open-source datasets, and supports cross-lingual voice cloning, custom voice design, noisy speech adaptation, and pronunciation correction.

telegram · zaihuapd · May 7, 10:06

**Background**: Text-to-speech (TTS) systems convert written text into spoken audio. Traditional TTS models often require separate models or fine-tuning for each language, limiting scalability. OmniVoice unifies hundreds of languages into a single model with zero-shot voice cloning, where a model can mimic a speaker's voice from just a few seconds of audio without additional training.

<details><summary>References</summary>
<ul>
<li><a href="https://huggingface.co/k2-fsa/OmniVoice">k2-fsa/OmniVoice · Hugging Face</a></li>
<li><a href="https://zhu-han.github.io/omnivoice/">OmniVoice - zhu-han.github.io</a></li>
<li><a href="https://dev.to/_46ea277e677b888e0cd13/omnivoice-open-source-tts-with-600-languages-and-zero-shot-voice-cloning-1mpn">OmniVoice: Open-Source TTS with 600+ Languages and Zero-Shot ...</a></li>

</ul>
</details>

**Tags**: `#语音合成`, `#多语言`, `#开源`, `#TTS`, `#小米`

---