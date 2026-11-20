<div align="center">

# Muhammad Hamid

**AI Automation Engineer · Python · MCP · RAG · Agent Evals**

I build tool-using AI agents and the plumbing that makes them trustworthy: permissioned tool
registries, human approval gates, full run traces, cost accounting, and eval suites that prove the
agent is not making numbers up. Then I ship the same class of fixes back upstream.

[![Portfolio](https://img.shields.io/badge/Portfolio-abouthamid.web.app-0b7285?style=for-the-badge&logo=googlechrome&logoColor=white)](https://abouthamid.web.app/)
[![Resume](https://img.shields.io/badge/Resume-Interactive-2ea44f?style=for-the-badge&logo=readdotcv&logoColor=white)](https://hamid-resume.web.app/)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-0077b5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/muhammad-hamid-digital-marketing/)
[![WhatsApp](https://img.shields.io/badge/WhatsApp-Direct-25d366?style=for-the-badge&logo=whatsapp&logoColor=white)](https://wa.me/923167417135)

![Merged PRs](https://img.shields.io/badge/merged%20PRs-50-2ea44f?style=flat-square)
![Open PRs](https://img.shields.io/badge/open%20PRs-60-0969da?style=flat-square)
![Upstream projects](https://img.shields.io/badge/upstream%20projects-25-6f42c1?style=flat-square)
![Public repos](https://img.shields.io/badge/public%20repos-82-6e7781?style=flat-square)
![Open to work](https://img.shields.io/badge/open%20to-AI%20automation%20contracts-8250df?style=flat-square)

</div>

---

## What I actually build

| | Focus | Evidence in this account |
|---|---|---|
| **Agent systems** | Tool-using agents with explicit permission levels (`read` / `write` / `external`), model-agnostic LLM clients, MCP tool servers, full run traces, cost accounting per run | [ai-marketing-growth-os](https://github.com/hamid-digitalmarketer/ai-marketing-growth-os), [shopify-growth-mcp](https://github.com/hamid-digitalmarketer/shopify-growth-mcp) |
| **Reliability & evals** | Labeled eval datasets, metric reporters, self-evaluating test labs, known-good vs known-broken agents, CI coverage gates | [ai-agent-testing-lab](https://github.com/hamid-digitalmarketer/ai-agent-testing-lab), [ai-marketing-shared](https://github.com/hamid-digitalmarketer/ai-marketing-shared) |
| **Human-in-the-loop** | Approval queues with explicit state machines (`pending → approved → rejected → executed → measured`), plan-preview-apply for every write action, audit logging | [ai-marketing-growth-os](https://github.com/hamid-digitalmarketer/ai-marketing-growth-os), [shopify-growth-mcp](https://github.com/hamid-digitalmarketer/shopify-growth-mcp) |
| **RAG, retrieval & extraction** | Embedding/document-QA pipelines, offline model loading, HTML text extraction, structured data pulls (upstream work, see below) | [rag-docker](https://github.com/mikesilvers/rag-docker), [geniebot](https://github.com/iamvisheshsrivastava/geniebot), [trafilatura](https://github.com/adbar/trafilatura) |
| **Deployment** | FastAPI services, Docker / Compose, Firebase & Cloud Functions, GitHub Actions CI with coverage gates, zero-API-key demo modes | [searchpulse-ai](https://github.com/hamid-digitalmarketer/searchpulse-ai), [conversionbridge](https://github.com/hamid-digitalmarketer/conversionbridge) |

**Python is the default language. TypeScript where the surfaces are MCP servers and browser tooling.**

---

## Featured: AI automation core

| Project | What it does | Stack |
|---|---|---|
| [**ai-marketing-growth-os**](https://github.com/hamid-digitalmarketer/ai-marketing-growth-os) | Agentic operations platform: tool registry with permission gates, MCP adapters, evidence-backed recommendations (never hallucinated metrics), approval queue for every write, per-run tracing and cost accounting, eval harness against labeled datasets. `docker compose up` runs end-to-end on sample data | Python · FastAPI · Pydantic v2 · Docker |
| [**shopify-growth-mcp**](https://github.com/hamid-digitalmarketer/shopify-growth-mcp) | Production **MCP server** exposing **61 tools** over products, orders, inventory, metafields, SEO/GEO and feeds — read-only by default, with plan → preview → bound approval → apply and a full audit trail on writes. Works with Claude, Cursor, ChatGPT, VS Code, Codex | TypeScript · MCP · Shopify GraphQL |
| [**ai-agent-testing-lab**](https://github.com/hamid-digitalmarketer/ai-agent-testing-lab) | Reliability lab for AI agents: 7 labeled eval suites asking the questions that matter — did it call only permitted tools, did it invent a number, did it skip the approval gate. Ships a known-good agent that must pass and a broken one that must fail, so the lab validates itself | Python · pytest |
| [**ai-marketing-shared**](https://github.com/hamid-digitalmarketer/ai-marketing-shared) | The shared substrate behind the other repos: Pydantic v2 schemas, `Tool` base class with permission levels, provider abstraction (OpenAI / Anthropic / local HTTP / deterministic mock), tracing, cost controls, eval harness | Python · Pydantic v2 |
| [**searchpulse-ai**](https://github.com/hamid-digitalmarketer/searchpulse-ai) | Search-analytics service with the arithmetic done correctly (click-weighted CTR, impression-weighted position), striking-distance and traffic-drop diagnostics. 26 tests, 84% coverage, `/health` liveness check, Docker Compose + CI | Python · FastAPI · Pandas |
| [**ai-search-visibility-auditor**](https://github.com/hamid-digitalmarketer/ai-search-visibility-auditor) | Audits whether AI crawlers (GPTBot, ClaudeBot, PerplexityBot, Google-Extended, …) can actually reach your content, `llms.txt` validation, AI-citation readiness scoring | Python · Streamlit |

---

## Featured: automation that lands on revenue systems

| Project | What it does | Stack |
|---|---|---|
| [**conversionbridge**](https://github.com/hamid-digitalmarketer/conversionbridge) | Privacy-first server-side conversion gateway for Meta CAPI and GA4 — fail-closed consent, atomic deduplication, no PII leakage | Python · FastAPI · Firebase |
| [**whatsapp-attribution-router**](https://github.com/hamid-digitalmarketer/whatsapp-attribution-router) | UTM-preserving click-to-chat attribution with 48h deduplication, Sheets + GoHighLevel sync | JavaScript · Python |
| [**conversion-tracking-doctor**](https://github.com/hamid-digitalmarketer/conversion-tracking-doctor) | Breaks down GA4 / Ads / Meta Pixel / server-side tracking drift and tells you which event actually broke | Python |
| [**ppc-waste-detector**](https://github.com/hamid-digitalmarketer/ppc-waste-detector) | Finds search-query bleed, cannibalisation, PMax junk traffic and zero-conversion spend | Python · SQLite |
| [**meta-lead-quality-analyzer**](https://github.com/hamid-digitalmarketer/meta-lead-quality-analyzer) | Lead scoring and CRM revenue feedback loop — bot and disposable-email detection, offline conversion sync | Python |
| [**ai-marketing-mix-copilot**](https://github.com/hamid-digitalmarketer/ai-marketing-mix-copilot) | Bayesian Marketing Mix Modeling and incrementality testing for budget allocation | Python |
| [**seo-doctor**](https://github.com/hamid-digitalmarketer/seo-doctor) | Technical crawler: broken links, canonical loops, redirect chains, crawl-over-crawl comparison | Python CLI |
| [**geo-visibility-lab**](https://github.com/hamid-digitalmarketer/geo-visibility-lab) | Local SEO proximity-grid rank tracking against Google Business Profile | Python · GeoJSON |
| [**ecommerce-seo-optimizer**](https://github.com/hamid-digitalmarketer/ecommerce-seo-optimizer) | Catalogue-scale listing audits and fixes — titles, descriptions, structured data | Python · Streamlit |
| [**envscope**](https://github.com/hamid-digitalmarketer/envscope) | Audits `.env` against `.env.example` and a JSON schema without ever printing a secret | Python CLI |

**Security & AppSec work lives on a separate account:** [@mhamidlad](https://github.com/mhamidlad).

---

## Upstream contributions

**50 merged pull requests across 25 upstream projects**, 60 more in review. Every fix ships with a
regression test that reproduces the defect before it is patched — no drive-by formatting PRs, no
badge farming.

| Project | Merged | What the fixes covered |
|---|:---:|---|
| [vibgrate/cli](https://github.com/vibgrate/cli) | 8 | SBOM and lockfile edge cases (pnpm catalogs/engines, Swift `Package.resolved` v1, Cargo root crates, Go workspaces), `vg scan` reporting snapshots |
| [simple-invoicing](https://github.com/nikhilb2/simple-invoicing-free-gst-billing-software) | 5 | Invoice and credit-note date windows, GST credited-total comparison, ESLint cleanup, password policy |
| [iamvisheshsrivastava/Smart_CSV_Toolkit](https://github.com/iamvisheshsrivastava/Smart_CSV_Toolkit) | 3 | pandas 2.x `applymap` removal, readable pipeline option labels, `size_multiplier` help text |
| [iamvisheshsrivastava/AirKube](https://github.com/iamvisheshsrivastava/AirKube) | 3 | Neo4j connector cleanup in `finally`, clean 404 for missing KG models, endpoint coverage |
| [selimfirat/pysad](https://github.com/selimfirat/pysad) | 3 | Full type hints for LODA and RSHash, postprocessing and streaming-scaler examples |
| [lukeautry/tsoa](https://github.com/lukeautry/tsoa) | 3 | Bundled `@tsoa/cli` route-template resolution, metadata deduplication, `Swagger.Discriminator` declarations |
| [rdlugs/sentryward](https://github.com/rdlugs/sentryward) | 2 | SSRF-prone NAT64 / 6to4 / reserved IPv4 blocking, login-timing account enumeration |
| [doobidoo/mcp-memory-service](https://github.com/doobidoo/mcp-memory-service) | 2 | **MCP** tool annotations, hermetic session/auth test isolation |
| [iamvisheshsrivastava/ab-lab](https://github.com/iamvisheshsrivastava/ab-lab) | 2 | Input validation for binomial/continuous simulation helpers |
| [iamvisheshsrivastava/geniebot](https://github.com/iamvisheshsrivastava/geniebot) | 2 | **RAG** bot: placeholder handling on `/summarize` when the LLM is unconfigured |
| [exmergo/dex](https://github.com/exmergo/dex) | 1 | Declared-join validation reporting missing columns instead of failing `--verify` |
| [MysterionRise/pubchem-finder](https://github.com/MysterionRise/pubchem-finder) | 1 | Molecular similarity search: MCP server and CLI fixes |
| [supabase/supabase-py](https://github.com/supabase/supabase-py) | 1 | PostgREST filter serialization (`null` / booleans in `in_()`) |
| [mikesilvers/rag-docker](https://github.com/mikesilvers/rag-docker) | 1 | Offline loading of pre-cached sentence-transformers models |
| [aws-samples/genai-db-modernizer](https://github.com/aws-samples/sample-aws-genai-db-modernizer) | 1 | Dependency floor alignment with the ATX image |
| [anveshachuri/recarena](https://github.com/anveshachuri/recarena) | 1 | Repeated-slate check computed once in `BatchSimulator.step` |
| [cfgaudit/cfgaudit](https://github.com/cfgaudit/cfgaudit) | 1 | Every `--package` / `-p` flag checked for a version pin |
| [wemake-services/imgproxykit](https://github.com/wemake-services/imgproxykit) | 1 | Django import typo in smoke tests, failures propagated to exit code |
| [OpenWave-India/modeldiff](https://github.com/OpenWave-India/modeldiff) | 1 | Non-ASCII reports when stdout is redirected (cp1252 → UTF-8) |
| [laaielichter/Gulliver](https://github.com/laaielichter/Gulliver) | 1 | CLI rejects window/limit values below one |
| [markline-dev/markline](https://github.com/markline-dev/markline) | 1 | OpenAPI sample generation: sanitise tag-derived result variable names |
| [adbar/trafilatura](https://github.com/adbar/trafilatura) | 1 | Drop heading permalink anchors (`¶`/`§`) from extracted text |
| [Opencomplai/opencomplai](https://github.com/Opencomplai/opencomplai) | 1 | CI concurrency and permission tightening |
| [finos/open-resource-broker](https://github.com/finos/open-resource-broker) | 1 | Compute provisioning API fixes |
| [pygrpc/pygrpc-native](https://github.com/pygrpc/pygrpc-native) | 1 | gRPC server behaviour in the Rust binding |

**Most recent merges**

| Merged | Project | Change |
|---|---|---|
| 2026-11-13 | [markline-dev/markline#56](https://github.com/markline-dev/markline/pull/56) | `fix(openapi)` — sanitise tag-derived result variable names in SDK samples |
| 2026-11-11 | [adbar/trafilatura#1086](https://github.com/adbar/trafilatura/pull/1086) | `fix(htmlprocessing)` — drop heading permalink anchors from output |
| 2026-11-10 | [iamvisheshsrivastava/AirKube#28](https://github.com/iamvisheshsrivastava/AirKube/pull/28) | `fix` — clean 404 for missing KG models plus endpoint coverage |
| 2026-11-10 | [iamvisheshsrivastava/Smart_CSV_Toolkit#30](https://github.com/iamvisheshsrivastava/Smart_CSV_Toolkit/pull/30) | `fix(steps)` — correct Dataset Multiplier help text |
| 2026-11-10 | [iamvisheshsrivastava/Smart_CSV_Toolkit#28](https://github.com/iamvisheshsrivastava/Smart_CSV_Toolkit/pull/28) | `fix` — replace removed `DataFrame.applymap` with `map` |
| 2026-11-10 | [iamvisheshsrivastava/ab-lab#20](https://github.com/iamvisheshsrivastava/ab-lab/pull/20) | `fix` — validate simulation inputs before allocating |
| 2026-11-09 | [laaielichter/Gulliver#95](https://github.com/laaielichter/Gulliver/pull/95) | `fix(cli)` — refuse windows and limits below one |

**In review now (60 open)** — the largest single block is a locale-correctness sweep in
[iamkun/dayjs](https://github.com/iamkun/dayjs) (**53 locales** where `yearStart` disagreed with
CLDR `firstDay` / week rules), each PR one locale plus a table-driven test and the CLDR citation.
Alongside it: [vibgrate/cli#685](https://github.com/vibgrate/cli/pull/685) (gemspec dependency
parsing), [date-fns/date-fns](https://github.com/date-fns/date-fns)
(`exactOptionalPropertyTypes`), `MysterionRise/pubchem-finder`, `iamvisheshsrivastava/*`,
`adbar/trafilatura`, `markline-dev/markline`, `finos/open-resource-broker`, `wandb/rai-toolkit`,
`google/sbsim`, `OpnForm/OpnForm`, `Dpro-at/Tel-Agent`, `pygrpc/pygrpc-native`.

To date that is **164 pull requests opened** — 50 merged, 60 open, 54 closed without merge (mostly
upstream preferring a different implementation). Closed branches are left closed, not re-pinged.

→ [See all pull requests](https://github.com/hamid-digitalmarketer?tab=pull-requests) · [Audit log with every PR](CONTRIBUTIONS.md)

---

## Toolbox

![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)
![MCP](https://img.shields.io/badge/Model%20Context%20Protocol-000000?style=flat-square&logo=anthropic&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white)
![Pydantic](https://img.shields.io/badge/Pydantic%20v2-E92063?style=flat-square&logo=pydantic&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub%20Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white)
![Firebase](https://img.shields.io/badge/Firebase-FFCA28?style=flat-square&logo=firebase&logoColor=black)
![GCP](https://img.shields.io/badge/Google%20Cloud-4285F4?style=flat-square&logo=googlecloud&logoColor=white)
![Node.js](https://img.shields.io/badge/Node.js-339933?style=flat-square&logo=nodedotjs&logoColor=white)
![Go](https://img.shields.io/badge/Go-00ADD8?style=flat-square&logo=go&logoColor=white)
![Postgres](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)

**Agent engineering** — tool registries and permission levels, MCP servers (61 tools shipped), approval
state machines, provider abstraction (OpenAI / Anthropic / local / mock), run tracing, cost accounting
**Reliability** — labeled eval datasets, metric reporters, self-validating test labs, pytest / Vitest /
Jest, coverage gates in CI
**Backend & delivery** — FastAPI, Pydantic v2, Docker Compose, Firebase Cloud Functions, GitHub Actions,
Cloud Run
**Domain systems** — GA4 and server-side GTM, Meta Conversions API, BigQuery, Shopify GraphQL, Google
Ads / Meta Ads APIs, technical SEO and GEO tooling

---

## Selected results

| Engagement | Outcome |
|---|---|
| MHW Clothing | Organic traffic +40%, conversion rate +75%, CAC −70% |
| Healthrix BPO | Scaled acquisition to 200+ employees; won US healthcare and tech contracts |
| Riceland Healthcare System | Multi-location patient-acquisition funnels and search visibility |
| Latest Bedding (UK) | Built and led the cross-functional e-commerce marketing team |

---

## Work with me

I take **AI automation contracts** — agents that touch real systems, and the guardrails that make
them safe to run:

- **Agent build** — a tool-using agent wired to your APIs and data, with permission boundaries,
  approval gates and a trace you can audit
- **MCP server** — your internal systems exposed as MCP tools that Claude / Cursor / ChatGPT can drive
- **Eval harness** — labeled datasets and regression suites so a model or provider change cannot
  silently degrade the agent
- **Automation of the boring parts** — reporting, tracking QA, catalogue and feed pipelines, crawl
  diagnostics, spend forensics
- **Fractional technical lead** — I have run marketing departments for 8+ years, so the automation I
  build targets the number that actually moves

📬 [WhatsApp +92 316 7417135](https://wa.me/923167417135) · [abouthamid.web.app](https://abouthamid.web.app/) · [LinkedIn](https://www.linkedin.com/in/muhammad-hamid-digital-marketing/)

<sub>Lahore, Pakistan · Open to AI automation contracts and engineering roles · All GitHub metrics verified from the API on 2026-11-20</sub>
