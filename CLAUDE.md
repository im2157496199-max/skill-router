# Codex master-controller policy

For a new task without an explicitly named skill, invoke `skill-router` first.
The router selects the required skill sequence and executes it; it is not a
recommendation-only step. Explicit user-selected skills and an active workflow
take priority.
