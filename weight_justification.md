# potentially relevant snippets
#### NIST:
- For example, an individual‘s SSN, medical history, or financial account information is generally considered more sensitive than an individual‘s phone number or ZIP code. Organizations often require the PII confidentiality impact level to be set at least to moderate if a certain data field, such as SSN, is present. (3.2.3)
- For example, PII data composed of individuals‘ names, fingerprints, or SSNs uniquely and directly identify individuals, whereas PII data composed of individuals‘ ZIP codes and dates of birth can indirectly identify individuals or can significantly narrow large datasets. (3.2.1)
  - supports split into direct and quasi identifiers


#### HIPAA:
- “Safe Harbor” method: list of 18 PII that need to be removed
  - all of these elements receive higher weights
- Expert Guidance: maybe use ChatGPT as domain expert for scoring


#### GDPR:
- Processing of personal data revealing racial or ethnic origin, political opinions, religious or philosophical beliefs, or trade union membership, and the processing of genetic data, biometric data for the purpose of uniquely identifying a natural person, data concerning health or data concerning a natural person’s sex life or sexual orientation shall be prohibited.




\paragraph{Justification of entity weights and types.}
The assignment of categories and the numerical weights in Table~\ref{approach-tab:entity-weight-schema} follows established definitions and guidance about identifiability and sensitive data. We distinguish between (1) \emph{direct identifiers} that uniquely identify an individual (e.g., NAME, PATIENT\_ID), which receive the highest weights because they enable immediate re-identification; (2) \emph{special-category / health-sensitive} attributes (e.g., MEDICAL\_CONDITION, TREATMENT), which receive high weights in line with GDPR Article~9 and HIPAA de-identification guidance; and (3) quasi-identifiers and contextual attributes that receive intermediate or lower weights reflecting their context-dependent re-identification potential. The uniqueness score \(u(e)\) is IDF-inspired and captures corpus-wide rarity (see Section~\ref{approach-subsubsec:uniqueness}). These design choices follow NIST's recommendation to treat PII on a context-sensitive basis and HIPAA's Safe Harbor identifier list. For transparency, the full per-entity table is reported in Table~\ref{approach-tab:entity-weight-schema}. An initial draft of the entity-weights was generated with assistance from a large language model; the authors subsequently reviewed and finalized the assignments by cross-checking NIST SP 800-122, HIPAA Safe Harbor guidance and GDPR Article~9.
