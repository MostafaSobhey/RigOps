# RigOps Field Suite — Public Preview

A single-page public preview of **RigOps Field Suite**, a drilling, completion, and workover
decision workspace designed and engineered by **Mostafa A. Sobhy**.

**[▶ View the live preview](https://rigops.mostafa-sobhy.workers.dev/)**

---

## What this is

A **marketing and demonstration build only**, deliberately separate from the full suite.

**What runs here**

- **Well-control quick math** — fully live. Every input is editable and all eight outputs
  recompute on change, using the same formulas as the production calculation layer.
- **Kick scenario** — press *Play kick scenario* to drive shut-in drill pipe pressure to
  1,250 psi and watch the MAASP margin drain from 100% to roughly 44%.
- **AI product line** — four applied-AI products, each linked to the research or field practice
  behind it: the Drilling Co-pilot, the Drilling Engineer Suite (offset study and history
  analysis), the Virtual Flow Meter, and the ESP failure-prediction framework.
- The full engineering portfolio, publication list, and contact routes.

**What does not run here**

The other ten calculators and all seven decision documents appear as preview cards only. No
calculation logic for those tools is included in this repository.

## Why the split

The production suite enforces access control at the edge and holds the complete verified
calculation layer. Publishing that as a static site would put the engineering logic in public
with no way to enforce access. This preview exists so the work can be shared openly without
exposing the full system.

## Running it locally

No build step, no dependencies, no server.

```bash
open index.html
```

Everything is inlined into one file, so it works opened straight from disk — unlike the full
suite, which needs a local server for JavaScript modules.

## Before you publish

The live URL is set to `https://rigops.mostafa-sobhy.workers.dev` throughout the Open Graph
tags. If you later move to a custom domain, update the four `og:`/`twitter:` tags in
`index.html` and the link at the top of this README, then re-run the URL through
**linkedin.com/post-inspector** so LinkedIn refreshes its cached preview. Always inspect before
posting — a published post keeps its preview image permanently.

## Deploying

**GitHub** — create a public repository and upload the *contents* of this folder, not the
folder itself. `index.html` must sit at the repository root.

**Cloudflare Pages** — in the Cloudflare dashboard go to **Workers & Pages → Create → Pages →
Connect to Git**, select the repository, then set:

| Field | Value |
|---|---|
| Framework preset | None |
| Build command | *leave empty* |
| Build output directory | `/` |

There is no build step. Deploy takes under a minute, and every later push redeploys
automatically.

## Accessibility and privacy

- Responsive to mobile widths
- Visible keyboard focus on all interactive elements
- `prefers-reduced-motion` respected
- No local storage, session storage, analytics, tracking, or cookies
- No framework, no build tooling

## Important notice

All values shown are **worked examples**. RigOps is not an approved operating program, a
well-control procedure, an API certification, or a safety approval. The well-control screen is
decision support only and must never be the sole basis for a well-control action. Use verified
current-well data and obtain responsible engineering and supervisory approval before any field
application.

## Contact

- **Email** — mostafa-sobhy@aucegypt.edu
- **LinkedIn** — [in/mostafasobhey](https://www.linkedin.com/in/mostafasobhey/)
- **Google Scholar** — [Publications and citations](https://scholar.google.com/citations?user=YRDfA6MAAAAJ&hl=en)
- **ResearchGate** — [Research profile](https://www.researchgate.net/profile/Mostafa-Sobhy-4)

## License

See [LICENSE.md](LICENSE.md). The full RigOps Field Suite is not included in this repository.
