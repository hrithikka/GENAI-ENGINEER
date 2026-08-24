A full GenAI-engineer roadmap has a shared foundation through **Phase 4 or 5**. After that, you should choose a primary specialization based on the kind of systems you want to build: RAG/search, agents, LLM platform/LLMOps, applied ML/fine-tuning, multimodal AI, or AI product/backend engineering.

For you, the highest-leverage path is **RAG + agents + LLMOps**, because it builds directly on your Python, SQL, AWS, data pipelines, and prior RAG experience.

## Roadmap at a glance

```text
Phases 0–4: Shared foundation for every GenAI engineer
             ↓
Phase 5: Choose primary specialization
             ↓
Phase 6: Production engineering and portfolio
             ↓
Phase 7: Job-specific interview preparation and applications
```

| Phase | Focus | Choose a specialization yet? | Main output |
|---|---|---:|---|
| 0 | Computing and coding foundations | No | Small Python programs |
| 1 | Software engineering + data | No | Tested backend API |
| 2 | ML and LLM fundamentals | No | Classical ML project + LLM understanding |
| 3 | LLM application engineering | No | Structured-output AI application |
| 4 | RAG fundamentals + evaluation | No, but you can lean toward RAG | Citation-grounded RAG app |
| 5 | Specialization | **Yes** | Domain-focused advanced project |
| 6 | Production LLMOps and deployment | Keep your specialization | Production-grade capstone |
| 7 | Portfolio and interview prep | Target a job title | Resume, GitHub, system-design stories |

## Phase 0: Programming foundations

**Goal:** Become comfortable writing code independently.

Learn:
- Python syntax, functions, loops, collections, classes, exceptions.
- Files, JSON, CSV, environment variables.
- `pip`, virtual environments, dependency files.
- Git and GitHub: commit, branch, pull, merge, README.
- CLI and Linux fundamentals.

Build:
- CSV data cleaner.
- CLI expense tracker.
- Small API-data collector that saves normalized JSON or CSV.

**Do not specialize yet.** Every GenAI role requires basic programming fluency.

## Phase 1: Backend, databases, and engineering workflow

**Goal:** Learn how production applications are structured.

Learn:
- HTTP, REST APIs, status codes, request/response lifecycle.
- FastAPI, Pydantic, validation, error handling.
- PostgreSQL: tables, joins, indexes, transactions.
- Unit tests with `pytest`.
- Docker fundamentals.
- Logging, configuration, secrets management.
- Basic cloud deployment: AWS, GCP, or Azure.

Build:
- A FastAPI application with authentication basics, PostgreSQL persistence, tests, Docker, and deployed API documentation.

**Do not specialize yet.** This is the engineering layer used by all specializations.

## Phase 2: ML and LLM fundamentals

**Goal:** Know what models can and cannot do.

Learn conventional ML:
- Supervised vs. unsupervised learning.
- Train/validation/test splits.
- Overfitting, leakage, baseline models.
- Precision, recall, F1, accuracy, MAE, RMSE.
- Feature engineering and data preprocessing.
- scikit-learn workflows.

Learn LLM concepts:
- Tokens, context windows, embeddings, transformers, attention.
- Temperature and sampling.
- Hallucinations and grounding.
- Prompting, system instructions, few-shot examples.
- Fine-tuning vs. RAG vs. prompt engineering.
- Responsible-AI basics: bias, privacy, misuse, security.

The Hugging Face LLM course is a useful foundation for Transformers, tokenizers, datasets, inference, model training, and advanced LLM topics.[1]

Build:
- A ticket classifier, anomaly detector, or churn prediction model using scikit-learn.
- Document the dataset, baseline, metric, error analysis, and limitations.

**Do not specialize yet.** You need enough ML literacy to make sound choices, even if you later focus on applications rather than model training.

## Phase 3: LLM application engineering

**Goal:** Build reliable applications around models.

Learn:
- Calling model APIs from Python.
- System prompts, prompts, examples, model selection.
- Streaming, retries, timeouts, rate limits, and fallbacks.
- Token estimation, latency, and cost control.
- JSON/structured outputs and schema validation.
- Function/tool calling.
- Prompt-injection basics and input/output checks.
- Caching and asynchronous workloads.

Use schema-constrained output whenever an application needs to consume model data. Structured Outputs can enforce adherence to a supplied JSON Schema, which is much safer than parsing an unconstrained natural-language response.[2]

Build:
- Resume/job-description analysis service.
- Input: a resume and job description.
- Output: validated JSON: matched skills, missing skills, suggested resume edits, role fit, and limitations.
- Stack: FastAPI, Pydantic, PostgreSQL, LLM API, Docker.

