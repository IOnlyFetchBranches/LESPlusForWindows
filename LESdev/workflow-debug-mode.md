# Workflow Debug Mode (Developer Playbook)

This project includes a reusable Workflow Debug Mode intended for feature development and troubleshooting.

## Goals

- Provide a single toggle that enables extra debug behavior across workflows.
- Make UI automation steps observable (where the script clicks and in what order).
- Keep debug instrumentation optional and safe for normal users.

## Current implementation

- Tray menu toggle label: `Workflow Debug Mode`
- Runtime flag variable: `workflowdebug`
- Persisted state file: `resources/workflow_debug.txt`
- Backward compatibility migration: reads legacy `resources/smartundo_debug.txt` if the new file is missing.

## Reusable debug helpers

- `ShowMatchDebugBox(x, y, w, h)`
  - Draws a temporary red overlay rectangle on screen.
  - Use for image-match hitboxes or point-of-action visualization.

- `DebugStep(message, delayMs := 220)`
  - Shows a transient tooltip and sleeps for a short delay.
  - Use when you need to watch each UI automation step in sequence.

- `TryImagePatternClickInActiveWindow(...)`
  - Reusable bounded image-search/click routine.
  - Supports multiple image permutations, scale/variation sweeps, mouse restore, and debug output.

## Integration pattern for new workflows

When adding debug support to a new automation routine, follow this sequence:

1. Gate debug behavior with `if (workflowdebug = 1)`.
2. Show target areas with `ShowMatchDebugBox(...)` before interaction.
3. Add `DebugStep("what happens next", delay)` between actions.
4. Preserve and restore user cursor position if mouse automation is used.
5. Keep non-debug flow fast and unchanged.

## Example (pattern only)

```ahk
if (workflowdebug = 1){
    ShowMatchDebugBox(targetX - 8, targetY - 8, 16, 16)
    DebugStep("Opening context menu", 250)
}

MouseMove, %targetX%, %targetY%, 0
Click, Right

if (workflowdebug = 1){
    DebugStep("Selecting menu item", 250)
}
SendInput {Down 2}{Enter}
```

## Debug UX recommendations

- Keep debug delays short (about 150 to 300 ms) to stay usable.
- Prefer overlays and tooltips over modal dialogs for step-by-step traces.
- Reserve `MsgBox` for success/failure summaries or critical diagnostics.

## Notes for future agents

- Before adding workflow-specific debug toggles, prefer reusing the global `workflowdebug` flag.
- Reuse existing helpers first; only add new helpers if the current ones cannot express the behavior.
- Keep changes additive and avoid refactoring unrelated systems during hotfix work.
