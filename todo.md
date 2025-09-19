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

Generation-level defenses incorporate privacy mechanisms during inference. Methods such as DPVoteRAG and DPSparseVoteRAG distribute response generation across multiple voters, each using disjoint subsets of the data, and add noise to ensure differential privacy \cite{DPVoteRAG}. Other approaches use prompt-based defenses, employing strong system prompts to enforce privacy-preserving rules on generated output \cite{anthropic_strengthen_guardrails,aws_secure_rag,goodAndBad}. These methods preserve the original retrieval data and introduce protections only at inference. DP-based defenses provide formal privacy guarantees, while prompt-based defenses process all retrieved documents for each query, enabling more context-aware redaction.  

Despite these advantages, DPVoteRAG suffers from utility loss once the privacy budget is exhausted and adds inference overhead through multiple voters and noise mechanisms. Prompt-based defenses, by contrast, lack formal guarantees and remain vulnerable to prompt injection attacks (see Section \ref{literature-sec:privacy-attacks}). 


Query and output sanitization defenses act either before retrieval (malicious query filtering) or after generation (e.g., \ac{PII} detectors and redactors). Practical toolkits such as Microsoft Presidio and industry frameworks like AWS Bedrock provide recognizers (regex, rule-based logic, and NER) for common \ac{PII} types, while RAG-specific work recommends response sanitization as a mitigation strategy \cite{aws_bedrock_privacy,ragThief,microsoft_presidio}. These defenses are straightforward to deploy and preserve original data, helping maintain utility.  

Their main limitation is brittleness: query filters can be bypassed in adversarial settings (see Section \ref{literature-sec:privacy-attacks}), while output sanitizers risk false negatives for obfuscated or implicit identifiers. As a result, these approaches are best viewed as complementary safeguards rather than standalone defenses.