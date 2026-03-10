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

### 4: Machine Learning

- [ ] **Chapter Placement (Intentional Skip Ahead):** Mark this chapter as modular and assignable later in the book (not required to come right after Chapter 3).
- [ ] **State zero-prerequisite entry contract:** Explicitly assume no prior ML knowledge; define every term from first principles before using it.

- [ ] **Open with "Physics before algorithms":** Re-anchor the student in market data logic before ML jargon.
    - **4.1 Why ML appears here (and not earlier):** We first needed data integrity (tick -> bars -> stationarity/memory trade-off) before prediction.
    - **4.2 What problem we are solving:** "Given current bar conditions, predict next bar direction."
    - **4.3 Inputs are hypotheses, not magic:** Indicators/features are economic assumptions encoded numerically.

- [ ] **Build ML intuition from scratch (no math gatekeeping):**
    - **4.4 Traditional programming vs ML:** Handwritten rules vs learned rules from examples.
    - **4.5 Supervised learning only:** Inputs `X` + known outcomes `y`; defer unsupervised/reinforcement to a short awareness sidebar.
    - **4.6 Decision trees as 20-questions logic:** Sequential yes/no splits over features.
    - **4.7 Overfitting as memorization:** Why perfect training accuracy can fail in live markets.
    - **4.8 Random forest intuition:** Many constrained trees + voting to reduce noise memorization.

- [ ] **Define the chapter data contract clearly:**
    - **4.9 Feature matrix (`X`) structure:** Rows = dollar bars; columns = engineered features.
    - **4.10 Target variable (`y`) definition:** `1` if next bar closes higher, `0` otherwise.
    - **4.11 Causality rule:** Every feature at time `t` may use only information available at or before `t`.

- [ ] **Feature engineering roadmap (from your Week 9 flow):**
    - **4.12 Trend/Momentum block:** EMA variants and crossover logic.
    - **4.13 Mean-reversion block:** Bollinger bands and z-score distance from local mean.
    - **4.14 Volatility block:** Rolling dispersion/range-style volatility summaries.
    - **4.15 Statistical moments block:** Rolling mean, variance, skewness, kurtosis as shape descriptors.
    - **4.16 Feature intent labeling:** Require one-line economic rationale per feature to prevent indicator dumping.

- [ ] **Experiment design: the A/B shootout:**
    - **4.17 Pipeline A (`d=0`) baseline:** Raw-price-derived features (non-stationary benchmark).
    - **4.18 Pipeline B (`d=x`) candidate:** Fractionally differentiated features (stationarity + retained memory).
    - **4.19 Fair-test constraints:** Same tickers, same dates, same model config, same train/test window.
    - **4.20 Hypothesis-first workflow:** Students must write expected outcome before training.

- [ ] **Leakage defense as a core learning objective:**
    - **4.21 The "time machine" bug:** Why shuffling financial rows leaks future information.
    - **4.22 Golden split rule:** Strict time-ordered split (past train, future test).
    - **4.23 Validation hygiene checklist:** Timestamp monotonicity, NaN handling, alignment checks, no forward-looking transforms.

- [ ] **Training and evaluation without ML prerequisites:**
    - **4.24 Minimal model recipe:** RandomForestClassifier as implementation detail, not chapter centerpiece.
    - **4.25 Report-card interpretation:** Accuracy, precision, recall, F1-macro in trading language.
    - **4.26 What "better" means:** Prefer robust out-of-sample behavior over headline training accuracy.

- [ ] **Team workflow mirrors research practice:**
    - **4.27 Role framing:** Data Curator, Feature Analyst, Strategist, Backtester responsibilities.
    - **4.28 Reproducibility requirements:** Fixed random seed, logged configs, preserved feature lists.
    - **4.29 Scope control:** Use representative subset (30-50 tickers), not entire universe.

- [ ] **Close the chapter with realism and transition:**
    - **4.30 Limits of this chapter:** We built a classifier, not a profitable trading system.
    - **4.31 Common failure modes:** Regime shifts, transaction costs, class imbalance, false edge.
    - **4.32 Forward pointer:** Next chapter on validation/backtesting architecture and execution realism.

- [ ] **Add end-of-chapter apparatus (textbook-ready):**
    - **Chapter Summary:** Short paragraph for foundations, features, leakage, evaluation, and shootout findings.
    - **Key Terms:** supervised learning, feature matrix, target variable, overfitting, random forest, leakage, time split, F1-macro.
    - **Review Questions:** 6-8 conceptual checks requiring no coding background.
    - **Problems:** 3-5 applied prompts (label construction, leakage diagnosis, hypothesis writing, metric interpretation).
    - **Further Reading:** One beginner ML-for-finance primer + one robust validation reference.
