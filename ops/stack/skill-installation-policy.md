# Skill Installation & Invocation Policy

## Default behavior
For recurring production tasks, install and wire required skills/tools proactively after safety checks.
Do not wait for repeated manual reminders.

## Safety gate
Before installing third-party skills:
1. Source vetting (repo credibility, active maintenance)
2. Script/installer scan for risky permission changes
3. Least-privilege install path
4. Record findings in ops notes

## Invocation rule
When delegating a task, explicitly include required skill/tool in the execution instruction.
Example:
- `Use openai-image-gen for visual generation`
- `Use yt-repurpose-studio pipeline for script->render package`
