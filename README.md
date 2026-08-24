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

Phase 0 is your **developer foundation phase**. Its purpose is not to learn GenAI yet—it is to make you fully comfortable building small Python programs, using a terminal, managing code with Git, and creating clean project repositories.

For a complete beginner, expect **4–8 weeks** at 10–15 hours/week. For someone who already knows Python, you can use this as a gap checklist and finish it in 1–2 weeks.

## Phase 0 outcomes

By the end, you should be able to:

- Create a Python project from scratch with a virtual environment.
- Write readable Python programs with functions, classes, files, errors, and tests.
- Run a command-line tool with options such as `--input`, `--output`, and `--verbose`.
- Use Git branches, commits, pull requests, and `.gitignore`.
- Navigate Linux/macOS terminal environments and manage files safely.
- Keep secrets out of GitHub.
- Publish two or three small but clean GitHub projects.

GitHub’s core workflow includes repositories, branches, commits, and pull requests; branches let you develop features without changing the main codebase until you are ready to merge.[1][2]

## 0.1 Development environment

### Install and configure

Learn to install and verify:

- Python 3.x.
- VS Code or PyCharm Community Edition.
- Git.
- A terminal: macOS Terminal, Windows PowerShell/Windows Terminal, or Linux shell.
- Docker is optional in Phase 0; install it, but learn it in Phase 1.
- A GitHub account.
- PostgreSQL is optional until Phase 1.

Run and understand:

```bash
python --version
pip --version
git --version
```

On some systems, use `python3` and `pip3`.

### Editor setup

Configure your IDE for:

- Python extension/language server.
- Formatter: Ruff formatter or Black.
- Linter: Ruff.
- Debugger and breakpoints.
- Git integration.
- File explorer and terminal.
- Python interpreter selection.
- `.env` file exclusion from Git.

### Project folder layout

Start every project with a predictable layout:

```text
my_project/
├── README.md
├── .gitignore
├── requirements.txt
├── .env.example
├── src/
│   └── main.py
├── tests/
│   └── test_main.py
├── data/
│   └── sample_data.csv
└── docs/
```

Understand the purpose of each:
- `README.md`: problem, installation, usage, examples, design decisions.
- `.gitignore`: files Git must not track.
- `requirements.txt`: project dependencies.
- `.env.example`: names of required environment variables, never real values.
- `src/`: application source code.
- `tests/`: automated tests.
- `data/`: small public or synthetic test data only.
- `docs/`: diagrams, notes, or examples.

### Virtual environments and dependencies

Learn:

```bash
python -m venv .venv
source .venv/bin/activate       # macOS/Linux
.venv\Scripts\activate          # Windows PowerShell

python -m pip install requests
python -m pip freeze > requirements.txt
python -m pip install -r requirements.txt
```

Understand:
- Why each project needs an isolated environment.
- Global packages versus project packages.
- Why `python -m pip` is safer than invoking a random `pip`.
- Dependency version pinning.
- How to deactivate a virtual environment.

### Configuration and secrets

Learn:
- What API keys, credentials, tokens, and environment variables are.
- `.env` files and why they must not be committed.
- `os.getenv("VARIABLE_NAME")`.
- Safe defaults and meaningful configuration errors.
- `.env.example` with placeholders only.

Example:

```text
# .env.example
APP_ENV=development
API_KEY=replace_with_your_key
```

```python
import os

api_key = os.getenv("API_KEY")
if not api_key:
    raise RuntimeError("API_KEY is required. Set it in your environment.")
```

Environment variables are commonly read from `os.environ`; command-line settings can be supplied through `argparse`, and JSON/YAML files are also used for configuration.[3]

## 0.2 Python fundamentals

### Syntax and basic data types

Master:
- Variables and assignment.
- Naming conventions: `snake_case`, `PascalCase`, constants in `UPPER_CASE`.
- Comments and docstrings.
- `int`, `float`, `str`, `bool`, `None`.
- Type conversion: `int()`, `float()`, `str()`, `bool()`.
- Comparison operators: `==`, `!=`, `<`, `>`, `<=`, `>=`.
- Boolean operators: `and`, `or`, `not`.
- Truthy and falsy values.
- Operator precedence.
- `is` versus `==`.

