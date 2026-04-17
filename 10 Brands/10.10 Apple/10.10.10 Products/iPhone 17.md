---
group: Product
category: Smartphone
brand: Apple
productLine: iPhone 17
models:
  - name: iPhone 17
released: 2025-09-19
status: Current
policyRetrieved: 2026-04-16
policyLastUpdated: 2025-07-30
policyUrl: https://www.apple.com/legal/privacy/en-ww/
ftcActions: "$95M Siri class action settlement (January 2025) — unintended activations, sharing with contractors and advertisers 2014–2024. https://topclassactions.com/lawsuit-settlements/closed-settlements/apple-siri-class-action-settlement/"
severityTier: 3
severityPoints: 390
scopeScore: 100
intensityScore: 35
udxScore: 60
scoredDate: 2026-04-16
scoredBy: Claude
aliases:
  - iPhone 17
tags:
  - product
  - Apple
  - smartphone
  - Face-ID
  - biometric
  - iCloud
  - Siri
  - always-on-audio
  - location-tracking
  - surveillance-vector
---

# iPhone 17 — UDX Score: 60 (Moderate, Tier 3)

**Released:** September 19, 2025 | **Price:** $799 | **Chip:** A19
**Policy Retrieved:** April 16, 2026 | **Policy Last Updated:** July 30, 2025

---

## Pre-Scoring Checklist

- [x] Setup flow mapped — defaults vs opt-ins identified
- [x] Full privacy policy retrieved via web_fetch
- [x] iPhone-specific location and Siri privacy pages reviewed
- [x] Hardware specifications verified (Apple specs page + MacRumors)
- [x] FTC/legal actions checked — $95M Siri settlement (January 2025)
- [x] Default settings vs opt-in features verified
- [x] All data types have policy evidence
- [x] Uncertainties flagged explicitly

---

## Setup Flow: Defaults vs Opt-ins

**DEFAULT (on without user action or prompted with most users enabling):**
- Apple Account / PII — required
- Face ID — required for device security
- iCloud sync (contacts, reminders, notes, Safari) — on when Apple Account signed in
- iCloud Backup — prompted, default on
- iCloud Photos — prompted, most users enable (†flagged)
- Hey Siri always-on listening — on by default
- Siri processing — on by default
- Location Services — PROMPTED during setup; most users enable
- Significant Locations — on by default when location enabled
- Crowd-sourced location data to Apple — on when location enabled
- App Store / payment info — required for app purchases
- Crash Detection (hardware) — always-on, hardware-level
- Crash reports — automatic

**OPT-IN (excluded from scoring):**
- Apple Intelligence — requires explicit opt-in
- Improve Siri and Dictation — opt-in
- iCloud Analytics — opt-in
- Advanced Data Protection (E2E for most iCloud) — opt-in
- Health data recording — opt-in per app
- Location per third-party app — per-app permission

**E2E ENCRYPTED (Apple cannot access — scored at minimal handling):**
- Face ID / biometric data — on-device Secure Enclave only
- iMessage / FaceTime — E2E by default
- Health data in iCloud — E2E
- Significant Locations — E2E in iCloud
- Siri processing data — on-device where possible, random identifier otherwise

---

## Hardware Profile (iPhone 17 Base)

- **Face ID:** TrueDepth camera — dot projector, infrared camera, flood illuminator. Full 3D facial geometry scan.
- **Rear cameras:** 48MP Fusion main + 48MP Ultra Wide. No LiDAR (Pro models only).
- **Front camera:** TrueDepth (Face ID) + 12MP Center Stage
- **Always-On Display:** New to iPhone 17 base model (120Hz ProMotion OLED)
- **Microphone:** Bottom + top (spatial audio). Always-on for Hey Siri wake word detection.
- **GPS:** Precision dual-frequency (GPS, GLONASS, Galileo, QZSS, BeiDou, NavIC)
- **Motion:** High dynamic range gyroscope, dual-core accelerometer (256G), barometer
- **No LiDAR** — Pro models only (not scored here)
- **N1 wireless chip** — custom Apple networking chip

---

## Scoring Breakdown

### Formula: Score = Base Severity × Handling% × Capture Mode × Opt-Out Mode

---

### 1. Face ID — Facial Geometry
**Base:** 40 (SEVERE — facial recognition/geometry)

**Policy Evidence:** "Face ID data doesn't leave your device and is never backed up to iCloud or anywhere else. Only iPhone itself can access and use this data, and only when needed to confirm your identity." (Apple Face ID Privacy)

**Handling: 10%** — On-device Secure Enclave ONLY, authentication only, never shared, never transmitted
**Capture: 0.75x** | **Opt-out: 0.5x** (passcode alternative)

**Score: 40 × 0.10 × 0.75 × 0.5 = 1.5 / 40**

---

### 2. Always-On Audio (Hey Siri Wake Word)
**Base:** 40 (SEVERE — always-on audio surveillance capability)

