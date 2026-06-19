# Olivier Dehareng

**Computer Engineer, from prototype to production.**

I am a dual-trained computer engineer specialised in AI and business engineer specialised in finance. That combination means I can take a vague, high-value problem, design the system behind it, and own it from prototype to a tool people actually rely on. I work mostly with LLMs (retrieval, agents, evaluations, guardrails) and full-stack engineering, with a strong pull toward finance and regulated environments, where getting AI to behave well is hardest and matters most.

This page collects what I build, both open source and my own products.

## Open source

Public on GitHub. Each project exists to sharpen or prove a specific engineering skill.

**[rag-engine](https://github.com/DeharengOlivier/rag-engine)**
A Retrieval-Augmented Generation engine built from scratch. The point I wanted to make is that the hard part of RAG is not retrieval, it is trust. So it ships with grounding guardrails (it refuses when it lacks context and always cites its sources) and an evaluation harness that measures retrieval quality, the two things that decide whether an AI assistant over private knowledge can be relied on. It runs fully offline by default and lets you plug in real embedding and LLM providers when you want them.
Built with Python and numpy, with optional sentence-transformers and Anthropic or OpenAI providers.

**[lol-win-prediction](https://github.com/DeharengOlivier/lol-win-prediction)**
A machine-learning project that predicts the outcome of a League of Legends match from a single player's statistics, and explains which factors drive the result. I built it to practice doing ML correctly rather than optimistically. It handles data leakage explicitly, splits by game so opponents never straddle train and test, and reports ROC-AUC and F1 (around 0.96 AUC per role) instead of accuracy alone.
Built with Python, scikit-learn, XGBoost and SHAP.

**[real-estate-trading-game](https://github.com/DeharengOlivier/real-estate-trading-game)**
A full-stack real-estate trading game with an economic market simulation, a documented API and a web client. It was my way to design a real NoSQL data model and a small live market end to end, fully containerized so the whole stack starts with one command.
Built with FastAPI, MongoDB, Redis, React and Docker.

**[gpu-cloth-simulation](https://github.com/DeharengOlivier/gpu-cloth-simulation)**
A real-time cloth simulation whose physics runs entirely on the GPU. I built it to get hands-on with parallel programming and low-level graphics, integrating a mass-spring model in a compute shader and rendering it live.
Built with Rust, wgpu and WGSL.

## Products I am building (not open source)

The code stays private, but the products are live and I keep detailed technical write-ups of each in my [case-studies](https://github.com/DeharengOlivier/case-studies) repo.

**[Argustr](https://argustr.com)**
A multi-agent AI system for financial markets. Instead of a black-box buy or sell signal it produces structured, auditable reasoning, with explicit assumptions, conviction levels and a traceable logic path. The bet behind it is that in finance transparency drives adoption more than raw accuracy does. [Technical write-up.](https://github.com/DeharengOlivier/case-studies/blob/main/argustr.md)

**[L'Instant Clair](https://linstantclair.com)**
A French news platform designed to be run end to end by AI. Language models analyze and enrich each story through transparent pipelines, and a human layer adds methodology and editorial judgment. The objective is to rethink the economics of media with AI-augmented, transparent journalism. [Technical write-up.](https://github.com/DeharengOlivier/case-studies/blob/main/linstant-clair.md)

**[SaviKids](https://savikids.com)**
An edtech I am co-founding that turns lessons into personalised, AI-generated stories for children with dyslexia, ADHD or anxiety, with tutoring and gamification. The goal is to make learning genuinely accessible and engaging for neurodivergent kids. [Technical write-up.](https://github.com/DeharengOlivier/case-studies/blob/main/savikids.md)

**Aurelona**
My AI consulting and delivery practice. I scope, build, deploy and hand over AI solutions for small companies and a startup, owning both the engineering and the adoption rather than dropping a prototype and leaving. [Technical write-up.](https://github.com/DeharengOlivier/case-studies/blob/main/aurelona.md)

## Now

I am a Software Engineer at Innpact SA in Luxembourg, where I take LLM systems from idea to production and lead their adoption in a regulated financial setting. I also lead SaviKids, the edtech I am co-founding.

## Reach me

Portfolio at [olivierdehareng.com](https://olivierdehareng.com)
LinkedIn at [linkedin.com/in/deharengolivier](https://linkedin.com/in/deharengolivier)
Email at deharengolivier@gmail.com
