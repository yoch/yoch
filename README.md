# Yoch Melka

### Software Architect & AI Systems Engineer

I design and build reliable, intelligent, and highly optimized software products, from production-grade AI/RAG pipelines, domain-tuned rerankers and MCP agent tooling to custom search engines, IoT telemetry and low-level systems.

Over the past 15+ years, I have architected, deployed, and maintained full-stack systems across industries like healthcare, green energy, beauty tech, and industrial IoT. My focus is on writing memory-efficient, low-latency code and scaling infrastructure that lasts.

---

## 🛠️ Tech Stack & Capabilities

*   **AI & LLM Systems:** LLM Pipelines & Evaluatable RAG, Fine-tuned Rerankers, Vector Search, MCP Servers & Specialized harnesses.
*   **ML & Search:** Custom Full-Text Search, Classical ML, Computer Vision.
*   **Architectures & Systems:** Distributed Systems, Event-Driven Architecture, Microservices, IoT Telemetry, Embedded Interfaces.
*   **Databases & Messaging:** MySQL, PostgreSQL (PostGIS, TimescaleDB), MongoDB, Redis, MQTT, Modbus.
*   **Languages:** Python, Node.js / TypeScript, C / C++, SQL.
*   **DevOps & Infrastructure:** AWS (EC2, CloudWatch, SSM), Docker, PM2, GitHub Actions, Linux Administration.

---

## 🌟 Featured Open-Source Projects

### AI, LLM & Agents

#### 🧠 [camembert-pharmacy-reranker-distil](https://huggingface.co/ymelka/camembert-pharmacy-reranker-distil)
A lightweight French reranker for pharmacy search. Given a query such as *"générique de Doliprane 500 mg"*, it reorders candidate drugs from the public French drug database (BDPM) so that the right specialty comes first: right generic, dosage, form and population.
*   **Focus:** Domain fine-tuning evaluated on a frozen holdout, outperforming its base model while largely preserving general French reranking. Small enough (~68M parameters) to run on CPU.
*   *Tech:* DistilCamemBERT, Cross-Encoder Fine-tuning, Hugging Face.

#### 🧩 [cursor-cloud-mcp](https://github.com/yoch/cursor-cloud-mcp)
A local stdio MCP server to launch, follow up, supervise and track the cost of a fleet of Cursor Cloud Agents from Claude Code, Codex CLI or OpenCode. 19 tools, published on PyPI; write and delete operations are disabled by default.
*   *Tech:* Python, MCP, REST API.

### MQTT & IoT

