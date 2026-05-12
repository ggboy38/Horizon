---
layout: default
title: "Horizon Summary: 2026-05-12 (EN)"
date: 2026-05-12
lang: en
---

> From 38 items, 12 important content pieces were selected

---

1. [TanStack npm Supply-Chain Compromise Postmortem](#item-1) ⭐️ 9.0/10
2. [UCLA discovers first stroke rehab drug that repairs brain connections](#item-2) ⭐️ 9.0/10
3. [Deep Dive into Atmospheric Rendering Techniques](#item-3) ⭐️ 8.0/10
4. [Python vs Statically Typed Languages for AI Code](#item-4) ⭐️ 8.0/10
5. [EU Cracks Down on Addictive Social Media Designs for Kids](#item-5) ⭐️ 8.0/10
6. [Extremely Low Frequencies: A Deep Dive into VLF Radio](#item-6) ⭐️ 8.0/10
7. [James Shore: AI must reduce maintenance costs proportionally](#item-7) ⭐️ 8.0/10
8. ['Zombie Internet' Coined in Essay on AI's Mental Toll](#item-8) ⭐️ 8.0/10
9. [Shopify's River Agent Fosters Public Learning](#item-9) ⭐️ 8.0/10
10. [OpenAI to Release GPT-5.5-Cyber Cybersecurity Model](#item-10) ⭐️ 8.0/10
11. [China SAMR Conditionally Approves Tencent's Ximalaya Acquisition](#item-11) ⭐️ 8.0/10
12. [SpaceX in talks with Google on orbital data center launch](#item-12) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [TanStack npm Supply-Chain Compromise Postmortem](https://tanstack.com/blog/npm-supply-chain-compromise-postmortem) ⭐️ 9.0/10

TanStack published a postmortem detailing a supply-chain compromise of its npm packages, where an attacker pushed a malicious commit from a fork to the main branch via GitHub's shared object storage, deploying a worm that stole tokens and installed a dead man's switch. This incident highlights critical weaknesses in npm postinstall scripts and CI/CD security, affecting widely-used open-source packages and demonstrating that trusted publishing alone is insufficient to protect against CI compromise. The malicious payload included a systemd user service (Linux) and a LaunchAgent (macOS) that monitored token revocation and could execute a destructive 'rm -rf ~' command. The attack leveraged GitHub's shared object storage, making the malicious commit URI indistinguishable from the legitimate repository.

hackernews · varunsharma07 · May 11, 21:08 · [Discussion](https://news.ycombinator.com/item?id=48100706)

**Background**: npm is the largest JavaScript package registry, and supply-chain attacks occur when trusted packages are compromised. CI/CD pipelines often use tokens for authentication, and npm's postinstall scripts can execute arbitrary code. This attack is part of a broader wave of npm supply-chain attacks in 2025, including the Sha1-Hulud campaign.

<details><summary>References</summary>
<ul>
<li><a href="https://grokipedia.com/page/Sha1-Hulud_npm_supply_chain_attack">Sha1-Hulud npm supply chain attack</a></li>
<li><a href="https://emilyxiong.medium.com/brief-history-of-npm-supply-chain-attacks-in-year-2025-a887dd2e11a4">Brief History of NPM Supply Chain Attacks in Year 2025 | Medium</a></li>

</ul>
</details>

**Discussion**: Community comments emphasized the danger of postinstall scripts, with some recommending pnpm to mitigate risks. Others pointed out that trusted publishing does not protect against CI compromise, and GitHub's shared object storage is a significant security concern. A dead man's switch in the payload could cause catastrophic data loss if the token is revoked.

**Tags**: `#supply-chain security`, `#npm`, `#open-source security`, `#CI/CD`, `#malware`

---

<a id="item-2"></a>
## [UCLA discovers first stroke rehab drug that repairs brain connections](https://stemcell.ucla.edu/news/ucla-discovers-first-stroke-rehabilitation-drug-repair-brain-damage) ⭐️ 9.0/10

UCLA Health researchers identified DDL-920, the first drug to fully reproduce the effects of physical stroke rehabilitation in mice, promoting brain rewiring and restoring lost connections. This breakthrough could revolutionize stroke rehabilitation by providing a pharmacological alternative to physical therapy, potentially benefiting millions of stroke survivors worldwide who have limited recovery options. The study identified a brain substrate and circuitry underlying rehab effects, and DDL-920 targets this pathway to mimic the main effect of physical rehab. Further studies are needed before human trials can begin.

hackernews · bookofjoe · May 11, 17:53 · [Discussion](https://news.ycombinator.com/item?id=48098261)

**Background**: Stroke often causes brain cell death and damage to connections, but some cells can recover over time. Physical rehabilitation promotes neuroplasticity, where healthy brain areas take over lost functions, but no drug previously existed that could replicate this process.

<details><summary>References</summary>
<ul>
<li><a href="https://stemcell.ucla.edu/news/ucla-discovers-first-stroke-rehabilitation-drug-repair-brain-damage">UCLA discovers first stroke rehabilitation drug to repair brain damage</a></li>
<li><a href="https://newsroom.ucla.edu/releases/ucla-discovers-first-stroke-rehabilitation-drug-to-reestablish-brain-connections-in-mice">UCLA discovers first stroke rehabilitation drug to reestablish brain connections in mice | UCLA</a></li>
<li><a href="https://www.uclahealth.org/news/release/ucla-discovers-first-stroke-rehabilitation-drug-repair-brain">UCLA discovers first stroke rehabilitation drug to repair brain damage in mice | UCLA Health</a></li>

</ul>
</details>

**Discussion**: Comments noted that while the drug targets surviving brain networks, it cannot reverse cell death at the infarct core. Some users drew parallels to psychedelics' ability to reopen critical periods, and shared the PubMed link to the compound. Others questioned whether it might work for Alzheimer's disease.

**Tags**: `#stroke rehabilitation`, `#neuroscience`, `#drug discovery`, `#brain repair`, `#UCLA`

---

<a id="item-3"></a>
## [Deep Dive into Atmospheric Rendering Techniques](https://blog.maximeheckel.com/posts/on-rendering-the-sky-sunsets-and-planets/) ⭐️ 8.0/10

Maxime Heckel published a detailed blog post with an interactive web demo explaining how to render skies, sunsets, and planets using physically-based atmospheric scattering algorithms. This work makes high-quality atmospheric rendering accessible to web developers and game creators, enabling realistic skyboxes and planetary scenes directly in the browser without external tools. The implementation is released under the MIT license, allowing reuse in projects, and builds upon classic research such as Nishita et al.'s 1993 paper on atmospheric scattering.

hackernews · ibobev · May 12, 13:26 · [Discussion](https://news.ycombinator.com/item?id=48107997)

**Background**: Atmospheric scattering is the physical phenomenon where light is scattered by particles in the atmosphere, causing the blue sky, red sunsets, and other visual effects. Rendering it in computer graphics requires simulating multiple scattering events, which is computationally expensive. The article explains simplified models that run efficiently on modern web browsers using WebGL or similar technologies.

<details><summary>References</summary>
<ul>
<li><a href="http://nishitalab.org/user/nis/cdrom/dobampeg/HWW02.pdf">Interactive Rendering of Atmospheric Scattering</a></li>
<li><a href="https://medium.com/@liangairan1212/atmosphere-scattering-rendering-76ea5eb7253b">Atmosphere Scattering Rendering . Volume Rendering | Medium</a></li>

</ul>
</details>

**Discussion**: Community comments are overwhelmingly positive, with users praising the beauty and clarity of the post. Some highlight related work like Sebastian Lague's planetary atmosphere video and SpaceEngine, while others note the MIT license makes it a practical solution for game skyboxes.

**Tags**: `#graphics`, `#rendering`, `#atmospheric scattering`, `#web`, `#game development`

---

<a id="item-4"></a>
## [Python vs Statically Typed Languages for AI Code](https://medium.com/@NMitchem/if-ai-writes-your-code-why-use-python-bf8c4ba1a055) ⭐️ 8.0/10

A Medium article and its extensive comment thread debate whether Python remains the best choice for AI-generated code, with many experienced developers advocating for statically typed languages like Rust and Scala. This debate reflects a significant shift in developer workflows as AI-assisted coding becomes mainstream, potentially influencing language adoption and tooling choices for reliability and productivity. Proponents of static typing argue it provides natural guardrails and faster feedback loops for AI agents, while Python's readability remains an advantage for reviewing generated code.

hackernews · indigodaddy · May 11, 20:45 · [Discussion](https://news.ycombinator.com/item?id=48100433)

**Background**: AI code generation tools like GitHub Copilot and ChatGPT can produce code in various languages. Statically typed languages (e.g., Rust, Scala) catch errors at compile time via type checking, while dynamically typed languages (e.g., Python) perform checks at runtime. The choice of language affects how well AI models can generate correct code and how easily humans can review it.

**Discussion**: Commenters overwhelmingly favor statically typed languages for AI-generated code, with one noting the static vs dynamic debate is decisively over and static has won. Others highlight Python's readability as key for code review, but emphasize that for agentic flows, Rust and Scala's advanced type systems provide superior guardrails and feedback.

**Tags**: `#AI code generation`, `#static vs dynamic typing`, `#Python`, `#Rust`, `#developer tools`

---

<a id="item-5"></a>
## [EU Cracks Down on Addictive Social Media Designs for Kids](https://www.cnbc.com/2026/05/12/tiktok-instagram-social-media-addictive-eu-crack-down.html) ⭐️ 8.0/10

The European Union announced a crackdown on social media companies like TikTok and Instagram for using addictive design features that specifically target children. This regulatory action sets a precedent for algorithmic accountability and could force platforms to redesign their services to protect minors, potentially influencing global standards for online child safety. The crackdown is expected to be enforced under the EU's Digital Services Act (DSA), particularly Article 28, which mandates platforms to protect minors from addictive behaviors and harmful content.

hackernews · thm · May 12, 11:00 · [Discussion](https://news.ycombinator.com/item?id=48106534)

**Background**: Social media platforms use persuasive design techniques like infinite scrolling and personalized feeds to maximize engagement, creating addictive feedback loops. Children are especially vulnerable due to lower self-regulation. The EU's DSA aims to create a safer online environment by requiring platforms to assess and mitigate systemic risks, including those targeting minors.

<details><summary>References</summary>
<ul>
<li><a href="https://www.euronews.com/next/2026/05/12/is-social-media-addictive-by-design-and-can-you-beat-the-algorithm">Is social media addictive by design and can you beat the... | Euronews</a></li>
<li><a href="https://digital-strategy.ec.europa.eu/en/library/commission-publishes-guidelines-protection-minors">Commission publishes guidelines on the protection of minors | Shaping Europe’s digital future</a></li>
<li><a href="https://www.designorate.com/ux-dark-patterns-and-social-media-addiction/">UX Dark Patterns and Social Media Addiction</a></li>

</ul>
</details>

**Discussion**: Comments on the news highlight that addictive design affects adults too, with some arguing for algorithm liability regardless of age. Others note that the child-focused framing is pragmatic, while questioning why protections stop at age 18.

**Tags**: `#regulation`, `#social media`, `#addictive design`, `#EU`, `#ethics`

---

<a id="item-6"></a>
## [Extremely Low Frequencies: A Deep Dive into VLF Radio](https://computer.rip/2026-05-09-extremely-low-frequencies.html) ⭐️ 8.0/10

A new article provides an in-depth historical and technical overview of VLF radio communications, covering its early discovery, military applications, and antenna engineering. VLF is critical for submarine communication because its waves can penetrate seawater, and the article sheds light on a niche but vital technology that has been used for over a century. VLF operates in the 3-30 kHz range, requiring massive antennas like the Cutler array, and the article discusses historical stations such as Jim Creek and Grimeton.

hackernews · pinewurst · May 12, 03:59 · [Discussion](https://news.ycombinator.com/item?id=48104041)

**Background**: Very Low Frequency (VLF) radio waves range from 3 to 30 kHz, with wavelengths up to 100 km. They can propagate as ground waves and penetrate up to 40 meters into seawater, making them ideal for submarine communications. VLF systems require extremely large antennas due to the long wavelengths.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Very_low_frequency">Very low frequency - Wikipedia</a></li>

</ul>
</details>

**Discussion**: Commenters shared personal connections to VLF stations, such as a relative who worked on classified experiments at the Pentagon, and recommended visiting the operational Grimeton station. The discussion was appreciative and added real-world context to the article.

**Tags**: `#VLF`, `#radio`, `#history`, `#technology`, `#communication`

---

<a id="item-7"></a>
## [James Shore: AI must reduce maintenance costs proportionally](https://simonwillison.net/2026/May/11/james-shore/#atom-everything) ⭐️ 8.0/10

James Shore warns that if AI coding tools increase productivity by a factor of X, they must also reduce maintenance costs by the same factor, otherwise total costs will explode. This insight highlights a critical hidden risk of AI-assisted programming: while speed gains are celebrated, maintenance cost growth could offset them and lead to unsustainable project costs. Shore uses a simple multiplication argument: doubling code output while maintenance cost per unit stays the same doubles total maintenance costs, and quadruples them if output and per-unit costs both double.

rss · Simon Willison · May 11, 19:48

**Background**: AI coding agents like GitHub Copilot or Cursor's AI can generate code rapidly, but the resulting code often requires more maintenance due to quality issues or lack of context understanding. Maintenance is a major part of software lifecycle costs, and if AI only accelerates initial writing without improving long-term sustainability, teams may face increasing debt.

**Tags**: `#AI coding agents`, `#maintenance costs`, `#software engineering`, `#productivity`

---

<a id="item-8"></a>
## ['Zombie Internet' Coined in Essay on AI's Mental Toll](https://simonwillison.net/2026/May/11/zombie-internet/#atom-everything) ⭐️ 8.0/10

Journalist Jason Koebler published an article on 404 Media titled 'Your AI Use Is Breaking My Brain', introducing the term 'Zombie Internet' to describe the current online ecosystem where AI-generated content and human interactions are increasingly indistinguishable. This article gives a name to a widespread but previously ill-defined phenomenon, helping to articulate the mental exhaustion many feel when navigating online spaces flooded with AI content. It also highlights the erosion of authenticity and the blurring of human and machine communication. Koebler defines 'Zombie Internet' as more insidious than the 'Dead Internet' theory, encompassing not just bots talking to bots but also humans interacting with bots, people using AI to talk to others, and AI-generated spam for profit. The article specifically calls out examples like AI influencers, automated YouTube channels, and fake Reddit comments.

rss · Simon Willison · May 11, 19:21

**Background**: The 'Dead Internet' theory is a conspiracy theory that suggests most online content and interactions are bot-generated, especially since 2016, to control public opinion. The 'Zombie Internet' concept, as described by Koebler and others, goes further by highlighting the mixture of human and AI activity where AI-generated content is often indistinguishable from human writing. This leads to a confusing online environment where authenticity is compromised.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Dead_Internet_theory">Dead Internet theory</a></li>
<li><a href="https://www.fastcompany.com/91489308/zombie-internet-devastating-consequences-advertising-social-media-human-web-dead-internet-moltbook-ai-tbpn">The ‘ zombie internet ’ has arrived—and it has... - Fast Company</a></li>
<li><a href="https://medium.com/majordigest/the-rise-of-the-zombie-internet-and-its-impact-c31e2b5190ec">The Rise of the Zombie Internet and Its Impact | by Valentin... | Medium</a></li>

</ul>
</details>

**Tags**: `#AI`, `#internet culture`, `#content quality`, `#zombie internet`, `#authenticity`

---

<a id="item-9"></a>
## [Shopify's River Agent Fosters Public Learning](https://simonwillison.net/2026/May/11/learning-on-the-shop-floor/#atom-everything) ⭐️ 8.0/10

Shopify deployed River, an internal AI coding agent that operates exclusively in public Slack channels, refusing direct messages. This design forces all interactions to be visible to every employee, creating a transparent learning environment. This approach turns the entire company into a 'Lehrwerkstatt' (teaching workshop), enabling osmosis learning where employees pick up skills by observing others' work with AI. It mirrors Midjourney's early public Discord strategy, which helped users master complex prompting through shared experimentation. River does not respond to direct messages; users must create public channels. In the last 30 days, 5,938 employees used River, authoring one in eight merged pull requests. CEO Tobias Lütke himself works with River in a public channel where over 100 people observe and contribute.

rss · Simon Willison · May 11, 15:46

**Background**: The German term 'Lehrwerkstatt' literally means 'teaching workshop,' referring to an environment where learning happens by being close to the work itself. Shopify aims to become a Lehrwerkstatt at scale, and River's public-only design is a key enabler. Midjourney's early success is attributed to its public Discord interface, which forced users to share prompts and learn from each other.

<details><summary>References</summary>
<ul>
<li><a href="https://www.zenml.io/llmops-database/building-a-public-ai-agent-workspace-for-organizational-learning">Shopify: Building a Public AI Agent Workspace for Organizational Learning - ZenML LLMOps Database</a></li>
<li><a href="https://x.com/simonw/status/2053529689122328947">Simon Willison on X: "Shopify's River agent system lives in Slack and can only be used in public so that other employees can learn from what you do with it Reminds me of how Midjourney's Discord-only launch helped people figure out the weird & complex craft of image prompting by watching each other" / X</a></li>
<li><a href="https://di.gg/ai/m6d25q7g?rank=16">Shopify deploys River AI agent in Slack channels · KRO · Digg</a></li>

</ul>
</details>

**Tags**: `#AI`, `#coding agent`, `#organizational learning`, `#transparency`, `#software engineering`

---

<a id="item-10"></a>
## [OpenAI to Release GPT-5.5-Cyber Cybersecurity Model](https://t.me/zaihuapd/41332) ⭐️ 8.0/10

OpenAI plans to release GPT-5.5-Cyber, a specialized cybersecurity model based on GPT-5.5, within days. The model will initially be available only to vetted trusted defenders, not the general public. This marks a significant step in applying frontier AI to cybersecurity, potentially enhancing defense capabilities against cyber threats. The controlled access model reflects growing concern about dual-use risks, as similar specialized models could be used offensively. GPT-5.5-Cyber is built on GPT-5.5, which OpenAI recently called its smartest and most intuitive model yet. OpenAI is collaborating with governments and industry to determine trusted access mechanisms, following a similar strategy to its earlier life sciences model GPT-Rosalind.

telegram · zaihuapd · May 12, 01:30

**Background**: OpenAI has been developing domain-specific AI models for high-value sectors, such as GPT-Rosalind for drug discovery. The cybersecurity domain presents unique challenges, as powerful AI tools could be used both for defense and offense. By limiting initial access to vetted defenders, OpenAI aims to mitigate risks while still advancing defensive capabilities.

<details><summary>References</summary>
<ul>
<li><a href="https://openai.com/index/gpt-5-5-with-trusted-access-for-cyber/">Scaling Trusted Access for Cyber with GPT - 5 . 5 and... | OpenAI</a></li>
<li><a href="https://kingy.ai/news/the-openai-gpt-5-5/">OpenAI 's GPT - 5 . 5 - Cyber : The AI Model That's Not For You... - Kingy AI</a></li>

</ul>
</details>

**Tags**: `#AI`, `#Cybersecurity`, `#OpenAI`, `#Model Release`

---

<a id="item-11"></a>
## [China SAMR Conditionally Approves Tencent's Ximalaya Acquisition](https://www.samr.gov.cn/xw/zj/art/2026/art_c1b14339020e464fb46aa655a720ba48.html) ⭐️ 8.0/10

On May 11, 2026, China's State Administration for Market Regulation conditionally approved Tencent's acquisition of Ximalaya, imposing five behavioral remedies to prevent anti-competitive effects in the online audio market. This decision sets a precedent for merger control in China's online audio sector, directly curbing potential monopolistic practices by Tencent. The remedies protect consumers, content creators, and downstream auto manufacturers from price hikes, exclusive deals, and bundling. The five remedies include: no price increases or service degradation; maintaining free and popular content ratios; no exclusive copyright deals and removal of existing exclusives; no tying audio platforms with car manufacturers; and no restrictions on multi-platform content distribution by hosts.

telegram · zaihuapd · May 12, 09:55

**Background**: Under China's Anti-Monopoly Law, the antitrust authority may conditionally approve mergers that could restrict competition. Tencent dominates messaging and gaming; Ximalaya is China's largest online audio platform. The deal raised concerns about market concentration in digital audio, which also involves music and in-car entertainment services. Prior cases, such as the 2021 music copyright case, show China's firm stance against exclusive licenses.

<details><summary>References</summary>
<ul>
<li><a href="http://fldj.mofcom.gov.cn/article/j/201412/20141200835988.shtml">商务部反垄断局负责人关于《关于经营者集中附加限制性条件的规定（试行）》的解读</a></li>
<li><a href="https://m.mp.oeeee.com/a/BAAFRD000020210724523788.html">反垄断重锤落下，监管为何责令腾讯解除网络音乐独家版权？</a></li>

</ul>
</details>

**Tags**: `#antitrust`, `#merger control`, `#China`, `#regulation`, `#online audio`

---

<a id="item-12"></a>
## [SpaceX in talks with Google on orbital data center launch](https://www.wsj.com/tech/spacex-google-in-talks-to-explore-data-centers-in-orbit-7b7799e2) ⭐️ 8.0/10

Google is negotiating with SpaceX for rocket launch agreements to advance Project Suncatcher, its orbital data center initiative aimed at running AI workloads in space. This partnership could revolutionize cloud and AI infrastructure by overcoming terrestrial constraints on energy, cooling, and land, potentially making large-scale AI compute more sustainable and efficient. Project Suncatcher aims to deploy solar-powered satellites with custom AI chips by 2027, and SpaceX is simultaneously marketing orbital data centers as a core value proposition in its upcoming IPO.

telegram · zaihuapd · May 12, 16:28

**Background**: Orbital data centers are proposed as a solution to the growing energy demands of AI, leveraging abundant solar power in space and eliminating cooling constraints. Google's Project Suncatcher, announced in late 2025, builds on earlier space-based computing concepts from the military and companies like Amazon and Microsoft.

<details><summary>References</summary>
<ul>
<li><a href="https://blog.google/innovation-and-ai/technology/research/google-project-suncatcher/">Meet Project Suncatcher, a research moonshot to scale machine learning compute in space.</a></li>
<li><a href="https://www.forbes.com/sites/anishasircar/2025/11/11/google-unveils-project-suncatcher-to-run-ai-on-solar-satellites-in-orbit/">Google Plans To Run AI Data Centers In Space With Project Suncatcher</a></li>
<li><a href="https://arstechnica.com/google/2025/11/meet-project-suncatcher-googles-plan-to-put-ai-data-centers-in-space/">Meet Project Suncatcher, Google’s plan to put AI data centers in space - Ars Technica</a></li>

</ul>
</details>

**Tags**: `#SpaceX`, `#Google`, `#轨道数据中心`, `#云计算`, `#太空技术`

---