# free-google-ai-tools

> 10 free Google AI tools nobody talks about — the stack worth $200+/mo that google quietly ships for free.
>
> no hype. honest writeups including what's free, what isn't, and the catch.

curated by [@exploraX_](https://x.com/exploraX_).

---

## the rules

- must be a Google AI product or open-source release
- must have a meaningful free tier (not just a trial)
- must be actively maintained as of 2026
- if there's a catch (regional waitlist, paid features mixed in, daily limits), it gets named in the writeup

**important:** "free" doesn't mean "unlimited." every tool below has caps. the writeups state them honestly so you know what you're getting.

---

## the list

| # | tool | what it replaces | catch? |
|---|------|------------------|--------|
| 1 | [NotebookLM](#1-notebooklm) | notion AI + perplexity + readwise | daily caps |
| 2 | [Google AI Studio](#2-google-ai-studio) | openai playground + paid API credits | none |
| 3 | [Gemini CLI](#3-gemini-cli) | claude code ($20/mo by default) | none |
| 4 | [Jules](#4-jules) | devin + cursor agent | 15 tasks/day |
| 5 | [Stitch](#5-stitch) | galileo AI + early-stage figma | regional beta |
| 6 | [Gemma 4](#6-gemma-4) | paying for hosted LLM inference | runs locally — needs hardware |
| 7 | [Illuminate](#7-illuminate) | snipd + manual research reading | waitlist in some regions |
| 8 | [Learn About (LearnLM)](#8-learn-about-learnlm) | paid tutoring | none |
| 9 | [Google Labs FX](#9-google-labs-fx) | midjourney + suno (partially) | video gen is paid |
| 10 | [Google Colab](#10-google-colab) | paid cloud GPU rentals | T4 only, session timeouts |

---

## 1. NotebookLM

**replaces:** notion AI + perplexity + readwise
**url:** [notebooklm.google.com](https://notebooklm.google.com)

upload sources (PDFs, websites, audio, YouTube). it summarizes, builds mind maps, generates quizzes, drafts slide decks, even turns your notes into a podcast you can listen to on a walk. genuinely changes how you research dense material.

**free tier:** 100 notebooks total. 50 sources per notebook. 50 chat queries/day. 3 audio overviews/day. 3 video overviews/day. 10 reports/day.

**the catch:** the 50-source-per-notebook cap is real. for big research projects you'll split material across notebooks. Plus tier ($7.99/mo via Google AI Plus) raises it to 300 sources if you outgrow free.

---

## 2. Google AI Studio

**replaces:** openai playground + paid API credits
**url:** [aistudio.google.com](https://aistudio.google.com)

web playground for gemini 3 pro and flash. comes with a free API key. generous rate limits. paste a 1M-token context window and watch it actually use it.

**free tier:** generous daily quotas across all gemini models including pro. free API key for personal use.

**the catch:** the free API key has rate limits — fine for prototyping and personal projects, not for production. terms of service forbid using free-tier output to train competing models.

---

## 3. Gemini CLI

**replaces:** claude code ($20/mo by default)
**repo:** [github.com/google-gemini/gemini-cli](https://github.com/google-gemini/gemini-cli)
**license:** Apache 2.0

google's official open-source terminal agent. one command (`npx @google/gemini-cli`) and you've got an agent in your terminal that reads your codebase, runs shell commands, edits files, and ships PRs.

**free tier:** entire CLI is free. uses your free AI Studio API key.

**the catch:** subject to the same free API rate limits as AI Studio. for heavy daily use you may hit caps. easy fix: also wire it to a paid OpenRouter or Anthropic key as a fallback.

---

## 4. Jules

**replaces:** devin ($20/mo) + cursor agent ($20/mo)
**url:** [jules.google](https://jules.google)

assign jules a github issue. it spins up a secure cloud VM, clones your repo, writes a plan, makes the changes, opens a PR. you review the diff and merge.

**free tier:** 15 tasks/day, 3 concurrent tasks, runs on gemini flash.

**the catch:** flash isn't as strong as the pro model for complex changes. and 15 tasks/day fills up fast if you're using it seriously. pro tier ($19.99/mo) gives you 5x the limits and gemini 3.1 pro.

---

## 5. Stitch

**replaces:** galileo AI + early-stage figma work
**url:** [stitch.withgoogle.com](https://stitch.withgoogle.com)

google's free figma killer. describe an interface, get production-ready HTML/CSS/Tailwind + figma export. march 2026 update added voice canvas, infinite canvas, and MCP integration with cursor.

**free tier:** 350 standard + 200 experimental generations per month.

**the catch:** still in Google Labs beta. unavailable in some countries. output quality is solid but generic — it generates from its own models, not your team's design system.

---

## 6. Gemma 4

**replaces:** paying for hosted LLM inference (groq, openrouter, anthropic API)
**repo:** [ai.google.dev/gemma](https://ai.google.dev/gemma)
**license:** Apache 2.0

google's flagship open model. 2B, 4B, 26B-MoE (3.8B active), and 31B variants. 256K context. instruction-tuned and base versions. 150M+ downloads.

**free tier:** entire model weights are free. apache 2.0 — use commercially. runs on ollama with one command.

**the catch:** you're running it on your hardware. the 4B fits on a laptop, the 26B-MoE needs ~16GB VRAM quantized, the 31B needs a real GPU. tops out below frontier models — great for local work, not for replacing claude opus.

---

## 7. Illuminate

**replaces:** snipd + manual research reading
**url:** [illuminate.google.com](https://illuminate.google.com)

paste an arxiv preprint link. illuminate turns dense research papers into a 6-8 min conversation between two AI hosts breaking down the key points. perfect for commute reading you can't do at a desk.

**free tier:** entire tool is free.

**the catch:** still on a waitlist for some regions. arxiv-only — won't work on regular PDFs or non-arxiv academic sources. classified as experimental, could be shut down or rolled into NotebookLM.

---

## 8. Learn About (LearnLM)

**replaces:** paid tutoring + udemy on niche topics
**url:** [learning.google/experiments/learn-about](https://learning.google/experiments/learn-about/)

adaptive AI tutor. drop in any topic you're stuck on. highlight a word, click "go deeper," and the interface adapts in real time to your comprehension level. visual explanations, follow-up questions, quizzes, the works.

**free tier:** entire tool is free.

**the catch:** classified as Google Labs experiment — same uncertainty as Illuminate. LearnLM itself is now baked into Gemini, so the standalone "Learn About" experience may eventually fold into Gemini directly.

---

## 9. Google Labs FX

**replaces:** midjourney ($10/mo) + suno ($10/mo) — partially
**url:** [labs.google/fx](https://labs.google/fx)

google labs creative suite. ImageFX for text-to-image (imagen 4). MusicFX for text-to-music (musicLM). Flow for text-to-video (veo 3.1). 18+ only.

**free tier:** limited daily generations for image and music.

**the catch:** this is the messiest one. VideoFX has been absorbed into Flow, and Whisk + ImageFX are migrating into Flow by April 30, 2026. the heavy veo 3.1 video generation features are paid (Google AI Pro $19.99/mo). image and music stay free for casual use. don't expect a free runway replacement.

---

## 10. Google Colab

**replaces:** paid cloud GPU rentals (runpod, vast.ai)
**url:** [colab.research.google.com](https://colab.research.google.com)

free T4 GPU + 12GB RAM in a browser tab. enough to fine-tune small models, run stable diffusion, prototype agents. the launching pad for half the ML projects on github.

**free tier:** free T4 GPU access with session-based usage limits.

**the catch:** sessions disconnect after a few hours of inactivity. T4 is a 2018 GPU — fine for prototyping, slow for serious training. for bigger workloads you need Colab Pro ($9.99/mo) or Pro+ ($49.99/mo) which give A100/V100 access.

---

## disclaimers

**on "free."** every tool above has limits. "free" means "you can get real value without paying," not "unlimited." the writeups state the actual caps.

**on availability.** some Labs tools (Illuminate, Stitch, Learn About) have regional waitlists or country restrictions. if a link doesn't work for you, that's why.

**on stability.** Google Labs experiments can get shuttered, migrated, or paywalled with little notice. this list is accurate as of mid-2026 — check each tool's current status before building a workflow around it.

**on the replacements.** these don't always match the polish of their paid counterparts. NotebookLM's free tier won't replace a paid Notion AI workspace for a team. Jules' free tier won't replace Devin for a production codebase. these are starting points, not endpoints.

---

## related

see also [`open-source-vs-saas`](https://github.com/Moh4696/open-source-vs-saas) — 10 open-source github repos that replace major paid SaaS tools.

---

## contributing

found a free Google AI tool that belongs here? open a PR with:
- official google URL
- what's actually free vs paid
- the honest catch

no submissions accepted without an honest "catch" section. that's the whole point.

---

## license

this list and writeups are CC0 — public domain. fork, remix, repost, no attribution needed.

the individual tools listed are owned by Google. see each tool's terms of service for usage details.
