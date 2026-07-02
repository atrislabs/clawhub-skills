# ClawHub Skills by Atris

[![GitHub stars](https://img.shields.io/github/stars/atrislabs/clawhub-skills?style=social)](https://github.com/atrislabs/clawhub-skills/stargazers)

Skills for [OpenClaw](https://openclaw.ai) published on [ClawHub](https://claw-hub.net).

## Skills

| Skill | Description | Install |
|-------|-------------|---------|
| [atris](./atris/) | Codebase intelligence - structured navigation maps with file:line references | `clawhub install atris` |
| [member-runtime](./member-runtime/) | Load and run [MEMBER.md](https://github.com/atrislabs/member) team members | `clawhub install member-runtime` |
| [chief-of-staff](./chief-of-staff/) | Daily briefing agent that learns your patterns (requires member-runtime) | `clawhub install chief-of-staff` |

## Publishing

```bash
clawhub publish ./atris --slug atris --name "Atris" --version 1.1.0
clawhub publish ./member-runtime --slug member-runtime --name "Member Runtime" --version 1.0.0
clawhub publish ./chief-of-staff --slug chief-of-staff --name "Chief of Staff" --version 1.0.0
```

## License

MIT

## Atris ecosystem

[atris](https://github.com/atrislabs/atris) · [member](https://github.com/atrislabs/member) · [chief-of-staff](./chief-of-staff/) · [`FOR_AGENTS.md`](FOR_AGENTS.md)
