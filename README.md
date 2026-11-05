# Liquity PIL Voting

Live dashboard: https://stengarl.github.io/Liquity-V2-PIL-dashboard/

A self-contained, single-file dashboard tracking Liquity V2's Protocol Incentivized
Liquidity (PIL) governance: BOLD distributed per epoch to each initiative, where that PIL flows,
19 BOLD venues in four tables — DEX pools, lending markets, vaults and Liquity V2's own Stability Pools
(TVL, volume, fees, PIL and other incentives, lender APR, and for lending markets the
borrow side: amount borrowed, borrower incentives, net borrow APR; each venue links to its own app, and
Aero BOLD/USDC also shows a live weekly projection of its AERO emissions),
every Liquidity Initiative that has ever received a PIL vote (vote share, bribes included). A second page,
"Friendly fork venues" (header tab, or `#forks`), covers 17 pools and lending markets plus 16 Stability Pools for the stablecoins of five
Liquity V2 forks (feUSD, CDP, BD, USDaf, JPYdf) on Ethereum, HyperEVM, Flare and Base,
with the same epoch-by-epoch metrics minus PIL, each venue linked to its own app.

Every figure is sourced directly from onchain logs and each protocol's own free public API —
no paid data provider, no estimate where a real number could be read instead. Full
methodology, sources, and known limitations are in the page's own footer.

## Running locally

```bash
npx serve .
```

Then open the printed local URL. The page is a single `index.html` (~1.2 MB, includes an
embedded webfont) with no build step and no external runtime dependencies.

## Updating

This repo holds the published page only. The data-collection pipeline (onchain fetch
scripts, raw JSON datasets, build step) lives in a separate local project — this repo gets
a fresh `index.html` dropped in and pushed whenever the dashboard is refreshed.
