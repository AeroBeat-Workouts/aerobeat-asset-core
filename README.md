# aerobeat-asset-core

Shared AeroBeat asset-side contracts such as avatars, cosmetics, environments, and other reusable asset definitions.

## Architecture role

`aerobeat-asset-core` is the lane owner for reusable asset contracts. It gives the platform one dependency-light home for shared asset definitions without forcing those concerns into feature, UI, or content repos.

## Intended consumers

Asset packs, feature repos, UI repos, and assemblies should depend on this repo when they need stable asset-side definitions or validation contracts.

## Repository status

This repo is the canonical home for shared asset-lane contracts in the six-core AeroBeat architecture. Keep the public surface centered on reusable asset definitions and asset validation boundaries rather than turning the repo into a generic project bucket.
