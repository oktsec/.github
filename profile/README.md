<p align="center">
  <strong>Oktsec</strong><br>
  Security infrastructure for AI agent communication
</p>

<p align="center">
  Identity verification, policy enforcement, and audit trail for inter-agent messaging.<br>
  No LLM. Single binary. Deploy in minutes.
</p>

---

### What we build

AI agents are starting to talk to each other — calling tools, delegating tasks, sharing data. But there's no standard way to verify who's sending what, enforce who can talk to whom, or audit what happened.

**Oktsec** is a security proxy that sits between AI agents and enforces three layers:

- **Identity** — Ed25519 signatures verify every message sender
- **Policy** — YAML-based ACLs control which agent can message which
- **Audit** — Every message logged with content hash, verification status, and policy decision

Messages are also scanned against 144+ detection rules to catch prompt injection, credential leaks, PII exposure, and data exfiltration — powered by [Aguara](https://github.com/garagon/aguara).

### Get started

```bash
oktsec init          # Discover MCP servers, generate config + keypairs
oktsec wrap cursor   # Route your MCP client through oktsec
oktsec serve         # Start proxy + dashboard
```

### Links

- [Documentation & source](https://github.com/oktsec/oktsec)
- [Aguara — security scanner for AI agents](https://github.com/garagon/aguara)
- [Website](https://oktsec.com)
