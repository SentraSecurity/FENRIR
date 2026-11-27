![PROJECT FENRIR](fenrir-banner.png)
🐺 PROJECT FENRIR

Autonomous AI Cybersecurity Agent

<p align="center">
  <strong>Observe. Analyze. Learn. Defend.</strong>
</p><p align="center">
  <img src="https://img.shields.io/badge/Version-0.4.0-00D9FF?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Python-3.10+-3776AB?style=for-the-badge&logo=python&logoColor=white" />
  <img src="https://img.shields.io/badge/Platform-Kali%20Linux-557C94?style=for-the-badge&logo=kalilinux&logoColor=white" />
  <img src="https://img.shields.io/badge/AI-Hybrid-8A2BE2?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Status-Development-orange?style=for-the-badge" />
</p>---

Overview

PROJECT FENRIR is an experimental AI-powered defensive cybersecurity agent designed to observe, inspect, analyze, remember, and learn from security-related information.

Inspired by the intelligence and adaptability of a cybernetic organism, FENRIR combines local AI, external threat intelligence, persistent memory, and modular security inspection tools into a unified agent architecture.

Its objective is to evolve from a conventional security monitoring tool into an intelligent defensive assistant capable of understanding user instructions, conducting authorized inspections, and explaining security findings.

Core Philosophy

OBSERVE → ANALYZE → REMEMBER → LEARN → VALIDATE → EVOLVE

FENRIR follows a continuous intelligence cycle:

- OBSERVE: Collect security observations and authorized telemetry.
- ANALYZE: Examine indicators, files, domains, IP addresses, and events.
- REMEMBER: Preserve historical observations and verified knowledge.
- LEARN: Improve detection capabilities using reviewed data.
- VALIDATE: Evaluate model performance and detection quality.
- EVOLVE: Promote improved models after human approval.

Architecture

                 USER
                  |
          TEXT / VOICE INTERFACE
                  |
             FENRIR AGENT
                  |
          ┌───────┴────────┐
          |                |
      HYBRID BRAIN     TOOL ROUTER
          |                |
    ┌─────┴─────┐     ┌────┴─────────┐
    |           |     |              |
 LOCAL AI   EXTERNAL  SECURITY     MEMORY
            INTEL     INSPECTOR    ENGINE
    |           |     |              |
    └─────┬─────┘     └────┬─────────┘
          |                |
          └───────┬────────┘
                  |
             SAFETY ENGINE
                  |
             AUDIT SYSTEM
                  |
          SECURITY REPORTS

Key Features

1. Hybrid AI Brain

- Local AI inference through Ollama.
- External threat intelligence integration.
- Natural-language interaction.
- Context-aware responses.
- Offline-capable local reasoning.

2. Conversational Agent

- Text-based communication.
- Voice input and output architecture.
- Natural-language command interpretation.
- Task planning and tool routing.
- Security findings explained in understandable language.

3. Security Inspector

Planned inspection modules:

Module| Function
File Inspector| File metadata and security inspection
Hash Analyzer| SHA-256 fingerprint analysis
Domain Inspector| Domain intelligence and reputation
IP Inspector| IP intelligence and reputation
Network Inspector| Authorized local asset discovery

4. Memory Engine

Long-term Memory

- Verified threat intelligence.
- Historical indicators.
- Detection knowledge.
- Approved model information.

Episodic Memory

- Previous analyses.
- Security observations.
- Agent decisions.
- Errors and outcomes.

5. Autonomous Learning

- Collect reviewed security observations.
- Prepare training datasets.
- Train candidate detection models.
- Evaluate precision, recall, and F1-score.
- Compare candidate models against approved models.
- Require human approval before model promotion.
- Support model rollback.

6. Safety and Governance

- Authorization-aware operations.
- Human approval for sensitive actions.
- Audit logging.
- Data provenance.
- Safe handling of suspicious files.
- No uncontrolled self-replication.
- No unauthorized exploitation or access.

Technology Stack
Component| Technology
Core language| Python
AI runtime| Ollama
Local AI model| Qwen 2.5 1.5B
API framework| FastAPI
Memory| SQLite
Learning| Lightweight ML
Security core| Python / Rust
Environment| Kali Linux WSL2
Interface| Web Dashboard
Voice| Speech-to-Text / Text-to-Speech

Project Structure
```bash
PROJECT_FENRIR/
│
├── fenrir/
│   ├── agent/
│   │   ├── core.py
│   │   ├── conversation.py
│   │   ├── planner.py
│   │   └── router.py
│   │
│   ├── brain/
│   │   ├── local_model.py
│   │   └── reasoning.py
│   │
│   ├── voice/
│   │   ├── speech_input.py
│   │   └── speech_output.py
│   │
│   ├── inspector/
│   │   ├── file_inspector.py
│   │   ├── domain_inspector.py
│   │   └── ip_inspector.py
│   │
│   ├── memory/
│   ├── safety/
│   └── app.py
│
├── dashboard/
├── learning/
├── data/
├── tests/
├── requirements.txt
├── .env.example
└── README.md
```
The structure describes the target v0.4 architecture. Individual modules may still be under development.

