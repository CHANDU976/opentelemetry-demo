# Team form

**Team name:** 29

| Member | SRN | Built |
| --- | --- | --- |
| Chandan B L | PES2UG23AM021 | Brain: LLM tool-calling investigation, rules ranking, evidence checker, schema<br>Hands: runbook, approval gate, Action API client, kill switch, verification, reports, docs |
| Syeda | PES1UG23AM331 | Eyes: telemetry tools (metrics, traces, logs, runtime), detection/watcher<br>Brain: LLM tool-calling investigation, rules ranking, evidence checker, schema |
| Aditi | PES1UG23AM020 | Eyes: telemetry tools (metrics, traces, logs, runtime), detection/watcher<br>Brain: LLM tool-calling investigation, rules ranking, evidence checker, schema |
| Sidda Baasanthi Reddy | PES1UG23AM299 | Brain: LLM tool-calling investigation, rules ranking, evidence checker, schema<br>Hands: runbook, approval gate, Action API client, kill switch, verification, reports, docs |
| Riddhi | PES1UG23AM175 | Eyes: telemetry tools (metrics, traces, logs, runtime), detection/watcher<br>Brain: LLM tool-calling investigation, rules ranking, evidence checker, schema |

**AI models used by the agent:** Groq (via OpenAI-compatible API; rule-based fallback without LLM)

**AI coding assistants used while building:** Claude (Anthropic) — helped write and review code and docs.
Every member has read and can explain and change the code they committed.

**Third-party libraries:** requests, PyYAML, pydantic, python-dotenv, jsonschema, pytest (optional).
Python standard library `http.server` for the web approval page. No agent framework.

**Data sources used:** Prometheus, Jaeger, OpenSearch / `docker logs`, Docker inspect/stats (read-only),
our own Action API server `action_api/server.py` (the only writer: docker restart, flagd flag variant, Locust users,
after approval only). Feature-flag settings are never read for diagnosis.
