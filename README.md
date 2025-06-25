# GitHub Copilot Tips Presentation

## Prerequisites

- Python 3.13+
- uv
- git

## Setup

### Initial Project Setup

1. Add `.github/copilot-instructions.md`

2. Initialize the application:
   ```bash
   uv init --app
   ```

3. Add Mac and Windows specific files to auto-generated .gitignore

4. Add `.pre-commit-config.yaml`

5. Install pre-commit:
   ```bash
   uv add pre-commit
   uv run pre-commit install
   ```

### Installing Insight Ingenious

1. Clone the repository:
   ```bash
   git clone https://github.com/Insight-Services-APAC/Insight_Ingenious.git
   ```

2. Add as dependency:
   ```bash
   uv add ./Insight_Ingenious
   ```

3. Set up the cloned repository:
   ```bash
   cd Insight_Ingenious
   uv sync
   uv run pre-commit install
   uv run pre-commit run --all-files
   cd ..
   ```

## Copilot Tips

### Core Principles

1. **Always double-check** AI suggestions. Especially bash commands.
2. Iterate on `.github/copilot-instructions.md` and other system prompts (https://code.visualstudio.com/docs/copilot/copilot-customization)
3. When starting a greenfield project, provide clear architecture guidance (e.g., DDD, Vertical Slice Architecture, Clean Code Uncle Bob Style)
4. Lint and format aggressively using pre-commit

### Essential Shortcuts & Features

5. CMD+I and CMD+K,CMD+W are your friends
6. Use the # feature to point to specific files. You can also use #codebase which is the same as @workspace. Also add relevant tools to the task in context for Agent Mode.
7. Use the auto-create commit message functionality to generate started commit messages

### Tools & Extensions

8. Set up the web search tool with Tavily and also use the #fetch function for precise fetching of documentation
9. Remove unnecessary tools from agent mode to avoid confusing the agent. Watch out for auto-injected prompts by Copilot extensions.

### Agent Management

10. Steer the agent as needed
11. Use only `uv run python -c ...` and `bash` commands for testing and validation of each feature
12. Refine prompts using github.com/copilot
13. Ask the agent to double check that the docs and comments it made are actually aligned to the codebase

### High-Level Strategy

14. Use gitingest and a long-context LLM to get guidance on high-level state and potential future directions
15. Pay attention to usage limits

### UI Development

16. Use screenshots to create UI code. Make sure to specify your CSS and JS stack.

### Staying Current

17. Stay current with podcasts (e.g., OpenAI, Anthropic, Google Developer, Lex Fridman, Lenny's Podcast)

## General LLM Code Gen Tips

- Use well-documented, highly used in public repo tech stacks (e.g. Flask, Django, FastAPI, React, Vue, Angular, Alpine)
- If one LLM can't do it, try another one
- Keep the context as clean as possible. Only keep what you need in there to avoid confusing the model.