**Policy Evidence:** "Your device will indicate in Siri Settings whether the things you say are processed on your device and not sent to Apple servers." (Apple Siri Privacy)

**Handling: 10%** — On-device Neural Engine only for wake word, not stored, not shared
**Capture: 1.0x** (always listening) | **Opt-out: 0.75x**

**Score: 40 × 0.10 × 1.0 × 0.75 = 3.0 / 40**

---

### 3. PII (5 Types: Name, Email, Phone, Address, DOB)
**Base:** 100 (MEDIUM × 5 — required for Apple Account)

**Policy Evidence:** "When you create an Apple Account... we may collect a variety of information, including Account Information [email, age], Contact Information [name, email, physical address, phone], Payment Information [billing address and payment card information]." (Apple Privacy Policy, July 30, 2025)

**Handling: 65%** — Cloud accessible to Apple, service + fraud + marketing use, shared with service providers and partners (Apple Card/Goldman Sachs, law enforcement)
**Capture: 1.0x** | **Opt-out: 1.0x** (required)

**Score: 100 × 0.65 × 1.0 × 1.0 = 65.0 / 100**

---

### 4. Precise GPS + Location History
**Base:** 30 (HIGH)

**Policy Evidence:** "If Location Services is on, your device will periodically send the geo-tagged locations of nearby Wi-Fi hotspots and cell towers in an anonymous and encrypted form to Apple." (Apple Location Services Privacy)

**Handling: 45%** — Anonymized/encrypted cloud storage, infrastructure use, shared with partners and licensees, retention period unspecified
**Capture: 0.75x** (prompted, most enable) | **Opt-out: 0.75x**

**Score: 30 × 0.45 × 0.75 × 0.75 = 7.59 / 30**

---

### 5. Activity/Routine Patterns (Significant Locations)
**Base:** 30 (HIGH)

**Policy Evidence:** "Your Significant Locations & Routes are synced between your devices using end-to-end encryption and cannot be read by Apple." (Apple Location Services Privacy)

**Handling: 20%** — E2E encrypted in iCloud, Apple cannot access, personalization only, not shared
**Capture: 0.75x** | **Opt-out: 0.75x** (Settings > Privacy > Location Services > System Services)

**Score: 30 × 0.20 × 0.75 × 0.75 = 3.375 / 30**

---

### 6. Siri Voice Queries
**Base:** 20 (MEDIUM — voice commands, search queries)

**Policy Evidence:** "Unless you opt in to Improve Siri and Dictation, your audio data is not stored by Apple. This data is associated with a random, device-generated identifier that is not tied to your Apple Account." (Apple Siri Privacy)

**FTC/Legal Evidence:** $95M class action settlement (January 2025) — unintended activations resulted in private conversations shared with Apple contractors and advertisers through December 2024.

**Handling: 60%** — Server-side processing, random identifier (not Apple Account), documented contractor and advertiser sharing via settlement
**Capture: 0.5x** (user-activated) | **Opt-out: 0.75x**

**Score: 20 × 0.60 × 0.5 × 0.75 = 4.5 / 20**

---

### 7. Social Graph / Contacts
**Base:** 20 (MEDIUM)

**Policy Evidence:** "If you sign in to iCloud, apps are granted access by default to iCloud Drive." Contacts sync to iCloud by default when signed in.

**Handling: 55%** — iCloud cloud storage (accessible to Apple without ADP), sync use, service providers
**Capture: 1.0x** | **Opt-out: 0.75x**

**Score: 20 × 0.55 × 1.0 × 0.75 = 8.25 / 20**

---

### 8. Content Consumption / App Store Activity
**Base:** 30 (HIGH — content consumption, purchase history)

**Policy Evidence:** "We create a Subscriber ID that is unique to you and the developer or publisher... The Subscriber ID may be used to provide reports to the developer or publisher, which include information about the subscription you purchased and your country of residence." (Apple Privacy Policy)

**Handling: 65%** — Cloud storage, developer Subscriber ID sharing, analytics
**Capture: 0.75x** | **Opt-out: 0.75x**

**Score: 30 × 0.65 × 0.75 × 0.75 = 10.97 / 30**

---

### 9. Payment Information
**Base:** 20 (MEDIUM)

**Policy Evidence:** "Payment Information: Data about your billing address and method of payment, such as bank details, credit, debit, or other payment card information." (Apple Privacy Policy)

**Handling: 55%** — Secure cloud, transaction processing, payment processors and partners
**Capture: 1.0x** | **Opt-out: 1.0x** (required)

**Score: 20 × 0.55 × 1.0 × 1.0 = 11.0 / 20**

---

### 10. Device Information
**Base:** 10 (LOW)

**Policy Evidence:** "Device Information: Data from which your device could be identified, such as device serial number, or about your device, such as browser type." (Apple Privacy Policy)

**Handling: 50%** | **Capture: 1.0x** | **Opt-out: 1.0x** (unavoidable)

