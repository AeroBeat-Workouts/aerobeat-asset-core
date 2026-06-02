# AeroBeat Asset Core Downscope Alignment

**Date:** 2026-05-01  
**Status:** Stale  
**Agent:** Chip 🐱‍💻

---

## Goal

Align `aerobeat-asset-core` with the downscoped AeroBeat v1 asset truth so the repo clearly represents internal/shared asset concepts without reasserting the removed workout-package asset subset model.

---

## Overview

The parent polyrepo audit established an important distinction that now needs to be reflected in code and docs: AeroBeat still absolutely has internal/shared asset concepts — UI assets, environments, future avatars, future cosmetics/skins, and other controlled product-side assets — but the old workout-package `assets/` subset is no longer part of the authored package truth.

`aerobeat-asset-core` is therefore a high-risk contract surface. If it stays framed as generic package-asset infrastructure, it will keep reintroducing the wrong worldview into templates and downstream repos. This slice should identify where the repo still implies package-local gameplay asset bundling, then realign it toward the approved product-side/internal asset story without deleting legitimate future asset lanes.

---

## REFERENCES

| ID | Description | Path |
| --- | --- | --- |
| `REF-01` | Active plan for this repo-local cleanup slice | `.plans/2026-05-01-aerobeat-asset-core-downscope-alignment.md` |
| `REF-02` | Updated AeroBeat docs source of truth | `/home/derrick/.openclaw/workspace/projects/aerobeat/aerobeat-docs` |
| `REF-03` | Parent coordination plan and matrix | `/home/derrick/.openclaw/workspace/projects/openclaw-chip/.plans/2026-05-01-aerobeat-polyrepo-downscope-audit.md` |
| `REF-04` | Recently aligned content/tool surfaces | `/home/derrick/.openclaw/workspace/projects/aerobeat/aerobeat-content-core` |

---

## Tasks

### Task 1: Audit `aerobeat-asset-core` for stale downscope assumptions

**Bead ID:** `oc-7a9`  
**SubAgent:** `primary`  
**Role:** `research`  
**References:** `REF-01`, `REF-02`, `REF-03`, `REF-04`  
**Prompt:** Audit this repo against the updated docs and aligned contract surfaces. Identify stale asset-core assumptions such as generic workout-package asset subset truth, package-local asset bundling language, or abstractions/docs/examples/tests that fail to distinguish internal/product-side assets from removed authored package `assets/` concepts. Do not edit yet; produce an execution-ready list.

**Folders Created/Deleted/Modified:**
- `.plans/`
- `docs/`
- `src/`
- `tests/`

**Files Created/Deleted/Modified:**
- `.plans/2026-05-01-aerobeat-asset-core-downscope-alignment.md`
- `docs/**`
- `src/**`
- `tests/**`

**Status:** ✅ Complete

**Results:** Completed the stale asset-scope audit. Main finding: the repo is already largely aligned and has almost no tracked product surface beyond `README.md`. No tracked code/tests/examples/docs reassert the removed workout-package `assets/` model. The only useful follow-up is a narrow README clarification that explicitly distinguishes valid internal/shared product-side asset concepts (UI assets, environments, future avatars/cosmetics/skins) from the removed authored workout-package `assets/` subset model.

---

### Task 2: Apply the repo cleanup and scope alignment

**Bead ID:** `oc-7wq`  
**SubAgent:** `primary`  
**Role:** `coder`  
**References:** `REF-01`, `REF-02`, `REF-03`, `REF-04`  
**Prompt:** After the audit/action list is approved, update this repo so its shared asset-core contracts, docs, examples, and tests match the downscoped AeroBeat asset truth. Commit and push by default.

**Folders Created/Deleted/Modified:**
- `.plans/`
- `docs/`
- `src/`
- `tests/`

**Files Created/Deleted/Modified:**
- `.plans/2026-05-01-aerobeat-asset-core-downscope-alignment.md`
- `docs/**`
- `src/**`
- `tests/**`

**Status:** ⏳ In Progress

**Results:** Coder bead is now executing as a narrow README truth-lock pass: keep the repo framed around internal/shared product-side assets, explicitly state that authored workout-package `assets/` are no longer current contract truth, preserve environments as valid authored package content, and avoid implying the old package-local gameplay asset bundling model.

---

### Task 3: QA and audit the alignment

**Bead ID:** `oc-hq5` (QA), `oc-b6m` (Auditor)  
**SubAgent:** `primary`  
**Role:** `qa` then `auditor`  
**References:** `REF-01`, `REF-02`, `REF-03`, `REF-04`  
**Prompt:** Independently verify that this repo represents internal/shared asset concepts truthfully without reasserting the removed workout-package `assets/` subset model.

**Folders Created/Deleted/Modified:**
- `.plans/`
- `docs/`
- `src/`
- `tests/`

**Files Created/Deleted/Modified:**
- `.plans/2026-05-01-aerobeat-asset-core-downscope-alignment.md`
- `docs/**`
- `src/**`
- `tests/**`

**Status:** ⏳ In Progress

**Results:** QA pass completed with no fixes required and recommended auditor handoff. QA confirmed that `README.md` now clearly separates internal/shared product-side asset contracts from removed authored workout-package `assets/`, preserves `environments/` as valid authored package content, keeps future/internal lanes like UI assets, avatars, cosmetics, and skins intact, and avoids implying package-local gameplay asset bundling is still canonical. QA also confirmed this remained a narrow docs-only slice: the latest relevant commit `d20addb` changed only `README.md`, and no other tracked files reassert the removed package-asset worldview.

---

## Final Results

**Status:** ⚠️ Partial

**What We Built:** Draft repo-local plan for the next shared asset-scope cleanup slice.

**Reference Check:** Pending repo audit and execution.

**Commits:**
- None yet.

**Lessons Learned:** The product still has assets; what changed is where they belong in the contract. Shared asset repos must preserve that distinction explicitly.

---

*Completed on 2026-05-01*