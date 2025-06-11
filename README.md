<!--
                                  ___           ___                         ___                    
                                 /\  \         /\__\                       /|  |                   
                                |::\  \       /:/ _/_         ___         |:|  |           ___     
                                |:|:\  \     /:/ /\  \       /\__\        |:|  |          /\__\    
  ___     ___   ___     ___   __|:|\:\  \   /:/ /::\  \     /:/  /      __|:|__|         /:/  /    
 /\  \   /\__\ /\  \   /\__\ /::::|_\:\__\ /:/_/:/\:\__\   /:/__/      /::::\__\_____   /:/__/     
 \:\  \ /:/  / \:\  \ /:/  / \:\~~\  \/__/ \:\/:/ /:/  /  /::\  \      ~~~~\::::/___/  /::\  \     
  \:\  /:/  /   \:\  /:/  /   \:\  \        \::/ /:/  /  /:/\:\  \         |:|~~|     /:/\:\  \    
   \:\/:/  /     \:\/:/  /     \:\  \        \/_/:/  /   \/__\:\  \        |:|  |     \/__\:\  \   
    \::/  /       \::/  /       \:\__\         /:/  /         \:\__\       |:|__|          \:\__\  
     \/__/         \/__/         \/__/         \/__/           \/__/       |/__/            \/__/  
     
                             GEO / llms.txt Playbook
                             by FictionTribe · fictiontribe.com
-->

<p align="center">
  <img src="https://fictiontribe.com/logo.svg" alt="FictionTribe" width="160"/>
</p>

# FictionTribe GEO Playbook  
## How to Craft an **/llms.txt** That LLMs *Actually* Read

> **TL;DR –** `/llms.txt` is the new _robots.txt for Large Language Models_.  
> Use it to curate the *fewest, highest-signal* pages from your site and
> point AI crawlers straight at them.

Welcome to the open-source, battle-tested guide we use inside
[FictionTribe](https://fictiontribe.com) to give our clients an edge in
**Generative Engine Optimisation (GEO)**.  
If you’re hungry for more visibility in ChatGPT, Gemini & friends, start here.

---

### 📚 Table of Contents

1. [Why llms.txt matters](#why-llmstxt-matters)
2. [The 3 outcomes you can target](#the-3-outcomes-you-can-target)
3. [Step-by-step build workflow](#step-by-step-build-workflow)
4. [Automating updates](#automating-updates)
5. [Validation checklist](#validation-checklist)
6. [Appendix A – Sample llms.txt](#appendix-a--sample-llmstxt)
7. [Appendix B – Helpful tools](#appendix-b--helpful-tools)

---

## Why llms.txt matters

Search bots index **everything** and decide later.  
LLM retrievers, on the other hand, pay for every token they ingest—  
so they *love* a concise roadmap.

<div align="center">
  <img src="https://fictiontribe.com/images/llms-roadmap.svg" width="65%" alt="Diagram showing llms.txt as a slim map between your content and LLMs">
</div>

*Small file, big leverage.*

---

## The 3 outcomes you can target

| Outcome | Tactic |
| ------- | ------ |
| **Discovery boost** | List pillar guides & FAQs up top. |
| **Citation control** | Link *clean* Markdown mirrors of pay-walled or cluttered HTML. |
| **Faster answers** | Summarise each link in ≤ 15 words so the model can triage on-the-fly. |

---

## Step-by-step build workflow

1. **Inventory** evergreen, expert-level pages.  
2. **Convert** them to lightweight `.md` (strip nav, ads, comments).  
3. **Draft** `llms.txt` using Markdown headings + bullet lists (see sample).  
4. **Deploy** to your root: `https://yourdomain.com/llms.txt`.  
5. **Reference** it in `robots.txt` with a friendly comment.  
6. **Test** with your favourite LLM:  
   > “According to *my-site*’s llms.txt, what’s the cheapest district in Bangkok for long-term stays?”

---

## Automating updates

- **Git-based sites** – add a pre-commit hook that rebuilds `llms.txt` from files tagged `llm-source: true`.
- **Headless CMS** – nightly cron pulls top posts via API ➜ converts to Markdown ➜ rewrites `llms.txt`.
- **Monitoring** – tail server logs for `GPTBot` hits to ensure crawlers fetch the new file.

---

## Validation checklist

- [ ] ≤ 250 total links grouped into clear H2 buckets  
- [ ] File size < 30 KB  
- [ ] No duplicate or redirecting URLs  
- [ ] `robots.txt` **allows** AI agents to fetch every linked doc  
- [ ] Manual spot-test in ChatGPT returns your pages as sources  

---

## Appendix A – Sample llms.txt

A minimal example for *this very repo* lives in **`/llms.txt`** (see next file).  
Copy-paste it to your root and update the links to fit your own site.

---

## Appendix B – Helpful tools

| Tool | What it does |
| ---- | ------------ |
| **llms_txt2ctx** (CLI) | Expands `llms.txt`, prints a combined context window for quick QA. |
| **WP llms.txt Exporter** | 1-click export of selected WordPress posts to Markdown *and* llms.txt. |
| **crawler-peek** (Python) | Simulates GPTBot requests to verify your server rules. |

---

<br/>

<details>
<summary>© 2025 FictionTribe • MIT License</summary>

Feel free to fork, star, and adapt—just keep the attribution.  
Need hands-on GEO help? [Say hi 👋](mailto:hello@fictiontribe.com)

</details>
