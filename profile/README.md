<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/wheelgap/wheelgap/main/docs/logo/wheelgap-lockup-dark.png">
  <img alt="wheelgap" src="https://raw.githubusercontent.com/wheelgap/wheelgap/main/docs/logo/wheelgap-lockup.png" height="56">
</picture>

**`pip install` should never have to compile.**

wheelgap finds the Python dependencies that have no prebuilt wheel for the platforms you ship to (ARM servers, Alpine, Windows on ARM, Python 3.15, free-threaded 3.14t), and tells you the exact change that fixes each one.

```bash
uvx wheelgap --fix
```

🔎 No install needed: [paste any public GitHub repo](https://wheelgap.github.io/tracker/check/) and see its gaps in your browser.

### Projects

| | |
| --- | --- |
| **[wheelgap](https://github.com/wheelgap/wheelgap)** | The CLI, GitHub Action, agent skill and MCP server. Reads your lockfile, reports what will build from source, and gives the upgrade that fixes it. |
| **[tracker](https://github.com/wheelgap/tracker)** | [Wheel coverage](https://wheelgap.github.io/tracker/) for the top 5,000 PyPI packages across 42 platform targets, updated nightly, plus the in-browser repo checker. |
| **[wheels](https://github.com/wheelgap/wheels)** | A [gap wheel index](https://wheelgap.github.io/wheels/): wheels PyPI is missing, each built twice from the sdist and published only when both builds match. |

### Where it fits

- **In CI:** the [GitHub Action](https://wheelgap.github.io/wheelgap/ci/) fails a pull request only when it adds a new gap, and comments the fix.
- **With AI coding agents:** a `check-wheels` skill and an [MCP server](https://github.com/wheelgap/wheelgap/blob/main/docs/mcp.md) for Claude Code, Cursor, Codex and others.
- **Upstream:** we send small, tested build changes to packages that are missing wheels, so the gap closes for everyone.

### Contributing

New contributors are welcome: start with a [good first issue](https://github.com/wheelgap/wheelgap/labels/good%20first%20issue). Documentation lives at [wheelgap.github.io/wheelgap](https://wheelgap.github.io/wheelgap/).
