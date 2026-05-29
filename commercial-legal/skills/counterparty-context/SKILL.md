# counterparty-context

## Purpose
Looks up the counterparty in Airtable to provide context for the review.

## Inputs
- Counterparty name

## Steps
1. Search Airtable Strategic Counterparties table
2. Return counterparty class (Standard, Strategic, Competitor)
3. Flag if counterparty is a known competitor or strategic partner

## Outputs
- Counterparty class and any relevant flags

## Notes for Lawyers
If counterparty is flagged as a competitor, matter is automatically escalated to James Cook.
