# depth

An agent skill that turns a shallow task request into the version a top professional would do: deeper, not bigger.

Based on the "depth" prompt by [Felix Rieseberg](https://x.com/felixrieseberg) ([X post](https://x.com/felixrieseberg/status/2110023283169247623)) from his tutorial [How to be more ambitious: A tutorial for humans with models](https://felixrieseberg.com/how-to-be-more-ambitious-a-tutorial-for-humans-with-models/).

Before it rewrites your prompt, it answers four questions:

1. What would a top professional in this field do here that you are not asking for?
2. What is the rawest material they would start from, instead of what was already digested for you?
3. What specific methods and tools would they use?
4. What, other than you or the agent, would show the result is right?

Then it rewrites your prompt to ask for exactly that. It does not start the task.

## Install

With [`skills`](https://github.com/vercel-labs/skills):

```sh
npx skills add alexsorokoletov/depth
```

While this repo is private, `npx skills` clones it with your own git credentials. You need read access and a working `git clone` (SSH key or `gh auth login`).

## Use

In Claude Code: `/depth <your task>`. Or say "deeper version" or "level up this prompt".
