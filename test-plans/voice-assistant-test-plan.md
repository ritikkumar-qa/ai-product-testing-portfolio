# 📋 Test Plan — Android Voice Assistant (Release Testing)

## 1. Objective

Make sure a new build of a voice assistant app is stable, understands users in English, Hindi and Hinglish, and works on low-end to flagship Android phones before release.

## 2. Scope

**In scope**
- Wake word & activation
- Voice recognition (3 languages)
- Replies, interruption & follow-ups
- Device actions (apps, calls, alarms)
- Offline / bad network behaviour
- Battery, heat & long-session stability

**Out of scope**
- Backend load testing
- Security / penetration testing

## 3. Approach

| Type | How |
|---|---|
| Functional | Run test cases in [`test-cases/`](../test-cases/voice-assistant-test-cases.md) |
| Exploratory | 30-min free-use sessions, note anything odd |
| Regression | Run [regression checklist](../checklists/regression-checklist.md) on every new build |
| Real-world | Test in noisy rooms, outdoors, while moving |

## 4. Devices

| Tier | Android | Why |
|---|---|---|
| Budget (3 GB RAM) | 11 | Most users in India |
| Mid-range (6 GB) | 13 | Common daily phone |
| Flagship (8 GB+) | 14+ | Latest OS behaviour |

## 5. Entry & Exit Criteria

**Start testing when:** build installs cleanly and app opens.

**Ready to release when:**
- 0 open Critical bugs
- 0 open Major bugs in core voice flow
- ≥ 95% of test cases pass
- Regression checklist fully green

## 6. Bug Reporting

Every bug uses the [bug report template](../bug-reports/bug-report-template.md).
Flow: **Reproduce → Document → Report → Retest**

## 7. Risks

| Risk | Mitigation |
|---|---|
| Accent / dialect variation | Test with multiple speakers |
| Phone-specific mic issues | Cover 3 device tiers |
| Patchy network | Test on 4G, WiFi & offline |
