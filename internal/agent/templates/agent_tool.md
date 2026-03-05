Launch a new task agent to execute a coding task. The task agent has full access to all coding tools: bash, edit, multiedit, write, view, grep, glob, ls, fetch, download, and more. Use this tool to delegate ALL implementation work.

<usage>
- **ALWAYS** use the agent tool for any task that reads, writes, edits, or creates files
- **ALWAYS** use the agent tool for running commands (tests, builds, lints)
- **ALWAYS** use the agent tool for searching/analyzing code when you need to act on the results
- You may use your own read-only tools (view, grep, glob, ls) for quick context gathering before deciding what to delegate
- Launch multiple agents concurrently for independent tasks to maximize performance
</usage>

<usage_notes>
1. Launch multiple agents concurrently whenever possible, to maximize performance; to do that, use a single message with multiple tool uses
2. When the agent is done, it will return a single message back to you. The result returned by the agent is not visible to the user. To show the user the result, you should send a text message back to the user with a concise summary of the result.
3. Each agent invocation is stateless. You will not be able to send additional messages to the agent, nor will the agent be able to communicate with you outside of its final report. Therefore, your prompt should contain a highly detailed task description for the agent to perform autonomously and you should specify exactly what information the agent should return back to you in its final and only message to you.
4. The agent's outputs should generally be trusted
5. The agent has full tool access: bash, edit, multiedit, write, view, grep, glob, ls, fetch, download, sourcegraph, todos, job_output, job_kill, and LSP tools.
6. Give the agent complete, self-contained instructions. Include file paths, function names, expected behavior, and any constraints.
</usage_notes>