#### 🚀 [mqttium](https://github.com/yoch/mqttium)
A dependency-free, async-native MQTT 3.1.1 and 5.0 client for Python, with explicit backpressure and durable (SQLite-backed) sessions. Fully typed, with CI, coverage and [documentation](https://mqttium.readthedocs.io).
*   *Tech:* Python, asyncio, MQTT 5, TLS / WebSocket.

#### 📊 [mqtt-python-client-bench](https://github.com/yoch/mqtt-python-client-bench)
A comparative end-to-end benchmark of popular Python MQTT clients (paho, awscrt, gmqtt, mqttium, aiomqtt, amqtt, zmqtt) against a local Mosquitto broker. Every count is confirmed by a party that shares no code with the client. [Live report](https://yoch.github.io/mqtt-python-client-bench/).
*   *Tech:* Python, Mosquitto, CPU/memory/latency measurement.

#### 🔌 [modpoll2mqtt](https://github.com/yoch/modpoll2mqtt)
A Modbus-to-MQTT gateway for reliable telemetry ingestion in production environments (fork of modpoll). [Documentation](https://yoch.github.io/modpoll2mqtt).
*   **Focus:** Zero-leak memory profile, connection resilience, and rapid payload parsing.
*   *Tech:* Python, Modbus Protocol, MQTT.

### Search, Data & ML

#### 🔍 [frozenminisearch](https://github.com/yoch/frozenminisearch)
A lightweight, immutable full-text search index for Node.js with a MiniSearch-compatible API, using a fraction of the RAM.
*   **Focus:** Ultra-low RAM footprint, zero-dependency, binary snapshot support, and heavy performance benchmarking.
*   *Tech:* TypeScript, Algorithmic Tries, Levenshtein Distance, Benchmarking Suites.

#### 💊 [fr.gouv.medicaments.rest](https://github.com/yoch/fr.gouv.medicaments.rest)
A REST API over the public French drug databases (human drugs from BDPM, veterinary drugs from ANMV), refreshed daily and designed to be called by LLM agents as well as by applications.
*   **LLM-ready:** Compact Markdown / summary output that fits agent context windows, tool-ready drug shortage alerts, typo-tolerant prefix and fuzzy search.
*   *Tech:* Node.js, Data Normalization, API Design.

#### 🗺️ [sparse-som](https://github.com/yoch/sparse-som)
Fast Self-Organizing Maps (Kohonen maps) for sparse, high-dimensional data such as text, with online and parallel batch algorithms, command-line tools and a Python package. Described in a [published paper](https://doi.org/10.5220/0006499500540063).
*   **Focus:** Time complexity that depends on non-zero values only, much faster than the classical algorithm on very sparse datasets.
*   *Tech:* C++, OpenMP, Python bindings, LIBSVM format.

---

## ⚙️ Production Systems & Case Studies (Selected Work)

I serve as a Software Architect and Lead Developer for complex business platforms, managing products from conception to high-load production.

### ⚡ Industrial IoT & Energy Management Platform
Architected the backend and telemetry ingestion pipelines for a real-time energy monitoring dashboard used in commercial buildings and hospitality networks.
*   **Achievements:** Scaled timeseries ingestion (MQTT, Modbus, Zigbee) into PostgreSQL/TimescaleDB. Integrated native utility APIs (Enedis/GRDF).
*   **Tech Stack:** Python, SQLAlchemy, Celery, TimescaleDB, MQTT.

### 🩺 Healthcare & Clinical AI Assistants
Designed and deployed production-grade RAG systems and structured document extraction pipelines for the pharmaceutical and medical sectors.
*   **Achievements:** Built a conversational RAG assistant using a dual-model pipeline. Engineered document processing APIs for pharmacy automation, handling multi-format data ingestion, medical transcription, and structured data extraction from clinical PDF forms.
*   **Tech Stack:** Node.js, Python, Qdrant Vector DB, LLM APIs, PDF Parsing Engines.

### 🧴 High-Load Computer Vision & Dermacosmetics API
Engineered the core API and cloud infrastructure for a computer vision platform analyzing skin and hair conditions from mobile-uploaded photos.
*   **Achievements:** Built scalable, asynchronous image processing pipelines on AWS. Developed robust operational monitoring (SSM, CloudWatch alerts) to guarantee 99.9% availability.
*   **Tech Stack:** Python, PyTorch/OpenCV integrations, AWS SSM/CloudWatch, Docker.

---

## 📈 Technical Background & Philosophy

My approach to engineering is rooted in a strong scientific foundation (Master's degree in Computer Science and early research work in Classical ML/SOMs).

I believe that:
1.  **Performance is a feature:** A 10x reduction in memory or CPU usage translates directly to infrastructure savings and a better user experience.
2.  **Telemetry is mandatory:** A system is only as reliable as its monitoring. If it is not monitored, it is broken.
3.  **Simplicity scales:** Prefer boring, robust technologies (Postgres, Redis, clean Unix/Linux pipelines) over complex distributed state unless strictly necessary.
4.  **Evaluate on your own data:** Generic benchmarks don't predict production behaviour. Models, retrieval and prompts are evaluated and optimized on real data from the target domain, against held-out test sets, before they ship.

---

## 📬 Connect with Me

*   **LinkedIn:** [linkedin.com/in/joshua-melka](https://linkedin.com/in/joshua-melka)
