# US timely filing limits

This is a CSV of claim timely filing limits for US health payers, with a source link for every value. It covers Medicare, Medicaid fee-for-service in all 50 states and DC, TRICARE, VA Community Care and five large commercial payers. Each row gives the initial claim limit, the corrected claim or resubmission limit where the source states one, and the first-level appeal limit where the source states one.

Every value was copied from an official government page or the payer's own provider manual or provider site, then checked on the date in `source_date_checked`. If a value couldn't be confirmed from a source that opened, it's left blank and the row is marked `unverified`. Nothing here is estimated.

## Files

| File | What it contains |
|---|---|
| `timely-filing-limits.csv` | The data: 60 rows, 56 verified and 4 unverified |
| `medicare-appeal-levels.md` | Medicare's five appeal levels, with deadlines and the 2026 and 2027 amount-in-controversy thresholds |
| `CONTRIBUTING.md` | How to fix or add a row |
| `LICENSE` | CC BY 4.0 |

## Columns

| Column | Meaning |
|---|---|
| `payer` | Payer or program name |
| `state` | Two-letter state code. `US` means a federal program or a national payer policy |
| `plan_type` | For example Medicare Part A/B, Medicaid FFS or Commercial |
| `initial_claim_limit` | Deadline for the first submission of a claim, in the source's own wording |
| `corrected_claim_limit` | Deadline for a corrected, replacement or resubmitted claim, if the source states one |
| `appeal_limit` | Deadline for the first-level appeal or reconsideration, if the source states one |
| `source_url` | The page or document the values came from |
| `source_date_checked` | The date the source was last read (YYYY-MM-DD) |
| `notes` | Exceptions, the start of the clock, and how old or official the source is |
| `status` | `verified` or `unverified` |

A blank cell means the checked source didn't state that value. It doesn't mean there's no limit.

## Before you rely on a row

- **Commercial and Medicare Advantage limits are set by your contract and by state law.** The commercial rows only show the default each payer publishes, and that default can be different in your state, your network or your provider agreement. Your participation agreement always comes first.
- **Medicaid managed care plans set their own limits.** The state rows cover fee-for-service Medicaid only.
- **Check where the clock starts.** Some limits run from the date of service, some from the discharge or "through" date, some from the end of the month of service, and some from the date on a prior EOB or remittance advice. The `notes` column says which, when the source says.
- **Some sources are old or secondary.** Where the newest available source is an older manual or bulletin, or a copy of the regulation hosted by Cornell's Legal Information Institute, the notes say so.
- Rules change. Check the `source_date_checked` date and open the source before you file.

### Unverified rows

These four rows have blank values because a usable official source couldn't be opened or found on the check date:

- MaineCare (ME): the MaineCare Benefits Manual Chapter I, section 1.10 text couldn't be retrieved.
- Utah Medicaid (UT): the official site denied access.
- Aetna (commercial): the public provider manual has no general filing limit.
- Humana (commercial): the 2026 provider manual has no general filing limit.

A pull request with an official source fixes any of these. See `CONTRIBUTING.md`.

## Tools

Free calculators that use the same federal rules:

- [Timely filing and appeal deadline calculator](https://medicalbilling101.com/tools/timely-filing-calculator/)
- [Appeal letter generator](https://medicalbilling101.com/tools/appeal-letter-generator/)
- [RVU calculator](https://medicalbilling101.com/tools/rvu-calculator/)
- [Global period calculator](https://medicalbilling101.com/tools/global-period-calculator/)

Guides:

- [How to appeal a denied Medicare claim](https://medicalbilling101.com/how-to-appeal-a-denied-medicare-claim/)
- [Corrected claim resubmission guide by payer type](https://medicalbilling101.com/corrected-claim-resubmission-guide-step-by-step-instructions-for-corrected-claims-by-payer-type/)

## Disclaimer

This dataset is general reference information. It isn't legal, billing or compliance advice. Filing limits change, and the binding limit for any claim is in your payer contract, the payer's current provider manual, state law and federal regulation. Check the source before you file or write off a claim. The maintainers accept no liability for claims denied based on this data.

## License and attribution

The data and documents are licensed under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/). You can reuse them, including commercially, if you credit the source:

> US timely filing limits, compiled by Manikandan J, CPC, CRCR (Medical Billing 101, https://medicalbilling101.com). CC BY 4.0.

The underlying regulations and government publications are public. This license covers the compilation and the notes.

## Maintainer

Manikandan J, CPC, CRCR, founder of [Medical Billing 101](https://medicalbilling101.com). Please send corrections as an issue or pull request.
