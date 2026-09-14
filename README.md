# Olivier Dehareng

Engineer, focused on computer science and finance. I run a small company, [Aurelona](https://aurelona.com), under which I build and operate my own products. Most of that work is closed source; the open-source part is at the bottom of this page.

## Aurelona

Aurelona is the company behind everything below. It has three branches.

**Aurelona Digital**, at [aurelona.com](https://aurelona.com). Services for businesses: websites, applications, quotes and delivery.

**Aurelona Accounting**, at [accounting.aurelona.com](https://accounting.aurelona.com). Accounting software for Belgian non-profits (ASBL), built around the obligations these organisations actually have rather than a generic ledger. Free tier, a paid tier at 19 EUR, quotes above that.

**Aurelona Development**. The products I build and run myself, listed next.

## Products

**Argustr**, at [argustr.com](https://argustr.com)
Decision support for financial markets. A team of specialised AI agents analyses a listed asset (equities, indices, crypto, currencies) the way an analysis desk would: data collection, adversarial debate, argued decision. The part that matters most comes after. Every call is verified later against real market prices and the system publishes its own track record, wins and losses alike. Multi-agent engine on LangGraph with a deterministic verification layer, FastAPI backend, Next.js front end.

**SaviKids**, at [savikids.com](https://savikids.com)
A child photographs a page of their exercise book and the app turns it into a personalised, audio-first lesson adapted to how that child learns (dyslexia, ADHD, dyscalculia, anxiety and more). The mobile app is deliberately thin; the backend reads the photo, writes the lesson, checks it is correct and safe, and voices it. French, Bulgarian and English. Built by the Belgian non-profit ASBL SAVIKIDS EDUCATION, which I co-founded in 2026. Flutter app, contract-first OpenAPI backend, Next.js site.

**L'instant Clair**, at [linstantclair.com](https://linstantclair.com)
An editorial media augmented by AI: a publishing loop that runs on a schedule with language models, with a public site, a back office and a business edition. Express and Prisma backend, SolidStart site, Next.js admin, shared Zod contracts, Playwright end-to-end tests.

**Duet**
One envelope a day, for two people. Each answers on their own side without seeing anything, and when both have answered everything opens at once. The central guarantee, that you cannot see the other's answer before giving yours, is not a check on top of the code: it is a type. The pending state has no field where the other answer could live. Flutter and Dart.

**L'Intrus**
A local social-deduction game for 3 to 15 players on a single phone. No account, no connection, no data leaving the device. Each player gets a secret word, one or two get a different one, and the Shadow gets none. Five game modes, 4,156 original word pairs in French and English, characters generated in 3D from a first name, in-app purchases on Apple and Google, remote content signed with Ed25519. Playable end to end, validated on iOS and Android.

**Le Crible Politique**, at [crible.eu](https://crible.eu), source [here](https://github.com/DeharengOlivier/crible-politique)
A political self-assessment tool for France and Belgium. You answer statements and it computes your proximity to each party, explained statement by statement, with a deterministic published formula, no AI at runtime, no account and no server storage. For something as sensitive as politics, a transparent and reproducible method beats a black box. Next.js, React and TypeScript.

**Ember**, at [embersocial.app](https://www.embersocial.app)
A social network for emotional sharing. Every post answers a question: a shared question of the day, a thematic catalogue, questions proposed by members, and questions composed for you from your own answers. Memories are kept in time capsules. Fastify backend, TanStack web, Flutter mobile, all derived from one OpenAPI contract.

**BlindBox**
Personality-first dating. One person a week, chosen by a compatibility questionnaire. Their photo arrives 95 percent blurred and unblurs only when both people have written six more messages. A monologue reveals nothing. Same technical foundation as Ember.

**Runf**
Meeting people through running. Dart backend with PostGIS, Flutter mobile, all derived from an OpenAPI contract.

**Amiable**
A shared-expense register for separated parents. Each expense is recorded with its date, amount, receipt and the split rule that applies, and the app produces a statement meant to hold up between the two. React Native mobile.

**Mobile games**
Simple games with one mechanic and a short loop, built on Godot 4 or Flutter: Alcyon (vertical ascent), Chromatic Rush (3D endless runner, six worlds, offline), Foxfire (an infinite sliding game from misty dawn to bioluminescent night), Eclat (on-rails 3D with procedural glass breaking) and a two-player chess clock that needs no account.

## Open source

Each project exists to sharpen or prove a specific engineering skill.

**[down-the-stack](https://github.com/DeharengOlivier/down-the-stack)**
One real web request, followed from the keystroke to the radio wave. An interactive 3D simulation of a captured HTTPS page load, decoded byte by byte, down to the 802.11 waveform and back up the other side. Every byte on screen comes from a real packet capture that ships with the repository, the protocol encoders are tested to reproduce it byte for byte, and the TLS records are genuinely decrypted in the browser rather than faked. English and French. This is the first module of a larger project: hyper-visual, rigorous simulations to let anyone understand computing by seeing it run.
Built with TypeScript and Three.js.

**[probative](https://github.com/DeharengOlivier/probative)**
Turns a repository into a Cyber Resilience Act (EU 2024/2847) evidence pack. Deterministic, offline, zero dependencies. It prepares the technical evidence and cites the Official Journal text article by article, and it deliberately states no legal conclusion about compliance and no overall score. It also ships as a Claude Code skill, so an agent can build the evidence pack for the repository it is working in.
Built with Node.js, standard library only.

**[rag-engine](https://github.com/DeharengOlivier/rag-engine)**
A Retrieval-Augmented Generation engine built from scratch. The point I wanted to make is that the hard part of RAG is not retrieval, it is trust. So it ships with grounding guardrails (it refuses when it lacks context and always cites its sources), an evaluation harness that measures retrieval quality, and PII anonymisation that strips personal data before anything is indexed. It runs fully offline by default and lets you plug in real embedding and LLM providers, or Microsoft Presidio, when you want them.
Built with Python and numpy, with optional sentence-transformers, Anthropic or OpenAI providers, and Presidio.

**[cubby](https://github.com/DeharengOlivier/cubby)**
A command-line tool that keeps a Downloads folder tidy on its own, filing each new file through a three-stage cascade: it reads the filename first, peeks inside the content when the name is uninformative (a UUID-named PDF still lands in Invoices), and falls back to the file type last. The domain is pure, the classification engine has zero IO and is driven by an injected text-extraction port, with a background agent on launchd or systemd. Fully tested, including a fuzz pass that proves the engine is total over arbitrary input.
Built with Python (standard library only at runtime), packaged as a pip-installable CLI.

**[herdr-cockpit](https://github.com/DeharengOlivier/herdr-cockpit)**
A WezTerm configuration that turns the terminal into a dedicated cockpit for AI coding agents, driven by Herdr. Self-contained, MIT licensed.

**[lol-win-prediction](https://github.com/DeharengOlivier/lol-win-prediction)**
Predicts the outcome of a League of Legends match from a single player's statistics, and explains which factors drive the result. It handles data leakage explicitly, splits by game so opponents never straddle train and test, and reports ROC-AUC and F1 (around 0.96 AUC per role) instead of accuracy alone.
Built with Python, scikit-learn, XGBoost and SHAP.

**[gpu-cloth-simulation](https://github.com/DeharengOlivier/gpu-cloth-simulation)**
A real-time cloth simulation whose physics runs entirely on the GPU: a mass-spring model integrated in a compute shader and rendered live.
Built with Rust, wgpu and WGSL.

**[real-estate-trading-game](https://github.com/DeharengOlivier/real-estate-trading-game)**
A full-stack real-estate trading game with an economic market simulation, a documented API and a web client, fully containerised so the whole stack starts with one command.
Built with FastAPI, MongoDB, Redis, React and Docker.

**[case-studies](https://github.com/DeharengOlivier/case-studies)**
Short write-ups of work I do not open source: adaptive learning, decision support scored against reality, automated editorial, consulting practice and engineering under confidentiality. No client names, no architecture, no code.

## Beyond this page

Alongside my own products I do delivery work covered by confidentiality, mostly taking LLM systems from a first prototype to something people depend on daily, with the retrieval, evaluation and guardrail work that decides whether they can be trusted at all. Happy to walk through any of it in a conversation.

## Reach me

Portfolio at [olivierdehareng.com](https://olivierdehareng.com)
LinkedIn at [linkedin.com/in/deharengolivier](https://linkedin.com/in/deharengolivier)
Email at deharengolivier@gmail.com