**Score: 10 × 0.50 × 1.0 × 1.0 = 5.0 / 10**

---

### 11. Usage / Crash Data
**Base:** 10 (LOW)

**Policy Evidence:** "Usage Data: Data about your activity on and use of our offerings, such as app launches within our services, including browsing history; search history; product interaction; crash data, performance and other diagnostic data." (Apple Privacy Policy)

**Handling: 40%** | **Capture: 0.5x** (crash-triggered) | **Opt-out: 0.75x**

**Score: 10 × 0.40 × 0.5 × 0.75 = 1.5 / 10**

---

### 12. Crash Detection (Motion Sensors)
**Base:** 10 (LOW — classified LOW: safety-specific, on-device only, no profiling use)

**Policy Evidence:** "Hardware sensors and advanced motion algorithms can detect a severe car crash and automatically dial emergency services." (Apple iPhone 17 product page)

**Handling: 10%** — On-device, emergency use only, not retained
**Capture: 1.0x** (always-on hardware) | **Opt-out: 0.75x**

**Score: 10 × 0.10 × 1.0 × 0.75 = 0.75 / 10**

---

### 13. iCloud Photos (†)
**Base:** 30 (HIGH)

**† Uncertainty:** iCloud Photos prompted during setup. Scored as default based on majority user behavior.

**Policy Evidence:** iCloud Photos are NOT end-to-end encrypted by default. Apple can access them without Advanced Data Protection (ADP), which is opt-in only.

**Handling: 70%** — Cloud accessible to Apple, law enforcement access, no specified retention maximum
**Capture: 1.0x** | **Opt-out: 0.75x**

**Score: 30 × 0.70 × 1.0 × 0.75 = 15.75 / 30**

---

## Score Compilation

| Data Type | Base | Score |
|-----------|------|-------|
| Face ID biometric | 40 | 1.5 |
| Always-on audio (Hey Siri) | 40 | 3.0 |
| PII (5 types) | 100 | 65.0 |
| GPS / crowd-sourced location | 30 | 7.59 |
| Significant Locations | 30 | 3.375 |
| Siri voice queries | 20 | 4.5 |
| Social graph / contacts | 20 | 8.25 |
| Content / App Store | 30 | 10.97 |
| Payment information | 20 | 11.0 |
| Device information | 10 | 5.0 |
| Usage / crash data | 10 | 1.5 |
| Crash Detection motion | 10 | 0.75 |
| iCloud Photos (†) | 30 | 15.75 |
| **TOTAL** | **390** | **138.2** |

**Scope:** min(390/200, 1) × 100 = **100**
**Intensity:** min(138.2/390 × 100, 100) = **35.4%**
**UDX:** √(100 × 35.4) = **60**

---

## UDX: 60 — Moderate (Tier 3, High End)

Apple scores better than most major platforms due to on-device biometrics, E2E health data, and no data selling — but broad scope and accessible iCloud data without ADP keeps it in Moderate.

**Single most impactful user action:** Enable Advanced Data Protection. Estimated score drops to ~45–50.

---

## Key Privacy Concerns

1. **iCloud Photos accessible to Apple** — Standard iCloud is not E2E. Apple can access your photo library for legal requests.
2. **Siri contractor/advertiser sharing (documented)** — $95M settlement establishes real sharing through December 2024.
3. **Subscriber IDs shared with developers** — Enables cross-session tracking per developer.
4. **Location shared with unnamed partners** — "Partners and licensees" not specified in policy.
5. **PII in accessible iCloud** — Contacts, calendar, notes not E2E by default.

---

## Pro Model Hardware Differences

- **LiDAR Scanner (Pro/Pro Max only)** — Spatial mapping capability. Score impact: adds ~MEDIUM (20) spatial mapping data type. Estimated UDX impact: +2–3 points.
- **iPhone Air** — Same surveillance hardware profile, score would be near-identical.

---

## Optional Features (Not Scored)

| Feature | If Enabled | Score Impact |
|---------|-----------|--------------|
| Advanced Data Protection | Reduces | UDX ~45–50 |
| Improve Siri & Dictation | Increases | Audio stored/reviewed |
| iCloud Analytics | Increases | Behavioral data shared |
| Apple Intelligence | Increases | On-screen content processing |
| Third-party app location (Always) | Increases | Continuous third-party location |

---

## Sources

- Apple Privacy Policy: https://www.apple.com/legal/privacy/en-ww/ (July 30, 2025)
- Siri & Dictation Privacy: https://www.apple.com/legal/privacy/data/en/ask-siri-dictation/
- Location Services Privacy: https://www.apple.com/legal/privacy/data/en/location-services/
- iPhone 17 Specs: https://www.apple.com/iphone-17/specs/
- $95M Siri Settlement: https://topclassactions.com/lawsuit-settlements/closed-settlements/apple-siri-class-action-settlement/
- Research Date: April 16, 2026
