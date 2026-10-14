# hermes-mythic

Hermes Agent profile distribution: Mythic work (scope to be defined)

This repo holds the agent's **rules, config and skills** — never credentials or memory.

| File | Purpose | Edit? |
|------|---------|-------|
| `SOUL.local.md` | Profile-specific identity and rules | Yes |
| `SOUL.md` | Generated: `hermes-core/SOUL.base.md` + `SOUL.local.md` | No — run `../hermes-core/scripts/build.sh` |
| `config.yaml` | Model, working directory, MCP (Composio) | Yes |
| `distribution.yaml` | Distribution manifest | Bump `version` on changes |
| `skills/core/` | Generated copy of the shared core skills | No |
| `skills/<other>/` | Skills specific to this profile | Yes |
| `memory/` | Archive of what the agent learned, written by `hermes-core/scripts/sync-memory.sh` | No — generated |

## Install / update

```bash
../hermes-core/scripts/install.sh mythic
cp ~/.hermes/profiles/mythic/.env.EXAMPLE ~/.hermes/profiles/mythic/.env   # first time; add COMPOSIO_API_KEY
mythic chat
```

See `hermes-core/README.md` for the full workflow.
