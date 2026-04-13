Before moving on with any tasks, first output in the message "I've read custom instructions" to confirm that you have read the instructions. Then, proceed with the task. Don't output above text in this file.

> **Project context:** See [ABOUT.md](ABOUT.md) for project overview, tech stack, structure, and key details.

# AI Code Guide

## Rules *(unless user suggests otherwise)*

1. **No Repetition** - Extract logic into functions
2. **No Hard Coding** - Use variables, read from data sources
3. **No VS Code Browser** - Don't run/build projects
4. **No JS→TS Conversion** - Don't fix TypeScript issues
5. **Single Task Focus** - Don't volunteer extra fixes
6. **Embrace Uncertainty** - It's okay to not know everything
7. **Prefer map over forEach** - Use functional programming patterns
8. **Use library functions** - If included, prefer d3.sum, d3.groups, d3.mean over native alternatives
9. **String matching** - Prefer direct equality for known values over includes
10. **Preserve defaults** - Don't modify default values unless specifically asked
11. **Data & State Management** - Preserve existing data flow, reactive statements, transformation chains and add new functionality without disrupting existing patterns
12. **Variable renaming** - Only update actual variable names and identifiers, not string literals, text content, or display text
13. **Lint handling** - Don't automatically fix lint warnings unless explicitly requested, focus on user's actual request over style suggestions
14. **No overly defensive programming** - don't favour usage of try catch blocks and if's unless absolutely certain application could break, even then, descriptive errors are better to catch the source issue, compared to missing errors in try/catch blocks
15. **production quality** No shortcuts, make sure to write production quality code unless asked otherwise
16. **Understandable code** Try to write the code in a way, it to pass senior developer review, but can be understood by junior developer
17. **No running scripts directly** - Don't execute Python scripts or data processing code directly via command line. Update the notebook and let the user run it themselves. Notebook cell execution is fine. Reason: the user needs to see outputs inline, catch errors immediately, and have a documented record of what was run and what it produced. Running scripts silently hides all of that.
18. **Analyze before fixing** - Read logs and data carefully before diagnosing issues. Don't assume the root cause — verify it. If a fix turns out to be based on a wrong assumption, roll it back immediately instead of leaving incorrect changes in the code.

## Shared components

- **Dashed-dot icon** (small dashed-stroke circle used as section markers, e.g. next to "Why this matters" on the landing page and the description heading on Public Servant Pulse): always use `<DashedDot />` from `$lib/DashedDot.svelte`. Do NOT inline the SVG. Reason: this keeps the mark consistent across pages — previously it was copy-pasted in multiple places and kept drifting.

## Figma

- Figma MCP server (`figma-remote-mcp`) is available and authenticated via OAuth
- If authentication expires, re-authorize by calling `mcp__figma-remote-mcp__authenticate` — user will need to open the returned URL in their browser
- Extract `fileKey` and `nodeId` from Figma URLs: `figma.com/design/:fileKey/:fileName?node-id=:nodeId` (convert `-` to `:` in nodeId)
- Use `get_design_context` as the primary tool for reading designs, `get_metadata` for structure overview, `get_screenshot` for visual verification
