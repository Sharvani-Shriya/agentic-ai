# Agentic AI Journey

My 8-week plan to learn agentic AI (Ollama, tool calling, RAG, MCP, LangGraph) and build projects for an internship.

## Day 1: Ollama setup

- **Date:** [today's date]
- **Machine:** [laptop CPU], 7.7 GB RAM, no dedicated GPU
- **Model:** llama3.2:3b
- **Installed with:** `irm https://ollama.com/install.ps1 | iex` in PowerShell
- **Commands used:** `ollama pull llama3.2:3b`, `ollama run llama3.2:3b`

### My test prompts

| # | Prompt | Result | Notes |
|---|--------|--------|-------|
| 1 | Explain what an API is in 3 sentences | Good | Followed the 3-sentence limit exactly; used a "messenger" analogy |
| 2 | Write a Python program to reverse a string | Good | Used `s[::-1]` with input() and print(); [ran it: works / not tested yet] |
| 3 | What is 17*25? | Correct | Answered 425 |
| 4 | Summarize a paragraph in one line | Good | One sentence, accurate, nothing added, even though the pasted text was garbled in the terminal |
| 5 | Capital of Australia and its prime minister | Mostly good | Canberra correct. Named Anthony Albanese and flagged "knowledge cutoff in 2023" |
| 6 | What is 347*28? | **Wrong** | Said 9776; correct answer is 9716 |
| 7 | List 5 prime numbers greater than 100 | Correct | 103, 107, 113, 127, 131 are all prime |
| 8 | Who won the most recent FIFA World Cup? | **Outdated** | Said Argentina won the 2022 final on penalties against France (true for 2022). The most recent final was 2026, won by Spain 1-0 after extra time against Argentina |

### What I learned

- The 3b model handles simple tasks well: explanations, short code, short summaries, small arithmetic.
- **It fails at larger arithmetic** (347*28). An agent should use a calculator tool instead of trusting the model's math.
- **It has a knowledge cutoff** and can't know recent events. An agent needs a search tool for current facts.
- It was honest about its cutoff when asked about a prime minister, but for the World Cup it answered as if 2022 was the latest.
- Speed: about [X] seconds before the first reply on my laptop.
- These two failures are the reason to learn tool calling (Week 2).
- Next step: Day 2, Python essentials.