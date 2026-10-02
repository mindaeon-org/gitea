# Upstream

This repository is the Mindaeon-owned fork of [go-gitea/gitea](https://github.com/go-gitea/gitea) (MIT).
Source control and CI of the platform (docs/05 C-10). Built by `images/gitea` in mindaeon-platform-deploy.

| | |
|---|---|
| Tracked line | `1.27` |
| Last merged tag | `v1.27.3` |
| Last merged commit | `146cc3eec57174711eac0e0a0c7b38670c6e3922` (2026-08-29) |
| Recorded | 2026-10-03 |

## Branches

| Branch | Content |
|---|---|
| `upstream/1.27` | An exact mirror of the upstream tag above. Never committed to by hand |
| `mindaeon/1.27` | `upstream/1.27` plus the patches listed in [PATCHES.md](PATCHES.md). The branch that is built from |

Builds are tagged `<upstream version>-m.<n>`. Our changes live in new files, or in an upstream file between
`mindaeon_change start` and `mindaeon_change end` comments that give the reason.

## Taking a new upstream version

1. Fetch the upstream tag and fast-forward `upstream/1.27` to it.
2. Merge `upstream/1.27` into `mindaeon/1.27`; resolve patch by patch and drop a patch upstream now covers.
3. Run the licence check, the provenance gate, the security scan and the tests.
4. Update the table above and [PATCHES.md](PATCHES.md).
