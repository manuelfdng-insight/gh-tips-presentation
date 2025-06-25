Set up all **#file:Insight_Ingenious** features in the top-level directory by installing the Ingenious library at the project root. Proceed iteratively until every feature provided by the `ingen` CLI is fully functional.

### Guidelines

- You may debug and modify the Ingenious library as needed to ensure all features work as intended.
- Use only `uv run python -c ...` and `bash` commands for testing and validation of each feature.
- **Do not** test any Scrapfly functionality.
- Create a comprehensive `PLAN.md` that outlines:
    - Each step, checkpoint, and test.
    - Strict adherence to this plan until all features are implemented, debugged, and verified.
- As you proceed, document:
    - Issues encountered
    - Configuration notes
    - Code modifications
    - Troubleshooting steps
- Temporarily mock all external services. Use the web search tool to verify the accuracy of your mocks.