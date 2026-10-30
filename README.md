# cursor-rules — pinned source for harnessator

A governed **[harnessator](https://github.com/aignerdevelopment/harnessator)
source** produced by `harnessator harvest` from
[sanjeed5/awesome-cursor-rules-mdc](https://github.com/sanjeed5/awesome-cursor-rules-mdc) —
**241 curated Cursor AI rule files**, CC0 licensed, harvested unchanged;
the upstream `LICENSE` travels with them. Each component's `origin`
records the exact upstream commit.

Quality note: this collection is community/LLM-generated breadth, not
hand-audited wisdom — the point of the profiles below is *choosing*
deliberately instead of enabling 241 rules blindly. See
`HARVEST-NOTES.md` for the excluded legacy sets and the reviewed
sanitize findings.

## Consume it

```sh
harnessator source add https://github.com/aignerdevelopment/cursor-rules.git --ref v0.1.0
harnessator enable cursor-rules:web-react     # or another profile - see below
harnessator setup
```

## Profiles

| profile | rules |
|---|---|
| `essentials` | git, typescript, python |
| `web-react` | react, next-js, typescript, tailwind, vite, shadcn, zustand, trpc |
| `python-data` | python, pandas, numpy, scikit-learn, matplotlib, sqlalchemy, pytest |
| `backend-go` | go, postgresql, redis, servemux |
| `devops` | docker, kubernetes, terraform, ansible, nginx, github-actions |
| `ml-core` | python, pytorch, transformers, huggingface, cuda |

Any rule can also be enabled individually (`harnessator enable
cursor-rules:rule/terraform`); `harnessator search rule react` browses
the corpus. Renderings are per harness: the cursor target regenerates
faithful `.mdc` files (globs/alwaysApply hints preserved), text harnesses
receive the lifted rule bodies.

## Update policy

Re-harvest from an upstream commit, re-curate the profiles that this
README documents, one reviewable commit per refresh, tag `v0.N.0`.
Consumers move by updating their lock, never by surprise.
