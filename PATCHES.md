# Patches carried on `mindaeon/1.27`

One row per change that is not upstream's. A row is removed when its removal condition is met.

| # | Patch | Files | Why | Removed when |
|---|---|---|---|---|
| 1 | Pin `github.com/couchbase/goutils` to v0.1.2 | go.mod, go.sum, vendor (applied by the image build, `images/gitea/Dockerfile` in mindaeon-platform-deploy; not yet a commit on this branch) | From 1.26.0 the binary links goutils v0.3.0, whose licence (BUSL-1.1) forbids including it in a product offered for a fee; v0.1.2 is Apache-2.0 | Upstream drops the Couchbase session provider, or goutils is relicensed |
