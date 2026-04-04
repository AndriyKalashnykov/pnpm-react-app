# CLAUDE.md — pnpm-react-app

## Project Overview

React front-end application bootstrapped with Create React App and managed with pnpm.
Includes a Docker build (multi-stage: Node builder + Nginx server).

- **Language / Framework:** TypeScript, React 18
- **Package Manager:** pnpm
- **Node version:** 18 (see `.nvmrc`)
- **Owner:** AndriyKalashnykov/pnpm-react-app

## Quick Reference

```bash
make install   # pnpm install
make build     # pnpm build
make run       # install + pnpm start
make clean     # rm -rf node_modules/ build/
make update    # pnpm update
make upgrade   # pnpm upgrade
make image     # install + build + docker build
make release VERSION=x.y.z  # tag and push release
```

## Repository Layout

```
src/            # React application source (TypeScript)
public/         # Static assets served by CRA
Dockerfile      # Multi-stage build (node:18-alpine -> nginx:1.19-alpine)
Makefile        # Developer task runner
.github/
  workflows/
    ci.yml            # CI: install, build (push/PR)
    cleanup-runs.yml  # Weekly old-run cleanup
  dependabot.yml      # GitHub Actions auto-update
```

## Build & Test

```bash
pnpm install   # install dependencies
pnpm build     # production build
pnpm test      # run tests (react-scripts test)
pnpm start     # dev server
```

## CI/CD

- **ci.yml** triggers on push to `main`, version tags (`v*`), and pull requests.
- **cleanup-runs.yml** runs weekly (Sunday midnight) to prune old workflow runs.
- Dependabot keeps GitHub Actions up to date.

## Conventions

- Makefile targets use `#target: @ Description` comment format for `make help`.
- All workflow actions are pinned to SHA for supply-chain security.
