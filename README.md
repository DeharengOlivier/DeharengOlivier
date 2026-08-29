# Olivier Dehareng

Engineer, focused on computer science and finance. The vast majority of my work is not open source.

## Open source

Ordered most-substantial first. Each project exists to sharpen or prove a specific engineering skill.

**[rag-engine](https://github.com/DeharengOlivier/rag-engine)**
A Retrieval-Augmented Generation engine built from scratch. The point I wanted to make is that the hard part of RAG is not retrieval, it is trust. So it ships with grounding guardrails (it refuses when it lacks context and always cites its sources), an evaluation harness that measures retrieval quality, and PII anonymization that strips personal data before anything is indexed, the things that decide whether an AI assistant over private knowledge can be relied on in a regulated setting. It runs fully offline by default and lets you plug in real embedding and LLM providers, or Microsoft Presidio, when you want them.
Built with Python and numpy, with optional sentence-transformers, Anthropic or OpenAI providers, and Presidio.

**[cubby](https://github.com/DeharengOlivier/cubby)**
A command-line tool that keeps a Downloads folder tidy on its own, filing each new file through a three-stage cascade: it reads the filename first, peeks inside the content when the name is uninformative (a UUID-named PDF still lands in Invoices), and falls back to the file type last. I built it to practice clean, layered architecture in the small. The domain is pure, the classification engine has zero IO and is driven by an injected text-extraction port, with use-case and adapter layers around it and a background agent that runs on launchd or systemd. It is fully tested, including a fuzz pass that proves the engine is total over arbitrary input, and ships a one-command installer.
Built with Python (standard library only at runtime), packaged as a pip-installable CLI.

**[lol-win-prediction](https://github.com/DeharengOlivier/lol-win-prediction)**
A machine-learning project that predicts the outcome of a League of Legends match from a single player's statistics, and explains which factors drive the result. I built it to practice doing ML correctly rather than optimistically. It handles data leakage explicitly, splits by game so opponents never straddle train and test, and reports ROC-AUC and F1 (around 0.96 AUC per role) instead of accuracy alone.
Built with Python, scikit-learn, XGBoost and SHAP.

**[gpu-cloth-simulation](https://github.com/DeharengOlivier/gpu-cloth-simulation)**
A real-time cloth simulation whose physics runs entirely on the GPU. I built it to get hands-on with parallel programming and low-level graphics, integrating a mass-spring model in a compute shader and rendering it live.
Built with Rust, wgpu and WGSL.

**[crible-politique](https://github.com/DeharengOlivier/crible-politique)**
Le Crible Politique, a political self-assessment tool for France and Belgium. You answer statements and it computes your proximity to each party, explained statement by statement, with a deterministic published formula, no AI at runtime, no account and no server storage. I built it to show that for something as sensitive as politics a transparent, reproducible method beats a black box.
Built with Next.js, React and TypeScript.

**[real-estate-trading-game](https://github.com/DeharengOlivier/real-estate-trading-game)**
A full-stack real-estate trading game with an economic market simulation, a documented API and a web client. It was my way to design a real NoSQL data model and a small live market end to end, fully containerized so the whole stack starts with one command.
Built with FastAPI, MongoDB, Redis, React and Docker.

## Beyond this page

Most of what I build is closed source: products I run end to end, and delivery work covered by confidentiality. The engineering is the same across all of it, taking an LLM system from a first prototype to something people depend on daily, with the retrieval, evaluation and guardrail work that decides whether it can be trusted at all. Happy to walk through any of it in a conversation.

## Reach me

Portfolio at [olivierdehareng.com](https://olivierdehareng.com)
LinkedIn at [linkedin.com/in/deharengolivier](https://linkedin.com/in/deharengolivier)
Email at deharengolivier@gmail.com