Practice:
- Parse `"42"` to an integer.
- Validate a user’s age or score.
- Check whether an optional variable is `None`.
- Format a message using f-strings.

### Strings

Learn:
- Indexing and slicing.
- Immutability.
- Methods: `.lower()`, `.upper()`, `.strip()`, `.split()`, `.join()`, `.replace()`, `.find()`.
- f-strings.
- Multiline strings.
- Escaping quotes and newline characters.
- Basic regular expressions with `re`.

Practice:
- Normalize names, emails, and phone-number-like strings.
- Extract order IDs from text.
- Build a simple log-line parser.

### Collections

#### Lists

Learn:
- Creation, indexing, slicing.
- `.append()`, `.extend()`, `.insert()`, `.remove()`, `.pop()`, `.sort()`.
- Iteration.
- List comprehensions.
- Copying versus referencing.
- Nested lists.

#### Tuples

Learn:
- Immutability.
- Packing/unpacking.
- When a tuple is preferable to a list.

#### Dictionaries

Learn:
- Keys, values, items.
- `.get()`, `.keys()`, `.values()`, `.items()`.
- Adding, updating, deleting.
- Nested dictionaries.
- Dictionary comprehensions.
- Avoiding `KeyError`.

#### Sets

Learn:
- Unique values.
- Set operations: union, intersection, difference.
- Membership checks.

Practice:
- Count word frequencies with a dictionary.
- Remove duplicates with a set.
- Convert raw CSV-style rows into dictionaries.
- Group transactions by category.

### Control flow

Master:
- `if`, `elif`, `else`.
- Nested conditions.
- `match/case` basics if using modern Python.
- `for` loops.
- `while` loops.
- `break`, `continue`, `pass`.
- `range()`.
- `enumerate()`.
- `zip()`.
- Iterating through dicts and nested data.

Practice:
- Validate a list of records and separate valid/invalid entries.
- Build a menu-driven CLI program.
- Calculate summary statistics from a list of numbers.

### Functions

Learn:
- Defining and calling functions.
- Positional and keyword arguments.
- Default values.
- `*args` and `**kwargs`.
- Return values.
- Scope: local, global, nonlocal.
- Pure functions and side effects.
- Docstrings.
- Type hints.

Example:

```python
def calculate_total(prices: list[float], tax_rate: float = 0.0) -> float:
    subtotal = sum(prices)
    return subtotal * (1 + tax_rate)
```

Practice:
- Break a 100-line script into small functions.
- Write functions that validate input and return useful error messages.
- Add type hints and docstrings to every public function.

### Errors and exceptions

Learn:
- Syntax errors versus runtime errors versus logical errors.
- `try`, `except`, `else`, `finally`.
- Common exceptions: `ValueError`, `TypeError`, `KeyError`, `IndexError`, `FileNotFoundError`.
- Raising exceptions deliberately with `raise`.
- Creating custom exceptions only after you understand built-ins.
- Never using bare `except:` unless you intentionally re-raise.

Example:

```python
def parse_positive_integer(value: str) -> int:
    try:
        result = int(value)
    except ValueError as exc:
        raise ValueError(f"Expected an integer, got {value!r}") from exc

    if result <= 0:
        raise ValueError("Value must be positive")

    return result
```

Practice:
- Read a CSV file and handle missing files.
- Safely parse numeric fields with invalid values.
- Return a helpful error instead of crashing.

### Modules and packages

Learn:
- `import module`.
- `from module import function`.
- Standard library versus third-party packages.
- Creating your own modules.
- `__name__ == "__main__"`.
- Package folders and `__init__.py` at a conceptual level.
- Avoiding circular imports.

Example:

```python
if __name__ == "__main__":
    main()
```

### Object-oriented programming

You do not need advanced design patterns in Phase 0. Cover:

- Classes and objects.
- Instance attributes and methods.
- Constructors: `__init__`.
- Class attributes versus instance attributes.
- Inheritance at a basic level.
- Composition: one class containing/using another.
- `@dataclass`.
- `__repr__` conceptually.

Example:

