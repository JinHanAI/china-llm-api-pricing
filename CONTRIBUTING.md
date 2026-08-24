# Contributing

Thanks for helping keep Chinese LLM API prices accurate.

## Price changes (the main contribution)

1. Open the vendor's official pricing doc (or a dated third-party snapshot like OpenRouter) and confirm the new number.
2. Edit `china-llm-api-pricing.json` — update the price AND `asOf` if every entry was re-checked, and make sure `source` points to the page you used.
3. PR description must contain the source link. **PRs without a verifiable source will not be merged.**
4. If a number can't be verified, set it to `null` and add a `note` — never guess.

## Scope rules

- **Official list prices only.** Relay, reseller, or negotiated-markup prices are out of scope.
- Cached-input prices, context windows, and GA status belong in their fields, not the note.
- New models are welcome once their official API is GA (not rumor, not waitlist).

## Everything else

Typos, schema improvements, README table fixes — normal PR, no special requirements.

## Cadence

The maintainers re-verify all entries monthly (first week of the month).
