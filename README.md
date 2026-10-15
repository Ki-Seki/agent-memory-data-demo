# agent-memory-data-demo

A small, made-up data repository for [agent-memory](https://github.com/Ki-Seki/agent-memory):
fourteen memories of a fictional developer, Alex, who works on a web shop (`shop-web`), a data
pipeline (`etl-jobs`) and a thesis folder. Use it to see the file format and try `mem ui`
without touching your own memories.

Each memory is one Markdown file under `memories/YYYY/MM/`, exactly as the agent-memory hooks
write them: frontmatter with `type`, `scope`, a one-line `description` and provenance under
`source`, then the memory itself.

| | |
|---|---|
| types | `user` (who Alex is), `feedback` (how Alex wants work done), `project` (facts about one project), `reference` (where to find things) |
| scopes | `global` memories load in every session; `here` memories load only in the folder or repository they were recorded in |
| languages | English and Chinese, as real stores tend to be |

## Try it

```bash
git clone https://github.com/Ki-Seki/agent-memory
git clone https://github.com/Ki-Seki/agent-memory-data-demo
cd agent-memory
AGENT_MEMORY_DATA=../agent-memory-data-demo bin/mem ui        # needs numpy
AGENT_MEMORY_DATA=../agent-memory-data-demo bin/mem list --all
AGENT_MEMORY_DATA=../agent-memory-data-demo bin/mem search deploy --all
```

`AGENT_MEMORY_DATA` points the commands at this repository instead of your configured one, so
nothing is installed and your own memories are not touched. Edits made in `mem ui` are committed
to your clone of this repository.

Everything here is invented; the people, hosts, URLs and repositories do not exist.