```python
from dataclasses import dataclass

@dataclass
class Document:
    title: str
    content: str
    source: str

    def word_count(self) -> int:
        return len(self.content.split())
```

Practice:
- Create `Expense`, `Task`, or `Document` classes.
- Prefer small data classes and functions over unnecessary inheritance.

### Pythonic style

Learn:
- PEP 8 conventions.
- Meaningful names.
- Small single-purpose functions.
- Avoid deeply nested code.
- Early returns.
- Comprehensions when they remain readable.
- `with` statements for files/resources.
- `pathlib.Path` instead of manually concatenating file paths.
- Basic logging with Python’s `logging` module instead of only `print()`.

## 0.3 Files, formats, and data basics

### File paths and file operations

Learn:
- Relative vs. absolute paths.
- Current working directory.
- `pathlib.Path`.
- Read, write, append modes.
- Text encoding, especially UTF-8.
- The `with open(...)` pattern.

```python
from pathlib import Path

path = Path("data") / "notes.txt"
text = path.read_text(encoding="utf-8")
```

### CSV

Learn:
- CSV rows, headers, delimiters, quoting.
- Python `csv` module.
- Introductory Pandas: `read_csv`, `head`, `info`, `shape`, `columns`, filtering, missing values, `to_csv`.
- Data type mistakes and null values.
- Validating input columns.

### JSON

Learn:
- JSON objects, arrays, strings, numbers, booleans, and null.
- Python dictionary/list mapping.
- `json.load`, `json.loads`, `json.dump`, `json.dumps`.
- Pretty printing.
- JSON parsing errors.
- Basic nested JSON traversal.

```python
import json
from pathlib import Path

records = json.loads(Path("data/records.json").read_text())
```

### Other useful formats

Know at a high level:
- YAML: readable configuration; be cautious with unsafe loaders.
- `.env`: key-value configuration variables.
- Markdown: documentation format for GitHub.
- HTML: basic structure only; useful later for web scraping and frontends.
- Parquet: efficient analytics storage; learn seriously during data/ML phases.

### Data cleaning basics

Learn:
- Missing values.
- Duplicate records.
- Type conversion.
- Whitespace normalization.
- Date parsing.
- Simple validation rules.
- Basic summary statistics: count, min, max, mean, median.
- Data-quality reporting.

Build:
- A CLI tool that takes a CSV file, validates expected columns, removes duplicates, normalizes text fields, reports invalid records, and writes cleaned data plus a JSON summary report.

## 0.4 Terminal and Linux fundamentals

You do not need Linux administration yet. You need enough fluency to develop, debug, and deploy applications.

### Shell concepts

Understand:
- Shell versus terminal versus command prompt.
- Working directory.
- Absolute and relative paths.
- Files versus directories.
- Hidden files such as `.env` and `.gitignore`.
- Quoting: `'...'` vs. `"..."`.
- Exit codes: success is commonly `0`.
- Standard input, output, and error.

### Navigation and files

Practice until automatic:

```bash
pwd
ls
ls -la
cd folder_name
cd ..
mkdir project_name
touch file.txt
cp source.txt copy.txt
mv old_name.txt new_name.txt
rm file.txt
rm -r folder_name
cat file.txt
less file.txt
head file.txt
tail file.txt
```

Basic navigation, creation, copying, moving, and file listing are core command-line skills; `man command_name` opens local manual documentation for commands.[4]

### Search, text processing, and redirection

Learn:

```bash
grep "ERROR" app.log
grep -r "API_KEY" .
find . -name "*.py"
wc -l data.csv
sort names.txt
uniq names.txt
command > output.txt
command >> output.txt
command 2> errors.txt
command1 | command2
```

Understand:
- Pipes `|`.
- Redirection: `>`, `>>`, `2>`.
- Globs: `*.py`, `data/*.csv`.
- Why `rm -rf` is dangerous.
- How to inspect before deleting.

### Processes and networking basics

Learn:

```bash
ps
ps aux
top
kill PID
curl http://localhost:8000
curl -X POST ...
```

Understand:
- Process ID (PID).
- Foreground vs. background process.
- Ports and localhost.
- Why “address already in use” happens.
- How to stop a local server safely.

### Permissions

