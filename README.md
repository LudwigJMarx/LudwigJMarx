# Ludwig J. Marx

**Go, Rust & Python · Next.js**

I build financial research tools, and I fix things in other people's open-source
projects. It's mostly the same work either way: API integrations, data
processing, and calculations where you can hold the result against a written
definition and see whether it holds.

I trade on eToro as a Popular Investor. That's how I got into this, really. I
wanted better tools for my own research, and that pulled me into broker APIs,
indicator definitions, and the question of what a performance number is actually
worth.

Available for open-source contribution work. Debugging existing codebases and
building data integrations is where I'm most useful.
[Portfolio](https://www.ludwigjmarx.dev) · [Contact](mailto:ludwig@ludwigjmarx.dev)

## Merged elsewhere

Pull requests that other maintainers took into their projects:

| Project | What it fixed | Language |
| --- | --- | --- |
| [ifc-lite #4900](https://github.com/LTplus-AG/ifc-lite/pull/4900) | The parser pointed its worker URL at a file the package doesn't ship. Now it points at the one it does. | TypeScript |
| [ezBookkeeping #677](https://github.com/mayswind/ezbookkeeping/pull/677) | Monthly schedules counted from the end of the month ignored the template's time zone. | Go |
| [ezBookkeeping #678](https://github.com/mayswind/ezbookkeeping/pull/678) | Edit-scope tests built their boundaries outside the time zone they were testing, so they went red depending on where you ran them. | Go |

## My own projects

**[vigil](https://github.com/LudwigJMarx/vigil)** · Go, SQLite, TypeScript

A self-hosted account timeline and scoring tool for B2B sales. It shows what
each signal contributed to a score, and it says so when a signal can't be
scored. One binary, one database file.

**[Onestein](https://github.com/LudwigJMarx/Onestein)** · Rust

A messaging protocol stack and library for networks that are slow, intermittent,
or simply not there. Protocol logic stays separate from application storage and
transport. Experimental, and nobody outside has audited it.

**[mesura](https://github.com/LudwigJMarx/mesura)** · Python

A test bench for trading-strategy claims. You hand it a reported number, it
tells you what the sample behind it can support.
[mesura-web](https://github.com/LudwigJMarx/mesura-web) does the trade-record
part in the browser, TypeScript, with every calculation checked against the
Python one.

**[factorbase](https://github.com/LudwigJMarx/factorbase)** · Python, pandas

A catalogue of stock-screening factors. Each one comes with its formula written
out, what it needs as input, and a tested reference implementation. Choices like
smoothing and initialization are documented, which means you can reproduce a
result instead of guessing how it was meant.

**[portfolio](https://github.com/LudwigJMarx/portfolio)** · TypeScript, Next.js

The source of [ludwigjmarx.dev](https://www.ludwigjmarx.dev). Every claim on the
page gets checked against the GitHub API while the page renders, and comes back
as verified, disputed, or unverified with the reason it couldn't be checked. If
an API call is refused, the page prints why. It doesn't let a failure pass as a
zero.

## How I work

A bug fix starts with a failure I can reproduce. Then a regression test that is
red before the change and green after it, and I run both rather than claim them.
The diff stays on the problem. Commands, output, and why I took this route and
not the obvious one go into the PR, so a reviewer can check the work instead of
taking my word for it.
