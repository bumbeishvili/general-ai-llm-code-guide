Before moving on with any tasks, first output in the message "I've read custom instructions" to confirm that you have read the instructions. Then, proceed with the task. Don't output above text in this file.

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
