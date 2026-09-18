### Ludwig J. Marx

I work on protocols, parsers and data flows. The seams where a system meets
something it did not write itself: an API that changed without telling anyone,
a file format, a feed that arrives in a shape the documentation does not
mention.

Much of that comes from finance. I trade on eToro as a Popular Investor and
build my own tooling for it, which is where most of these seams turn up:
brokers whose API moves without notice, market data in shapes nobody wrote
down.

### Currently building

[Onestein](https://github.com/LudwigJMarx/Onestein), a messaging protocol stack
for networks that are slow, intermittent, censored or absent. The same message
travels over Tor, Bluetooth, a local network or a memory card. No server has to
exist, and nobody hands out an identifier.

It is the protocol and the library, and it will not become a messenger. The
library opens no file, no socket and reads no clock. That is not an omission:
the one thing a library cannot do for a messenger is make a secret disappear.
Whoever owns the storage owns that, so the state goes out to the caller in
plain numbers and comes back.

Draft 0, and the README says so at the top rather than in a footnote. There is
no second implementation, so every conformance test is a conversation with
itself; the partial answers are foreign oracles for the primitives, property
tests over the formats, and a generator in another language written from the
documents. No cryptographer has read it. Nobody uses it.

Rust, eleven crates, hybrid X25519 and ML-KEM-768. Apache-2.0 or MIT for the
code, CC BY-SA 4.0 for the specification.

[factorbase](https://github.com/LudwigJMarx/factorbase), a catalogue of
stock-screening factors. 192 entries: technical indicators, fundamental ratios,
chart signals and cross-sectional rankings, each with the formula it is
defined by and an implementation tested against that formula.

Indicator libraries compute. They rarely say what they computed. Two packages
will both hand you "RSI(14)" and disagree, because one smoothed with Wilder's
1/n and the other with a 2/(n+1) exponential average, and neither wrote it
down. Every such choice here is stated in the entry, next to the formula, and
the entries also say what a factor does not do: one of them carries the
arithmetic showing it will not screen out gap risk, which is the thing people
reach for it to do.

The rule that earned its keep: at least one test per family compares against
something written outside the package. Four arithmetic defects once survived
279 self-consistent tests, because every test recomputed them faithfully from
the same wrong premise. Wilder's published example found all four in an
afternoon.

Python, pandas, MIT licensed. No data source, and there will not be one.

[vigil](https://github.com/LudwigJMarx/vigil), a self-hosted signal layer for
long-cycle B2B sales: a timeline per account, and a score built from the weight
and the age of what is on it.

A lead score out of a sales tool is a number you cannot argue with, which makes
it useless to the person deciding whether to write today. vigil returns the
contributions the total is made of, and names every signal kind it had no rule
for, so an account that is quiet and a scoring model that understood nothing do
not produce the same empty list. It sends no message on your behalf and makes no
request to LinkedIn; capture is a click, and the absence is enforced in CI
rather than promised in a README.

Go, SQLite, a Chrome extension in TypeScript. One static binary and one file,
Apache-2.0 licensed.

### How I work

**Reproduce before diagnosing.** A command or test that shows the failure comes
first, including when the cause looks obvious. Especially then.

**The failing test ships with the fix.** Red before, green after, both actually
run, with the output in the pull request. A suite nobody has tried to break is
a suite of unknown value, so I mutate the code and confirm it fails.

**Evidence over assertion.** What an issue thread claims is a claim. It gets
checked against the code, and where it turns out wrong, the rebuttal is part of
the contribution.

**The reasoning is part of the delivery.** Why this way and not the obvious
one, and what was discarded. That belongs in the commit body.

### Languages

TypeScript, Python, Go, Rust.

