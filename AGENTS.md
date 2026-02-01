# Real-World Facts Search Rule

When users ask about current events, real-time data, recent statistics, or information requiring up-to-date web search:

1. Use `ddg-search_search(query="...", max_results=N)` for searches:
   - Use 3-5 results for factual questions
   - Use 5-8 results for broader searches
   - Include current terms like "current" or "latest"

2. Use `ddg-search_fetch_content(url="...")` for detailed content from specific URLs

3. Prefer ddg-search over webfetch

4. Always cite sources when providing facts

5. If results unclear, refine the query

# Python Project Execution Rule

When running Python commands in Python projects:

1. Detect Python project:
   - Check if `pyproject.toml` exists OR
   - Check if `.venv/` or `venv/` directory exists

2. For Python projects, use local Python in this order:
   - Try `uv run python <command>` or `uv run <command>` first
   - If uv unavailable, use `.venv/bin/python <command>` (or `venv/bin/python`)
   - Use pip via `uv pip install <package>` or `.venv/bin/pip install <package>`

3. For non-Python projects:
   - Use global `python <command>`

Examples:
- `python script.py` → `uv run python script.py` or `.venv/bin/python script.py`
- `python -m pytest` → `uv run pytest` or `.venv/bin/python -m pytest`
- `pip install package` → `uv pip install package` or `.venv/bin/pip install package`