Installation

Requirements

- Python 3.10 or newer
- Kali Linux or another compatible Linux environment
- Ollama
- Recommended: 4 GB or more RAM
- Internet connection for external intelligence sources

1. Clone the repository

```bash

git clone https://github.com/SentraSecurity/FENRIR.git
cd FENRIR
unzip -o project_fenrir_v0_4.zip
cd project_fenrir_v0_4
```

3. Create a virtual environment

```bash
python3 -m venv .venv
source .venv/bin/activate
```

4. Install dependencies

```bash

pip install --upgrade pip
pip install -r requirements.txt
```

5. Install Ollama

```bash

curl -fsSL https://ollama.com/install.sh | sh
```

Start the Ollama service:

```bash

ollama serve
```

Open another terminal and download the model:

```bash

ollama pull qwen2.5:1.5b
```

6. Configure environment

```bash

cp .env.example .env
```

Review the configuration before launching the application.

7. Launch

If the agent CLI entry point is available:

```bash

python3 -m fenrir.agent.core
```

If the FastAPI application is configured:

```bash

uvicorn fenrir.app:app --host 127.0.0.1 --port 8080
```

Dashboard:

```bash

http://127.0.0.1:8080
```

API documentation:

```bash

http://127.0.0.1:8080/docs
```

Note: Launch commands depend on the modules included in the checked-out version. The v0.4 architecture and all planned components are not necessarily implemented yet.

Development Roadmap

Version| Milestone
v0.1| Initial project foundation
v0.2| Learning Engine and model registry
v0.3| AI Brain and Memory Engine
v0.4| Conversational Hybrid AI Agent
v0.5| Advanced Security Inspector
v0.6| Voice Intelligence
v0.7| Autonomous Threat Analysis
v0.8| Advanced Dashboard
v1.0| Integrated Defensive Intelligence Platform

Security Disclaimer

PROJECT FENRIR is intended for defensive cybersecurity research, education, and authorized security testing.

Users are responsible for ensuring they have permission to inspect any systems, networks, files, or infrastructure.

FENRIR is designed with human oversight for sensitive operations. Autonomous learning does not imply autonomous authorization to access or modify external systems.

Do not use this project for unauthorized access, disruption, exploitation, or malicious activity.

Contributing

Contributions, bug reports, feature proposals, and security improvements are welcome.

Before submitting changes:

1. Test the affected modules.
2. Document new dependencies.
3. Preserve safety controls.
4. Avoid committing secrets, tokens, or private data.
5. Include reproducible steps for reported bugs.

License

Choose and add an appropriate open-source license before distributing the project. Until then, all rights are reserved by the project owner.

---

<p align="center">
  <strong>PROJECT FENRIR</strong><br/>
  <em>Intelligence that observes. Systems that learn. Defense that evolves.</em>
</p>

# PROJECT FENRIR v0.1.0
A defensive, local-first cybersecurity monitoring prototype for Kali Linux on WSL2.
This starter release provides a FastAPI dashboard, event journal, local health checks,
and a Rust hashing/indicator engine. It does **not** propagate, exploit, or modify
remote systems.

## Requirements
- Kali Linux on WSL2
- Python 3.11+
- Rust stable + Cargo (for the optional Rust core)

## Quick start
```bash
sudo apt update
sudo apt install -y python3 python3-venv python3-pip cargo rustc
git clone https://github.com/SentraSecurity/FENRIR.git
cd FENRIR
unzip project_fenrir_v0_1.zip
cd project_fenrir_v0_1
python3 -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
uvicorn fenrir.app:app --host 127.0.0.1 --port 8080
```
Open `http://127.0.0.1:8080` in the Windows browser.

## Rust core
```bash
cd rust_core
cargo build --release
cargo run --release -- hash ../README.md
```
The Rust component computes SHA-256 and checks a local text indicator list.
It does not execute samples.

## Configuration
Copy `.env.example` to `.env`. The default bind address is localhost only.
Do not expose the dashboard to the public internet.

## Current scope
- Dashboard status and event journal
- Local machine/interface inventory
- File hashing (read-only)
- Local indicator matching (SHA-256)
- Manual event recording

## Not yet implemented
- Packet capture, active network scanning, quarantine, sandbox execution,
  autonomous remediation, remote scanning, or self-updating behavior.
These require explicit scope controls, audit logging, and isolated testing first.
