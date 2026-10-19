# pstack for AgenC (unofficial)

This folder is an **unofficial, community AgenC packaging of [pstack](https://github.com/cursor/plugins/tree/main/pstack)
by Lauren Tan ([@poteto](https://github.com/poteto))**. This repo is a fork of
[cursor/plugins](https://github.com/cursor/plugins), where pstack is developed. It is **not affiliated with
or endorsed by** Lauren Tan or Cursor. All credit for pstack goes to its author.

- Upstream: https://github.com/cursor/plugins/tree/main/pstack
- Based on upstream commit [`d457567332aa6989e753ea289f30ea2bfbc80bc0`](https://github.com/cursor/plugins/tree/d457567332aa6989e753ea289f30ea2bfbc80bc0/pstack) (pstack version 0.15.28)
- Questions or problems with this AgenC packaging: please open an issue
  [in this repo](https://github.com/Macro-Harder/pstack-agenc/issues), not upstream.

The skill content is unchanged. Only the plugin packaging differs, so that the AgenC CLI (tested with
0.19.9) can install it as a plugin; see [NOTICE](NOTICE) for the full list of changes. The rest of
this fork is upstream cursor/plugins as is; the upstream pstack README is at
[../pstack/README.md](../pstack/README.md).

## Install

From the root of the project you want the skills in:

```sh
git clone --depth 1 https://github.com/Macro-Harder/pstack-agenc.git /path/to/pstack-agenc
agenc plugin install /path/to/pstack-agenc/pstack-agenc --scope project
```

AgenC copies the plugin into `.agents/plugins/` in that project.

## Check it

```sh
agenc plugin validate /path/to/pstack-agenc/pstack-agenc --json   # expect "success": true
agenc skills list --json                                          # pstack skills show with "origin": "plugin"
```

With 0.19.9 the install above lists 56 skills with origin `plugin`, one per `skills/*/SKILL.md`.

## License

MIT, same as upstream. The original [LICENSE](LICENSE) (Copyright (c) 2026 Lauren Tan) is kept verbatim.
