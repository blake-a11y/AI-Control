# AI Model Landscape — Task-Based Recommendations

## Document Metadata

- **Research date:** 2026-04-23
- **Next refresh due:** 2026-07-22
- **Analyst:** Perplexity Research
- **Sources cited:** 45
- **Provider scope:** OpenAI, Anthropic, Google (Gemini), xAI (Grok), Perplexity — all sub-models included
- **All sources dated within:** 2026-01-18 to 2026-04-23 *(90-day window from research date)*

***

## Executive Summary

The 90-day window from late January to late April 2026 delivered the most concentrated release cadence on record from the five covered providers. OpenAI retired GPT-4o and the original GPT-5 family, replaced them with GPT-5.4 (March 5, 2026), and then launched GPT-5.5 on April 23, 2026 — the day of this report — claiming the top spot on the Artificial Analysis Intelligence Index at a score of 60, the highest ever recorded. Anthropic released Claude Opus 4.7 on April 16, 2026 with a 87.6% SWE-bench Verified score, leading all publicly accessible coding benchmarks and holding an implied 92.5% Polymarket probability of topping the LMSYS Chatbot Arena at month-end. Google's Gemini 3.1 Pro (February 19, 2026) delivered the highest ARC-AGI-2 score among frontier models at 77.1% — more than double its predecessor — while holding the same $2/$12 per million token price, making it the strongest value proposition at the frontier. xAI's Grok 4.20 (API: March 10, 2026) emerged as the leader in real-time data grounding and long-context economics, offering a 2M token window at $2/$6 per million tokens. Perplexity's Sonar family achieved an industry-best SimpleQA factuality F-score of 0.858 and remains the only in-scope option with web search natively integrated into every query.[^1][^2][^3][^4][^5][^6][^7][^8][^9]

***

## Task-to-Model Recommendation Matrix

| # | Task Type | Primary Recommendation | Secondary / Fallback | Why | Source |
|---|-----------|------------------------|----------------------|-----|--------|
| 1 | Web research with live citations | **Perplexity Sonar Deep Research** | Perplexity Sonar Pro | Sonar Deep Research is the only in-scope model with mandatory web retrieval on every query, synthesizing hundreds of sources into cited long-form reports; Sonar Pro achieves industry-best factuality F-score of 0.858 on SimpleQA[^8][^10] | Perplexity Complete Guide 2026, 2026-01-20; Perplexity API docs, 2026-02-03 |
| 2 | Long-context document analysis (100k+ tokens) | **Grok 4.20** | Gemini 3.1 Pro | Grok 4.20's 2M token context is the largest among in-scope models at competitive pricing ($2/$6/M); Gemini 3.1 Pro's 1M context with 84.9% MRCR v2 8-needle retrieval is the strongest among remaining models[^9][^11] | AI/ML API Grok 4.20 review, 2026-04-22; Google DeepMind model card, 2026-02-18 |
| 3 | Code generation — general purpose | **Claude Opus 4.7** | GPT-5.5 | Claude Opus 4.7 leads SWE-bench Verified at 87.6% and holds a 1549 Elo on the LMSYS coding leaderboard (Claude 4.6 family holds top 3 spots); GPT-5.5 delivers "state-of-the-art intelligence on Artificial Analysis Coding Index at half the cost of competitors"[^4][^12][^13] | Vellum benchmark analysis, 2026-04-15; OpenAI GPT-5.5 announcement, 2026-04-23 |
| 4 | Code generation — agentic (multi-file, terminal access) | **Claude Opus 4.7** | GPT-5.3 Codex | Claude Opus 4.7 leads SWE-bench Pro (agentic coding) at 64.3%, versus GPT-5.4 at 57.7% and Gemini 3.1 Pro at 54.2%; leads MCP-Atlas tool invocation benchmark by 9.2 points over GPT-5.4[^4][^14] | Vellum benchmark analysis, 2026-04-15; apiyi.com Claude Opus 4.7 benchmark review, 2026-04-17 |
| 5 | Creative writing (fiction, marketing copy, brainstorming) | **Claude Opus 4.7** | GPT-5.5 | Claude Opus 4.7 release notes specifically highlight improved creativity for slides, documents, and interfaces; Anthropic's constitutional AI training prioritizes nuanced, instruction-following output that consistently wins human-preference evaluations[^15][^16] | Claude Opus 4.7 YouTube review, 2026-04-15; LLM Stats Claude Opus 4.7 launch, 2026-04-15 |
| 6 | Structured data extraction (JSON from unstructured text) | **GPT-5.4** | Claude Opus 4.7 | GPT-5.4 introduced Tool Search in its API, enabling deferred loading of only relevant tool definitions for improved selection accuracy in production; its 83% GDPval knowledge-work score supports precision extraction; both models support native structured outputs[^17][^18] | OpenAI API guide (GPT-5.4), 2026-03-05; mean.ceo AI model releases, 2026-03-31 |
| 7 | Mathematical and quantitative reasoning | **GPT-5.5** | Claude Opus 4.7 | GPT-5.5 tops the Artificial Analysis Intelligence Index at 60 as of April 23, 2026; GPT-5.4 scored AIME 2025: 99, BRUMO 2025: 97 — the strongest pre-5.5 math scores published; Claude Opus 4.7 scores AIME 2025: 98 as runner-up[^19][^20][^3] | BenchLM Which LLM to Use, 2026-04-08; Artificial Analysis Intelligence Index, 2026-04-23 |
| 8 | Real-time / social media sentiment analysis | **Grok 4.20** | Perplexity Sonar Pro | Grok 4.20 ingests ~68M X posts per day via the live X firehose — providing real-time social grounding unavailable to any other in-scope model; Perplexity Sonar Pro's continuous web retrieval is the best fallback for non-X social sources[^2][^21] | Awesome Agents Grok 4.20 review, 2026-04-12; Tech Insights Week 9, 2026-02-21 |
| 9 | Translation and multilingual tasks | **Gemini 3.1 Pro** | GPT-5.5 | Gemini 3.1 Pro leads MGSM and MMLU-ProX multilingual benchmarks; on a 25-model translation benchmark (OpenMark, March 2026) Gemini 3.1 Pro tied for second at 61% accuracy with the best speed-to-accuracy ratio in the top tier; BenchLM provisional multilingual leaderboard shows Gemini 3.1 Pro at 100.0% weighted score[^22][^23] | OpenMark translation benchmark, 2026-03-13; BenchLM multilingual leaderboard, 2026-04-22 |
| 10 | Summarization of long documents | **Grok 4.20** | Gemini 3.1 Pro | Grok 4.20's 2M context window allows ingestion of the largest documents without chunking; Gemini 3.1 Pro posts 84.9% MRCR v2 at 128k for long-context retrieval accuracy as the strongest alternative within its 1M context cap[^9][^11] | AI/ML API Grok 4.20 review, 2026-04-22; Google DeepMind model card, 2026-02-18 |
| 11 | Image analysis / OCR / vision tasks | **Gemini 3.1 Pro** | GPT-5.5 | Gemini 3.1 Pro natively processes text, image, audio, and video simultaneously without transcription — the only in-scope model with this capability; scores ~90.3 on OmniDocBench (highest frontier LLM OCR score); GPT-5.5 is the omnimodal fallback with native text/image/audio/video processing[^24][^25][^26] | Lumichats Gemini 3.1 review, 2026-04-12; ofox.ai OCR benchmark, 2026-04-06 |
| 12 | Conversational chat / general Q&A | **GPT-5.5** | Gemini 3.1 Pro | GPT-5.5 tops Artificial Analysis Intelligence Index at 60 and is designed for "more intuitive" behavior requiring less guidance; Gemini 3.1 Pro held Elo 1493 on LMSYS Chatbot Arena as of April 6, 2026 (third overall)[^5][^13][^3] | RoboRhythms GPT-5.5 launch, 2026-04-22; LMSYS Chatbot Arena rankings, 2026-04-06 |
| 13 | Technical explanation for non-experts | **Claude Opus 4.7** | GPT-5.5 | Claude's constitutional AI training emphasizes accessible explanation and precise instruction-following; Claude Opus 4.7 adds a new xhigh effort mode for deeply structured reasoning that translates well to layered pedagogical output[^16][^14] | LLM Stats Claude Opus 4.7 launch, 2026-04-15; apiyi.com benchmark review, 2026-04-17 |
| 14 | Competitive / market research synthesis | **Perplexity Sonar Deep Research** | Grok 4.20 | Sonar Deep Research synthesizes hundreds of sources into long-form, cited research reports via API; it is the only in-scope model with mandatory live retrieval making it structurally suited to competitive intelligence; Grok 4.20's X firehose adds real-time social/market signal[^10][^9] | Perplexity API docs, 2026-02-03; AI/ML API Grok 4.20 review, 2026-04-22 |
| 15 | Legal and regulatory research | **Claude Opus 4.7** | Gemini 3.1 Pro | Claude Opus 4.7 scores 94.2% on GPQA Diamond — closest proxy for the analytical depth required in legal research — and its 1M context window supports full-contract ingestion; Gemini 3.1 Pro leads at 94.3% GPQA Diamond in head-to-head comparisons[^16][^6] | LLM Stats Claude Opus 4.7, 2026-04-15; Serenitiesai Gemini 3.1 Pro, 2026-02-19 |
| 16 | Financial analysis and modeling logic | **GPT-5.5** | Claude Opus 4.7 | GPT-5.5 tops the Artificial Analysis Intelligence Index for quantitative depth; Claude Opus 4.7 leads the Finance Agent benchmark at 64.4% (state-of-the-art at its release), 3.7 points above Opus 4.6's 60.7%[^16][^5] | LLM Stats Claude Opus 4.7, 2026-04-15; RoboRhythms GPT-5.5, 2026-04-22 |
| 17 | Prompt engineering and meta-prompting | **Claude Opus 4.7** | GPT-5.4 | Claude Opus 4.7 leads MCP-Atlas (tool invocation) by 9.2 points over GPT-5.4 and introduced Routines in Claude Code for automated prompt scheduling; its xhigh effort mode supports deeply structured meta-reasoning[^14][^27] | apiyi.com benchmark review, 2026-04-17; ScriptByAI Claude timeline, 2026-04-20 |
| 18 | Adversarial reasoning / red-teaming / debate | **Claude Opus 4.7** | GPT-5.5 | Claude Opus 4.7 verifies its own outputs before reporting back — a critical property for adversarial stress-testing; Anthropic notes it "can catch its own mistakes" and carries safeguards derived from the Project Glasswing deployment[^16][^14] | LLM Stats Claude Opus 4.7 launch, 2026-04-15; apiyi.com benchmark review, 2026-04-17 |

