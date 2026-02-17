# LiteLizard MVP Acceptance Checklist v2

Source of truth: `/Users/jane/.codex/worktrees/49de/liteLizard/docs/LiteLizard_spec_v2_draft.md`

## Functional checks
- [ ] 1. Open folder and display `.md` files in explorer tree.
- [ ] 2. Create a new `.md` document and load it into editor.
- [ ] 3. New paragraph creation generates a unique persistent `paragraphId`.
- [ ] 4. Drag-and-drop paragraph reorder updates in-memory order and keeps `paragraphId` unchanged.
- [ ] 5. Analysis pane stays aligned by `paragraphId` after reorder.
- [ ] 6. Global analysis button runs document-level analysis.
- [ ] 7. Local analysis button reruns only target paragraph analysis.
- [ ] 8. Analysis result renders `paragraphId / meaningRelative / readerReactionPrediction / order`.

## Save and persistence checks
- [ ] 9. Without explicit save, disk files are unchanged.
- [ ] 10. On explicit save, both `.md` and `.litelizard.analysis.json` are updated atomically.
- [ ] 11. Closing editor without save restores prior disk state.

## Security and API checks
- [ ] 12. Logged-out users cannot execute analysis.
- [ ] 13. No user API key input exists in settings UI.
- [ ] 14. Client sends analysis requests only to product server API.
- [ ] 15. Auth failure or request failure shows retry guidance and preserves existing persisted analysis.

## Quality checks
- [ ] Unit tests pass for paragraph ID persistence, reorder behavior, and save gating.
- [ ] Unit tests pass for analysis JSON schema validation.
- [ ] Desktop tests pass for login-gated analysis flow.
- [ ] E2E smoke test covers global and local analysis triggers.
