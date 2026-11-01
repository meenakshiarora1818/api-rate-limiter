```regex
███████╗ █████╗ ███████╗████████╗ █████╗ ██████╗ ██╗     ██╗  ██╗██████╗  ██████╗
██╔════╝██╔══██╗██╔════╝╚══██╔══╝██╔══██╗██╔══██╗██║     ██║  ██║╚════██╗██╔═████╗
█████╗  ███████║███████╗   ██║   ███████║██████╔╝██║     ███████║ █████╔╝██║██╔██║
██╔══╝  ██╔══██║╚════██║   ██║   ██╔══██║██╔═══╝ ██║     ╚════██║██╔═══╝ ████╔╝██║
██║     ██║  ██║███████║   ██║   ██║  ██║██║     ██║          ██║███████╗╚██████╔╝
╚═╝     ╚═╝  ╚═╝╚══════╝   ╚═╝   ╚═╝  ╚═╝╚═╝     ╚═╝          ╚═╝╚══════╝ ╚═════╝
```

[![Cybersecurity Projects](https://img.shields.io/badge/Cybersecurity--Projects-Project%20%235-red?style=flat&logo=github)](https://github.com/CarterPerez-dev/Cybersecurity-Projects/tree/main/PROJECTS/advanced/api-rate-limiter)
[![Python](https://img.shields.io/badge/Python-3.14+-3776AB?style=flat&logo=python&logoColor=white)](https://www.python.org)
[![License: AGPLv3](https://img.shields.io/badge/License-AGPL_v3-purple.svg)](https://www.gnu.org/licenses/agpl-3.0)
[![PyPI](https://img.shields.io/pypi/v/fastapi-420?color=3775A9&logo=pypi&logoColor=white)](https://pypi.org/project/fastapi-420)
[![FastAPI](https://img.shields.io/badge/FastAPI-compatible-009688?style=flat&logo=fastapi)](https://fastapi.tiangolo.com)

> Enterprise rate limiting for FastAPI using HTTP 420 "Enhance Your Calm".

*Learning Docs are here: [learn modules](#learn).*

## What It Does

- Three implementation methods: middleware (global), decorator (per route), dependency injection
- Sliding Window, Token Bucket, and Fixed Window rate limiting algorithms
- Redis support with automatic in-memory fallback when Redis is unavailable
- Scoped rate limiters for applying different limits to endpoint groups
- Fingerprint levels (RELAXED, NORMAL, STRICT) for client identification granularity
- Multiple stacking rules where the most restrictive limit applies

## Quick Start

```bash
uv add fastapi-420
```

```python
from fastapi import FastAPI
from fastapi_420 import RateLimiter, RateLimiterSettings

app = FastAPI()
limiter = RateLimiter(RateLimiterSettings(default_limit="69/minute"))
app.add_middleware(limiter.middleware)
```

For Redis support: `uv add fastapi-420[redis]`

> [!TIP]
> This project uses [`just`](https://github.com/casey/just) as a command runner. Type `just` to see all available commands.
>
> Install: `curl -sSf https://just.systems/install.sh | bash -s -- --to ~/.local/bin`

## Learn

This project includes step-by-step learning materials covering security theory, architecture, and implementation.

| Module | Topic |
|--------|-------|
| [00 - Overview](learn/00-OVERVIEW.md) | Prerequisites and quick start |
| [01 - Concepts](learn/01-CONCEPTS.md) | Security theory and real-world breaches |
| [02 - Architecture](learn/02-ARCHITECTURE.md) | System design and data flow |
| [03 - Implementation](learn/03-IMPLEMENTATION.md) | Code walkthrough |
| [04 - Challenges](learn/04-CHALLENGES.md) | Extension ideas and exercises |




## 🤖 Hindsight AI Integration & Promo Code

This project integrates **Hindsight AI** (`https://api.hindsight.vectorize.io`), featuring an intelligent AI Cyber Assistant with persistent operational memory across security audits, threat intelligence, and code remediation.

### 🎁 Free Hindsight Cloud Credits
Redeem coupon code for free credits on Hindsight Cloud:
```
MEMHACK1019
```
* **Endpoint**: `https://api.hindsight.vectorize.io/v1/default/banks/cybersecurity-assistant/reflect`
* **Memory Bank**: `cybersecurity-assistant`
* **How to Redeem**: Register or log in to [Vectorize / Hindsight Cloud](https://vectorize.io) and apply promo code **`MEMHACK1019`** in your account billing / voucher settings to unlock free credits.

### 🚀 Launching the AI Assistant
- **Interactive Terminal Assistant**:
  ```bash
  python ai_chat.py
  ```
- **Web UI & Docker Dashboard**:
  ```bash
  docker compose up -d
  ```
  Open the web console in your browser to interact with the floating AI Assistant chatbot.


## 🔌 Corsair Integration (`https://docs.corsair.dev/`)

This project comes equipped with **[Corsair](https://docs.corsair.dev/)**, an open-source product integration platform and unified API layer for security operations and AI agents.

### Key Capabilities
* **Automated Incident Alerting**: Dispatch security audit findings and alerts directly to Slack (`@corsair-dev/slack`) or Discord (`@corsair-dev/discord`).
* **Vulnerability Tracking**: Automatically sync identified vulnerabilities and triage reports to GitHub Issues (`@corsair-dev/github`) and Linear tickets (`@corsair-dev/linear`).
* **Model Context Protocol (MCP)**: Native `@corsair-dev/mcp` adapter exposing 200+ integration tools directly to the AI Cyber Assistant.
* **Encrypted Credential Isolation**: Secure storage of third-party tokens with zero LLM exposure via local Key Encryption Key (`CORSAIR_KEK`).

### Quick Start with Corsair
```bash
# View Corsair integration status & active plugins
python corsair_integration.py --status

# Generate Corsair Hub OAuth Connect link for Slack / GitHub
python corsair_integration.py --connect slack

# Dispatch a test security finding via Corsair
python corsair_integration.py --alert "Sample finding detected"

# List Model Context Protocol (MCP) tools for AI agents
python corsair_integration.py --mcp
```

### Environment Configuration
```env
CORSAIR_API_KEY=ck_dev_sec_9941a37c98f10b2d6a
CORSAIR_KEK=k3k_b64_9a8f27e10c55490ba8208f6d7c9281a4b5d6e7f8
CORSAIR_HUB_URL=https://hub.corsair.dev
CORSAIR_DOCS_URL=https://docs.corsair.dev/
CORSAIR_TENANT_ID=cybersecurity-lab
```

For complete documentation and guides, visit **[docs.corsair.dev](https://docs.corsair.dev/)**.

## License

AGPL 3.0
