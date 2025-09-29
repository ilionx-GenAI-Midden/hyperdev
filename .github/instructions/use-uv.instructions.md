---
applyTo: '**'
---
Use UV for Dependency Management: When generating code that requires dependencies, or when running scripts, use the `uv` tool for managing dependencies and executing scripts. Do not use `pip` or `requirements.txt` for dependency management.

New projects should be initialized with `uv init --bare`. This will create a new project without example scripts.

Dependencies can be added with `uv add <my_package_name>`. A specific version can be specified using `uv add <my_package_name>==1.2.3`, but prefer trying to add without explicit version numbers.
Scripts can be run with `uv run <my_script.py>`.

Existing dependencies are stored in @pyproject.toml, you can read the file but you shouldn't add dependencies to it directly.

It is forbidden to use `pip` or requirements.txt! Anything can be done using UV. If you are unsure, check the UV documentation via web search. If you successfully do so, update the @use-uv.mdc rule.
