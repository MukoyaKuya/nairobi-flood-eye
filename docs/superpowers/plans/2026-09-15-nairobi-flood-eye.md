# Nairobi Flood Eye Implementation Plan

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:subagent-driven-development (recommended) or superpowers:executing-plans to implement this plan task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Give Nairobi residents a recognizable map entry point and direct access to official warnings without implying the app issues alerts.

**Architecture:** Reuse the existing location catalogue and first-run template. Future warning ingestion remains a separate adapter and is outside this first increment.

**Tech Stack:** JavaScript, Cesium, Vite, Node.js 24 or 26.

**Spec:** [Nairobi Flood Eye design](../specs/2026-09-15-nairobi-flood-eye-design.md)

## Global Constraints

- Never present a simulated or unavailable flood condition as a live official alert.
- Keep upstream MIT attribution and review third-party data and asset terms before deployment.

---

### Task 1: Nairobi map entry point

**Files:** `src/locations.js`, `src/locations.test.mjs`

- [x] Add the Nairobi location, bounds, and five orientation points.
- [x] Validate it through the location tests.

### Task 2: Safety-focused first-run card

**Files:** `index.html`, `src/ui/templates/welcome.html`

- [x] Brand the page and first-run card.
- [x] Link to KMD and NDOC with a clear prototype caveat.
- [x] Verify the production build.

### Task 3: Product roadmap

**Files:** `docs/NAIROBI_FLOOD_EYE.md`

- [x] Define the next data, preparedness, and response features with provenance rules.
