# playbook-retriever

## Purpose
Looks up the correct playbook from the skill library based on matter type.

## Inputs
- Matter type (e.g. Commercial Sales NDA)

## Steps
1. Match matter type to the correct skill in the library
2. Load the matching SKILL.md and CLAUDE.md config
3. Return the playbook positions for the agent to use

## Outputs
- Playbook positions for the relevant matter type

## Notes for Lawyers
This skill ensures the right playbook is always applied to the right matter type.
