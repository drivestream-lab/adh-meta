# adh-meta

Control-plane for the **ADH** programme in `drivestream-lab`.

| File | Purpose |
| --- | --- |
| `config/programme.yaml` | Identity: slug `adh`, org `drivestream-lab` |
| `config/governance-drivestream-lab.yaml` | Teams, repos, gitflow, board **ADH** |
| `config/harness-drivestream-lab.yaml` | Constitution + skills per stack |
| `config/scaffold-drivestream-lab.yaml` | Cookiecutter for `adh`; `adh-iac-local` brownfield |
| `config/service-catalog-drivestream-lab.yaml` | Service map |

Factory secrets live in `~/.config/launchpad/env.d/adh.env` — never commit them.

```bash
launchpad --client adh doctor
launchpad --client adh status --meta
```
