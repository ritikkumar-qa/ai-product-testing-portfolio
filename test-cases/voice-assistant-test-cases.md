# 🎙️ Voice Assistant — Test Cases

Generic manual test cases for an Android voice AI assistant. Written as a QA practice reference (no product-internal data).

**Legend:** ✅ Pass · ❌ Fail · ⚠️ Partial · ⏭️ Skipped

## 1. Wake & Activation

| ID | Scenario | Steps | Expected Result |
|---|---|---|---|
| TC-001 | Activate assistant | Tap mic / say wake word | Listening indicator appears within 1s |
| TC-002 | Wake word in quiet room | Say wake word from 1m distance | Assistant activates |
| TC-003 | Wake word with TV playing | Say wake word with background noise | Activates; no false triggers from TV |
| TC-004 | False trigger check | Talk normally for 5 min without wake word | Assistant does NOT activate |

## 2. Voice Input & Language

| ID | Scenario | Steps | Expected Result |
|---|---|---|---|
| TC-010 | English command | "What's the time?" | Correct time spoken |
| TC-011 | Hindi command | "Abhi kitne baje hain?" | Understands & replies correctly |
| TC-012 | Hinglish command | "Kal ka weather batao" | Understands mixed language |
| TC-013 | Fast speech | Speak command quickly | Command recognised |
| TC-014 | Long pause mid-sentence | Pause 2s in middle of command | Does not cut off early |
| TC-015 | Unclear audio | Mumble a command | Asks to repeat; no wrong action |

## 3. Conversation & Interruption

| ID | Scenario | Steps | Expected Result |
|---|---|---|---|
| TC-020 | Interrupt reply | Speak while assistant is talking | Stops & listens to new input |
| TC-021 | Follow-up question | Ask follow-up without context repeat | Remembers previous context |
| TC-022 | Cancel | Say "ruk jao" / "stop" | Stops immediately |

## 4. Device Actions

| ID | Scenario | Steps | Expected Result |
|---|---|---|---|
| TC-030 | Open app | "YouTube kholo" | Correct app opens |
| TC-031 | Call contact | "Call Mummy" | Confirms contact before calling |
| TC-032 | Set alarm | "Subah 6 baje alarm laga do" | Alarm set at 6:00 AM |
| TC-033 | Permission denied | Deny mic permission, open app | Clear message asking for permission |

## 5. Network & Stability

| ID | Scenario | Steps | Expected Result |
|---|---|---|---|
| TC-040 | No internet | Turn off data, give command | Friendly offline error; no crash |
| TC-041 | Network switch | Switch WiFi → mobile data mid-reply | Recovers or shows retry |
| TC-042 | Background & resume | Minimise app 10 min, reopen | Resumes without crash |
| TC-043 | Low battery mode | Enable battery saver | Still responds to commands |
| TC-044 | Long session | Use continuously 30 min | No lag, overheating or memory crash |

## Test Devices (example matrix)

| Device tier | Android version | RAM |
|---|---|---|
| Budget | Android 11 | 3 GB |
| Mid-range | Android 13 | 6 GB |
| Flagship | Android 14+ | 8 GB+ |
