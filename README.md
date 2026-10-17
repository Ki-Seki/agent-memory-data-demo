# agent-memory-data-demo

An example data repository for [agent-memory](https://github.com/Ki-Seki/agent-memory): what yours
looks like once it has a remote. Everything in it is made up, including the developer, Alex, and
every project, host and link.

- **[`memories/`](memories)** holds one Markdown file per memory, in `memories/YYYY/MM/`: a
  frontmatter with the type, the scope, a one-line description and, under `source`, where it came
  from; then the memory itself.
- **[The commit history](https://github.com/Ki-Seki/agent-memory-data-demo/commits/main)** is what
  the hooks write: one commit per change, such as `memory: +1 ~0 -0 (claude-code: shop-web-v3-plan)`,
  with `Tool`, `Session-Id` and `Host` trailers. Pushing to a remote like this one is how memories
  reach your other machines.

Your own data repository should be **private**: it holds what you tell your agents.

## Try it

- In the browser: the [live demo](https://ki-seki.github.io/agent-memory/demo/).
- On your machine, in a throwaway copy of these memories:

  ```bash
  uvx --from "agent-memory-git[ui]" mem ui --demo
  ```

- On a clone of this repository (edits are committed to your clone):

  ```bash
  git clone https://github.com/Ki-Seki/agent-memory-data-demo
  AGENT_MEMORY_DATA=$PWD/agent-memory-data-demo uvx --from "agent-memory-git[ui]" mem ui --keywords-only
  ```
