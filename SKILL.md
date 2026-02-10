---
name: plan-naming-conventions
description: use this skill whenever creating a new plan file.
---

# Plan Naming Conventions

Use this skill whenever creating a new plan file.

## File Name Format

```
plan:{#####}:{description}.md
```

- `{#####}` — Zero-padded, 5-digit, auto-incremented number. Check existing plan files in the target directory to determine the next number.
- `{description}` — Short, lowercase, hyphen-separated description of the plan.

## Steps

1. List existing plan files matching the `plan:*` pattern in the target directory.
2. Find the highest `{#####}` number.
3. Increment by 1 and zero-pad to 5 digits.
4. Create the file as `plan:{next_number}:{description}.md`.
