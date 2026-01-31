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
