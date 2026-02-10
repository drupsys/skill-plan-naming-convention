# Plan Naming Conventions

A [Claude Code](https://docs.anthropic.com/en/docs/claude-code) skill that enforces a consistent naming convention for plan files. When creating a new plan file, Claude Code will automatically find the next auto-incremented number and apply the correct format.

## Install

Clone this repo into your Claude Code skills directory:

```bash
git clone git@github.com:drupsys/skill-plan-naming-convention.git ~/.claude/skills/plan-naming-conventions
```

Once installed, the `/plan-naming-conventions` skill is available in all your Claude Code sessions and is automatically invoked whenever you ask Claude Code to create a plan file.

## Naming Format

Plan files follow this pattern:

```
plan:{#####}:{description}.md
```

| Part | Description |
|---|---|
| `{#####}` | Zero-padded, 5-digit, auto-incremented number |
| `{description}` | Short, lowercase, hyphen-separated summary |

**Example:** `plan:00003:migrate-auth-to-jwt.md`

## How It Works

1. Lists existing `plan:*` files in the target directory
2. Finds the highest `{#####}` number
3. Increments by 1 and zero-pads to 5 digits
4. Creates the file as `plan:{next_number}:{description}.md`

## License

MIT
