# Contributing to PM Skills

Contributions are welcome. Please read these guidelines before submitting a pull request.

## Before You Start

Open a GitHub issue to discuss your proposed skill or command. This prevents duplicate work and ensures the contribution fits the repository scope.

## Skill Standards

Every skill must:
- Have `name` and `description` in YAML frontmatter — `description` must be a quoted string
- Live in its own subdirectory: `skills/skill-name/SKILL.md`
- Include a `## Purpose` and `## Instructions` section in the body
- Use `$ARGUMENTS` as the placeholder for user input
- Not reference or reproduce content from other open-source repositories

## Naming Conventions

- Skills: lowercase kebab-case nouns (`prd-writer`, `user-personas`)
- Router commands (short skills that invoke a parent skill): lowercase kebab-case verbs (`write-prd`, `build-personas`)

## PR Process

1. Fork the repository
2. Create a branch: `feature/skill-name` or `feature/command-name`
3. Add the skill or command following the standards above
4. Open a pull request with a description of what it does and what gap it fills
5. Keep PRs focused — one skill or command per PR

## Code of Conduct

Be constructive in reviews. All contributors are listed in the README.
