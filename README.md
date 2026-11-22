# Ludwig J. Marx

I test trading rules against chance, and I build the backend code that runs the tests.

Most backtests look better than the strategy behind them. A filter drops data
without a message. A hedge is counted from before the fill. A data vendor
changes how it counts volume, and a filter starts to trade the data instead of
the market. I look for these errors before I trust a number, in my own research
and in other people's code.

**Quant research · Backend in Python, Go, Rust and R**
[ludwigjmarx.com](https://ludwigjmarx.com) · [ludwig@ludwigjmarx.com](mailto:ludwig@ludwigjmarx.com)

## Research

I register each study before the first run: rule family, measure and pass
criterion. A test sample stays closed until the rule is fixed. QuantConnect
computes every reported number again, with real orders where the rule trades.
Failed tests stay in the paper.

| No. | Working paper | What holds | Code |
| --- | --- | --- | --- |
| 01 | The Opening Gap and Intraday Breakouts in Nasdaq-100 Futures | 16.8% a year with real orders in Micro Nasdaq-100 futures from 2020 to 2026. The rule fails the registered hurdle and loses money in the test sample 2015 to 2019. | [quant-research](https://github.com/LudwigJMarx/quant-research/tree/main/wp01-opening-gap-breakouts) |
| 02 | Trend Filtering with a Band Indicator | A weekly trend filter cuts the largest loss of the S&P 500 from −55% to −34%. Its return edge is not proven, and outside the US it trails simple moving averages. | Not published. The indicator is proprietary. |

## Track record

I run a public portfolio on eToro as a Popular Investor. The platform measures
the numbers, not me.

## Open source

Maintainers merged these fixes into their projects:

| Project | What went wrong | Language |
| --- | --- | --- |
| [laya](https://github.com/NandhaKishorM/laya/pulls?q=is%3Apr+author%3ALudwigJMarx+is%3Amerged) ![stars](https://img.shields.io/github/stars/NandhaKishorM/laya?style=flat-square&label=%E2%98%85&labelColor=21262d&color=e3b341) | Three fixes. Any line that started with a sign-off word counted as the start of a signature, so everything after it got cut. The research scripts computed the repo root one level too short. One function was defined twice, and the two copies could drift apart without any test noticing. | Python |
| [ezBookkeeping](https://github.com/mayswind/ezbookkeeping/pulls?q=is%3Apr+author%3ALudwigJMarx+is%3Amerged) ![stars](https://img.shields.io/github/stars/mayswind/ezbookkeeping?style=flat-square&label=%E2%98%85&labelColor=21262d&color=e3b341) | Two fixes. Monthly schedules counted from the end of the month ignored the template's time zone. Edit-scope tests went red or green depending on where you ran them. | Go |
| [bevy_replicon](https://github.com/simgine/bevy_replicon/pull/764) ![stars](https://img.shields.io/github/stars/simgine/bevy_replicon?style=flat-square&label=%E2%98%85&labelColor=21262d&color=e3b341) | Seven places read a size out of a network message and trusted it. One truncated packet took the client down. | Rust |
| [Mustang](https://github.com/ZUGFeRD/mustangproject/pull/1276) ![stars](https://img.shields.io/github/stars/ZUGFeRD/mustangproject?style=flat-square&label=%E2%98%85&labelColor=21262d&color=e3b341) | One payment term the importer could not parse stopped the import of the whole e-invoice. | Java |
| [ifc-lite](https://github.com/LTplus-AG/ifc-lite/pull/4900) ![stars](https://img.shields.io/github/stars/LTplus-AG/ifc-lite?style=flat-square&label=%E2%98%85&labelColor=21262d&color=e3b341) | The parser pointed its worker URL at a file the package doesn't ship. | TypeScript |

## How I work

In research, I write the test down before I read the data. A second platform
with its own data and execution checks every result trade by trade.

In code, I first make the bug happen on my machine. Then I write a test that is
red before the fix and green after, and I run both. The diff stays on the
problem. The pull request gets the commands and the output. It also says why I
didn't take the obvious route, so you can check the work instead of trusting me.

## Background

Seven years in banking and financial advice, among them private banking and
investment advice at a savings bank. Before that, ten years of IT and SAP
operations in the German armed forces.