***

## Model Profiles

### 1. GPT-5.5
**Provider:** OpenAI  
**Full name:** GPT-5.5 (codename "Spud"); sub-models: GPT-5.5 Pro  
**Released:** April 23, 2026[^26][^5]

**Access methods:** ChatGPT (Plus at $20/mo, Pro at $200/mo, Team/Enterprise); API in Responses and Chat Completions APIs "coming very soon"; available in Codex. Consumer rollout live April 23; API access requires additional safeguards review. Available via Cursor (when API opens) and Poe[^5][^26]

**Context window:** 1,000,000 tokens (confirmed at launch; exact surcharge thresholds pending full API documentation)[^28]

**Pricing tier:** API (announced): $5/M input, $30/M output (standard); $30/M input, $180/M output (GPT-5.5 Pro); Batch/Flex: 0.5× standard; Priority: 2.5× standard[^29][^30]

**Key strengths:** Leads Artificial Analysis Intelligence Index at 60 — highest composite score ever recorded across 356 evaluated models. OpenAI states GPT-5.5 delivers "state-of-the-art intelligence at half the cost of competitive frontier coding models" on the Artificial Analysis Coding Index and uses significantly fewer tokens per task in Codex. First fully retrained base model (not a fine-tune of GPT-5.x) since GPT-4.5, with native omnimodal processing across text, image, audio, and video in a single system. Strongest performance on GPQA at 93.6% per Vellum leaderboard.[^12][^31][^20][^3][^26]

**Key weaknesses:** API not live as of research date; consumer-only rollout at launch with additional safeguards required for developer access. GPT-5.5 Pro at $180/M output is the most expensive token rate of any in-scope model. Token efficiency advantage vs. Claude Opus 4.7 not yet independently verified.[^26][^29]

**Last updated by provider:** April 23, 2026[^32]

**Top task category:** Mathematical and quantitative reasoning

***

### 2. GPT-5.4
**Provider:** OpenAI  
**Full name:** GPT-5.4; sub-models: GPT-5.4 Thinking, GPT-5.4 Pro, GPT-5.4 mini, GPT-5.4 nano  
**Released:** March 5, 2026 (GPT-5.4); March 17–18, 2026 (mini/nano)[^18][^33]

**Access methods:** ChatGPT (all paid plans; GPT-5.4 Thinking is the strong reasoning option); API via Responses and Chat Completions (model: `gpt-5.4`); Codex; Cursor (native); Poe; major enterprise wrappers[^34][^17]

**Context window:** 1,050,000 tokens (standard 272K window by default; 1M opt-in via `model_context_window` param; inputs over 272K priced at 2× input rate)[^35][^17]

**Pricing tier:** $2.50/M input, $15/M output (standard, ≤272K); $5/M input, $22.50/M output (>272K, full session); GPT-5.4 Pro: $30/M input, $180/M output; mini: $0.20/M input; nano: lowest tier[^36][^37]

**Key strengths:** Record scores on OSWorld-Verified and WebArena Verified computer-use benchmarks at launch. AIME 2025: 99, BRUMO 2025: 97, MRCRv2: 97 — strongest published math/reasoning benchmarks before GPT-5.5. Tool Search API feature enables deferred tool loading in large tool ecosystems, the most mature structured-output tooling of any in-scope model. 33% fewer per-claim errors and 18% fewer overall errors vs. GPT-5.2.[^19][^17][^18]

**Key weaknesses:** Long-context surcharge doubles input pricing above 272K tokens; superseded by GPT-5.5 on Artificial Analysis Intelligence Index as of April 23, 2026. Output pricing ($15/M standard) is higher than Gemini 3.1 Pro ($12/M) and Grok 4.20 ($6/M).[^3][^28][^35]

**Last updated by provider:** March 5, 2026 (GPT-5.4); March 17, 2026 (mini/nano)[^33]

**Top task category:** Structured data extraction (JSON / function calling)

***

### 3. Claude Opus 4.7
**Provider:** Anthropic  
**Full name:** Claude Opus 4.7; model ID: `claude-opus-4-7`  
**Released:** April 16, 2026[^38][^16]

**Access methods:** Claude.ai (Pro plan at $20/mo; free tier limited to Claude Sonnet 4.6); Anthropic API; Amazon Bedrock; Google Cloud Vertex AI; Microsoft Foundry; GitHub Copilot (replacing Opus 4.5/4.6)[^39][^38]

**Context window:** 1,000,000 tokens (with improved long-context retrieval vs. Opus 4.6)[^16][^39]

**Pricing tier:** $5/M input, $25/M output; long-context premium (>200K): $10/M input, $37.50/M output; prompt caching: 90% discount on cache reads; batch processing: 50% discount. Important: updated tokenizer inflates token consumption ~35% vs. Opus 4.6 on the same input[^40][^39][^29]

**Key strengths:** Leads SWE-bench Verified at 87.6% (up from 80.8% for Opus 4.6, +6.8pp), SWE-bench Pro at 64.3% (+10.9pp over Opus 4.6), and the Finance Agent benchmark at 64.4%. 94.2% on GPQA Diamond and 69.4% on Terminal-Bench 2.0. Verifies its own outputs before reporting — a structural property unique among in-scope models for adversarial and agentic tasks. Polymarket consensus gives Anthropic 92.5% implied probability of holding the LMSYS Chatbot Arena top spot at end of April 2026.[^15][^4][^1][^16]

