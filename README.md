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

1. **Always double-check** AI suggestions
2. Iterate on `.github/copilot-instructions.md` and other system prompts
3. Review every bash command
4. Reference: https://code.visualstudio.com/docs/copilot/copilot-customization
5. Use the # feature to point to specific files
6. Use only `uv run python -c ...` and `bash` commands for testing and validation of each feature
7. CMD+I and CMD+K,CMD+W are your friends
8. Remove unnecessary tools from agent mode to avoid confusing the agent
9. Use the #fetch function for precise fetching of documentation
10. Stay current with podcasts (e.g., OpenAI, Anthropic, Google Developer, Lex Fridman, Lenny's Podcast)
11. When starting a greenfield project, provide clear architecture guidance (e.g., DDD, Vertical Slice Architecture, Clean Code Uncle Bob Style)
12. Lint and format aggressively using pre-commit
13. Use gitingest and a long-context LLM to get guidance on high-level state and potential future directions
14. Pay attention to usage limits