# Ludwig J. Marx

**Go, Rust & Python · Next.js**

I build financial research tools and contribute fixes to open-source projects.
My work focuses on API integrations, data processing and calculations whose
results can be checked against a written definition.

I trade on eToro as a Popular Investor. Building tools for my own research led
me into broker APIs, indicator definitions and the evidence behind performance
claims.

Available for open-source contribution work, particularly debugging existing
codebases and building data integrations.
[Portfolio](https://www.ludwigjmarx.dev) · [Contact](mailto:ludwig@ludwigjmarx.dev)

## Selected contributions

Merged pull requests in other maintainers' projects:

| Project | Change | Language |
| --- | --- | --- |
| [ifc-lite #4900](https://github.com/LTplus-AG/ifc-lite/pull/4900) | Corrected the parser's worker URL to point to the file shipped in the package. | TypeScript |
| [ezBookkeeping #677](https://github.com/mayswind/ezbookkeeping/pull/677) | Fixed monthly schedules counted from the end of the month to use the template's time zone. | Go |
| [ezBookkeeping #678](https://github.com/mayswind/ezbookkeeping/pull/678) | Made edit-scope tests construct boundaries in the time zone being tested. | Go |

## Selected projects

**[vigil](https://github.com/LudwigJMarx/vigil)** · Go, SQLite, TypeScript

A self-hosted account timeline and scoring tool for B2B sales. Returns each
signal's contribution to the score and identifies signals it cannot score.
Runs as one binary with one database file.

**[Onestein](https://github.com/LudwigJMarx/Onestein)** · Rust

A messaging protocol stack and library for intermittent networks. Keeps
protocol logic separate from application storage and transport. Experimental;
not independently audited.

**[mesura](https://github.com/LudwigJMarx/mesura)** · Python

A test bench for trading-strategy claims. Examines what reported performance
and the underlying sample can support.
[mesura-web](https://github.com/LudwigJMarx/mesura-web) brings trade-record
analysis to the browser in TypeScript, with calculations checked against the
Python implementation.

**[factorbase](https://github.com/LudwigJMarx/factorbase)** · Python, pandas

A catalogue of stock-screening factors with explicit formulas, input
requirements and tested reference implementations. Documents choices such as
smoothing and initialization so that a result can be reproduced.

**[portfolio](https://github.com/LudwigJMarx/portfolio)** · TypeScript, Next.js

The source of [ludwigjmarx.dev](https://www.ludwigjmarx.dev). Every claim on the
page is checked against the GitHub API when the page renders, and each one
shows up as verified, disputed, or unverified with the reason it could not be
checked. A refused API call prints its reason instead of passing as a zero.

## How I work

For a bug fix, I start with a reproducible failure and include a regression
test that fails before the change and passes after it. I keep the diff focused
and document the verification commands, results and reasons for the approach
so a reviewer can check the work.
