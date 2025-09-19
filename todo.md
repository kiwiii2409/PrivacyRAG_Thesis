### Meeting TODO's
- Summarize Chapter 3 more
- Check capitalization for titles etc.
- Consistency regarding textit, texttt, textbf etc.
- **show example for each category question and show scores of all three baselines (probably just one in the appendix and show text for all three baselines)**
- mention in presentation: compare time of sage to my approach 
- **clean up appendix **

### NEW TODO's
- polish citation (order and position inside respective sentence)
- **expand limitations section**
- **add figures for document scores**
- add "7jm u" to sources

### Meeting TODO done:
- Hyperparameters: Leave in current state
- Rename 3.1 to RAG Privacy Risks
- 5.3.2 move reasoning above scoring, add reasoning (sampled small dataset and found values)
- reorder scoring in evaluation scoring and results section (weakest to strongest)
- emphasize: our approach closer to stdRAG for general but closer to SAGE for specific questions
- improve reasoning for CL=2 decision using percentage-wise comparison
  - briefly explain in approach or in experiments
- remove knapsack vs. greedy from ablation study (briefly explain differnce in approach)
- remove extraction model comparison from ablation study add to separaate section before experiments if needed (no)
- formalize 2.1 RAG pipeline
- formalize 2.2 Threat model
- move position of entity-weight schema (first references on page 15 but placed in page 11, maybe add refernce on page 11), ALSO: ADD SOME REASONING (IDEAS: )
- add appraoch overview figure to illustrate pipeline
- better name for approach instead of sAnon or selective anonymization => CLAM Cross-document Linkage Aware MAsking



## RULES: 
First-use term being defined: \emph{term}; subsequent mentions in roman.

Foreign phrases not naturalized in English/German: \emph{in vivo}, \emph{a priori}.

Code, CLI flags, JSON keys, config options, API names: \texttt{--top-k}, \texttt{entity_type}.

Software packages and datasets: roman text unless a published title; cite normally.

Titles of standalone works (books, theses, journals) in prose: italics; article/chapter titles in quotes per style.

Figure/table captions or section headers: follow template; bold is acceptable where the class uses it, but avoid ad‑hoc bold emphasis in running text.