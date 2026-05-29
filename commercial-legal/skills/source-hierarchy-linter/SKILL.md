# source-hierarchy-linter

## Purpose
Deterministic checklist that confirms the playbook is being followed in the correct order.

## Inputs
- List of clause findings from clause-fact-extractor
- Playbook positions from playbook-retriever

## Steps
1. Check each finding against the playbook in order
2. Flag any finding that skips or contradicts the playbook hierarchy
3. Return a pass/fail for each provision

## Outputs
- Pass/fail checklist for each playbook provision

## Notes for Lawyers
This skill runs deterministically — no AI judgment involved. It is a mechanical check only.
