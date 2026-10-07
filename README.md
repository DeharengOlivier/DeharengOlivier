# Olivier Dehareng

**Software engineer · Applied AI, systems & developer tools**

I build software across the stack: retrieval and evaluation pipelines, GPU compute shaders, network protocol visualisations, developer tools, web applications and mobile products. I run [Aurelona](https://aurelona.com), where I develop my own products alongside client work.

My public work includes **10 engineering projects**, from a RAG engine that runs without an API key to a Rust physics solver running on the GPU. I care about what happens beyond the demo: how a system is evaluated, what it does when inputs are wrong, and whether someone else can inspect and reproduce its behaviour.

I'm interested in **software engineering roles in applied AI, evaluation, developer infrastructure and systems**.

[Portfolio](https://olivierdehareng.com) · [All repositories](https://github.com/DeharengOlivier?tab=repositories) · [Email](mailto:deharengolivier@gmail.com) · [LinkedIn](https://www.linkedin.com/in/dehareng-olivier)

## Selected open-source work

### [rag-engine](https://github.com/DeharengOlivier/rag-engine) — Retrieval, grounding & evaluation

An offline-first RAG pipeline with pluggable embeddings and model providers, optional PII redaction before indexing, source citations and a retrieval-score threshold for refusing unsupported queries. The evaluation harness measures retrieval recall and keyword coverage; the default pipeline needs no network or API key.

**Python · NumPy · optional OpenAI / Anthropic providers**

[Architecture and design](https://github.com/DeharengOlivier/rag-engine#why-this-design) · [Evaluation](https://github.com/DeharengOlivier/rag-engine/tree/main/evals)

### [down-the-stack](https://github.com/DeharengOlivier/down-the-stack) — Network protocols, byte by byte

An interactive 3D journey through a real captured HTTPS request. Protocol encoders are checked against the published capture, and TLS 1.3 records are decrypted in the browser. Reconstructed Wi-Fi framing and the modelled physical layer are explicitly distinguished from captured data.

**TypeScript · Three.js · TLS · TCP/IP · signal processing**

[What is measured and what is reconstructed](https://github.com/DeharengOlivier/down-the-stack#every-byte-is-real) · [Tests](https://github.com/DeharengOlivier/down-the-stack/tree/main/tests)

### [gpu-cloth-simulation](https://github.com/DeharengOlivier/gpu-cloth-simulation) — Parallel physics on the GPU

A mass-spring cloth simulation with WGSL compute shaders, ping-pong state buffers and a separate render pipeline. Headless GPU tests check physical invariants; a benchmark documents throughput by grid size. Built as a parallel-programming learning project at ECAM.

**Rust · wgpu · WGSL · GPU compute**

[Architecture](https://github.com/DeharengOlivier/gpu-cloth-simulation#architecture) · [Performance measurements](https://github.com/DeharengOlivier/gpu-cloth-simulation#performance)

### [probative](https://github.com/DeharengOlivier/probative) — Reproducible technical evidence

An offline CLI that turns an npm-based Node.js repository into a Cyber Resilience Act technical evidence pack, including a dependency SBOM and source-linked findings. Evidence is tied to a commit and content digests. It runs no project scripts, has no runtime dependencies, and prepares evidence rather than claiming legal compliance.

**Node.js · supply-chain evidence · deterministic analysis**

[What it checks](https://github.com/DeharengOlivier/probative#what-it-does)

### [cubby](https://github.com/DeharengOlivier/cubby) — File automation with an undo path

A CLI and background agent that classifies files by extension, filename and document content. Moves are journaled and reversible; existing files are never overwritten. Includes previews, explanations, duplicate handling and installation diagnostics for macOS and Linux.

**Python · CLI / background services · filesystem safety**

[Safety guarantees](https://github.com/DeharengOlivier/cubby#safety-guarantees) · [Command reference](https://github.com/DeharengOlivier/cubby#command-reference)

## More public engineering projects

| Project | Engineering focus | Stack |
| --- | --- | --- |
| [Le Crible Politique](https://github.com/DeharengOlivier/crible-politique) | Explainable, deterministic political self-assessment for France and Belgium; published scoring, uncertainty intervals and browser-side computation. [Website](https://crible.eu). | TypeScript, Next.js, React |
| [lol-win-prediction](https://github.com/DeharengOlivier/lol-win-prediction) | Per-role XGBoost classification from **end-of-game** statistics; game-grouped splits, training-only feature selection, leakage checks and SHAP explanations. | Python, scikit-learn, XGBoost |
| [herdr-cockpit](https://github.com/DeharengOlivier/herdr-cockpit) | A WezTerm setup for AI coding agents, with project spaces, keyboard integration and a terminal dashboard for token usage and cost. | Lua, Python, shell |
| [simulateur-salaire-portage-france](https://github.com/DeharengOlivier/simulateur-salaire-portage-france) | Offline salary-scenario CLI and interactive terminal UI; decimal arithmetic, constrained target solving and payslip reconciliation. Estimates are separated from verified payslip totals. | Python, Decimal, curses |
| [real-estate-trading-game](https://github.com/DeharengOlivier/real-estate-trading-game) | An academic full-stack market simulation with server-side authorisation, a documented API and a containerised database/cache/web stack. | FastAPI, MongoDB, Redis, React, Docker |

## Products beyond the public repositories

Open source is one part of my work. I also develop web and mobile products through Aurelona and co-founded **ASBL SAVIKIDS EDUCATION**. These projects are at different stages of development; their public pages describe them in more detail.

| Product | What I work on |
| --- | --- |
| [Argustr](https://argustr.com) | Multi-agent financial analysis, with decisions evaluated later against market prices. LangGraph, FastAPI and Next.js. |
| [SaviKids](https://apps.aurelona.com/savikids) | Turning photographed schoolwork into personalised audio lessons, with content checks and a thin Flutter client. |
| [Aurelona Accounting](https://gestion.aurelona.com) | Accounting software built around the needs of Belgian non-profits. |
| [L'instant Clair](https://linstantclair.com) | An AI-assisted editorial workflow spanning scheduled publishing, a public site and an administration interface. |
| [Duet](https://apps.aurelona.com/duet) | A two-person daily question app whose pending state does not expose the other person's answer. Flutter and Dart. |
| [Ember](https://apps.aurelona.com/ember), [BlindBox](https://apps.aurelona.com/blindbox) & [Runf](https://apps.aurelona.com/runf) | Social and mobile applications, with shared API contracts across backend and client implementations. |
| L'Intrus & Amiable | An offline social-deduction game and a shared-expense register for separated parents. |
| [Chromatic Rush](https://apps.aurelona.com/chromatic-rush) & [Chess clock](https://apps.aurelona.com/chess-clock) | A Godot runner and a Flutter chess clock using monotonic time to handle interruptions. |

I also work on smaller game prototypes: **Alcyon, Foxfire and Eclat**.

[Product studio](https://apps.aurelona.com) · [High-level case studies](https://github.com/DeharengOlivier/case-studies)

## How I approach engineering

- **Make claims inspectable.** Publish the scoring formula, the captured bytes, the evaluation method or the benchmark setup alongside the implementation.
- **Test the boundary that matters.** Examples include held-out labels in ML, GPU state transitions, filesystem moves and server-side authorisation.
- **Design for failure and recovery.** Refusal paths, explicit errors, reversible operations and reproducible outputs matter as much as the happy path.
- **Own the whole path.** Work from data and backend contracts through the interface, packaging, deployment and diagnostics.

Alongside these projects, I work on client systems under confidentiality, particularly LLM applications, retrieval, evaluation and guardrails. The [case studies](https://github.com/DeharengOlivier/case-studies) describe the problems without exposing client code or internal details.

## Let's talk

For software engineering opportunities or a technical conversation about any of these projects: **[deharengolivier@gmail.com](mailto:deharengolivier@gmail.com)**.
