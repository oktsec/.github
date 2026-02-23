<p align="center">
  <strong>Oktsec</strong><br>
  Security layer for AI agent-to-agent communication
</p>
<p align="center">
  Every message is signed, inspected, and logged. If it doesn't comply, it doesn't pass.<br>
  No LLM. No cloud. Single binary. Your infra, your data.
</p>

---

### What we build

AI agents are starting to talk to each other — calling tools, delegating tasks, sharing data. But there's no standard way to verify who's sending what, enforce who can talk to whom, or audit what happened.

**Oktsec** is an open-source security layer that sits between AI agents and enforces three layers:

- **Identity** — Ed25519 cryptographic signatures verify every message sender
- **Policy** — YAML-based rules control which agent can message which
- **Audit** — Every message logged with content hash, verification status, and policy decision

Messages are scanned against 151 detection rules to catch prompt injection, credential leaks, PII exposure, and data exfiltration — powered by the [Aguara](https://github.com/garagon/aguara) engine, which monitors 5 MCP registries daily.

Covers **7 of 10** categories in the [OWASP Top 10 for Agentic Applications](https://owasp.org/www-project-agentic-ai-threats/).

Runs as a **proxy**, a **Go SDK**, or an **MCP server**.

### Get started

```bash
oktsec init                      # Generate config, keypairs, and policy template
oktsec discover                  # Find MCP servers, HTTP agents, stdio agents
oktsec wrap --all --proxy http   # Route all agents through oktsec
oktsec dashboard                 # Start real-time SSE dashboard
```

### Links

- [Documentation & source](https://github.com/oktsec/oktsec)
- [Aguara — security scanner for AI agents](https://github.com/garagon/aguara)
- [Aguara Watch — live registry monitoring](https://watch.aguarascan.com)
- [Website](https://oktsec.com)