Learn:
- Read/write/execute permissions.
- User/group/other.
- `ls -l`.
- `chmod`.
- The idea of ownership with `chown`—do not use it broadly unless you understand it.

Linux permissions determine who may read, write, or execute files and directories; `ls -l` displays permission metadata, while `chmod` changes permissions.[5]

Practice:

```bash
chmod +x script.sh
chmod 600 .env
```

## 0.5 Git and GitHub

### Git concepts

Understand:
- Working directory.
- Staging area.
- Local repository.
- Remote repository.
- Commit history.
- Branch.
- Merge.
- Pull request.
- Merge conflict.
- `.gitignore`.

### Daily commands

Practice these until comfortable:

```bash
git init
git status
git add .
git add path/to/file.py
git commit -m "Add CSV validation"
git log --oneline
git diff
git branch
git switch -c feature/add-report
git switch main
git merge feature/add-report
git remote add origin <repository-url>
git push -u origin main
git pull
git clone <repository-url>
```

### Proper commit habits

Make small commits with meaningful messages:

```text
Add CSV input validation
Handle malformed JSON records
Add unit tests for duplicate removal
Document local setup
```

Avoid:

```text
updates
fix
final final 2
all changes
```

### Branch and pull-request workflow

For every nontrivial feature:

```text
main
  ↓
feature/clean-csv
  ↓
make focused commits
  ↓
push branch
  ↓
open pull request
  ↓
review diff
  ↓
merge into main
```

Practice opening pull requests even for solo work. GitHub’s beginner material specifically covers creating a branch, committing a change, opening a pull request, merging it, and deleting the finished branch.[6]

### Merge conflicts

Learn:
- Why conflicts occur.
- How to inspect conflict markers.
- How to choose or combine the correct code.
- How to test after resolving.
- How to abort a merge if needed.

### GitHub repository quality

Each repository should have:
- Clear name: `csv-data-cleaner`, not `project1`.
- Useful README.
- `.gitignore`.
- License if you wish to make reuse terms clear.
- Issues for tasks/bugs.
- Clean commit history.
- No credentials, databases, `.venv`, logs, or large generated outputs.

### Absolute security rule

Never commit:
- `.env`
- API keys
- AWS credentials
- database passwords
- access tokens
- private datasets
- employer documents
- customer data

If you accidentally publish a secret, revoke/rotate it immediately; deleting the file afterward does not necessarily remove it from Git history.

## 0.6 Testing, debugging, and code quality

### Debugging skills

Learn:
- Read the full traceback from bottom to top.
- Reproduce the failure with the smallest input.
- Use `print()` temporarily, then remove it.
- Use your IDE debugger and breakpoints.
- Inspect variables.
- Write a small isolated reproduction.
- Search official documentation before random fixes.
- Confirm the fix with a test.

### Unit testing with pytest

Learn:
- Test naming conventions.
- Arrange–Act–Assert structure.
- Assertions.
- Parametrized tests.
- Testing expected exceptions.
- Fixtures at a basic level.
- Edge cases: empty input, missing values, invalid data, duplicate items.

Example:

```python
import pytest
from src.cleaner import normalize_email

@pytest.mark.parametrize(
    ("raw_email", "expected"),
    [
        (" USER@Example.COM ", "user@example.com"),
        ("admin@test.org", "admin@test.org"),
    ],
)
def test_normalize_email(raw_email: str, expected: str) -> None:
    assert normalize_email(raw_email) == expected
```

### Formatting and linting

Learn:
- Formatter vs. linter.
- Configure Ruff and a formatter.
- Run checks before committing.
- Fix warnings rather than ignoring them blindly.
- Use type hints and run a type checker later; basic `mypy` can be introduced at the end of Phase 0.

Suggested routine:

```bash
pytest
ruff check .
ruff format .
```

## 0.7 Documentation and communication

Learn Markdown:
- Headings.
- Bullet and numbered lists.
- Code blocks.
- Tables.
- Links.
- Images/screenshots.
- Basic badges are optional.

Every project README should answer:

1. What problem does this solve?
2. What does it do?
3. What technologies does it use?
4. How do I set it up?
5. How do I run it?
6. What input/output does it expect?
7. How do I test it?
8. What are known limitations?
9. What would I improve next?

