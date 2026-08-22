# swing-suites — Repository Agent Guide

**Product:** Swing Suites — client marketing site (static HTML/CSS/JS)  
**Maturity:** PREVIEW  
**Stack:** Static site · `http-server` for local preview  
**Production sensitive:** **YES**

## Read First

- `README.md` if present
- `C:\dev\ai-shared\AGENT-COORDINATION.md`
- `C:\dev\ai-shared\ACTIVE-WORK.md`

## Shared AI System

| Resource | Path |
| -------- | ---- |
| Coordination | `C:\dev\ai-shared\AGENT-COORDINATION.md` |
| Active work | `C:\dev\ai-shared\ACTIVE-WORK.md` |
| Skills | `C:\dev\ai-shared\skills\` |

**Before writable work:** skill `git-wip-triage`; check ACTIVE-WORK claims.

## Development

```bash
npm install
npm start            # http://localhost:5200
```

## Validation

No build, lint, or test scripts in `package.json`. Manually verify pages in browser after changes.

After changes: skill `code-review` on the diff.

## Deployment

| Field | Value |
| ----- | ----- |
| **Target** | Vercel or static host (typical) |
| **Integration branch** | feature branches / PRs → Preview |
| **Production branch** | `main` |
| **Push deploys** | Preview on branch push; production on `main` |

Before push: skill `deployment-readiness`.

## Safety / Data

- Never commit `.env` or credentials
- No server-side logic in this repo

## Done

1. Manual browser check of changed pages
2. `code-review` on diff
3. UPDATE + RELEASE in ACTIVE-WORK if claimed

## Portfolio Standing Rules

- Follow `C:\dev\ai-shared\GITHUB-ACTIONS-CI-COST-CONTROL.md` — develop and validate locally first; use GitHub Actions for independent confirmation, not as the debug loop.
