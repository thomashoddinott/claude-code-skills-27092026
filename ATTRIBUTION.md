# Attribution

Some of these files are mine, some are adapted from other people's published work. This is which is which.

## Original

`global/skills/`: `desktop-summary`, `eli5`, `pull-ticket`

`project/skills/`: `commit`, `merge`, `pr`, `smoke-test`, `ticket`, `use-cases`, `user-stories`

## Adapted from [citypaul/.dotfiles](https://github.com/citypaul/.dotfiles) (MIT)

`project/skills/`: `planning`, `tdd`, `testing`, `refactoring`, `mutation-testing`

`project/agents/`: `adr`, `docs-guardian`, `learn`, `progress-guardian`, `refactor-scan`, `tdd-guardian`, `ts-enforcer`, and the directory `README.md`

### `pr-reviewer`: forked, then substantially rewritten

`pr-reviewer` began as the upstream `pr-reviewer` agent. The skeleton is not mine: the review categories, the report format, the action-items table, the quick-reference rule lists and the proactive/reactive framing all came from upstream.

Added here:

- The **smoke test as the gate into the review**: no line-level reading until the feature has been driven end to end in the real app, with the agent narrating and diffing the database while the human drives
- **Acceptance-criteria verification** against the linked ticket, at review time and again at merge
- The **architectural macro-read**, with a forced pause for the reviewer's steer
- **Change-shape classification** (additive, reductive, substitutive) and a liveness check on every test the change adds or leaves behind
- **Mockup fidelity** as a sixth review category
- **Batched CSS triage** and **batched test-quality triage**, so nitpicks don't crowd out findings with real stakes
- The **zero-tool-calls rule** during triage: all analysis happens up front
- The **merge gates** and the hand-over to the `merge` skill
- The **review record**: one note on the MR, after the fixes, recording what was decided and why
- A CLI-only flow for GitLab in place of GitHub MCP tools

## Adapted from [mustafakendiguzel/claude-code-ui-agents](https://github.com/mustafakendiguzel/claude-code-ui-agents) (MIT)

`project/agents/`: `css-architecture`, `design-system`

---

## Upstream licences

### citypaul/.dotfiles

```
MIT License

Copyright (c) 2024 Paul Hammond

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```

### mustafakendiguzel/claude-code-ui-agents

```
MIT License

Copyright (c) 2025 Mustafa Kendigüzel

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```
