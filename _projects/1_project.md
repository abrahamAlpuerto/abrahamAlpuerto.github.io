---
layout: page
title: FinAgent Orchestration
description: A Multi-Agent System for Autonomous Trading (NeurIPS 2025)
img: assets/img/finagent_architecture.jpg
importance: 1
category: research
---

**Abstract:**
Financial markets are noisy and dynamic, making them a "mission-critical playground" for AI agents. Traditional algorithmic trading requires massive engineering teams. In this work, we developed a framework that maps the components of a traditional trading desk—Alpha, Risk, Portfolio, and Execution—into autonomous AI agents orchestrated by a central planner.

### System Architecture

The system utilizes a "Manager-Worker" topology where a central **Orchestrator** delegates tasks using the **Model Context Protocol (MCP)**.

1. **Alpha Agents:** Propose signal structures (e.g., momentum or microstructure factors) based on academic literature.
2. **Risk Agents:** Impose strict constraints on volatility and drawdown, acting as a "gate" before any trade is executed.
3. **Memory Agent:** Uses a UUID-based hashing system to store state and rationale, ensuring auditability without leaking future data into the context window.

### Key Innovations

- **Separation of Reasoning & Calculation:** LLMs (like GPT-4o) are used _only_ for reasoning and code generation. All numerical calculations are delegated to deterministic tools (Python/Pandas) to prevent "hallucination" in financial calculations.
- **Leakage Prevention:** The architecture strictly enforces a walk-forward evaluation. Future labels (returns) are physically blocked from the Alpha Agents' context windows.

### Performance

We backtested the system on both US Equities and Bitcoin:

- **Stocks (Hourly):** Achieved a **20.42% return** with a **Sharpe Ratio of 2.63**, significantly outperforming the S&P 500 (Sharpe 1.86) and minimizing maximum drawdown to -3.59%.
- **Crypto (Minute-level):** Achieved an **8.39% return** over a 17-day high-volatility period, compared to 3.80% for Buy & Hold.

<div class="row">
  <div class="col-sm mt-3 mt-md-0">
    {% include figure.html path="assets/img/cumulative_returns_graph.jpg" title="Cumulative Returns" class="img-fluid rounded z-depth-1" %}
  </div>
</div>
<div class="caption">
  Comparison of our Agentic Strategy (Green) vs. Benchmarks (Blue).
</div>