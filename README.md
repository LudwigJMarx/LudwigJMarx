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
| [laya](https://github.com/NandhaKishorM/laya/pulls?q=is%3Apr+author%3ALudwigJMarx+is%3Amerged) ![stars](https://img.shields.io/github/stars/NandhaKishorM/laya?style=flat-square&label=%E2%98%85&labelColor=21262d&color=e3b341) | Three fixes. Any line that started with a sign-off word counted as the start of a signature, so everything after it got cut. The research scripts computed the repo root one level too short. One function was defined twice, and the two copies could drift apart without any test noticing. | Python |
| [ezBookkeeping](https://github.com/mayswind/ezbookkeeping/pulls?q=is%3Apr+author%3ALudwigJMarx+is%3Amerged) ![stars](https://img.shields.io/github/stars/mayswind/ezbookkeeping?style=flat-square&label=%E2%98%85&labelColor=21262d&color=e3b341) | Two fixes. Monthly schedules counted from the end of the month ignored the template's time zone. Edit-scope tests went red or green depending on where you ran them. | Go |
| [bevy_replicon](https://github.com/simgine/bevy_replicon/pull/764) ![stars](https://img.shields.io/github/stars/simgine/bevy_replicon?style=flat-square&label=%E2%98%85&labelColor=21262d&color=e3b341) | Seven places read a size out of a network message and trusted it. One truncated packet took the client down. | Rust |
| [Mustang](https://github.com/ZUGFeRD/mustangproject/pull/1276) ![stars](https://img.shields.io/github/stars/ZUGFeRD/mustangproject?style=flat-square&label=%E2%98%85&labelColor=21262d&color=e3b341) | One payment term the importer could not parse stopped the import of the whole e-invoice. | Java |
| [ifc-lite](https://github.com/LTplus-AG/ifc-lite/pull/4900) ![stars](https://img.shields.io/github/stars/LTplus-AG/ifc-lite?style=flat-square&label=%E2%98%85&labelColor=21262d&color=e3b341) | The parser pointed its worker URL at a file the package doesn't ship. | TypeScript |

Pull requests to 12 more projects are still open, among them go-ethereum,
Ollama, Microsoft qlib, Umami and Hyperswitch.

## How I work

First I make the bug happen on my machine. Then a test that is red before the
fix and green after, and I actually run both. The diff stays on the problem.
The PR gets the commands, the output, and why I didn't take the obvious route,
so you can check the work instead of trusting me.
