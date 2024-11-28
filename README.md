The contents of this repository were created by following the [setup steps](https://davidvujic.github.io/python-polylith-docs/setup/#uv)
in the `python-polylith` documentation:

```bash
$ uv init --name=polylith-bug-report
$ uv add --dev polylith-cli
$ uv add --dev ipython  # optional, for convenience

$ uv run poly create workspace --name bug_report --theme loose
```

Now edit pyproject.toml according to the instructions [here](https://davidvujic.github.io/python-polylith-docs/setup/#edit-the-configuration_1)
by adding the following sections:
```toml
[build-system]
requires = ["hatchling"]
build-backend = "hatchling.build"

[tool.hatch.build]
dev-mode-dirs = ["components", "bases", "development", "."]
```

Finally, run:
```
$ uv sync
```