**Still do not fully specialize.** At this point, you can explore one or two paths but should have the common toolkit first.

## Phase 4: RAG and evaluation

**Goal:** Ground model responses in trustworthy data.

Learn the end-to-end RAG pipeline:

```text
Data sources
  → extraction and cleaning
  → chunking and metadata
  → embeddings
  → vector index
  → retrieve / filter / rerank
  → LLM response using evidence
  → citations, evaluation, monitoring
```

Learn:
- PDF, HTML, Markdown, and database ingestion.
- Chunking strategies and metadata design.
- Embeddings and similarity search.
- PostgreSQL + pgvector as a strong first vector stack.
- Keyword, vector, and hybrid retrieval.
- Rerankers and context optimization.
- Citation-aware answers and refusal when evidence is insufficient.
- Evaluation: retrieval relevance, answer correctness, groundedness, faithfulness, latency, and cost.

RAG architecture commonly uses an embedding model for indexing/retrieval before supplying selected content to a generative model.[3]

Build:
- A cited documentation/policy assistant using public documents.
- Add 50–100 manually curated evaluation questions.
- Report baseline versus improved results after improving chunking, retrieval filters, or reranking.

### When can you choose?

You can choose a **primary specialization after Phase 4**.

Why not earlier? Before RAG and evaluation, you usually do not yet understand the core production failures of GenAI: retrieval misses, stale context, prompt injection, hallucinations, quality regressions, cost spikes, and weak observability.

You may explore earlier, but commit after Phase 4.

## Phase 5: Choose your specialization

Choose **one primary lane** and optionally one secondary lane. Learn the shared material first, then build a serious project aligned to the job title you want.

| Specialization | What you build | Deep skills | Typical titles | Best fit |
|---|---|---|---|---|
| RAG / AI search engineer | Knowledge assistants, enterprise search, document intelligence | Ingestion, chunking, hybrid search, pgvector/vector DBs, reranking, retrieval evaluation, citations, permissions | GenAI Engineer, RAG Engineer, Search Engineer, Applied AI Engineer | Data engineers, backend engineers |
| AI agents / agentic systems engineer | Tool-using assistants, workflow automation, operations copilots | Tool schemas, workflows, state, planning, approvals, retry logic, agent evaluation, tracing | AI Agent Engineer, GenAI Engineer, Applied AI Engineer | Backend, automation, platform engineers |
| LLMOps / AI platform engineer | Shared AI infrastructure for teams | Model gateways, deployment, observability, evaluation platforms, caching, cost controls, IAM, CI/CD | LLMOps Engineer, AI Platform Engineer, MLOps Engineer | DevOps, cloud, data-platform engineers |
| Applied ML / fine-tuning engineer | Custom models and domain adaptation | PyTorch, Transformers, datasets, fine-tuning/PEFT, GPUs, experiment tracking, model evaluation | Applied Scientist, ML Engineer, NLP Engineer | Strong ML/math-oriented engineers |
| Multimodal AI engineer | Vision-language, voice, OCR, image/video workflows | Vision, OCR, speech-to-text, multimodal prompts, image pipelines, model evaluation | Multimodal AI Engineer, Computer Vision Engineer | Vision, media, document-AI interests |
| AI backend/product engineer | User-facing AI products and copilots | UX for AI, backend systems, auth, streaming, tool integrations, experimentation, reliability | AI Engineer, Product Engineer—AI, Full-Stack AI Engineer | Full-stack/backend engineers |
| AI security / governance engineer | Safe and compliant AI systems | Threat modeling, prompt injection, PII controls, red teaming, access policies, auditability | AI Security Engineer, Responsible AI Engineer, AI Governance Engineer | Security/compliance-focused engineers |

### Specialization decision guide

| If you enjoy… | Choose… | Start specializing after… |
|---|---|---|
| SQL, document pipelines, data modeling, search relevance | RAG / AI search | Phase 4 |
| APIs, automation, workflows, practical task completion | Agents / agentic systems | Phase 4, ideally after solid RAG |
| Cloud, Docker, Kubernetes, CI/CD, monitoring, reliability | LLMOps / AI platform | Phase 3–4 |
| Training models, math, PyTorch, experiments | Applied ML / fine-tuning | Phase 2; commit after Phase 4 |
| Images, video, OCR, speech, document extraction | Multimodal AI | Phase 3–4 |
| Building polished user applications | AI product/backend | Phase 3 |
| Security, privacy, policy, risk reduction | AI security/governance | Phase 3–4 |

