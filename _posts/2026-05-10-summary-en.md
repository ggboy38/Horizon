---
layout: default
title: "Horizon Summary: 2026-05-10 (EN)"
date: 2026-05-10
lang: en
---

> From 32 items, 8 important content pieces were selected

---

1. [Bun's AI-assisted Rust rewrite achieves 99.8% test pass rate](#item-1) ⭐️ 8.0/10
2. [Internet Archive Switzerland Launches as Independent Digital Library](#item-2) ⭐️ 8.0/10
3. [Gowers Tests ChatGPT 5.5 Pro on Math Problems](#item-3) ⭐️ 8.0/10
4. [Distributing Mac software frustrates developers](#item-4) ⭐️ 8.0/10
5. [HTML vs Markdown: A Better Output Format for Claude](#item-5) ⭐️ 8.0/10
6. [NASA Rotor Breakthrough Enables Heavier Mars Helicopters](#item-6) ⭐️ 8.0/10
7. [Chinese Grey Market Sells Claude API Access at 90% Off, Report Reveals](#item-7) ⭐️ 8.0/10
8. [xAI Leaks Grok Build Coding Tool, Aims to Rival Claude Code](#item-8) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [Bun's AI-assisted Rust rewrite achieves 99.8% test pass rate](https://twitter.com/jarredsumner/status/2053047748191232310) ⭐️ 8.0/10

Bun's team used an AI model called Mythos to rewrite its JavaScript runtime from Zig to Rust in just 6 days, achieving a 99.8% pass rate on the Linux x64 glibc test suite. This experiment demonstrates the unprecedented speed of AI-assisted large-scale code porting, which could reshape software maintenance and language migration. For Bun, moving to Rust may improve stability and reduce memory bugs that have plagued its Zig implementation. The port is still experimental and the Bun team has not committed to adopting it; all generated code may be discarded. The rewrite targeted Linux x64 with glibc and used proprietary AI resources (Mythos model) with unlimited tokens.

hackernews · heldrida · May 9, 10:12 · [Discussion](https://news.ycombinator.com/item?id=48073680)

**Background**: Bun is a modern JavaScript runtime known for speed, originally written in Zig, a systems programming language focused on safety and performance. Zig's low-level nature has led to crashes and memory bugs. Rust is another systems language with strong memory safety guarantees, making it an attractive alternative. AI-assisted code porting is an emerging technique where large language models translate entire codebases between languages.

<details><summary>References</summary>
<ul>
<li><a href="https://bun.sh/">Bun — A fast all-in-one JavaScript runtime</a></li>
<li><a href="https://en.wikipedia.org/wiki/Zig_(programming_language)">Zig (programming language)</a></li>

</ul>
</details>

**Discussion**: Community reactions are mixed: Some developers are impressed by the speed and see AI porting as a game-changer, while others express skepticism about relying on proprietary AI and the experimental nature of the code. A Bun team member clarified that the rewrite is not yet committed and likely to be discarded, calling the thread an overreaction.

**Tags**: `#Bun`, `#Rust`, `#Zig`, `#AI-assisted porting`, `#JavaScript runtime`

---

<a id="item-2"></a>
## [Internet Archive Switzerland Launches as Independent Digital Library](https://blog.archive.org/2026/05/06/internet-archive-switzerland-expanding-a-global-mission-to-preserve-knowledge/) ⭐️ 8.0/10

Internet Archive Switzerland has been announced as an independent, mission-aligned organization to build a distributed digital library, separate from the US-based Internet Archive. This move enhances legal resilience for digital preservation by creating a decentralized network that can better withstand DMCA takedown threats and jurisdictional attacks. The Swiss organization joins Internet Archive Canada and Internet Archive Europe as independent entities, but community members noted initial website content includes placeholder text, suggesting it may still be in early stages.

hackernews · hggh · May 9, 12:00 · [Discussion](https://news.ycombinator.com/item?id=48074265)

**Background**: The Internet Archive, a US-based nonprofit, has faced legal challenges including DMCA takedown lawsuits. By establishing independent, peer organizations in other countries with different copyright laws, the Archive aims to create a distributed preservation network that can share content without being vulnerable to a single jurisdiction's legal actions.

<details><summary>References</summary>
<ul>
<li><a href="https://www.dpworkshop.org/dpm-eng/challenges/accountability.html">Legal Issues | Digital Preservation Management</a></li>
<li><a href="https://www.dpconline.org/handbook/institutional-strategies/legal-compliance">Legal Compliance - Digital Preservation Handbook</a></li>

</ul>
</details>

**Discussion**: Commenters suggested that distributed, mission-aligned organizations should peer with each other but have no technical channel for DMCA complaints, similar to Usenet piracy networks. Others noted that Internet Archive Canada operated as a subsidiary with shared resources, raising questions about true independence for the Swiss branch.

**Tags**: `#Internet Archive`, `#digital preservation`, `#distributed systems`, `#Switzerland`, `#legal resilience`

---

<a id="item-3"></a>
## [Gowers Tests ChatGPT 5.5 Pro on Math Problems](https://gowers.wordpress.com/2026/05/08/a-recent-experience-with-chatgpt-5-5-pro/) ⭐️ 8.0/10

Timothy Gowers, a prominent mathematician, shared his experience using ChatGPT 5.5 Pro to solve mathematical problems, noting its significantly improved reasoning abilities compared to earlier models. He found it capable of solving 'gentle problems' suitable for beginning PhD students, but required careful guidance. This experience suggests that advanced LLMs like GPT-5.5 Pro are beginning to approach the level of human expertise in specialized domains like mathematics, potentially changing how research mentoring and problem-solving are done. It also highlights the growing divide between free and paid AI tiers, as the Pro version is costly and not available to free users. Gowers used the model iteratively, providing step-by-step guidance similar to mentoring a student. The model could rewrite arguments as LaTeX files and trace its own reasoning, but still made frequent errors that required correction. GPT-5.5 Pro was released on April 23, 2026, and is behind a paywall.

hackernews · _alternator_ · May 9, 02:41 · [Discussion](https://news.ycombinator.com/item?id=48071262)

**Background**: Large language models (LLMs) like OpenAI's GPT series are AI systems trained on vast text data to generate human-like text. Earlier models struggled with complex reasoning, especially in mathematics, often producing plausible-sounding but incorrect results. GPT-5.5 Pro is a premium version designed to handle advanced reasoning tasks. Mathematicians have been exploring whether these tools can assist in research or even solve open problems.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/GPT-5.5">GPT - 5 . 5 - Wikipedia</a></li>
<li><a href="https://aimlapi.com/models/gpt-5-5-pro">GPT - 5 . 5 Pro API — One API 400+ AI Models | AIMLAPI.com</a></li>

</ul>
</details>

**Discussion**: Comments on the article reflected a mix of excitement and skepticism. Some users agreed that GPT-5.5 Pro is the first LLM that can be guided to solve tedious problems correctly, though at high cost. Others argued that the achievement is more a testament to the mathematician's guidance than the model's independent capability, sparking debate about the nature of AI-assisted research.

**Tags**: `#AI`, `#LLM`, `#mathematics`, `#ChatGPT`, `#machine learning`

---

<a id="item-4"></a>
## [Distributing Mac software frustrates developers](https://blog.kronis.dev/blog/apple-is-increasing-my-cortisol-levels) ⭐️ 8.0/10

Developer KronisLV published a blog post venting about the difficulties of distributing Mac software due to Apple's notarization and Gatekeeper requirements, sparking a rich discussion on Hacker News with 365 points and 246 comments. This highlights a significant developer pain point that could discourage indie developers from targeting macOS, potentially reducing software diversity on the platform and pushing developers toward web or alternative ecosystems. Notarization requires a $99/year Apple Developer Program membership and a complex code signing workflow; Apple's documentation is described as poor, leading developers to reverse-engineer the process. The post author also notes that certificate costs from other providers (like Certum for Windows) are similarly high.

hackernews · LorenDB · May 9, 14:40 · [Discussion](https://news.ycombinator.com/item?id=48075366)

**Background**: Gatekeeper is a macOS security feature that enforces code signing and verifies downloaded applications before allowing them to run. Notarization is a process introduced by Apple where developers submit their software for automated security scanning, and if it passes, they receive a ticket to attach to the app. Since macOS Catalina, notarization is required for software distributed outside the Mac App Store to run without additional warnings.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Gatekeeper_(macOS)">Gatekeeper (macOS) - Wikipedia</a></li>
<li><a href="https://support.apple.com/guide/security/gatekeeper-and-runtime-protection-sec5599b66df/web">Gatekeeper and runtime protection in macOS - Apple Support</a></li>
<li><a href="https://www.sentinelone.com/blog/maco-notarization-security-hardening-or-security-theater/">What is macOS Notarization? - An Easy Guide 101</a></li>

</ul>
</details>

**Discussion**: Commenters expressed mixed sentiments: some argued users can disable Gatekeeper if they dislike the friction, while others criticized Apple's backward compatibility and poor documentation. A commenter named ofek shared a detailed guide on how to distribute binaries, filling the gap left by Apple. Another noted that desktop and mobile software distribution is effectively a cartel, and web software avoids these gatekeepers.

**Tags**: `#macOS`, `#developer experience`, `#app distribution`, `#Gatekeeper`, `#notarization`

---

<a id="item-5"></a>
## [HTML vs Markdown: A Better Output Format for Claude](https://simonwillison.net/2026/May/8/unreasonable-effectiveness-of-html/#atom-everything) ⭐️ 8.0/10

Thariq Shihipar from Anthropic's Claude Code team advocates using HTML instead of Markdown as the output format for Claude, providing concrete examples and prompt templates to generate richer, more structured explanations. This shift in best practice can significantly improve the quality of LLM-generated content, enabling SVG diagrams, interactive widgets, and better navigation, which makes technical explanations clearer and more engaging. While Markdown is more token-efficient, modern LLMs like Claude have larger context windows, making the trade-off worthwhile for the additional capabilities HTML offers, such as in-page navigation and dynamic visuals.

rss · Simon Willison · May 8, 21:00

**Background**: Markdown has been the default output format for many LLM users due to its simplicity and token efficiency, especially when context windows were limited. HTML, however, allows for more expressive and interactive content, such as embedded SVG diagrams and JavaScript widgets. Claude supports 'artifacts,' which are self-contained HTML documents that can include rich formatting and interactivity. This article encourages users to leverage HTML for ad-hoc explanations to make them more pleasant to navigate.

<details><summary>References</summary>
<ul>
<li><a href="https://albato.com/blog/publications/how-to-use-claude-artifacts-guide">Claude Artifacts: What They Are and How to Use Them (2026)</a></li>
<li><a href="https://support.claude.com/en/articles/9487310-what-are-artifacts-and-how-do-i-use-them">What are artifacts and how do I use them? | Claude Help Center</a></li>

</ul>
</details>

**Tags**: `#prompt engineering`, `#LLM`, `#HTML`, `#Claude`, `#best practices`

---

<a id="item-6"></a>
## [NASA Rotor Breakthrough Enables Heavier Mars Helicopters](https://arstechnica.com/space/2026/05/engineers-at-nasas-jet-propulsion-lab-make-a-breakthrough-in-rotor-technology/) ⭐️ 8.0/10

NASA JPL engineers achieved a breakthrough in rotor technology by spinning next-generation helicopter blades to Mach 1.08 in a Mars-simulating chamber, demonstrating the ability to generate more lift in Mars' thin atmosphere. This breakthrough paves the way for heavier Mars aerial vehicles capable of carrying more scientific instruments and flying longer distances, significantly expanding the scope of Mars exploration beyond the Ingenuity helicopter. During 137 test runs in JPL's 25-Foot Space Simulator, the rotor blades exceeded Mach 1 (reaching Mach 1.08) while withstanding simulated Martian atmospheric conditions without structural failure.

telegram · zaihuapd · May 9, 14:21

**Background**: Mars' atmosphere is only about 1% as dense as Earth's, making powered flight extremely challenging. Rotorcraft must spin blades at very high speeds to generate sufficient lift, but supersonic blade tips create shockwaves and vibrations. This test proves that blades can safely operate beyond Mach 1, enabling larger and more capable Mars aircraft.

<details><summary>References</summary>
<ul>
<li><a href="https://www.jpl.nasa.gov/news/nasa-pushes-next-gen-mars-helicopter-rotor-blades-past-mach-1/">NASA Pushes Next-Gen Mars Helicopter Rotor Blades Past Mach 1 Next-gen Mars helicopter rotor blades exceed Mach 1 - Phys.org Engineers at NASA's Jet Propulsion Lab make a breakthrough in ... NASA tests supersonic Mars helicopter blades - AeroTime Testing the Next Generation of Mars Helicopter Rotor Blades ... NASA Pushes Mars Helicopter Blades Beyond Mach 1 in Tests NASA rotor tests prove Mars aircraft can break Mach 1 safely</a></li>
<li><a href="https://arstechnica.com/space/2026/05/engineers-at-nasas-jet-propulsion-lab-make-a-breakthrough-in-rotor-technology/">Engineers at NASA's Jet Propulsion Lab make a breakthrough in ...</a></li>
<li><a href="https://phys.org/news/2026-05-gen-mars-helicopter-rotor-blades.html">Next-gen Mars helicopter rotor blades exceed Mach 1 - Phys.org</a></li>

</ul>
</details>

**Tags**: `#NASA`, `#Mars`, `#rotor technology`, `#drone`, `#space exploration`

---

<a id="item-7"></a>
## [Chinese Grey Market Sells Claude API Access at 90% Off, Report Reveals](https://www.tomshardware.com/tech-industry/artificial-intelligence/chinese-grey-market-sells-claude-api-access-at-90-percent-off-through-proxy-networks-that-harvest-user-data) ⭐️ 8.0/10

A recent report uncovers a Chinese grey market that sells access to Anthropic's Claude API at up to 90% below official prices, using proxy networks. The services often swap Claude Opus models with cheaper alternatives and harvest user prompts and outputs for data theft and model distillation. This practice undermines Anthropic's pricing and security, exposing users to fraud and data breaches. It highlights significant risks in the AI API ecosystem that affect developers and enterprises relying on third-party API access for their applications. The report details three methods: cost reduction via stolen credit cards, batch accounts, or human verification fraud; model swapping where cheap models substitute for Claude Opus; and data theft where prompts and outputs are collected and resold for model distillation. Users risk exposing code and trade secrets.

telegram · zaihuapd · May 10, 01:48

**Background**: Claude is a series of large language models developed by Anthropic, with Claude Opus being one of the most advanced. Model distillation is a machine learning technique where knowledge from a large model is transferred to a smaller one, enabling efficient deployment. Grey market proxy services bypass official API restrictions but often engage in fraud and data misuse, posing ethical and security challenges.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Model_distillation">Model distillation</a></li>
<li><a href="https://www.anthropic.com/claude/opus">Claude Opus 4.7 \ Anthropic</a></li>

</ul>
</details>

**Tags**: `#API security`, `#grey market`, `#Claude`, `#data theft`, `#AI models`

---

<a id="item-8"></a>
## [xAI Leaks Grok Build Coding Tool, Aims to Rival Claude Code](https://tech.ifeng.com/c/8t0yrbeeuwt) ⭐️ 8.0/10

xAI's Grok Build desktop coding tool has been leaked, revealing a cross-platform agent workflow app that autonomously executes multi-step development tasks, powered by Grok 4.3 Early Access. This leak signals xAI's major push into the AI coding tool market, directly competing with Anthropic's Claude Code. Training models up to 10 trillion parameters suggests a significant scale-up in capability. Grok Build supports local file and Git permissions, integrates MCP (Model Context Protocol), official skills, and plugins. xAI is reportedly training models with 1T, 1.5T, 6T, and 10T parameters, plus an image/video model Imagine V2.

telegram · zaihuapd · May 10, 13:34

**Background**: Grok Build is a local-first AI coding agent that executes code on the user's machine. Claude Code is Anthropic's agentic coding tool for developers, integrated into the terminal and IDE. The Model Context Protocol (MCP) is an open standard by Anthropic for connecting AI to external systems.

<details><summary>References</summary>
<ul>
<li><a href="https://grokipedia.com/page/Grok_Build">Grok Build — Grokipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/Claude_Code">Claude Code</a></li>
<li><a href="https://www.buildbygrok.com/">Build by Grok | Local-First AI Coding Agent</a></li>

</ul>
</details>

**Tags**: `#xAI`, `#Grok`, `#coding tool`, `#AI model`, `#Claude Code`

---