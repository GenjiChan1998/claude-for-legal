# research-agent

## Purpose
Pulls all relevant context for a matter before drafting begins.

## Inputs
- Matter ID from Airtable
- Triage output from triage-agent
- NDA document text
- Counterparty name

## Steps
1. Load the correct playbook using playbook-retriever skill
2. Search closed matters for similar precedents using precedent-retriever skill
3. Extract all clauses from the NDA using clause-fact-extractor skill
4. Look up counterparty context using counterparty-context skill
5. Run source-hierarchy-linter to confirm playbook-first ordering
6. Return a structured research packet

## Output
Returns a research packet containing:
{
  "playbook": "MNDA positions from CLAUDE.md",
  "precedents": ["list of similar closed matters"],
  "extracted_clauses": ["list of clauses from the NDA"],
  "counterparty_context": "Standard / Strategic / Competitor",
  "linter_result": "pass / fail",
  "research_notes": "any additional context"
}

## Notes for Lawyers
This agent gathers facts only. It does not make recommendations.
All recommendations come from the synthesis-agent in Week 3.