**Key weaknesses:** Tokenizer update inflates effective token counts by up to 35%, making the sticker price misleading for cost modeling. Prefilling assistant messages now returns a 400 error — a breaking change for existing integrations. Surpassed by the unreleased Claude Mythos Preview (93.9% SWE-bench Verified) in nearly every category.[^41][^42][^40]

**Last updated by provider:** April 16, 2026[^38]

**Top task category:** Code generation — agentic (multi-file, terminal access)

***

### 4. Claude Sonnet 4.6
**Provider:** Anthropic  
**Full name:** Claude Sonnet 4.6; released February 17, 2026  
**Sub-family context:** Middle tier of the current Anthropic lineup (Haiku 4.5 → Sonnet 4.6 → Opus 4.7)[^27][^43]

**Access methods:** Claude.ai (Free and Pro tiers — the default model on the free tier); Anthropic API; Amazon Bedrock; Google Cloud Vertex AI; Cursor (native)[^43][^44]

**Context window:** 200K standard; 1M in beta (API only)[^44]

**Pricing tier:** $3/M input, $15/M output (standard); batch: 50% discount; prompt caching up to 90% discount[^43][^44]

**Key strengths:** Holds Elo 1523 on the LMSYS coding leaderboard — third globally, behind only Opus 4.6 variants. Described by Anthropic as "a full upgrade across coding, computer use, long-context reasoning, agent planning, knowledge work, and design". Best price-to-performance ratio in the Anthropic lineup for production workloads; 20% cheaper input than Opus while retaining strong coding and reasoning.[^45][^27][^43]

