# Contributing

Corrections and new rows are welcome. A change can only be accepted if someone else can check it.

## Every change needs

1. **An official source URL.** This means a federal or state regulation, a state Medicaid provider manual or bulletin, or the payer's own provider manual or provider website. Blog posts, billing company articles, forum posts and AI answers aren't accepted.
2. **The wording the source uses.** Copy the limit as the source states it (for example "365 days from the date of service"). Don't round "90 days" to "3 months".
3. **The date you checked**, in `source_date_checked` (YYYY-MM-DD).
4. **Any exceptions** in `notes`: where the clock starts, claim types it doesn't cover, or a different limit for out-of-state providers or for claims with Medicare or other insurance as primary.

## Rules

- If the source doesn't state a value, leave the cell blank. Don't fill it in from memory or from another payer.
- Set `status` to `verified` only when you read every value in the row in the linked source.
- Commercial rows show the payer's published default. Don't add limits from a specific provider contract.
- Put one source in each row. If the corrected claim limit or appeal limit comes from a different document, name that document in `notes`.

## How to submit

Open a pull request that edits `timely-filing-limits.csv`. In the description, quote the sentence from the source that supports the change. If you can't open a pull request, open an issue with the same information.
