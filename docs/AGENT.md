# Agent SOP: Pacwin Operations

## Operational Mandates
- **Single Source of Truth:** `pacwin.psm1` is the heart of the project.
- **Cross-Version Compatibility:** Every change must be tested in both PowerShell 5.1 (Desktop) and PowerShell 7+ (Core).
- **Concurrency Safety:** Ensure RunspacePools are properly disposed of and thread-safety is maintained in shared state.

## Core Workflows
1. **Adding a Parser:**
   - Locate the target manager's output format.
   - Implement a new `_pw_parse_<manager>` function.
   - Return a standardized `[PSCustomObject]`.
2. **Extending the CLI:**
   - Map the new functionality to both a verbose and a pacman-style flag.
   - Update the `docs/wiki/Command_Reference.md`.
3. **Bug Fixes:**
   - Reproduce with a Pester test in `tests/`.
   - Apply the fix in the orchestrator or specific wrapper.

## Security SOP
- **Sanitization:** All user input used in string-based command execution MUST be sanitized through the internal sanitization layer.
- **Path Validation:** Always use absolute paths or validated relative paths for system operations.

## Related Docs
- [Project Identity](./IDENTITY.md)
- [Project Soul](./SOUL.md)
- [Wiki Index](./wiki/index.md)