# Gemini Email Summary Injection

**Category**: Indirect Prompt Injection
**Model Affected**: Google Gemini (Workspace)
**Discovered by**: Mozilla Bug Bounty Program
**Date**: July 2024
**Severity**: :large_orange_circle: Medium
---
## Description
Hidden prompt injection in HTML email causes Gemini to summarize with manipulated intent. Achieved via white text + zero-point font-size injected into the email body.
---
## Attack Flow

Attacker crafts HTML email with invisible directives.
Victim uses Gemini to summarize email.
AI obeys malicious instructions and rewrites the summary to mislead user.
---
## Mitigations

Filter or flatten invisible text before summarization.
Apply LLM sandboxing or task separation logic.