A practical rule: **do not specialize in agents until you can build and evaluate a deterministic RAG/tool workflow.** Agents are harder to debug because they add multi-step decision-making and tool interactions.

## Phase 6: Production engineering

**Goal:** Turn the Phase 5 project into a system an organization could responsibly operate.

Every specialization needs:
- Docker, CI/CD, automated unit/integration tests.
- Cloud deployment and infrastructure basics.
- IAM, secret management, least privilege, audit logging.
- Authentication and authorization.
- Tracing across user requests, LLM calls, retrieval, and tool calls.
- Latency, error, token, and cost monitoring.
- Evaluation data/versioning and regression gates.
- Human feedback and a process to turn real failures into test cases.
- Fallback behavior and graceful failure.

For agents in particular, trace the complete session, including LLM calls, tool inputs/outputs, retrieval behavior, context, state changes, and decision points. Production evaluation should cover output quality, tool use, goal completion, groundedness, latency, cost, and safety—not only whether the final text sounds good.[4][5]

### Capstone by specialization

| Lane | Production capstone |
|---|---|
| RAG / AI search | Role-aware enterprise knowledge assistant with hybrid search, reranking, citations, access-controlled retrieval, 100-question evaluation suite, and quality dashboard |
| AI agents | Data-quality incident investigation agent with read-only SQL tools, traceable analysis, approval gate before ticket creation, failure recovery, and tool-use evaluations |
| LLMOps / platform | Internal LLM gateway that supports model routing, prompt/version management, rate limits, caching, telemetry, evaluation runs, and cost dashboards |
| Applied ML / fine-tuning | Domain-specific classification or extraction model using PEFT, experiment tracking, offline/online evaluation, model registry, API serving, and monitoring |
| Multimodal | Invoice/document-processing platform combining OCR, vision-language extraction, human-review queue, confidence scoring, and data-validation checks |
| AI product/backend | Multi-tenant AI copilot with streaming, auth, user feedback, model fallbacks, analytics, and controlled tool integrations |
| AI security/governance | Secure RAG gateway with prompt-injection detection, sensitive-data redaction, document access enforcement, red-team suite, and audit dashboard |

## Phase 7: Job-ready portfolio and interviews

**Goal:** make your skills obvious to recruiters and hiring managers.

Have 2–3 projects:
- One broadly relevant RAG or LLM application.
- One project specific to your primary specialization.
- One production-quality project that proves deployment, evaluation, monitoring, and security.

Each project should include:
- Clear problem and business/user value.
- Architecture diagram.
- Public/synthetic data only.
- Setup documentation and `.env.example`.
- Tests and a reproducible evaluation dataset.
- Deployment details, cost/latency choices, and security design.
- Demo video or screenshots.
- Measured before/after result, not only feature lists.

Prepare to explain:
- RAG vs. fine-tuning and when to use each.
- Vector search, hybrid search, reranking, and chunking.
- How you evaluate groundedness and retrieval quality.
- How you handle prompt injection and access control.
- How agents choose tools and how you bound their authority.
- Tradeoffs across model quality, latency, availability, and cost.
- How you deploy, monitor, and roll back an AI application.

## Best specialization for you

Your recommended path is:

```text
Primary: RAG / AI Search Engineer
Secondary: AI Agents / Agentic Systems
Differentiator: LLMOps + data-engineering reliability
```

This fits your existing data pipelines, SQL, AWS, API, monitoring, and RAG background. It also targets broad job titles: **GenAI Engineer, AI Engineer, Applied AI Engineer, RAG Engineer, AI Solutions Engineer, and LLM Engineer**.

Your flagship capstone should be a **data-quality and operations copilot**: it ingests runbooks and data documentation, retrieves cited evidence, uses read-only SQL/log tools to investigate an incident, produces a structured root-cause report, and requires approval before any operational action. It demonstrates RAG, agents, SQL, APIs, cloud deployment, security, evaluation, and business value in one system.

