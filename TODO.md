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
- [ ] **Create `metaphors.tex`:** Build a custom macro library so the agent/editor maintains consistency.
    - *Example:* Create a command `\metaphor{gravestone}{Price is a gravestone, not a map.}` to ensure the "Price as Gravestone" concept is used consistently across chapters.
  