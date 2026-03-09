# Textbook Architecture: Pre-Chapter 1 Setup

## 1. LaTeX Environment & Directory Structure

- [x] **Define Root Structure:** Create the following directory tree:
    - `/chapters`: Folder for individual `ch01.tex`, `ch02.tex` files.
    - `/assets`: Subfolders for `/images`, `/tables`, and `/code_listings`.
    - `/macros`: A `finance_commands.tex` file to hold consistent definitions.
    - `/preamble`: A `settings.tex` file for document class and packages.
- [x] **Configure Master File:** Create `main.tex` that uses `\include{chapters/chXX}` for modular chapter handling.
- [x] **Establish LaTeX Class:** Select a clean, professional textbook class (e.g., `tufte-book` or a custom `book` setup) that supports wide margins for side-notes and metaphors.

## 2. The "Metaphor Registry" (Semantic Consistency)
- [x] **Create `metaphors.tex`:** Build a custom macro library so the agent/editor maintains consistency.
    - *Example:* Create a command `\metaphor{gravestone}{Price is a gravestone, not a map.}` to ensure the "Price as Gravestone" concept is used consistently across chapters.
    - 
### 3. Introduction: Setting the Stage

- [x] **1.1 What Is the Market?** 
    - [x] **1.1.1 The Pre-1970s Exchange-Centric View:** Explain why legacy narratives over-focus on visible exchanges in media.
    - [x] **1.1.2 The Digital Revolution and NASDAQ Era:** Cover computerization, electronic execution, and how digital reporting changed market data.
    - [x] **1.1.3 The Market as a Real-Time Decision Field:** Every tick as a human, agent, or hybrid decision.
    - [x] **1.1.4 Primary vs Secondary Markets:** Issuance vs ongoing price discovery.
    - [x] **1.1.5 Core Market Participants:**
        - Institutional/market makers (dealers): provide the pipes, execute trades, and report data.
        - Brokers: enable trades by matching buyers and sellers and routing order flow.
        - Speculators (us): retail investors, pattern-seeking quants, and students learning market structure.
    - [x] **1.1.6 Dealers and Market Making:** Bid/ask spread mechanics, inventory risk, and flow capture.
    - [x] **1.1.7 Brokers and Order Routing:** Routing logic, execution quality, and the role of intermediated flow.
    - [x] **1.1.8 Financial Intermediaries:** Banks/funds as institutions that transform, pool, and repackage risk.
    - [ ] **1.1.9 Venue Structure and Fragmentation:** NYSE/NASDAQ, ECNs, dark pools, and cross-venue liquidity.
    - [ ] **1.1.10 Anatomy of a Market Event:** Who/what/where/when/why and "price as gravestone, not map."
    - [ ] **1.1.11 Transition to Data and Measurement:** Move from narrative intuition to quantifiable event streams.


- [ ] **Frame the chapter as an introduction to finance and systems thinking:** Match the lecture's "big picture first" structure.
    - **1.1 Why This Course, Why Now:** AI as an abstraction shift in computing and finance.
    - **1.1a Parallel Abstraction Ladders (CS vs Finance):** Binary -> punch cards -> assembly -> C/Java/Python -> code generation, alongside barter -> gold standard -> fiat -> electronic markets -> HFT/agentic trading.
    - **1.2 What Finance Is:** Business finance, investments, and financial markets/institutions.
    - **1.3 Risk and Return as Core Language:** Uncertainty, compensation for risk, and decision trade-offs.

- [ ] **Establish data as the substrate of every decision:** Ground the chapter in how data is produced and used.
    - **1.4 Internal Data:** Income statement, balance sheet, cash flow, and "book value" limits.
    - **1.5 External Data:** Market, survey, and macroeconomic inputs used by firms and investors.
    - **1.6 Digitization and Data Velocity:** Why modern finance is event-driven and latency-sensitive.

- [ ] **Bridge classic finance to quantitative market data:** Move from static reports to streams.
    - **1.12 From Statements to Streams:** Why accounting snapshots are insufficient for intraday systems.
    - **1.13 Tick Data Fundamentals:** Symbol, price, size, venue, timestamp, and event ordering.
    - **1.14 Aggregation and Interpretation:** OHLCV construction, volume semantics, and data quality pitfalls.

- [ ] **Add economic foundations used in strategy design:** Keep both micro and macro lenses from lecture.
    - **1.15 Microeconomics for Quants:** Supply, demand, equilibrium, and firm-level incentives.
    - **1.16 Macroeconomic Drivers:** CPI/PPI, unemployment, GDP, rates, and business-cycle stages.
    - **1.17 Market Reactions to Macro Prints:** Surprise vs expected releases and volatility transmission.
    - **1.18 Risk Premium Logic:** Why different borrowers/securities command different required returns.

- [ ] **Set the AI foundation before automation claims:** Keep AI content conceptual and safety-aware.
    - **1.19 From LLM Prediction to Reasoning:** Token prediction limits, chain-of-thought behavior, and planning.
    - **1.19a LLM Origin Story and Release Philosophy:** Google/DeepMind-era caution around hallucinations vs OpenAI's public release strategy; why safety posture affects downstream system design.
    - **1.20 Failure Modes:** Hallucination, garbage-in-garbage-out, bias, and non-determinism.
    - **1.21 Agentic System Loop:** Goal -> perceive -> plan -> act -> verify -> adapt, with human oversight.

- [ ] **Close with trading realism and discipline:** Align with lecture emphasis on expectations.
    - **1.22 Why Most Active Traders Lose:** Baseline evidence, survivorship bias, and false confidence.
    - **1.23 What This Book Optimizes For:** Process quality, risk controls, and repeatable decision systems.
    - **1.24 Chapter 2 Transition:** From context to measurement, feature design, and validation workflow.

- [ ] **Write end-of-chapter apparatus (Kurose-style):** Make Chapter 1 textbook-ready, not lecture-only.
    - **Chapter Summary:** One short paragraph per major section.
    - **Key Terms Glossary:** tick, spread, best execution, latency, CPI, business cycle, risk premium, agentic system.
    - **Review Questions:** 6-8 conceptual checks (no code).
    - **Problems:** 3-5 applied prompts (event reconstruction, macro interpretation, data-quality checks).
    - **Further Reading:** Lopez de Prado Ch. 1-2, one market microstructure paper, one accessible practitioner source.