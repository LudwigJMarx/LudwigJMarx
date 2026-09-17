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

[Talveo](https://github.com/LudwigJMarx/talveo), an application tracker for job
seekers, built around a matching score that can be recomputed and contested
rather than trusted.

Asking a language model "how well does this CV fit, 0 to 100?" gives you a
number nobody can recompute or challenge. Talveo splits the work. A model reads
the posting and judges each requirement on its own. A deterministic stage then
turns those judgements into a score. Same input, same result, including after a
model change.

TypeScript, Next.js, Postgres, MIT licensed.

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

