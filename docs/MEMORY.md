# Project Memory: Pacwin

## Status: v0.4.0 (Stabilization Phase)
- **Current Goal:** Refine the UI/TUI experience and enhance telemetry/diagnostics.
- **Last Milestone:** Fixed Scoop detection (sfsu hook support) and improved concurrent search performance.

## Persistent Context
- **Stack:** PowerShell (Advanced Functions, Runspaces, JSON Serialization).
- **Core Files:** `pacwin.psm1` (Logic), `pacwin.psd1` (Manifest), `docs/` (Standards).

## Active Tasks
- [ ] Implement UI Rebrand (MonolithUI style for TUI elements).
- [ ] Enhance diagnostic `doctor` command for deep-dive environment analysis.
- [ ] Prepare for v0.5.0 release.

## Technical Debt
- Some legacy parsers need refactoring for better locale independence.
- Pester test suite requires better coverage for edge-case installation failures.

## Notes
- *2026-05-18:* Jules Dev Standard applied. Documentation consolidated in `docs/`. Previous `wiki/` and `AGENTS.md` to be decommissioned.