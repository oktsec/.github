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

**Oktsec** is an open-source security proxy that sits between AI agents and enforces a multi-layer pipeline:

- **Identity** — Ed25519 cryptographic signatures verify every message sender
- **Policy** — YAML-based ACLs control which agent can message which, with default-deny mode
- **Content scanning** — 159 detection rules catch prompt injection, credential leaks, PII exposure, data exfiltration, MCP attacks, and supply chain risks
- **Quarantine** — High-severity messages are held for human review before delivery
- **Audit** — Every message logged to SQLite with content hash, verification status, triggered rules, and policy decision
- **Anomaly detection** — Background risk scoring with automatic alerts and optional auto-suspension

Content scanning is powered by the [Aguara](https://github.com/garagon/aguara) engine, which monitors 28K+ skills across 5 MCP registries daily via [Aguara Watch](https://watch.aguarascan.com).

Supports **MCP clients** (Claude Desktop, Cursor, VS Code, Cline, Windsurf), **OpenClaw**, and **NanoClaw**. Includes a deployment security auditor with 41 checks across all three platforms.

Covers **7 of 10** categories in the [OWASP Top 10 for Agentic Applications](https://owasp.org/www-project-agentic-ai-threats/).

Runs as a **proxy**, a [**Go SDK**](https://pkg.go.dev/github.com/oktsec/oktsec/sdk), or an **MCP server** (6 tools).

### Get started

```bash
oktsec discover                  # Find MCP servers, OpenClaw, NanoClaw
oktsec init                      # Generate config, keypairs, and policy
oktsec wrap cursor               # Route MCP client through oktsec
oktsec serve                     # Start proxy + dashboard
```

### Links

- [Documentation & source](https://github.com/oktsec/oktsec)
- [Aguara — security scanner for AI agents](https://github.com/garagon/aguara)
- [Aguara Watch — live registry monitoring](https://watch.aguarascan.com)
- [Website](https://oktsec.com)
