# smartup

An agent skill that turns a shallow task request into the version a top professional would do: deeper, not bigger. Before it rewrites your prompt, it answers four questions:

1. What would a top professional in this field do here that you are not asking for?
2. What is the rawest material they would start from, instead of what was already digested for you?
3. What specific methods and tools would they use?
4. What, other than you or the agent, would show the result is right?

Then it rewrites your prompt to ask for exactly that. It does not start the task.

## Install

With [`skills`](https://github.com/vercel-labs/skills):

```sh
npx skills add alexsorokoletov/smartup
```

Options:

```sh
npx skills add alexsorokoletov/smartup -g             # global (user-level), all projects
npx skills add alexsorokoletov/smartup -a claude-code # one agent only
npx skills add alexsorokoletov/smartup --list         # preview, no install
```

While this repo is private, `npx skills` clones it with your own git credentials. You need read access and a working `git clone` (SSH key or `gh auth login`).

Update or remove:

```sh
npx skills update smartup
npx skills remove smartup
```

## Use

In Claude Code: `/smartup <your task>`. Or say "smartup", "deeper version", or "level up this prompt".

## Credit

Based on the "depth" prompt by [Felix Rieseberg](https://x.com/felixrieseberg) ([X post](https://x.com/felixrieseberg/status/2110023283169247623)) from his tutorial [How to be more ambitious: A tutorial for humans with models](https://felixrieseberg.com/how-to-be-more-ambitious-a-tutorial-for-humans-with-models/).
