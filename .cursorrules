# AI & Developer Rules for Horror House Escape 🤖

This document outlines the standard operating procedures, rules, and expectations for any developer or AI Agent contributing to the **Horror House Escape** repository.

## 1. Authentication & GitHub CLI (`gh`)

The primary way we interact with issues and the project board from the terminal is via the GitHub CLI. 

If `gh` commands are failing with scope or authentication errors:
1. Ensure the user has run `gh auth login` or the appropriate auth refresh command.
2. If accessing or adding items to the **GitHub Project Board**, the CLI must have the **`project`** scope (not just `read:project`).
   - Run: `gh auth refresh -s project`
   - The user will need to authenticate this via their browser using the provided device code.

## 2. Issue Tracking & The Project Board

- **Always Create Issues First:** When starting a new feature, bug fix, or map addition, an Issue must be created representing that work.
- **Link To Project:** Once the Issue is created, it **MUST** be added to the project board ([Project #1](https://github.com/users/HuXu77/projects/1)).
  - Retrieve the issue URL (e.g., `https://github.com/HuXu77/HorrorHouseEscape/issues/X`).
  - Use the CLI to add it: `gh project item-add 1 --owner "HuXu77" --url "<ISSUE_URL>"`

## 3. Workflow & Board Columns

Depending on the type of work, follow these rules:
- **Scripts & Coding:** Needs to be tracked, committed to Git, and ideally reviewed. Move the ticket to `In Progress`, and upon completion, move to `Review / Testing`.
- **Studio Building / Human Tasks:** Things like placing models, baking lighting, or creating UI layouts that can't be easily version-controlled via text files should be noted as `To Do (Studio / Human)`. These don't require Pull Requests and can be moved straight to `Done` once verified in Studio.

## 4. Code Principles (Luau)

- **Readability:** Keep scripts clean, modular, and heavily commented. This is a collaborative project, and code needs to be easily understood by humans and AI alike.
- **Performance:** Pathfinding and monster logic should be optimized to prevent server lag.
- **Security:** Ensure any sensitive logic (e.g., unlocking doors, taking damage, winning) is handled on the **Server** (ServerScriptService) and not the Client, to prevent exploiters.