**Key weaknesses:** Weaker on the hardest single-task benchmarks (SWE-bench Verified: 79.6% vs. Opus 4.7's 87.6%); not suitable as the primary model for complex multi-file agentic coding.[^4][^46]

**Last updated by provider:** February 17, 2026[^27]

**Top task category:** Production API workloads requiring Claude-quality output at reduced cost

***

### 5. Claude Haiku 4.5
**Provider:** Anthropic  
**Full name:** Claude Haiku 4.5  
**Released:** Late 2025 (still current as of April 2026)[^43]

**Access methods:** Claude.ai (available on paid plans); Anthropic API; Amazon Bedrock; Vertex AI; Claude Code (native)[^47][^43]

**Context window:** 200,000 tokens[^44]

**Pricing tier:** $1/M input, $5/M output — lowest cost tier in the Anthropic lineup[^48][^43]

**Key strengths:** Fastest and cheapest Claude model for high-throughput applications; 97.6% on HumanEval (Python code generation) per Logic.inc benchmarks — the highest HumanEval score of any in-scope model. Suitable for real-time applications, classification, and lightweight agentic orchestration steps where Opus-level reasoning is not required.[^49][^47]

**Key weaknesses:** Weakest reasoning capability in the Claude lineup; not suitable for graduate-level reasoning, complex multi-step agentic tasks, or tasks requiring deep context synthesis.[^47][^44]

**Last updated by provider:** Late 2025 (last pricing confirmation: March 2026)[^43]

**Top task category:** High-throughput classification, lightweight extraction, and chatbot orchestration

***

### 6. Gemini 3.1 Pro
**Provider:** Google DeepMind  
**Full name:** Gemini 3.1 Pro (Preview); sub-models in the 3.x family: Gemini 3.0 Flash (GA), Gemini 3.1 Flash-Lite Preview, Gemini 3.1 Flash Image Preview  
**Released:** February 19, 2026[^24][^6]

**Access methods:** Google AI Studio (Pro models require paid billing as of April 1, 2026); Google AI Pro subscription ($19.99/mo); Google AI Ultra ($249.99/mo); Vertex AI; Gemini CLI (free: 60 req/min, 1,000 req/day); LangChain / n8n compatible via OpenAI-compatible API wrapper[^50][^51][^7]

**Context window:** 1,000,000 tokens[^52][^24]

**Pricing tier:** $2/M input (≤200K), $4/M input (>200K), $12/M output (≤200K), $18/M output (>200K). Pro models removed from free tier April 1, 2026; Flash-Lite remains free-tier eligible[^53][^51][^54]

**Key strengths:** Leads ARC-AGI-2 at 77.1% — more than double Gemini 3 Pro's 31.1% and the highest score of any in-scope model on this benchmark. Leads GPQA Diamond at 94.3% in head-to-head comparisons with contemporaneous models. Scores ~90.3 on OmniDocBench for OCR/document AI — the highest frontier LLM score. Native simultaneous processing of text, image, audio, and video in a single pass. Tied with GPT-5.4 at top of Artificial Analysis Intelligence Index (score: 57) as of March 2026; best cost-to-intelligence ratio at $2/$12 per million tokens among frontier models.[^25][^55][^6][^56][^24]

**Key weaknesses:** Free-tier access for Pro models eliminated April 1, 2026; Tier 2 rate limits require $250 cumulative spend over 30 days. Long-context pricing doubles above 200K tokens to $4/$18 per million.[^51][^54][^53]

**Last updated by provider:** February 19, 2026 (model); April 1, 2026 (billing policy)[^6][^51]

**Top task category:** Image analysis / OCR / vision tasks; ARC-AGI-2 novel reasoning

***

### 7. Grok 4.20 Beta 2
**Provider:** xAI  
**Full name:** Grok 4.20 Beta 2; also available: Grok 4.1 Fast  
**Released:** Beta public: February 17, 2026; API: March 10, 2026; Beta 2: March 24, 2026[^57][^2]

**Access methods:** xAI API (docs.x.ai); SuperGrok subscription (~$30/mo); X Premium+ ($40/mo or $395/yr); SuperGrok Heavy ($300/mo, extended reasoning); Cursor via BYOK (OpenAI-compatible base URL override; note: overrides all other models when active)[^58][^2][^59]

**Context window:** 2,000,000 tokens (256K default; 2M in agentic/tool-use modes)[^21][^58]

**Pricing tier:** $2/M input, $6/M output; cached input: $0.20/M; batch: 50% discount. Grok 4.1 Fast: $0.20/M input, $0.50/M output with same 2M context[^60][^58]

**Key strengths:** Largest context window among in-scope models at 2M tokens ($2/$6/M — the lowest output cost of any in-scope frontier model). Ingests ~68M X posts per day via the live X firehose, providing real-time social grounding unavailable to other in-scope models. Generation speed of 233–235 tokens/second — fastest among in-scope frontier models. 78% SWE-bench Verified and 94.0% HumanEval as of April 2026; holds Arena Elo 1491 (fourth overall, April 6, 2026), beating GPT-5.4-High. Humanity's Last Exam: 50.7% — leading the field on this hardest-difficulty benchmark.[^61][^9][^13][^58][^21][^60]

**Key weaknesses:** Beta label indicates potential instability; 16K max output tokens limits very long generative outputs. Cursor integration requires global base-URL override, breaking other model access until toggled off. ARC-AGI-2 score is significantly weaker than Gemini 3.1 Pro (~16% vs. 77.1%).[^62][^59][^58]

**Last updated by provider:** March 24, 2026[^58]

**Top task category:** Real-time / social media sentiment analysis; long-context document analysis

***

### 8. Perplexity Sonar Family
**Provider:** Perplexity AI  
**Full name:** Sonar, Sonar Pro, Sonar Reasoning Pro, Sonar Deep Research  
**Released:** New Sonar updated March 17, 2026; Sonar Deep Research: March 7, 2025 (still current)[^63][^64]

**Access methods:** Perplexity.ai web and mobile app (Free, Pro at $20/mo, Max at $200/mo); Perplexity API; OpenRouter (model ID: `perplexity/sonar-deep-research`); Max plan unlocks Sonar Deep Research and access to frontier guest models (GPT-5.x, Claude Opus, Gemini 3.x, Grok)[^65][^66][^63]

**Context window:** Sonar: 128K; Sonar Pro: 200K; Sonar Reasoning Pro: 128K; Sonar Deep Research: 128K[^65]

**Pricing tier:** Sonar API: $1/M input; Sonar Pro API: $3/M input; Sonar Deep Research API: $2/M input, $8/M output; consumer Pro: $20/mo; Max: $200/mo[^8][^66]

**Key strengths:** The only in-scope model family with mandatory web retrieval on every query — a structural advantage for any task requiring current information. Sonar Pro achieves SimpleQA factuality F-score of 0.858 — industry best. Generation speed of 1,200 tokens/second via Cerebras infrastructure — ~10× faster than Gemini 3.0 Flash. Sonar Deep Research autonomously reads and synthesizes hundreds of sources into structured, cited reports. Multi-model routing within Perplexity Max allows access to GPT-5.x, Claude Opus, Gemini, and Grok through a single interface for cross-model verification.[^10][^63][^8][^65]

**Key weaknesses:** Sonar's base model (Llama 3.3 70B) is less capable for complex reasoning than frontier models when web retrieval is not the primary advantage. Sonar Deep Research API ($8/M output) is expensive at scale; deep reasoning access (Sonar Reasoning Pro and frontier model guests) requires Max plan at $200/mo.[^66][^63][^65]

**Last updated by provider:** March 17, 2026 (Sonar update)[^63]

**Top task category:** Web research with live citations; competitive / market research synthesis

***

## Benchmark Snapshot

### 1. Artificial Analysis Intelligence Index
**URL:** https://artificialanalysis.ai/evaluations/artificial-analysis-intelligence-index  
**Date of latest publication:** Continuously updated; data retrieved April 23, 2026[^20][^3]
**What it measures:** A composite benchmark aggregating 10 challenging evaluations across mathematics, science, coding, and reasoning — the broadest publicly available composite index covering 356+ models

| Rank | Model | Score |
|------|-------|-------|
| 1 | GPT-5.5 (xhigh) | 60 |
| 2 | GPT-5.5 (high) | 59 |
| 3 | Claude Opus 4.7 (Adaptive Reasoning, Max Effort) | 57 |
| 4 | Gemini 3.1 Pro Preview | 57 |
| 5 | GPT-5.4 (xhigh) | 57 |

[^20][^3]

***

### 2. SWE-bench Verified
**URL:** https://benchlm.ai/benchmarks/sweVerified  
**Date of latest publication:** April 23, 2026[^46][^41]
**What it measures:** The ability of an AI agent to autonomously resolve real GitHub software engineering issues — the leading benchmark for agentic coding capability

| Rank | Model | Score |
|------|-------|-------|
| 1 | Claude Mythos Preview (restricted, not publicly accessible) | 93.9% |
| 2 | **Claude Opus 4.7** | 87.6% |
| 3 | **GPT-5.3 Codex** | 85.0% |
| 4 | Claude Opus 4.5 | 80.9% |
| 5 | **Gemini 3.1 Pro** | 80.6% |

*Bold = in-scope models only*[^41][^46]

***

### 3. LMSYS Chatbot Arena (Overall — Text)
**URL:** https://lmarena.ai/leaderboard/text  
**Date of latest publication:** April 6, 2026 (most recent published snapshot within research window)[^13][^67]
**What it measures:** Crowd-sourced human preference evaluation — blind A/B tests where users judge which model gives the better response; the industry standard for measuring perceived response quality across diverse real-world prompts

| Rank | Model | Arena Elo | Organization |
|------|-------|-----------|--------------|
| 1 | claude-opus-4-6-thinking | 1504 | Anthropic |
| 2 | claude-opus-4-6 | 1500 | Anthropic |
| 3 | gemini-3.1-pro-preview | 1493 | Google |
| 4 | grok-4.20-beta1 | 1491 | xAI |
| 5 | gemini-3-pro | 1486 | Google |
| 6 | gpt-5.4-high | 1484 | OpenAI |

*Note: Claude Opus 4.7 (released April 16) was not yet in the April 6 snapshot; Polymarket consensus gives Anthropic 92.5% probability of holding the top spot at April 30*[^67][^1][^13]

***

### 4. ARC-AGI-2
**URL:** https://arcprize.org/arc-agi/2  
**Date of latest publication:** Ongoing; model scores from February–April 2026[^6][^62]
**What it measures:** Novel abstract reasoning from visual grid-based puzzles specifically designed to resist training-data pattern matching; human average ~60%; pure LLMs score 0%

| Rank | Model | Score |
|------|-------|-------|
| 1 | **Gemini 3.1 Pro** | 77.1% |
| 2 | **Claude Opus 4.6** | 68.8% |
| 3 | **Claude Sonnet 4.6** | 60.4% |
| 4 | **GPT-5.2** | 52.9% |
| 5 | **Grok 4.20** | ~16% |

*Bold = in-scope models; Grok 4.20 ARC-AGI-2 score from Design for Online cross-benchmark table*[^62][^6]

***

## Access and Pricing Notes

**GPT-5.5 (OpenAI, April 23, 2026):** Consumer ChatGPT rollout live on launch day; API access announced but requires additional safeguards review before release. API pricing: $5/M input, $30/M output (standard); $30/M input, $180/M output (GPT-5.5 Pro). Batch/Flex at 0.5× standard; Priority at 2.5× standard.[^30][^5][^29]

**GPT-5.4 long-context surcharge (OpenAI):** The 1M token context is opt-in and must be explicitly enabled. Inputs exceeding 272K tokens are priced at 2× the standard input rate for the full session. This doubles costs for large-document workflows without prior configuration.[^37][^35]

**Claude Opus 4.7 tokenizer change (Anthropic, April 16, 2026):** Sticker price unchanged at $5/$25 per million tokens, but a new tokenizer inflates token consumption by up to 35% for the same input. Effective per-request costs can rise ~35% without any price-list change. Developers must revalidate cost models before migrating from Opus 4.6.[^40][^39]

**Gemini API free-tier removal (Google, April 1, 2026):** Pro models (including Gemini 3.1 Pro) removed from the free tier. Flash and Flash-Lite remain free-tier eligible. Tier 2 production rate limits now require $250 cumulative spend over 30 days. Mandatory monthly spending caps introduced — API pauses automatically at cap.[^68][^51]

**Grok 4.20 API open (xAI, March 10, 2026):** $2/M input, $6/M output — lowest output price among in-scope frontier models. Grok 4.1 Fast offers same 2M context at $0.20/$0.50 per million tokens for budget workloads. SuperGrok consumer: ~$30/mo.[^2][^58]

**Pricing summary (standard API, per 1M tokens, April 23, 2026):**

| Model | Input | Output | Context |
|-------|-------|--------|---------|
| GPT-5.5 | $5.00 | $30.00 | 1.0M |
| GPT-5.5 Pro | $30.00 | $180.00 | 1.0M |
| GPT-5.4 | $2.50 | $15.00 | 1.05M |
| GPT-5.4 Pro | $30.00 | $180.00 | 1.05M |
| Claude Opus 4.7 | $5.00 | $25.00 | 1.0M |
| Claude Sonnet 4.6 | $3.00 | $15.00 | 200K/1M beta |
| Claude Haiku 4.5 | $1.00 | $5.00 | 200K |
| Gemini 3.1 Pro | $2.00 | $12.00 | 1.0M |
| Gemini 3.1 Flash-Lite | $0.25 | $1.50 | 1.0M |
| Grok 4.20 | $2.00 | $6.00 | 2.0M |
| Grok 4.1 Fast | $0.20 | $0.50 | 2.0M |
| Sonar Deep Research | $2.00 | $8.00 | 128K |

[^54][^29][^28][^66][^58][^43]

***

## Drift Warnings

**1. Using GPT-5.4 for all coding work instead of Claude Opus 4.7:**  
Users default to GPT-5.4 for coding because of OpenAI's brand recognition, but Claude Opus 4.7 scores 87.6% on SWE-bench Verified vs. GPT-5.4's ~80–81.5%, and leads SWE-bench Pro (agentic coding) at 64.3% vs. GPT-5.4's 57.7%. The 6.6-point Pro gap is the most reliable signal of general coding capability since Pro tests multi-language, non-contaminated tasks. *Source: Vellum benchmark analysis, 2026-04-15; TokenMix SWE-bench 2026, 2026-04-19*.[^4][^46]

**2. Using GPT-5.x or Claude for real-time market/social intelligence:**  
Users choose GPT-5.5 or Claude Opus 4.7 for competitive research, but neither model has live data access without explicit web-browsing tool calls. Grok 4.20 ingests ~68M X posts daily via the X firehose and Perplexity Sonar retrieves live web content on every query — structural advantages that GPT and Claude cannot match from their static training data alone. *Source: Tech Insights 2026 Week 9, 2026-02-21; Perplexity model catalog, 2026-01-10*.[^21][^65]

**3. Treating Gemini 3.1 Pro as still "free to try" via the API:**  
As of April 1, 2026, Gemini 3.1 Pro requires paid API credentials — it was removed from the free tier. Developers who built prototypes on the free tier will hit 429 errors without billing enabled. Gemini 3.1 Flash-Lite ($0.25/$1.50 per million tokens) remains free-tier eligible and retains a 1M context window, making it the correct free-tier fallback. *Source: Google Gemini API free tier changes, 2026-04-15*.[^51][^54]

**4. Ignoring the Claude Opus 4.7 tokenizer change when estimating API costs:**  
Teams migrating from Opus 4.6 to 4.7 at the same $5/$25 sticker price may see bills increase up to 35% due to the new tokenizer encoding more tokens per character — especially in non-English text and large codebase contexts. The cost model must be re-benchmarked on actual workloads, not assumed from the rate card. *Source: Finout Claude Opus 4.7 pricing analysis, 2026-04-16; GlobalGPT pricing guide, 2026-04-16*.[^39][^40]

**5. Picking GPT-5.5 for long-document analysis over Grok 4.20:**  
Users assume the highest-ranked model on composite benchmarks handles all tasks best, but GPT-5.5's context window details are not yet fully documented. Grok 4.20's confirmed 2M context window at $2/$6 per million tokens is the largest confirmed among in-scope models and offers the lowest output cost at frontier quality. For tasks where document length exceeds 272K tokens, Grok 4.20 avoids both the GPT-5.4 surcharge and any Opus 4.7 long-context premium. *Source: AI/ML API Grok 4.20 review, 2026-04-22; LLM Stats GPT-5.5 vs. Claude Opus 4.7, 2026-04-22*.[^9][^29]

***

## Sources Cited

1. BenchLM.ai, "How to Choose an LLM in 2026: Which AI Model Is Best for Your Use Case," Glevd, 2026-04-08. https://benchlm.ai/blog/posts/which-llm-to-use

2. mean.ceo, "New AI Model Releases News | April 2026 (Startup Edition)," 2026-03-31. https://blog.mean.ceo/new-ai-model-releases-news-april-2026/

3. 9to5Mac, "Anthropic reveals new Opus 4.6 model," 2026-02-04. https://9to5mac.com/2026/02/05/anthropic-reveals-new-opus-4-6-model-with-more-autonomy-and-better-focus/

4. Vellum.ai, "LLM Leaderboard 2026 — Compare Top AI Models," 2026-04-22. https://www.vellum.ai/llm-leaderboard

5. Fazm.ai, "OpenAI API Updates April 2026," 2026-04-12. https://fazm.ai/blog/openai-api-updates-april-2026

6. CNBC, "OpenAI announces GPT-5.5," 2026-04-23. https://www.cnbc.com/2026/04/23/openai-announces-latest-artificial-intelligence-model.html

7. ScriptByAI, "Anthropic Claude Timeline: From Claude 1 to Claude Opus 4.7 (2026)," 2026-04-20. https://www.scriptbyai.com/anthropic-claude-timeline/

8. YouTube / Supreme Guru Tech, "Claude Opus 4.7 Just Dropped — Here's What's New (2026)," 2026-04-15. https://www.youtube.com/watch?v=awK2PQy_g5c

9. Releasebot.io, "OpenAI Release Notes — April 2026 Latest Updates," 2026-04-22. https://releasebot.io/updates/openai

10. Polymarket, "Which company has the best AI model end of April?" 2026-03-19. https://polymarket.com/event/which-company-has-the-best-ai-model-end-of-april

11. Lumichats, "Gemini 3.1 Pro: Google's Most Powerful AI (2026)," 2026-04-12. https://lumichats.com/blog/gemini-3-1-pro-complete-review-2026-google-most-powerful-ai-1m-context-vs-gpt-54-claude

12. AIToolsRecap, "Current Grok Version (April 2026): Grok 4.20 Beta 2," 2026-04-15. https://aitoolsrecap.com/Blog/current-grok-version-april-2026-xai-models-explained

13. Google DeepMind, "Gemini 3.1 Pro — Model Card," 2026-02-18. https://deepmind.google/models/model-cards/gemini-3-1-pro/

14. Vellum.ai, "Claude Opus 4.7 Benchmarks Explained," 2026-04-15. https://www.vellum.ai/blog/claude-opus-4-7-benchmarks-explained

15. RoboRhythms, "GPT-5.5 Just Shipped and OpenAI Finally Built a Real Agent," 2026-04-22. https://www.roborhythms.com/openai-gpt-5-5-launch-april-2026/

16. LLM Stats, "GPT-5.5 vs Claude Opus 4.7: Pricing, Speed, Benchmarks," 2026-04-22. https://llm-stats.com/blog/research/gpt-5-5-vs-claude-opus-4-7

17. Serenitiesai, "Gemini 3.1 Pro: 77% ARC-AGI-2 Score & Benchmarks (2026)," 2026-02-19. https://serenitiesai.com/articles/google-gemini-3-1-pro-review-benchmarks-2026

18. LLM Stats, "Claude Opus 4.7: Benchmarks, Pricing, Context & What's New," 2026-04-15. https://llm-stats.com/blog/research/claude-opus-4-7-launch

19. Lushbinary.com, "GPT-5.5 vs Claude Opus 4.7: Benchmarks, Pricing & Coding," 2026-04-22. https://lushbinary.com/blog/gpt-5-5-vs-claude-opus-4-7-comparison-benchmarks-pricing/

20. LinkedIn / Samin Samad, "Google Gemini 3.1 Pro Doubles ARC-AGI-2 Score," 2026-04-01. https://www.linkedin.com/posts/samin-samad-b02818166_something-massive-just-happened-in-the-ai-activity-7445470156912488448-XEcy

21. Kingy.ai, "GPT-5.5 Benchmarks Revealed: The 9 Numbers That Changed the AI Race," 2026-04-22. https://kingy.ai/ai/gpt-5-5-benchmarks-revealed-the-9-numbers-that-prove-chatgpt-5-5-just-changed-the-ai-race/

22. Mashable, "Google releases Gemini 3.1 Pro: Benchmarks, how to try it," 2026-02-19. https://mashable.com/article/google-releases-gemini-3-1-pro-benchmarks

23. apiyi.com, "Claude Opus 4.7 Benchmark Full Analysis," 2026-04-17. https://help.apiyi.com/en/claude-opus-4-7-benchmark-review-2026-en.html

24. Artificialanalysis.ai, "Artificial Analysis Intelligence Index," retrieved 2026-04-23. https://artificialanalysis.ai/evaluations/artificial-analysis-intelligence-index

25. Artificialanalysis.ai, "Comparison of AI Models across Intelligence, Performance, and Price," retrieved 2026-04-23. https://artificialanalysis.ai/models

26. Promptt.dev, "Artificial Analysis Intelligence Index Rankings March 2026," 2026-03-30. https://www.promptt.dev/blog/artificial-analysis-intelligence-index-rankings-march-2026

27. Timewell, "Perplexity AI Complete Guide 2026: Sonar Pro, Deep Research," 2026-01-20. https://timewell.jp/en/columns/perplexity

28. TokenMix.ai, "Grok 4 Benchmarks 2026: 78% SWE-bench, 91% MMLU," 2026-04-06. https://tokenmix.ai/blog/grok-4-benchmark

29. TechCrunch, "OpenAI launches GPT-5.4 with Pro and Thinking versions," 2026-03-04. https://techcrunch.com/2026/03/05/openai-launches-gpt-5-4-with-pro-and-thinking-versions/

30. Perplexity API Docs, "Sonar Deep Research," 2026-02-03. https://docs.perplexity.ai/docs/sonar/models/sonar-deep-research

31. TokenMix.ai, "SWE-Bench 2026: Claude Opus 4.7 Wins 87.6% vs GPT-5.3 85.0%," 2026-04-19. https://tokenmix.ai/blog/swe-bench-2026-claude-opus-4-7-wins

32. BenchLM.ai, "Grok 4.20 Benchmarks 2026: Scores, Rankings & Performance," 2026-04-22. https://benchlm.ai/models/grok-4-20-beta

33. AI/ML API, "Grok 4.20 Review 2026: Everything You Need to Know," 2026-04-22. https://aimlapi.com/blog/grok-4-20-review-2026-everything-you-need-to-know

34. Awesome Agents, "Grok 4.20 Review: Four Minds Are Better Than One," 2026-04-12. https://awesomeagents.ai/reviews/review-grok-4-20/

35. Tech Insights 2026 Week 9, "Grok 4.20 launch details," 2026-02-21. https://www.techbyjohan.com/tech-insights-2026-week-9/

36. BenchLM.ai, "SWE-bench Verified Benchmark 2026: 34 LLM scores," 2026-04-22. https://benchlm.ai/benchmarks/sweVerified

37. AIDevDay India, "LMSYS Chatbot Arena Leaderboard Current Top Models," 2026-01-31 (content current to April 6, 2026). https://aidevdayindia.org/blogs/lmsys-chatbot-arena-current-rankings/lmsys-chatbot-arena-leaderboard-current-top-models.html

38. AIDevDay India, "LMSYS High ELO Leaderboard: April 2026," 2026-01-26 (content current to April 6, 2026). https://aidevdayindia.org/blogs/lmsys-chatbot-arena-current-rankings/lmsys-chatbot-arena-high-elo-rankings.html

39. Design for Online, "The Best AI Models So Far in 2026," 2026-03-13. https://designforonline.com/the-best-ai-models-so-far-in-2026/

40. AIDevDay India, "LMSYS Chatbot Arena Coding Leaderboard April 2026," 2026-01-30 (content current to April 6, 2026). https://aidevdayindia.org/blogs/lmsys-chatbot-arena-current-rankings/lmsys-chatbot-arena-coding-leaderboard-2026.html

41. BenchLM.ai, "Multilingual Benchmarks 2026: MGSM, MMLU-ProX LLM Scores," 2026-04-22. https://benchlm.ai/multilingual

42. OpenMark.ai, "Best AI for Translation 2026: Top 25 Models Benchmarked," 2026-03-13. https://openmark.ai/best-ai-for-translation

43. BenchLM.ai, "Claude API Pricing: Haiku 4.5, Sonnet 4.6, and Opus 4.6 (April 2026)," 2026-04-12. https://benchlm.ai/blog/posts/claude-api-pricing

44. OpenAI, "Using GPT-5.4 | Developer Guide," 2026-03-05. https://developers.openai.com/api/docs/guides/latest-model

45. CloudZero, "OpenAI API Cost In 2026: Every Model Compared," 2026-04-08. https://www.cloudzero.com/blog/openai-pricing/

46. OpenAI, "Introducing GPT-5.5," 2026-04-23. https://openai.com/index/introducing-gpt-5-5/

47. Finout, "Claude Opus 4.7 Pricing: The Real Cost Story," 2026-04-16. https://www.finout.io/blog/claude-opus-4-7-pricing-the-real-cost-story-behind-the-unchanged-price-tag

48. GlobalGPT, "Claude Opus 4.7 Price: 2026 API Rates & Subscription," 2026-04-16. https://www.glbgpt.com/resources/claude-opus-4-7-price/

49. TokenCost.app, "Grok 4.20 API Pricing (Updated April 2026)," 2026-04-13. https://tokencost.app/models/grok-4-20

50. Verdent.ai, "Gemini 3.1 Flash-Lite vs Flash vs Pro: Which Should You Use?" 2026-03-11. https://www.verdent.ai/guides/gemini-3-1-flash-lite-vs-flash-vs-pro

51. Help.apiyi.com, "Google Gemini API free tier tightened: Pro models to become paid-only," 2026-04-15. https://help.apiyi.com/en/google-gemini-api-free-tier-changes-april-2026-guide-en.html

52. GlobalGPT, "Gemini 3.1 Pro API Pricing & Performance," 2026-02-25. https://www.glbgpt.com/hub/gemini-3-1-pro-api-pricing-performance-the-complete-guide-for-developers/

53. Lushbinary.com, "GPT-5.5 Developer Guide: Omnimodal, Coding & Agentic Workflows," 2026-04-22. https://lushbinary.com/blog/gpt-5-5-developer-guide-omnimodal-coding-agentic-workflows/

54. ofox.ai, "Best AI Model for OCR in 2026: Frontier LLMs vs Specialized Vision Models," 2026-04-06. https://ofox.ai/blog/best-ai-model-for-ocr-2026/

55. Galaxy.ai, "Sonar Deep Research Model Specs, Costs & Benchmarks (April 2026)," 2026-04-23. https://blog.galaxy.ai/model/sonar-deep-research

56. Anthropic, "Introducing Claude Opus 4.7," 2026-04-15. https://www.anthropic.com/news/claude-opus-4-7

57. Logic.inc, "AI model benchmarks March 2026 Guide," 2026-04-08. https://logic.inc/resources/ai-model-benchmarks-guide

58. ByteIota, "LLM Benchmarks 2026: What Changed and What Matters," 2026-04-16. https://byteiota.com/llm-benchmarks-2026-what-changed-and-what-matters/

59. Cursor Community Forum, "Adding Grok 4.20 breaks composer use," 2026-03-15. https://forum.cursor.com/t/adding-grok-4-20-breaks-composer-use/154915

60. TLDL.io, "LLM API Pricing 2026 — Compare GPT-5, Claude 4, Gemini," 2026-02-23. https://www.tldl.io/resources/llm-api-pricing-2026

---

## References

1. [Which company has the best AI model end of April? - Polymarket](https://polymarket.com/event/which-company-has-the-best-ai-model-end-of-april) - Anthropic's Claude Opus 4.7 release on April 16 propelled it to the top of LMSYS Chatbot Arena and c...

2. [Grok 4.20 Review: Four Minds Are Better Than One | Awesome Agents](https://awesomeagents.ai/reviews/review-grok-4-20/) - Real-time X firehose access is a genuine competitive advantage for financial and market research; 2M...

3. [Comparison of AI Models across Intelligence, Performance, and Price](https://artificialanalysis.ai/models) - Comparison and analysis of AI models across key performance metrics including quality, price, output...

4. [Claude Opus 4.7 Benchmarks Explained - Vellum](https://www.vellum.ai/blog/claude-opus-4-7-benchmarks-explained) - SWE-bench Verified jumps from 80.8% to 87.6%, a nearly 7-point gain that puts Opus 4.7 ahead of Gemi...

5. [GPT-5.5 Just Shipped and OpenAI Finally Built a Real Agent](https://www.roborhythms.com/openai-gpt-5-5-launch-april-2026/) - OpenAI just launched GPT-5.5 in April 2026 with real computer-use and multi-step agent workflows. He...

6. [Gemini 3.1 Pro: 77% ARC-AGI-2 Score & Benchmarks (2026)](https://serenitiesai.com/articles/google-gemini-3-1-pro-review-benchmarks-2026) - Google Gemini 3.1 Pro released today with 77.1% ARC-AGI-2 — doubling its predecessor. Full benchmark...

7. [Google Gemini 3.1 Pro Doubles ARC-AGI-2 Score, Outperforms ...](https://www.linkedin.com/posts/samin-samad-b02818166_something-massive-just-happened-in-the-ai-activity-7445470156912488448-XEcy) - Google's Gemini 3.1 Pro doubled its ARC-AGI-2 score in a single generation — from 31.1% to 77.1% — w...

8. [Perplexity AI Complete Guide 2026: Sonar Pro, Deep Research, and ...](https://timewell.jp/en/columns/perplexity) - In 2026, Perplexity AI has established itself as the definitive AI search platform. Sonar Pro leads ...

9. [Grok 4.20 Review 2026: Everything You Need to Know - AI/ML API](https://aimlapi.com/blog/grok-4-20-review-2026-everything-you-need-to-know) - Grok 4.20 leads on generation speed (235 vs ~80 tokens/second), context window (2M vs 128K tokens), ...

10. [Sonar deep research - Perplexity API](https://docs.perplexity.ai/docs/sonar/models/sonar-deep-research)

11. [Gemini 3.1 Pro - Model Card - Google DeepMind](https://deepmind.google/models/model-cards/gemini-3-1-pro/) - Gemini 3.1 Pro was evaluated across a range of benchmarks, including reasoning, multimodal capabilit...

12. [OpenAI Release Notes - April 2026 Latest Updates - Releasebot](https://releasebot.io/updates/openai) - Complete list of OpenAI latest updates for April 2026: get every product news, release note, and cha...

13. [LMSYS Chatbot Arena Leaderboard Current Top Models](https://aidevdayindia.org/blogs/lmsys-chatbot-arena-current-rankings/lmsys-chatbot-arena-leaderboard-current-top-models.html) - View the lmsys chatbot arena leaderboard current top models to see who leads the AI race. We track w...

14. [Claude Opus 4.7 Benchmark Full Analysis: Empirical Data Leading ...](https://help.apiyi.com/en/claude-opus-4-7-benchmark-review-2026-en.html) - Claude Opus 4.7 is the flagship Large Language Model released by Anthropic on April 16, 2026. It lea...

15. [Claude Opus 4.7 Just Dropped — Here's What's New (2026)](https://www.youtube.com/watch?v=awK2PQy_g5c) - Anthropic just released Claude Opus 4.7, their latest AI model. It's a major upgrade for coding and ...

16. [Claude Opus 4.7: Benchmarks, Pricing, Context & What's New](https://llm-stats.com/blog/research/claude-opus-4-7-launch) - Claude Opus 4.7 scores 87.6% on SWE-bench Verified, 94.2% on GPQA, 1M token context, 3.3x higher-res...

17. [Using GPT-5.4 | OpenAI API](https://developers.openai.com/api/docs/guides/latest-model) - 1M token context window: GPT-5.4 supports up to a 1M token context window, making it easier to analy...

18. [New AI Model Releases News | April, 2026 (STARTUP EDITION)](https://blog.mean.ceo/new-ai-model-releases-news-april-2026/) - Explore the New AI Model Releases News, April 2026, including Claude Mythos 5 and Gemini 3.1. Discov...

19. [How to Choose an LLM in 2026: Which AI Model Is Best for Your ...](https://benchlm.ai/blog/posts/which-llm-to-use) - A step-by-step framework for choosing the right LLM in 2026. We compare Claude Opus 4.6, Gemini 3.1 ...

20. [Artificial Analysis Intelligence Index](https://artificialanalysis.ai/evaluations/artificial-analysis-intelligence-index) - Compare AI model performance on Artificial Analysis Intelligence Index. A composite benchmark aggreg...

21. [Tech Insights 2026 Week 9](https://www.techbyjohan.com/tech-insights-2026-week-9/) - AI released the public beta of Grok 4.20 on February 17, 2026, available to SuperGrok (~$30/month) a...

22. [Best AI for Translation 2026: Top 25 Models Benchmarked | OpenMark](https://openmark.ai/best-ai-for-translation) - We benchmarked 25 AI models on translation across 6 languages — short phrases, domain terminology, a...

23. [Multilingual Benchmarks 2026: MGSM, MMLU-ProX LLM Scores](https://benchlm.ai/multilingual) - Compare 202 AI models on multilingual benchmarks with MGSM and MMLU-ProX. Evaluate cross-language re...

24. [Gemini 3.1 Pro: Google's Most Powerful AI (2026) — 1 Million ...](https://lumichats.com/blog/gemini-3-1-pro-complete-review-2026-google-most-powerful-ai-1m-context-vs-gpt-54-claude) - Google released a model with a 1-million-token context window that understands text, image, audio, a...

25. [Choosing By Use Case](https://ofox.ai/blog/best-ai-model-for-ocr-2026/) - A practical comparison of OCR capabilities across Gemini 3.1 Pro, Claude Opus 4.6, GPT-5.4, and spec...

26. [GPT-5.5 Developer Guide: Omnimodal, Coding & Agentic Workflows](https://lushbinary.com/blog/gpt-5-5-developer-guide-omnimodal-coding-agentic-workflows/) - ChatGPT access is available now — the consumer-facing deployment has passed safety review; API acces...

27. [Anthropic Claude Timeline: From Claude 1 to Claude Opus 4.7 (2026)](https://www.scriptbyai.com/anthropic-claude-timeline/) - See all Claude AI release dates from Anthropic, including Claude 1, 2, 3, 4, and the latest 4.7. Ful...

28. [GPT-5.5 vs Claude Opus 4.7: Benchmarks, Pricing & Coding ...](https://lushbinary.com/blog/gpt-5-5-vs-claude-opus-4-7-comparison-benchmarks-pricing/) - GPT-5.5 API pricing is $5 per million input tokens and $30 per million output tokens. Claude Opus 4....

29. [GPT-5.5 vs Claude Opus 4.7: Pricing, Speed, Benchmarks - LLM Stats](https://llm-stats.com/blog/research/gpt-5-5-vs-claude-opus-4-7) - Pricing diverges only on output. Both charge $5 per 1M input tokens on the standard tier. GPT-5.5 is...

30. [GPT-5.5 Benchmarks Revealed: The 9 Numbers That ... - Kingy AI](https://kingy.ai/ai/gpt-5-5-benchmarks-revealed-the-9-numbers-that-prove-chatgpt-5-5-just-changed-the-ai-race/) - API pricing (forthcoming): $5 / 1M input tokens and $30 / 1M output tokens for GPT-5.5 with a 1M con...

31. [LLM Leaderboard 2026 — Compare Top AI Models - Vellum](https://www.vellum.ai/llm-leaderboard) - Compare the latest LLM benchmarks for GPT, Claude, Gemini and more. Updated rankings across reasonin...

32. [OpenAI announces GPT-5.5, its latest artificial intelligence model](https://www.cnbc.com/2026/04/23/openai-announces-latest-artificial-intelligence-model.html) - The model is better at coding, using computers and pursuing deeper research capabilities, OpenAI say...

33. [OpenAI API Updates April 2026: GPT-5.4 Mini/Nano, Server ... - Fazm](https://fazm.ai/blog/openai-api-updates-april-2026) - Complete guide to every OpenAI API update in April 2026, including GPT-5.4 mini and nano model launc...

34. [GPT-5.4 by OpenAI: New Features, Computer Use & API Access](https://coursiv.io/blog/openai-gpt-5-4) - In the API version, the model supports a context window of up to 1 million tokens, allowing systems ...

35. [GPT-5.4 deep dive: pricing, context limits, and tool search explained](https://community.openai.com/t/gpt-5-4-deep-dive-pricing-context-limits-and-tool-search-explained/1375800) - The 1M context window is opt-in (and worth understanding first). The 1M token context is real, but i...

36. [OpenAI API Cost In 2026: Every Model Compared - CloudZero](https://www.cloudzero.com/blog/openai-pricing/) - OpenAI API costs range from $0.20 to $30 per million input tokens. Compare GPT-5.4, Mini, Nano prici...

37. [GPT-5.4 Pricing (2026): API Costs, Benchmarks & Worth the Upgrade?](https://www.glbgpt.com/hub/gpt-5-4-pricing/) - Get the official GPT-5.4 pricing for 2026. Compare API rates, the 272K surcharge, and see why GPT-5....

38. [Introducing Claude Opus 4.7 - Anthropic](https://www.anthropic.com/news/claude-opus-4-7) - Pricing remains the same as Opus 4.6: $5 per million input tokens and $25 per million output tokens....

39. [Claude Opus 4.7 Pricing: The Real Cost Story Behind the ... - Finout](https://www.finout.io/blog/claude-opus-4.7-pricing-the-real-cost-story-behind-the-unchanged-price-tag) - Anthropic released Claude Opus 4.7 on April 16, 2026, and the official headline is simple. Prices ar...

40. [Claude Opus 4.7 Price: 2026 API Rates & Subscription - GlobalGPT](https://www.glbgpt.com/resources/claude-opus-4-7-price/) - The official API rate for Claude Opus 4.7 is $5.00 per million (MTok) input tokens and $25.00 per mi...

41. [SWE-bench Verified Benchmark 2026: 34 LLM scores | BenchLM.ai](https://benchlm.ai/benchmarks/sweVerified) - As of April 21, 2026, Claude Mythos Preview leads the SWE-bench Verified leaderboard with 93.9% , fo...

42. [Claude Opus 4.7: What Changed for Coding Agents (April 2026)](https://www.verdent.ai/guides/what-is-claude-opus-4-7) - Pricing is unchanged: $5 per million input tokens, $25 per million output tokens, across API, Bedroc...

43. [Claude API Pricing: Haiku 4.5, Sonnet 4.6, and Opus 4.6 (April 2026)](https://benchlm.ai/blog/posts/claude-api-pricing) - Current Anthropic Claude API pricing from official model pages and the Claude Opus 4.7 launch announ...

44. [Claude API Pricing Guide 2026: Opus 4.6 ($5), Sonnet ... - DevTk.AI](https://devtk.ai/en/blog/claude-api-pricing-guide-2026/) - Updated March 2026. Official Claude 4.6 pricing: Opus ($5/$25), Sonnet ($3/$15), and Haiku ($1/$5) p...

45. [LMSYS Chatbot Arena Coding Leaderboard April 2026](https://aidevdayindia.org/blogs/lmsys-chatbot-arena-current-rankings/lmsys-chatbot-arena-coding-leaderboard-2026.html) - The Coding Family: Anthropic's Claude 4.6 variants now occupy the entire top 3 globally, with Claude...

46. [SWE-Bench 2026: Claude Opus 4.7 Wins 87.6% vs GPT-5.3 85.0%](https://tokenmix.ai/blog/swe-bench-2026-claude-opus-4-7-wins) - SWE-Bench Verified April 2026: Claude Opus 4.7 leads at 87.6%, GPT-5.3-Codex 85.0%, Gemini 3.1 Pro 8...

47. [Anthropic Claude API Pricing 2026 - Silicon Data](https://www.silicondata.com/use-cases/anthropic-claude-api-pricing-2026/) - A comprehensive breakdown of Anthropic Claude API pricing for 2026, covering per-token rates for Hai...

48. [Claude API Pricing (March 2026): Opus $5/M Tokens, Sonnet $3 ...](https://www.tldl.io/resources/anthropic-api-pricing) - Claude API pricing 2026: Opus $5.00/M input, $25.00/M output. Sonnet $3.00/$15.00, Haiku $0.25/$1.25...

49. [AI model benchmarks March 2026 Guide - Logic](https://logic.inc/resources/ai-model-benchmarks-guide) - Complete guide to AI model benchmarks in March 2026. Learn how to compare GPT, Claude, and Gemini pe...

50. [Gemini 3.1 Pro: Benchmarks, Pricing & Full Access Guide (2026)](https://almcorp.com/blog/gemini-3-1-pro-complete-guide/) - Gemini 3.1 Pro scores 77.1% on ARC-AGI-2—more than double Gemini 3 Pro. Full guide: verified benchma...

51. [Google Gemini API free tier tightened: Pro models to become paid ...](https://help.apiyi.com/en/google-gemini-api-free-tier-changes-april-2026-guide-en.html) - Author's Note: A detailed breakdown of the major changes to the Google Gemini API free tier as of Ap...

52. [Gemini 3.1 Pro Preview - Intelligence, Performance & Price Analysis](https://artificialanalysis.ai/models/gemini-3-1-pro-preview) - The model supports text, image, speech, and video input, outputs text, and has a 1m tokens context w...

53. [Gemini 3.1 Pro API Pricing & Performance: The Complete 2026 ...](https://www.glbgpt.com/hub/gemini-3-1-pro-api-pricing-performance-the-complete-guide-for-developers/) - Discover Gemini 3.1 Pro API pricing ($2/$12). Unlock 64K output, bypass Tier 2 limits, and get insta...

54. [Gemini 3.1 Flash-Lite vs Flash vs Pro: Which Should You Use?](https://www.verdent.ai/guides/gemini-3-1-flash-lite-vs-flash-vs-pro) - An honest comparison of all three Gemini 3.1 models — Flash-Lite, Flash, and Pro — with clear guidan...

55. [Artificial Analysis Intelligence Index Rankings March 2026](https://www.promptt.dev/blog/artificial-analysis-intelligence-index-rankings-march-2026)

56. [Google releases Gemini 3.1 Pro: Benchmarks, how to try it | Mashable](https://mashable.com/article/google-releases-gemini-3-1-pro-benchmarks) - Google says that Gemini 3.1 Pro achieved twice the verified performance of 3 Pro on ARC-AGI-2, a pop...

57. [Current Grok Version (April 2026): Grok 4.20 Beta 2 + What's Next](https://aitoolsrecap.com/Blog/current-grok-version-april-2026-xai-models-explained) - Current Grok version in April 2026 is Grok 4.20 Beta 2. See what changed, who gets access, and wheth...

58. [Grok 4.20 API Pricing (Updated April 2026) - TokenCost](https://tokencost.app/models/grok-4-20) - Grok 4.20 costs $2/1M input and $6/1M output tokens. 2.0M context window. Free token counter, monthl...

59. [Adding Grok 4.20 breaks composer use - Cursor - Community Forum](https://forum.cursor.com/t/adding-grok-4-20-breaks-composer-use/154915) - I added grok 4.20 successfully by using the Override OpenAI Base URL and the OpenAI APi Key settings...

60. [Grok 4.20 Benchmarks 2026: Scores, Rankings & Performance](https://benchlm.ai/models/grok-4-20-beta) - According to BenchLM.ai, Grok 4.20 ranks #24 out of 109 models on the provisional leaderboard with a...

61. [Grok 4 Benchmarks 2026: 78% SWE-bench, 91% MMLU Full Test](https://tokenmix.ai/blog/grok-4-benchmark) - Grok 4.20 hits 78% on SWE-bench Verified, placing it within striking distance of GPT-5.4 and ahead o...

62. [The Best AI Models So Far in 2026 | Design for Online®](https://designforonline.com/the-best-ai-models-so-far-in-2026/) - Gemini 3.1 Pro, Claude Sonnet 4.6, Grok 4.20 and more dropped in February 2026. We rank the best AI ...

63. [Meet New Sonar](https://www.perplexity.ai/hub/blog/meet-new-sonar) - A Blazing Fast Model Optimized for Perplexity Search

64. [Sonar Deep Research Model Specs, Costs & Benchmarks (April 2026)](https://blog.galaxy.ai/model/sonar-deep-research) - Detailed breakdown of Sonar Deep Research including features, pricing, benchmarks, and performance a...

65. [Perplexity AI Available Models: All Supported Models, Version ...](https://www.datastudios.org/post/perplexity-ai-available-models-all-supported-models-version-differences-capabilities-comparison) - Perplexity AI delivers a diverse model ecosystem for both consumer users and developers, combining a...

66. [Perplexity: Sonar Deep Research | Design for Online](https://designforonline.com/ai-models/perplexity-sonar-deep-research/) - Perplexity: Sonar Deep Research by Perplexity. 128K context, from $2.00/1M tokens. See benchmarks, c...

67. [LMSYS High ELO Leaderboard: The 1500+ Hard Prompt Tier ...](https://aidevdayindia.org/blogs/lmsys-chatbot-arena-current-rankings/lmsys-chatbot-arena-high-elo-rankings.html) - The elite bracket just shifted to 1500+ Elo! Discover the April 2026 high-Elo rankings. Claude Opus ...

68. [Gemini API Pricing: Free Tier Limits + April 2026 Changes | FindSkill.ai](https://findskill.ai/blog/gemini-api-pricing-guide/) - Gemini API pricing explained — free tier limits, paid tier costs per million tokens, April 2026 bill...