Sources
[1] Introduction - Hugging Face https://huggingface.co/learn/llm-course/en/chapter3/1
[2] Structured model outputs | OpenAI API https://developers.openai.com/api/docs/guides/structured-outputs
[3] RAG infrastructure for generative AI using Agent Platform ... https://docs.cloud.google.com/architecture/rag-capable-gen-ai-app-using-vertex-ai
[4] Evaluating AI Agents in Production: Best Practices | Arthur https://www.arthur.ai/column/evaluating-ai-agents-in-production
[5] Agent evaluation: Complete guide to testing AI agents in March 2026 https://www.openlayer.com/blog/agent-evaluation-complete-guide-testing-ai-agents
[6] Quick Start https://react.dev/learn
[7] REST - Glossary - MDN Web Docs https://developer.mozilla.org/en-US/docs/Glossary/REST
[8] HTTP request methods - MDN Web Docs https://developer.mozilla.org/en-US/docs/Web/HTTP/Reference/Methods
[9] Which Is the Best Python Web Framework: Django, Flask ... https://blog.jetbrains.com/pycharm/2025/02/django-flask-fastapi/
[10] API - Glossary - MDN Web Docs https://developer.mozilla.org/en-US/docs/Glossary/API
[11] React https://react.dev/
[12] HTTP: Hypertext Transfer Protocol - MDN Web Docs https://developer.mozilla.org/en-US/docs/Web/HTTP
[13] Top Python Web Development Frameworks in 2025 https://reflex.dev/blog/python-comparison
[14] JavaScript frameworks and libraries - Learn web development | MDN https://developer.mozilla.org/en-US/docs/Learn_web_development/Core/Frameworks_libraries
[15] Web APIs - MDN Web Docs - Mozilla https://developer.mozilla.org/en-US/docs/Web/API
[16] FastAPI - FastAPI https://fastapi.tiangolo.com/
[17] Comparing Django, Flask, and FastAPI | PDF https://www.scribd.com/presentation/898031459/Web-Lessons
[18] Angular vs React vs Vue : Which to choose for your career ... https://dev.to/danmugh/angular-vs-react-vs-vue-which-to-choose-for-your-career-as-a-ui-developer-283i
[19] React, Angular, Vue: What they can do and which one is for you https://blog.teamtreehouse.com/react-angular-vue
[20] Best Python API Frameworks: FastAPI vs Flask https://uvik.net/blog/python-api-framework/
[21] Angular vs React vs Vue: Detailed Framework Comparison - TinyMCE https://www.tiny.cloud/blog/vue-react-angular-js-framework-comparison/
[22] Understanding REST, gRPC, GraphQL, and OpenAPI to build your ... https://www.koyeb.com/blog/understanding-rest-grpc-graphql-and-openapi-to-build-your-apis
[23] How to choose between REST vs. GraphQL vs. gRPC vs. SOAP https://blog.postman.com/how-to-choose-between-rest-vs-graphql-vs-grpc-vs-soap/
[24] React vs. Angular vs. Vue: A Practical Comparison for 2026 https://www.ascendientlearning.com/blog/comparing-angular-react-vue-svelte
[25] API Architecture Styles: REST, gRPC, GraphQL, WebSockets, MQTT https://www.linkedin.com/posts/nikkisiapno_6-api-architecture-styles-you-should-know-activity-7409580763152838656-AHrM
[26] Comparing Angular, React, and Vue | PDF | Java Script - Scribd https://www.scribd.com/document/870666731/JavaScript-Frameworks-Angular-vs-React-vs-Vue
[27] Angular vs React vs Vue.js: A Comparative Study - 2022 - Zartis https://www.zartis.com/angular-vs-react-vs-vuejs/
[28] API architecture showdown - Rest vs graphQL vs gRPC https://pradeepl.com/blog/api/rest-vs-graphql-vs-grpc/
[29] Exploring API Architecture Styles: REST, GraphQL, SOAP, and Beyond https://www.solwey.com/blog/exploring-api-architecture-styles-rest-graphql-soap-and-beyond
[30] Master Generative AI Evaluation: From Single Prompts ... https://cloud.google.com/blog/topics/developers-practitioners/master-generative-ai-evaluation-from-single-prompts-to-complex-agents
[31] RAG Engine on Gemini Enterprise Agent Platform overview https://docs.cloud.google.com/gemini-enterprise-agent-platform/build/rag-engine/rag-overview
[32] Building Agents with Retrieval-Augmented Generation https://codelabs.developers.google.com/codelabs/production-ready-ai-with-gc/7-advanced-agent-capabilities/building-agents-with-retrieval-augmented-generation
[33] New tools for building agents | OpenAI https://openai.com/index/new-tools-for-building-agents/
[34] Fine-Tuning Transformers with Hugging Face - Coursera https://www.coursera.org/learn/fine-tuning-transformers-with-hugging-face
[35] The Complete Guide to Evaluating AI Agents in Production https://latitude.so/blog/complete-guide-evaluating-ai-agents-production
[36] Mastering Production RAG with Google ADK and Arize AX ... https://arize.com/blog/mastering-production-rag-with-google-adk-and-arize-ax-for-enterprise-knowledge-systems/
[37] How to Fine-Tune an LLM from Hugging Face - GeeksforGeeks https://www.geeksforgeeks.org/deep-learning/how-to-fine-tune-an-llm-from-hugging-face/