## Phase 0 project ladder

Build these in sequence. Do not make them perfect; finish, test, document, and publish each one.

| Level | Project | What it teaches |
|---|---|---|
| Small | Number/text utility CLI | Variables, strings, functions, conditions |
| Small | To-do or expense tracker | Lists, dicts, CRUD logic, JSON persistence |
| Medium | CSV cleaner and validator | Files, CSV, errors, data cleaning, CLI arguments |
| Medium | Public API data collector | `requests`, JSON, environment variables, retries |
| Medium | Log-file analyzer | Regex, file streaming, aggregation, reporting |
| Bigger | Personal document organizer | OOP/dataclasses, `pathlib`, JSON, tests, CLI |
| Phase-0 capstone | Data-quality CLI toolkit | Modular code, config, tests, logging, GitHub-quality docs |

### Recommended capstone: Data-quality CLI toolkit

Build a command-line tool that:

```bash
python -m src.main \
  --input data/raw_customers.csv \
  --output data/clean_customers.csv \
  --report reports/quality_report.json
```

Features:
- Checks that required columns exist.
- Normalizes column names and text fields.
- Detects missing values and duplicate rows.
- Validates email/date/number formats.
- Produces cleaned output.
- Produces a JSON quality report.
- Uses `logging`.
- Handles invalid input without a traceback for normal user mistakes.
- Includes 10–20 pytest tests.
- Includes a complete README and sample dataset.
- Uses Git branches and at least one pull request.

## Phase 0 mastery checklist

Move to Phase 1 when you can do all of these without a tutorial:

- [ ] Start and activate a Python virtual environment.
- [ ] Install and pin dependencies.
- [ ] Create a well-structured Python project.
- [ ] Read/write CSV and JSON safely.
- [ ] Write functions, classes, and basic modules.
- [ ] Handle errors intentionally.
- [ ] Use type hints and docstrings.
- [ ] Build an `argparse` command-line interface.
- [ ] Navigate the terminal and inspect processes/files.
- [ ] Use Git branches, commits, pull requests, and conflict resolution.
- [ ] Keep API keys and `.env` files out of GitHub.
- [ ] Write and run pytest tests.
- [ ] Use a formatter and linter.
- [ ] Publish a documented capstone project.

Once you complete this, you are ready for Phase 1: backend APIs, databases, Docker, testing depth, and cloud deployment.

Sources
[1] Hello World - GitHub Docs https://docs.github.com/en/get-started/using-github/hello-world
[2] Introduction to GitHub - Training - Microsoft Learn https://learn.microsoft.com/en-us/training/modules/introduction-to-github/
[3] Use cases for Python environment variables | Alexandra Zaharia https://alexandra-zaharia.github.io/posts/use-cases-for-python-environment-variables/
[4] File System Commands : TechWeb - Boston University https://www.bu.edu/tech/support/research/system-usage/using-file-system/navigation/
[5] Linux file permissions explained - Red Hat https://www.redhat.com/en/blog/linux-file-permissions-explained
[6] skills/introduction-to-github: Get started using GitHub in less than an ... https://github.com/skills/introduction-to-github
[7] argparse – Argument parser functions - Nokia Documentation Center https://documentation.nokia.com/sr/25-7/pysros/argparse.html
[8] Command Documentation - LinuxCommand.org https://linuxcommand.org/lc3_man_page_index.php
[9] jsonargparse (former yamlargparse) - Read the Docs https://jsonargparse.readthedocs.io/en/v2.32.2/
[10] Linux Commands - GeeksforGeeks https://www.geeksforgeeks.org/linux-unix/linux-commands/
[11] Python argparse Module - W3Schools https://www.w3schools.com/python/ref_module_argparse.asp
[12] Learn Git Branching https://learngitbranching.js.org/?locale=en_US
[13] Is there an official resource for all Linux commands? https://itsfoss.community/t/is-there-an-official-resource-for-all-linux-commands/13598
[14] Add support for Environment Variables to argparse - Ideas https://discuss.python.org/t/add-support-for-environment-variables-to-argparse/103449
[15] GitHub Learn - Skills https://skills.github.com/