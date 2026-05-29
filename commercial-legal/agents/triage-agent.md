# triage-agent

## Purpose
Evaluates an incoming NDA matter and returns a structured triage decision.

## Inputs
- Matter ID from Airtable
- Document text from the attached NDA
- Counterparty name
- Business context from the requester

## Steps
1. Load the playbook from CLAUDE.md
2. Identify SentiLink's role (mutual / discloser_only / recipient_only)
3. Assess the matter category and risk lane (1-4)
4. Determine urgency and SLA
5. Check counterparty against Strategic Counterparties table
6. Identify any blocking or missing facts
7. Decide if a clarifying question is needed
8. Determine if matter is automation eligible

## Output
Returns a structured JSON object:
{
  "category": "Commercial Sales NDA",
  "lane": 1,
  "urgency": "Standard",
  "sla": "2 business days",
  "blocking_facts": [],
  "helpful_facts": [],
  "counterparty_class": "Standard",
  "clarifying_question": null,
  "automation_eligible": true
}

## Escalation Rules
- Lane 3 or 4 → notify assigned lawyer before proceeding
- Counterparty is a known competitor → escalate to James Cook
- Any blocking facts present → pause and ask clarifying question

## Notes for Lawyers
This agent does not make legal judgments. It sorts and routes.
The assigned lawyer always has final say on lane and routing decisions.
