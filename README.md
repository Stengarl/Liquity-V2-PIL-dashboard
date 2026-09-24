# Liquity PIL Voting

Live dashboard: https://stengarl.github.io/pil-voting-dashboard/

A self-contained, single-file dashboard tracking Liquity V2's Protocol Incentivized
Liquidity (PIL) governance: weekly vote-share evolution across all initiatives, BOLD
distributed per epoch, 16 BOLD liquidity pools/vaults (TVL, volume, fees, PIL, APR), and
every Liquidity Initiative that has ever received a PIL vote (bribes included).

Every figure is sourced directly from onchain logs and each protocol's own free public API —
no paid data provider, no estimate where a real number could be read instead. Full
methodology, sources, and known limitations are in the page's own footer.

## Running locally

```bash
npx serve .
```

Then open the printed local URL. The page is a single `index.html` (~515 KB, includes an
embedded webfont) with no build step and no external runtime dependencies.

## Updating

This repo holds the published page only. The data-collection pipeline (onchain fetch
scripts, raw JSON datasets, build step) lives in a separate local project — this repo gets
a fresh `index.html` dropped in and pushed whenever the dashboard is refreshed.
