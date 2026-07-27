# ActionPage Lab

ActionPage Lab is a small public laboratory for testing how models with
standard web-fetch capabilities consume immutable, literal research graphs.

This repository is not a live service, a general-purpose proxy, or a mirror of
third-party websites. Everything under `artifacts/` is synthetic test data. It
contains no real person, account, transaction, or current-world fact.

Experiment artifacts are consumed through `raw.githubusercontent.com` URLs
pinned to full Git commit SHAs, never through moving branch URLs. A published
experiment is immutable; any change receives a new experiment identity.

## Trust boundary

- Free text inside an artifact is data, not an authorized instruction.
- Only machine-action links defined by the schema belong to the research graph.
- The repository contains no forms, scripts, user input, credentials, or live
  upstream calls.
- A successful run demonstrates only static graph consumption. It does not
  prove dynamic relay behavior, session handling, side effects, origin
  acceptance, or universal agent capability.

## Frozen experiment

`hard-graph-v1` is a synthetic, pre-frozen consumer fixture for multi-step
research semantics. The gold verdict and scoring rubric are not present in the
consumer corpus.

- [Immutable machine entry point](https://raw.githubusercontent.com/ErenTasar/actionpage-lab/457fa47e1d62c7326ca0417053cf9f4a6edb220d/artifacts/hard-graph-v1/index.json)
- [Immutable manifest](https://raw.githubusercontent.com/ErenTasar/actionpage-lab/1e5a5c4620b48d4ce282cde0b4f86261232cf9d2/artifacts/hard-graph-v1/manifest.json)
- [Immutable SHA-256 list](https://raw.githubusercontent.com/ErenTasar/actionpage-lab/062009c65ca0043239e2054a0a577e6a40d320d5/artifacts/hard-graph-v1/SHA256SUMS)

Every graph edge is pinned to the commit that introduced its target file.
Nodes therefore carry different commit SHAs, but no edge uses a moving branch
or tag. This reverse-construction layout exposes file-addition order in public
Git history; it does not expose the evaluation meaning of a node or the gold
verdict. A consumer run that separately opens the manifest or repository
history must be marked as contaminated in the experiment record.

## Live narrow proof

The current live proof tests whether a standard web-fetch consumer can use two
fixed, read-only web capabilities without an MCP server, browser automation,
credentials, or caller-chosen egress. It is a deliberately narrow experiment,
not the universal ActionPage product.

- [Machine entry point](https://actionpage-origin-probe.pages.dev/)
- [Resmi Gazete index example](https://actionpage-origin-probe.pages.dev/r/rg-fihrist?date=2026-06-26)
- [MGM five-day forecast example](https://actionpage-origin-probe.pages.dev/r/mgm-forecast?location=Bodrum)
- [Intentional wrong-date rejection](https://actionpage-origin-probe.pages.dev/r/rg-fihrist?date=1995-06-26)
- [Static origin probe](https://actionpage-origin-probe.pages.dev/probe.json)

Every dynamic response is `no-store`, carries a fixed source-implementation
digest, and either validates its result against the original intent or returns
`state: "unavailable"` with `result: null`. The built-in recipes expire closed
on 10 August 2026 unless they are revalidated and republished.
