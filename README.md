# Skill Router — Codex Master Controller

`skill-router` makes skills transparent to the user: a plain-language request
is classified, the smallest appropriate skill chain is chosen, and the work is
then executed.

It is tailored for a Codex workflow and covers this companion library:

- AI film production, directing, storyboard, character, prop, scene, and
  ComfyUI-oriented generation skills;
- Blender scenes, assets, cameras, animation, rendering, and automation;
- mixed film-to-Blender workflows.

`AI-Cinematic-Director-Skill` is intentionally excluded from this controller.
It remains an independent repository and is used only when explicitly named.

## Behavior

1. Read the live available-skills inventory plus relevant project-local skills.
2. Match the request to the most specific available skill(s).
3. Resolve only real prerequisites.
4. Read selected instructions and execute the task.
5. State important assumptions and verify the result.

The router does **not** hardcode a stale skill catalogue, does not invent
unavailable skills, and does not stop at a proposed route when the user asked
for actual work.

## Install

Install this folder as a Codex skill using the platform's skill installer, then
make it your default session entry point. The actual list of available skills
remains controlled by Codex, so this router can select only skills exposed to
the current session.

## Important limitation

A repository alone cannot force Codex to run a skill on every message. It must
be installed and enabled in the Codex environment (or explicitly included by a
project's instructions). Once enabled, this router handles unlabelled tasks;
an explicit user skill selection always wins.
