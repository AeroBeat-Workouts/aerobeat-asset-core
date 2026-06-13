# aerobeat-asset-core

Shared AeroBeat asset-side contracts for internal and shared product assets such as UI assets, environments, avatars, cosmetics, skins, and other reusable asset definitions.

## Architecture role

`aerobeat-asset-core` is the lane owner for reusable product-side asset contracts. It gives the platform one dependency-light home for shared asset definitions and validation boundaries without forcing those concerns into feature, content, UI, or tool repos.

## V1 scope stance

This repo is about internal/shared product asset truth, not the canonical authored workout-package model.

Within the active v1 architecture:

- product-side shared assets such as UI assets, avatars, cosmetics, skins, and reusable environment-side product assets belong here
- authored workout packages still validly carry songs, charts, sets, workouts, coaches, and `environments/`
- environments remain valid authored package content where the content lane teaches them
- legacy package-local gameplay `assets/` bundling is not current contract truth and should not be reintroduced here as if it were active v1 scope

## Lane boundaries

This repo intentionally owns:

- shared product-side asset DTOs, enums, and validation seams
- reusable asset definitions that multiple product repos may consume
- asset-lane vocabulary for internal/shared AeroBeat product surfaces

This repo intentionally does **not** own:

- authored workout-package schemas or package reference validation
- gameplay-mode/runtime rule contracts
- input-provider or UI interaction contracts
- app-specific tool workflow logic
- a generic dump bucket for every resource file in the ecosystem

## Current repository contents

Current checked-in content is intentionally minimal:

- the repo is presently a lane-definition and contract-home placeholder
- no broader runtime/testbed harness is checked in yet
- future checked-in code here should stay centered on shared product-side asset contracts rather than on package-local gameplay asset bundling

## Intended consumers

Feature repos, UI repos, assembly/shell repos, environment repos, and other product-side systems should depend on this package when they need stable shared asset definitions or validation contracts.

## Development and validation

Current validation for this README-normalization pass is intentionally lightweight:

- verify the README matches the shared six-core skeleton
- verify the wording keeps authored-content ownership in `aerobeat-content-core`
- verify the repo does not imply that removed package-local gameplay asset bundling is canonical v1 truth

At the moment, no repo-local hidden testbed or automated contract harness is checked in here.

## Repository status

This repo is the canonical home for shared Asset-lane contracts in the six-core AeroBeat architecture. Keep the public surface centered on reusable product-side asset definitions and asset validation boundaries rather than turning the repo into a generic project bucket or reintroducing removed package-local gameplay asset bundling as canonical truth.
