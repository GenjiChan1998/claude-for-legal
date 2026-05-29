# channel-audience-adapter

## Purpose
Picks the right format and tone based on who is receiving the output.

## Inputs
- Audience type (lawyer, business stakeholder, counterparty)
- Output type (memo, redline, email)

## Steps
1. Identify the audience and channel from the matter record
2. Select the appropriate format and tone
3. Apply the correct work-product header

## Outputs
- Formatted output ready for delivery

## Notes for Lawyers
Privileged headers are applied automatically for lawyer-facing outputs. Sanitized versions are produced for external audiences.
