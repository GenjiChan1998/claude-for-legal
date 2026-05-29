# intake-normalizer

## Purpose
Maps incoming email and form data to a standard schema for the orchestrator.

## Inputs
- Raw email content or form submission

## Steps
1. Extract counterparty name, matter type, document attachment, and requester
2. Map to standard Airtable matter schema
3. Flag any missing required fields

## Outputs
- Structured matter object ready for triage-agent

## Notes for Lawyers
This skill handles the messy free-text portions of incoming emails. It does not make any legal judgment.
