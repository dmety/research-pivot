# Portable private project records

Use a separate private folder per project; never put project records in the skill distribution. Resolve storage first. Work and local Codex may share this schema but require an explicit transport; no automatic synchronization is implied. Preserve prior versions and conflicts.

Maintain state.json containing:

- schema_version: 1; project_id; title; stage; updated_at; idea_version; next_action.
- facets: problem/contribution/evaluation lists of {id,text,status,evidence_ids}; status distinguishes hypothesis/proposed/accepted/superseded. Missing facets may be empty.
- papers: {id,title,url,version,access,retrieved_at,relevance,reason}; access is full_text/abstract_only/unavailable.
- evidence: {id,paper_id,location,text,mode,interpretation}; mode quote/paraphrase; quotations exact and brief.
- clusters: {id,facet,label,paper_ids,rationale,idea_version}.
- selected_paper_ids and selection_status: provisional/user_approved.
- graph: nodes {id,type,text,evidence_ids}, edges {from,to,relation,evidence_ids,basis,uncertainty}; type prior_contribution/limitation/future_work/proposed_contribution; basis explicit/inference.
- proposals: {id,old_version,facet_ids,critique,evidence_ids,proposed_text,tradeoffs,status}; status pending/accepted/edited/rejected.
- decisions: append-only {id,timestamp,actor,proposal_id,action,rationale,old_version,new_version}; human action only when actually given.
- experiments: {id,claim_ids,design,controls,metrics,config_refs,budget,status,confirmatory_or_exploratory,results_refs}; planned does not mean executed.
- search_log: {date,queries,provider,scope,exclusions,failures,paper_ids}.
- needs_review: {target_id,changed_dependency,reason,resolution}.

Keep long evidence and decision history in linked Markdown files when needed. Use stable relative references and source versions. Save proposed and accepted text separately. After each successful session record one next action and truthful save status. Resolve concurrent changes explicitly, never last-write-wins. Connector content and drafts remain subject to its authorization and review rules.
