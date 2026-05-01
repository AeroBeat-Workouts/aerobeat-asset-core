# aerobeat-asset-core

Shared AeroBeat asset-side contracts for internal and shared product assets such as UI assets, environments, avatars, cosmetics, skins, and other reusable asset definitions.

## Architecture role

`aerobeat-asset-core` is the lane owner for reusable product-side asset contracts. It gives the platform one dependency-light home for shared asset definitions without forcing those concerns into feature, UI, or content repos.

This repo is about internal/shared product asset truth. It is **not** the canonical home for authored workout-package `assets/`, and it should not imply that package-local gameplay asset bundling is part of the current contract.

## Relationship to authored content packages

The active authored package contract lives elsewhere. Authored workout packages still validly carry package content such as songs, charts, sets, workouts, coaches, and `environments/`, but legacy authored package `assets/` content is no longer current contract truth.

That means environments remain valid authored package content while broader product-side asset lanes such as UI assets, avatars, cosmetics, and skins remain shared/internal asset concerns represented by this repo.

## Intended consumers

Feature repos, UI repos, assemblies, and other product-side systems should depend on this repo when they need stable shared asset definitions or validation contracts.

## Repository status

This repo is the canonical home for shared asset-lane contracts in the six-core AeroBeat architecture. Keep the public surface centered on reusable product-side asset definitions and asset validation boundaries rather than turning the repo into a generic project bucket or reintroducing removed package-local gameplay asset bundling as canonical truth.
