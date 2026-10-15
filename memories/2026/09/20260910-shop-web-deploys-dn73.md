---
id: 20260910-shop-web-deploys-dn73
name: shop-web-deploys
type: project
scope: here
description: "shop-web: staging deploys from the release branch, production only from version tags"
created: 2026-09-10T11:00:00+08:00
updated: 2026-10-03T10:05:00+08:00
source:
  tool: codex
  session_id: 95e761d1-7731-4f10-906b-f2efc6f87718
  session_name: shop-web-release
  host: alex-laptop
  cwd: /Users/alex/code/shop-web
  git_root: /Users/alex/code/shop-web
  git_remote: github.com/example/shop-web
  git_branch: main
---
shop-web staging deploys automatically from the `release` branch. Production deploys only from tags like `v2.14.0`, cut from `release` after QA signs off.

**How to apply:** never tag from `main`; open the release PR into `release` first.
