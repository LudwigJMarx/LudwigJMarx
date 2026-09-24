# Ludwig J. Marx

I go looking for code that assumes something it never checks.

Most of the time nothing crashes. The number is just wrong. A monthly schedule
lands on the wrong day because nobody asked which time zone the month ends in.
An email reply shrinks to "Hi," because a greeting looked like a signature.
Sometimes it does crash: one short network packet, and the game client is gone.

The loud bugs get fixed because someone notices. The quiet ones stay and end up
in a report, a backtest or an invoice, and people make decisions on them.

That's how I got into this, actually. I trade on eToro as a Popular Investor and
wanted to know what a performance number is worth. Often less than it says. The
same question turned out to fit other people's code pretty well.

**Go, Rust & Python · Next.js** · open for contract and open-source work
[Portfolio](https://www.ludwigjmarx.dev) · [Contact](mailto:ludwig@ludwigjmarx.dev)

## Merged elsewhere

Maintainers took these into their projects:

| Project | What went wrong | Language |
| --- | --- | --- |
| [bevy_replicon #764](https://github.com/simgine/bevy_replicon/pull/764) | Seven places read a size out of a network message and trusted it. One truncated packet took the client down. | Rust |
| [laya #132](https://github.com/NandhaKishorM/laya/pull/132) | Any line starting with a sign-off word counted as the start of a signature, so everything after it got cut. | Python |
| [laya #133](https://github.com/NandhaKishorM/laya/pull/133) | The research scripts computed the repo root one level too short and failed on paths that don't exist. | Python |
| [ezBookkeeping #677](https://github.com/mayswind/ezbookkeeping/pull/677) | Monthly schedules counted from the end of the month ignored the template's time zone. | Go |
| [ezBookkeeping #678](https://github.com/mayswind/ezbookkeeping/pull/678) | Edit-scope tests went red or green depending on where you ran them. | Go |
| [ifc-lite #4900](https://github.com/LTplus-AG/ifc-lite/pull/4900) | The parser pointed its worker URL at a file the package doesn't ship. | TypeScript |

## How I work

First I make the bug happen on my machine. Then a test that is red before the
fix and green after, and I actually run both. The diff stays on the problem.
The PR gets the commands, the output, and why I didn't take the obvious route,
so you can check the work instead of trusting me.
