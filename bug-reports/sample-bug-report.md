# 🐞 Sample Bug Report

> Example written for practice on a generic voice assistant app. Not from any real product's internal tracker.

---

**Bug ID:** BUG-001  
**Title:** Assistant keeps speaking after user says "stop" in Hindi  
**Reported by:** Ritik Kumar  

## Environment

| Field | Value |
|---|---|
| App version | 1.4.2 (example) |
| Device | Budget Android phone, 3 GB RAM |
| Android version | 11 |
| Network | 4G |
| Language used | Hindi |

**Severity:** 🟠 Major · **Priority:** P1

## Steps to Reproduce

1. Open the assistant and ask a long question: "Mujhe Taj Mahal ke baare mein batao"
2. While the assistant is replying, say "ruk jao"
3. Observe the response

**Reproducible:** Sometimes (6 out of 10)

## Expected Result

Assistant stops speaking within 1 second and starts listening.

## Actual Result

Assistant continues the full reply. Saying "stop" in English works every time.

## Evidence

- Screen recording: _attached_
- Observation: happens more often with background fan noise

## Notes

- Likely the Hindi stop-word is not detected while audio is playing.
- Workaround: tap the mic button to interrupt.

### Retest Log

| Date | Build | Result | Notes |
|---|---|---|---|
| Day 1 | 1.4.2 | ❌ | Reproduced 6/10 |
| Day 4 | 1.4.3 | ✅ | Fixed — stops 10/10 |
