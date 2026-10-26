# Source and fidelity

Independent workflow adaptation of Kambhamettu et al., LitPivot, https://arxiv.org/abs/2604.02600 and https://arxiv.org/html/2604.02600v3 (2026-09-22), sections 4.2–4.4 and appendix B. Blog: https://huggingface.co/blog/allenai/litpivot (2026-10-23). Not affiliated with Ai2. Do not copy full paper text or prompts.

Original mechanisms: P/C/E segmentation, missing-facet detection, initial retrieval and substantive citation expansion, facet-specific clustering/ranking, researcher paper selection, evidence-grounded alignment/differentiation, bipartite contribution–limitation analysis, actionable rewrites, user acceptance/edit/rejection, inconsistency flags and user-controlled literature refresh.

Original implementation used Asta Paper Finder, Semantic Scholar services, several language models and React/Flask. This skill uses available tools and conversational tables instead; no Asta integration, identical ranking or UI reproduction is asserted. Exact API integrations require separate implementation/authorization. Experiment and writing assistance are extensions.

Grounding scores in a 17-person study and a 5-person follow-up do not establish true novelty, long-term impact or acceptance. No universal novelty score should be produced. Missing literature may reflect incomplete retrieval, access barriers or wrong vocabulary. Prior-work limitations may have been resolved after publication.

## Assessment record
Record selected facet/version, selected paper IDs, claim, evidence locations, support/contradiction/overlap/unknown, graph edges, alternatives, proposed rewrite, feasibility, uncertainties, validation and user decision. Explicitly scope conclusions to sources actually read. Show source coverage and unresolved disagreements.

## Practical triggers
New idea: find the missing facet and closest work. New paper: triage impact on existing claims. Overlapping work: compare settings, mechanisms and evaluation before suggesting a pivot. Results contradict hypothesis: retain results and revise interpretations. No material change: continue planned work. User tired: perform organization yourself and ask only the next essential research decision.
