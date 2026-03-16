<p align="center">
  <strong>Oktsec</strong><br>
  Runtime security for AI agents
</p>
<p align="center">
  Security proxy and MCP gateway in a single Go binary.<br>
  188 detection rules. Ed25519 identity. Hash-chained audit trail.<br>
  No LLM required. Your infra, your data.
</p>

---

### Projects

**[oktsec](https://github.com/oktsec/oktsec)** - Security proxy and MCP gateway for AI agents. 10-stage pipeline: rate limiting, identity verification, ACL, content scanning, intent validation, tool policies, verdict escalation, audit logging, anomaly detection. 11-page dashboard. Hooks for Claude Code, Cursor, and any MCP client. One command setup.

**[security-review](https://github.com/oktsec/security-review)** - Security review skill for AI-built projects. 130+ checks mapped to OWASP Top 10. Auto-detects your stack, finds issues, gives you the fix. Works in Claude Code, Cursor, Codex, Windsurf, and 38+ tools that support skills.

### Ecosystem

Content scanning is powered by the [Aguara](https://github.com/garagon/aguara) engine, which monitors 57K+ agent tools across 7 registries via [Aguara Watch](https://watch.aguarascan.com).

### Get started

```bash
# oktsec: security proxy for AI agents
brew install oktsec/tap/oktsec
oktsec run

# security-review: audit your AI-built project
npx skills add oktsec/security-review
```

### Links

- [oktsec.com](https://oktsec.com)
- [aguarascan.com](https://aguarascan.com)
- [watch.aguarascan.com](https://watch.aguarascan.com)
- [Documentation](https://oktsec.github.io/oktsec/)
