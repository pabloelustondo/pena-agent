# E001 - GitHub Copilot Cleanup

## Branch

`experiment/github-copilot-cleanup`

## Purpose

Final repository cleanup pass after initial restructuring.
Focus on repository hygiene, documentation consistency, and experiment readiness.

## Tool Surface

GitHub Copilot in VS Code.

## Observed Models Used

- Claude Sonnet 4.6
- GPT-5.3-Codex

## What Changed

- Cleaned root surface to keep project-level files/folders only.
- Consolidated AI-agent guidance into `AGENTS.md`.
- Reduced `.instructions.md` to a compatibility pointer.
- Verified and preserved canonical SDLC2 phase folders `01` through `11`.
- Added placeholder `README.md` files for lifecycle visibility where needed.
- Moved product domain/assumptions/constraints/tools docs into `docs/product/context/`.
- Kept SDLC2 methodology references under `docs/sdlc2/`.
- Ensured historical artifacts are under `docs/history/`.

## What Required Human Review

- Whether empty SDLC2 lifecycle folders should remain visible.
- Whether context docs belong under product context or SDLC2 methodology context.
- Final judgment on what belongs in root versus history archives.

## Lesson Learned

This experiment evaluates AI-assisted development workflows, not isolated LLM models.
