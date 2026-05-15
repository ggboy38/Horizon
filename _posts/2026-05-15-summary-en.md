---
layout: default
title: "Horizon Summary: 2026-05-15 (EN)"
date: 2026-05-15
lang: en
---

> From 38 items, 9 important content pieces were selected

---

1. [Pixel 10 Zero-Click Exploit Chain Disclosed by Project Zero](#item-1) ⭐️ 9.0/10
2. [vLLM v0.21.0: KV Offload, Spec Decoding, Blackwell Support](#item-2) ⭐️ 8.0/10
3. [O(x)Caml in Space: Stack Allocation Achieves Single-Digit Nanosecond Latency](#item-3) ⭐️ 8.0/10
4. [How to remove modem and GPS from 2024 RAV4 hybrid](#item-4) ⭐️ 8.0/10
5. [Antirez Launches DS4, Minimal DeepSeek 4 Runtime](#item-5) ⭐️ 8.0/10
6. [RTX 5090 eGPU Boosts M4 MacBook Air Gaming and AI](#item-6) ⭐️ 8.0/10
7. [OpenAI's Codex Now Integrated into ChatGPT Mobile App](#item-7) ⭐️ 8.0/10
8. [Nginx-Rift Exploit: New Vulnerability in Rewrite and Set Directives](#item-8) ⭐️ 8.0/10
9. [arXiv bans unverified LLM content for one year](#item-9) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [Pixel 10 Zero-Click Exploit Chain Disclosed by Project Zero](https://projectzero.google/2026/05/pixel-10-exploit.html) ⭐️ 9.0/10

Google Project Zero has disclosed a full zero-click exploit chain for the Pixel 10, starting from a remote Dolby audio decoding bug and escalating to kernel control via a vulnerable video driver. This research highlights how AI-powered features increase the zero-click attack surface and demonstrates that shallow vendor driver bugs can still undermine Android's security model, even on flagship devices. The exploit chain leverages a Dolby 0-click vulnerability (CVE-2025-54957) that affected all Android devices until patched in January 2026, combined with a kernel vulnerability in the video processing driver.

hackernews · happyhardcore · May 15, 13:39 · [Discussion](https://news.ycombinator.com/item?id=48148460)

**Background**: A zero-click exploit requires no user interaction, making it extremely dangerous. Project Zero is Google's elite security team that finds and discloses vulnerabilities to improve platform security. The Dolby audio decoding library contained a remote code execution bug that could trigger without the user opening a message.

<details><summary>References</summary>
<ul>
<li><a href="https://projectzero.google/2026/05/pixel-10-exploit.html">A 0-click exploit chain for the Pixel 10: When a Door Closes, a Window ...</a></li>
<li><a href="https://gbhackers.com/pixel-10-zero-click-exploit-chain/">Google Project Zero Details Pixel 10 Zero-Click Exploit Chain</a></li>

</ul>
</details>

**Discussion**: Community members expressed concern that AI features are increasing attack surface, as they often decode media before user interaction. One commenter praised Google's patch response time, noting it was faster than typical Android vendor response.

**Tags**: `#security`, `#exploit`, `#android`, `#kernel`, `#pixel`

---

<a id="item-2"></a>
## [vLLM v0.21.0: KV Offload, Spec Decoding, Blackwell Support](https://github.com/vllm-project/vllm/releases/tag/v0.21.0) ⭐️ 8.0/10

vLLM v0.21.0 introduces breaking build changes (C++20 requirement, transformers v4 deprecation), KV cache offloading integrated with the Hybrid Memory Allocator (HMA), speculative decoding that respects reasoning budgets, and a new TOKENSPEED_MLA attention backend for Blackwell GPUs. The release includes 367 commits from 202 contributors. These updates significantly improve the efficiency and flexibility of LLM inference, enabling longer context handling via KV offload, faster generation through improved speculative decoding, and support for the latest NVIDIA Blackwell GPUs. Users of vLLM for large-scale model serving will benefit from better memory utilization and broader model compatibility. The C++20 requirement is a breaking change for users compiling from source; transformers v5 migration is now recommended. The KV offload with HMA includes scheduler-side sliding window support and multi-connector HMA for distributed setups. Speculative decoding now correctly handles reasoning budgets, enabling use with reasoning models like DeepSeek-R1.

github · khluu · May 15, 08:44

**Background**: vLLM is a high-performance inference engine for large language models. KV cache offloading moves key-value cache data from GPU memory to CPU memory or disk, allowing models to handle very long contexts that exceed GPU HBM capacity. Speculative decoding accelerates inference by using a smaller draft model to propose multiple tokens, which a larger target model then verifies in parallel. The Hybrid Memory Allocator (HMA) optimizes memory allocation for different attention layer types, reducing fragmentation and improving throughput.

<details><summary>References</summary>
<ul>
<li><a href="https://docs.vllm.ai/en/latest/design/hybrid_kv_cache_manager/">Hybrid KV Cache Manager - vLLM</a></li>
<li><a href="https://vllm-project.github.io/2026/01/08/kv-offloading-connector.html">Inside vLLM’s New KV Offloading Connector: Smarter Memory ...</a></li>
<li><a href="https://developer.nvidia.com/blog/an-introduction-to-speculative-decoding-for-reducing-latency-in-ai-inference/">An Introduction to Speculative Decoding for Reducing Latency ...</a></li>

</ul>
</details>

**Tags**: `#vllm`, `#LLM inference`, `#GPU computing`, `#release notes`, `#AI/ML`

---

<a id="item-3"></a>
## [O(x)Caml in Space: Stack Allocation Achieves Single-Digit Nanosecond Latency](https://gazagnaire.org/blog/2026-05-14-borealis.html) ⭐️ 8.0/10

On 23 April 2026, the Borealis satellite booted in orbit on DPhi Space's ClusterGate-2, running a pure-OCaml CCSDS protocol stack with end-to-end encryption and post-quantum key rotation, and OxCaml's stack allocation annotations reduced p99.9 latency from 29 ns to 9 ns per packet. This demonstrates that garbage-collected languages like OCaml can achieve ultra-low latencies suitable for space software, by using stack allocation annotations to eliminate GC pressure entirely. The stack allocation annotations (via OxCaml's `stack_` keyword) removed all 394 minor GCs over 25 million packets, maintaining comparable throughput.

hackernews · yminsky · May 15, 10:55 · [Discussion](https://news.ycombinator.com/item?id=48147058)

**Background**: OCaml is a garbage-collected functional programming language. Traditionally, GC pauses have made it unsuitable for real-time systems like satellite software. OxCaml is an OCaml variant that introduces stack allocation annotations, allowing developers to move heap allocations to the stack to reduce GC pressure. CCSDS is a standard for spacecraft communication protocols.

<details><summary>References</summary>
<ul>
<li><a href="https://gazagnaire.org/blog/2026-05-14-borealis.html">Thomas Gazagnaire :: O (x)Caml in Space</a></li>
<li><a href="https://oxcaml.org/documentation/stack-allocation/reference/">OxCaml | Stack allocation | Reference</a></li>
<li><a href="https://tarides.com/blog/2025-04-03-ocaml-in-space-spaceos-is-on-a-satellite/">OCaml in Space: SpaceOS is on a Satellite! - tarides.com</a></li>

</ul>
</details>

**Discussion**: The community noted previous OCaml usage in space (GHGSat-D in 2016) and discussed the difficulty of bending garbage-collected languages for low-latency scenarios. One commenter questioned the trade-offs, while another pointed out that CCSDS protocols often reinvent the wheel, questioning if memory safety is the primary concern.

**Tags**: `#OCaml`, `#systems programming`, `#garbage collection`, `#space software`, `#low-latency`

---

<a id="item-4"></a>
## [How to remove modem and GPS from 2024 RAV4 hybrid](https://arkadiyt.com/2026/05/13/removing-the-modem-and-gps-from-my-rav4/) ⭐️ 8.0/10

A detailed guide has been published on physically removing the modem and GPS from a 2024 Toyota RAV4 hybrid to stop telemetry data collection. The guide includes step-by-step instructions and discusses workarounds such as using wired USB instead of Bluetooth to prevent data transmission. This matters for privacy-conscious vehicle owners concerned about continuous telemetry collection by automakers. The physical removal method provides a definitive solution, though it may affect safety features like SOS and potentially impact insurance premiums. Even after modem removal, if the phone connects via Bluetooth, the car uses the phone's internet to send telemetry; using a wired USB connection avoids this. The guide notes that CarPlay and Android Auto also capture telemetry, so a wired connection doesn't entirely eliminate data collection.

hackernews · arkadiyt · May 14, 17:08 · [Discussion](https://news.ycombinator.com/item?id=48138136)

**Background**: Modern vehicles are equipped with a telematic control unit (TCU) that collects and transmits data via cellular networks. This telemetry data includes location, driving behavior, and vehicle diagnostics, often shared with manufacturers and third parties. Disabling the TCU physically is one way to stop this transmission, but it may disable emergency call features and void warranties in some cases.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Telematic_control_unit">Telematic control unit</a></li>
<li><a href="https://www.geotab.com/glossary/telemetry/">What is telemetry? How it works and why fleets need it - Geotab</a></li>
<li><a href="https://www.zetronix.com/blog/post/disable-gps-tracking-car">Disable Car GPS Tracking: Privacy Steps Guide</a></li>

</ul>
</details>

**Discussion**: Commenters raised concerns about insurance pricing being tied to safety features like automatic crash notification, warning that removing the modem could increase premiums. Another user noted that Carfax mileage validation rejected an estimate lower than the last recorded value, suggesting data is shared widely. A technical detail was debated: whether wired USB prevents all telemetry, as CarPlay/Android Auto still capture data.

**Tags**: `#privacy`, `#automotive`, `#telemetry`, `#security`, `#DIY`

---

<a id="item-5"></a>
## [Antirez Launches DS4, Minimal DeepSeek 4 Runtime](https://antirez.com/news/165) ⭐️ 8.0/10

Antirez (Salvatore Sanfilippo) has released DS4, a minimal and specialized inference engine for DeepSeek V4 Flash, targeting Macs with 96GB RAM and NVIDIA GPUs. The project is open-source and prioritizes Metal and CUDA backends. DS4 enables local, private inference of a powerful 1M-context model like DeepSeek V4 Flash, reducing cloud dependency and latency. It highlights the trend toward specialized, hardware-optimized runtimes for specific models. DS4 is not a general GGUF runner but a narrow engine for DeepSeek V4 Flash, using Metal as primary target and supporting NVIDIA CUDA with special care for DGX Spark. It is built on top of llama.cpp and GGML, and requires 96GB VRAM for full operation.

hackernews · caust1c · May 14, 22:29 · [Discussion](https://news.ycombinator.com/item?id=48142108)

**Background**: DeepSeek V4 is a Mixture-of-Experts (MoE) model series released by DeepSeek in 2026, with versions like V4 Pro (1.6T params) and V4 Flash (284B params), both supporting a 1M-token context window. DS4 is the latest project by antirez, the creator of Redis, who aimed to create a focused, efficient inference runtime rather than a general framework.

<details><summary>References</summary>
<ul>
<li><a href="https://github.com/antirez/ds4">GitHub - antirez/ds4: DeepSeek 4 Flash local inference engine for Metal ...</a></li>
<li><a href="https://thecodersblog.com/deepseek-4-flash-local-inference-engine-2026/">DeepSeek 4 Flash: Local LLM Inference on Metal - The Coders Blog</a></li>
<li><a href="https://huggingface.co/deepseek-ai/DeepSeek-V4-Pro">deepseek-ai/DeepSeek-V4-Pro · Hugging Face</a></li>

</ul>
</details>

**Discussion**: Community members report positive experiences, with some noting DS4 feels close to Claude in quality but slower. There is discussion about whether intelligence saturation for coding tasks might reduce demand for larger models, and technical clarifications about VRAM requirements and backend support.

**Tags**: `#LLM`, `#inference`, `#runtime`, `#DeepSeek`, `#antirez`

---

<a id="item-6"></a>
## [RTX 5090 eGPU Boosts M4 MacBook Air Gaming and AI](https://scottjg.com/posts/2026-05-05-egpu-mac-gaming/) ⭐️ 8.0/10

An article demonstrates that connecting an RTX 5090 via eGPU to an M4 MacBook Air significantly improves gaming compatibility and LLM prompt processing speed, despite macOS limitations. This breakthrough bridges a major gap for Mac users who need high GPU performance for gaming and AI workloads, potentially driving demand for Apple to support external NVIDIA GPUs natively. The setup uses Thunderbolt 4 connectivity and requires workarounds for macOS driver limitations, with benchmarks showing substantial gains in both frame rates and prompt processing times.

hackernews · allenleee · May 14, 15:47 · [Discussion](https://news.ycombinator.com/item?id=48137145)

**Background**: eGPUs have historically required Intel Macs and AMD GPUs, but this project shows it's possible on Apple Silicon with custom solutions. GPU passthrough in virtual machines on macOS remains unsupported by Apple.

<details><summary>References</summary>
<ul>
<li><a href="https://www.makeuseof.com/how-build-diy-egpu/">I Built My Own eGPU for My Laptop (It's Easier Than I Expected) - MUO</a></li>
<li><a href="https://www.reddit.com/r/eGPU/comments/hdokxg/a_noobs_guide_to_a_do_it_yourself_egpu_very_easy/">A noob's guide to a Do It Yourself eGPU (VERY EASY and CHEAP) : r/eGPU</a></li>

</ul>
</details>

**Discussion**: Commenters express strong interest in native GPU passthrough support, with many noting the LLM performance improvements as particularly valuable. Some suggest alternative approaches like Vulkan translation layers.

**Tags**: `#eGPU`, `#macOS gaming`, `#LLM inference`, `#Apple Silicon`, `#GPU passthrough`

---

<a id="item-7"></a>
## [OpenAI's Codex Now Integrated into ChatGPT Mobile App](https://openai.com/index/work-with-codex-from-anywhere/) ⭐️ 8.0/10

OpenAI has integrated its AI coding agent Codex directly into the ChatGPT mobile app, enabling developers to write and debug code on the go for free. This move makes professional-grade coding assistance accessible anywhere, potentially boosting developer productivity and lowering barriers to mobile development. Codex is free to use on the mobile app for ChatGPT account holders, though interactions may be used for training. The tool supports file syncing and can handle complex coding tasks through natural language prompts.

hackernews · mikeevans · May 14, 20:06 · [Discussion](https://news.ycombinator.com/item?id=48140529)

**Background**: Codex is a suite of AI-driven coding agents by OpenAI that automates software engineering tasks. It was previously available via desktop app or CLI, and the mobile integration extends its reach to smartphones, leveraging ChatGPT's existing user base.

<details><summary>References</summary>
<ul>
<li><a href="https://grokipedia.com/page/OpenAI_Codex">OpenAI Codex</a></li>
<li><a href="https://github.com/openai/codex">GitHub - openai / codex : Lightweight coding agent that runs in your...</a></li>
<li><a href="https://news.google.com/stories/CAAqNggKIjBDQklTSGpvSmMzUnZjbmt0TXpZd1NoRUtEd2pjcXUtTUVSSEx2bW8yTG4wMUh5Z0FQAQ?hl=en-NG&gl=NG&ceid=NG:en">Google News - OpenAI adds Codex coding tool to ChatGPT mobile...</a></li>

</ul>
</details>

**Discussion**: The community largely welcomes the free mobile access, with some users praising its convenience for architectural decisions and code review on the go. However, a few note that the smaller screen and lack of keyboard can reduce effectiveness compared to desktop use.

**Tags**: `#OpenAI`, `#Codex`, `#mobile development`, `#AI coding assistant`

---

<a id="item-8"></a>
## [Nginx-Rift Exploit: New Vulnerability in Rewrite and Set Directives](https://github.com/DepthFirstDisclosures/Nginx-Rift) ⭐️ 8.0/10

A new Nginx exploit, dubbed Nginx-Rift, has been published on GitHub, targeting specific combinations of the rewrite and set directives. The exploit potentially allows for ASLR bypass and remote code execution under certain conditions. This vulnerability is significant because Nginx is one of the most widely used web servers globally. If exploited, it could lead to remote code execution on millions of servers, and the community debate highlights both the severity and the mitigation strategies. The exploit requires a rewrite directive with a question mark in the replacement string, followed by a set directive referencing a regex capture group (e.g., set $var $1). The proof-of-concept assumes ASLR is disabled, but the writeup claims a reliable ASLR bypass is possible. Patches have been released in Nginx versions 1.31.0 and 1.30.1, and F5 also provides mitigation using named captures.

hackernews · hetsaraiya · May 14, 17:17 · [Discussion](https://news.ycombinator.com/item?id=48138268)

**Background**: The Nginx rewrite directive is used to change request URIs using regular expressions, and the set directive allows assigning values to variables. ASLR (Address Space Layout Randomization) is a security technique that randomizes memory addresses to make exploitation harder. This vulnerability exploits a memory corruption issue when specific rewrite and set configurations are used together, potentially allowing an attacker to execute arbitrary code.

<details><summary>References</summary>
<ul>
<li><a href="https://nginx.org/en/docs/http/ngx_http_rewrite_module.html">Module ngx_http_rewrite_module - nginx</a></li>

</ul>
</details>

**Discussion**: The community discussion is polarized: some commenters downplay the severity because the published proof-of-concept requires ASLR to be disabled, while security professionals argue that ASLR bypass is possible and should be assumed. Others provide specific mitigation details, such as using named captures instead of unnamed ones. There is also concern about vulnerability scanners not yet detecting this issue in Docker images.

**Tags**: `#nginx`, `#exploit`, `#security`, `#vulnerability`, `#web-server`

---

<a id="item-9"></a>
## [arXiv bans unverified LLM content for one year](https://x.com/tdietterich/status/2055000956144935055) ⭐️ 8.0/10

arXiv announced a one-year ban on submissions containing unverified LLM-generated content, such as hallucinated citations and LLM metadata comments. After the ban, future submissions must first be accepted by a trusted peer-reviewed venue before being posted to arXiv. This is arXiv's first explicit policy to penalize LLM misuse, setting a critical precedent for academic integrity in AI-assisted writing. It directly affects researchers using LLMs and may influence other preprint platforms to adopt similar measures. Penalties apply to obvious unverified content like hallucinated citations, LLM metadata comments, and placeholder text such as 'table data is just an example, please replace with real experimental data.' arXiv's code of conduct holds authors fully responsible for all content, regardless of how it was generated.

telegram · zaihuapd · May 15, 04:30

**Background**: arXiv is a widely used preprint repository. In recent years, hallucinated citations and metadata generated by LLMs have polluted academic literature; a 2025 analysis estimated nearly 150,000 hallucinated citations across arXiv and other repositories. This policy aims to curb such issues by enforcing author accountability.

<details><summary>References</summary>
<ul>
<li><a href="https://www.nature.com/articles/d41586-026-00969-z">Hallucinated citations are polluting the scientific literature. What ...</a></li>
<li><a href="https://arxiv.org/abs/2605.07723">[2605.07723] LLM hallucinations in the wild: Large-scale evidence from ...</a></li>
<li><a href="https://en.wikipedia.org/wiki/Peer_review">Peer review - Wikipedia</a></li>

</ul>
</details>

**Tags**: `#arXiv`, `#LLM`, `#academic integrity`, `#policy`, `#AI-generated content`

---