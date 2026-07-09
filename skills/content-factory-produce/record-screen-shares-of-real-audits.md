---
name: record-screen-shares-of-real-audits
description: Capture screen recordings walking through actual client audits so the analysis work you already do becomes teachable, publishable proof of expertise.
category: Content Factory — Produce
stage: Produce
definitive_article: GAP — to be written
status: needs-work
---

# Record screen shares of real audits

**Use this when** you are about to perform a real audit or analysis for a client — a Website QA Audit, digital plumbing check, or campaign review — and can narrate while you work.

## Inputs
- A real client audit to perform (not a staged demo) — e.g., the Website QA Audit layers or Digital Plumbing checks
- Screen recording via Zoom or Descript with microphone narration
- Client permission to record, and a plan for redacting sensitive data (ad spend, emails, revenue) before publishing
- Access to the Content Library Google Drive folder

## Steps
1. Confirm with the client that the audit may be recorded and used as content; agree on what must be redacted or blurred.
2. Start a Zoom or Descript screen recording with mic on before you begin the audit — capture the real first-pass reactions, not a re-enactment.
3. Narrate GCT as you work: the Goal of each check, the Content of what you find on screen, and who this matters to (Targeting).
4. Work through the audit checklist out loud: state what you are checking, why it matters, what you found, and what you would do about it.
5. Pause briefly between checklist sections — clean topic boundaries make Process's clip extraction and timestamping faster.
6. After recording, note any frames containing sensitive client data so Process can cut or blur them.
7. Name the file `YYYY-MM-DD-clientname-audit-topic` and upload to the Content Library Drive folder.
8. Log in the Content Library tracker with status "Raw — ready for Process" plus the redaction notes.

## Definition of done (QA checklist)
- [ ] Recording covers a real audit on a real client property, narrated end to end
- [ ] Each check states what/why/finding/action (teachable, not just clicking around)
- [ ] Sensitive data identified and flagged for redaction before any publishing
- [ ] Clean section boundaries exist for clip extraction
- [ ] File uploaded to the Content Library and logged for the Process stage
- [ ] Linked back to the definitive article and relevant siblings

## Example(s)
- Example needed — run the Meta-Article Prompt after first real run. Candidate: a recorded Website QA Audit of a personal brand site such as those built for DealCon attendees.

## Run on a persistent agent (Fable 5)

A persistent agent (Claude Fable 5, or a comparable OpenAI/Google model that loops and holds memory) can drive the audit checklist itself, then self-verify the recording: redaction flags noted, section boundaries clean, file named and logged — looping until every Definition-of-done box checks, because one unflagged client number is a publishing incident. Memory keeps each client's redaction list and audit history, so repeat audits start from prior findings instead of zero. Log a meta-article example each run.
See `boil-the-ocean.md` for the full operating principles.

## Definitive article & links
- Hub: GAP — no definitive article yet; this skill flags the missing hub. Until written, ground runs in /website-qa-audit and /digital-plumbing (the audits being recorded).
- Related: /website-qa-audit, /digital-plumbing, /content-factory
- Sibling skills, in run order: this → `step-1-upload-video-to-google-drive-and-descript` → `extract-15-60-second-clips-from-long-form-video`
