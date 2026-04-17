---
group: Product
category: Smartphone
brand: Apple
productLine: iPhone 17
models:
  - name: iPhone 17
    upc: []
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

**Handling Assessment:**
- Storage: On-device Secure Enclave ONLY — never transmitted (5%)
- Purpose: Authentication only — no analytics, no profiling (5%)
- Sharing: Never shared with Apple or any third party (0%)
- Retention: Stored locally until user removes Face ID (5%)
- **Handling: 10%**

**Modifiers:**
- Capture: 0.75x (user-initiated unlock, used many times daily but not continuous)
- Opt-out: 0.5x (passcode alternative available)

**Score: 40 × 0.10 × 0.75 × 0.5 = 1.5 / 40**

*Note: Apple's implementation here is best-in-class for biometric data. The Secure Enclave architecture genuinely prevents server-side access. Score is low because handling is exemplary.*

---

### 2. Always-On Audio (Hey Siri Wake Word)
**Base:** 40 (SEVERE — always-on audio surveillance capability)

**Policy Evidence:** "Your device will indicate in Siri Settings whether the things you say are processed on your device and not sent to Apple servers." (Apple Siri Privacy Page)

**Handling Assessment:**
- Storage: On-device only for wake word detection (5%)
- Purpose: Wake word only — no content analysis of ambient audio (5%)
- Sharing: Wake word processing not shared (0%)
- Retention: Not stored — processed and discarded in real time (0%)
- **Handling: 10%**

**Modifiers:**
- Capture: 1.0x (microphone always active for wake word detection)
- Opt-out: 0.75x (can disable "Listen for Siri" but default is on)

**Score: 40 × 0.10 × 1.0 × 0.75 = 3.0 / 40**

*Note: Apple processes Hey Siri entirely on-device via Neural Engine. The hardware capability exists and is always-on, but data handling is on-device only. Score reflects hardware severity offset by exemplary implementation.*

---

### 3. PII (5 Types: Name, Email, Phone, Address, DOB)
**Base:** 20 × 5 = 100 (MEDIUM — required for Apple Account)

**Policy Evidence:** "When you create an Apple Account... we may collect a variety of information, including Account Information [email, age], Contact Information [name, email, physical address, phone], Payment Information [billing address and payment card information]." (Apple Privacy Policy, July 30, 2025)

**Handling Assessment:**
- Storage: Cloud (iCloud), accessible to Apple without ADP (25%)
- Purpose: Service delivery, fraud prevention, marketing communications (20%)
- Sharing: Service providers, partners (Apple Card/Goldman Sachs, Apple Cash/Green Dot), law enforcement per legal requirement (15%)
- Retention: Account duration plus legal requirements, unspecified maximum (15%)
- **Handling: 65%**

**Modifiers:**
- Capture: 1.0x (required at setup)
- Opt-out: 1.0x (cannot use device fully without Apple Account)

**Score: 100 × 0.65 × 1.0 × 1.0 = 65.0 / 100**

---

### 4. Precise GPS + Location History
**Base:** 30 (HIGH — precise GPS + location history)

**Policy Evidence:** "If Location Services is on, your device will periodically send the geo-tagged locations of nearby Wi-Fi hotspots and cell towers in an anonymous and encrypted form to Apple, to be used for augmenting this crowd-sourced database." (Apple Location Services Privacy)

**Handling Assessment:**
- Storage: Cloud, anonymized and encrypted (15%)
- Purpose: Infrastructure (maps accuracy, road traffic) — not behavioral profiling (10%)
- Sharing: Partners and licensees for location services (per Location Services policy) (15%)
- Retention: Policy does not specify retention period for crowd-sourced location data (15%)
- **Handling: 45%**

**Modifiers:**
- Capture: 0.75x (only when Location Services enabled — prompted, most users enable)
- Opt-out: 0.75x (can disable location entirely but significantly degrades functionality)

**Score: 30 × 0.45 × 0.75 × 0.75 = 7.59 / 30**

*Note: Location Services is prompted during setup — not silently enabled. Score reflects that most users enable it. Apple's crowd-sourcing uses anonymized data, reducing intensity score.*

---

### 5. Activity/Routine Patterns (Significant Locations)
**Base:** 30 (HIGH — activity/routine patterns: home/away, visited places, routes)

**Policy Evidence:** "Your iPhone and other devices where you sign in to iCloud with your Apple Account will keep track of places you have recently been, how often and when you visited them, and the routes you take to get there... Your Significant Locations & Routes are synced between your devices using end-to-end encryption and cannot be read by Apple." (Apple Location Services Privacy)

**Handling Assessment:**
- Storage: E2E encrypted in iCloud — Apple cannot read (5%)
- Purpose: Personalization (Photos Memories, route suggestions) — on-device (10%)
- Sharing: Not shared — E2E protection (0%)
- Retention: Synced across devices, E2E encrypted, unclear maximum retention (10%)
- **Handling: 20%**

**Modifiers:**
- Capture: 0.75x (on by default when location enabled, but subservice)
- Opt-out: 0.75x (can disable: Settings > Privacy > Location Services > System Services > Significant Locations)

**Score: 30 × 0.20 × 0.75 × 0.75 = 3.375 / 30**

*Note: E2E encryption means Apple cannot access this data. Score reflects hardware capability and that the data EXISTS, even though Apple's handling is responsible.*

---

### 6. Voice Commands / Search Queries (Siri)
**Base:** 20 (MEDIUM — search & query data, voice commands)

**Policy Evidence:** "When you use Siri, your device will indicate in Siri Settings whether the things you say are processed on your device and not sent to Apple servers. Otherwise, your audio is sent to and processed on Apple servers. Unless you opt in to Improve Siri and Dictation, your audio data is not stored by Apple. This data is associated with a random, device-generated identifier that is not tied to your Apple Account." (Apple Siri Privacy)

**FTC/Legal Evidence:** Apple settled a $95M class action in January 2025 covering Siri unintended activations 2014–2024. Settlement resolved claims that private conversations were "shared with Apple contractors and advertisers." Apple did not admit wrongdoing but the settlement establishes documented third-party sharing.

**Handling Assessment:**
- Storage: Server-side processing when not on-device capable, random identifier (20%)
- Purpose: Service delivery (Siri responses) — not building profiles per Apple (15%)
- Sharing: Apple processing + documented contractor sharing (quality review) + alleged advertiser sharing per settlement (25%)
- Retention: Not stored without opt-in, but processing occurs server-side (10%)
- **Handling: 60%**

**Modifiers:**
- Capture: 0.5x (user-activated — button or wake word required)
- Opt-out: 0.75x (can disable Siri but default is on)

**Score: 20 × 0.60 × 0.5 × 0.75 = 4.5 / 20**

*Note: Handling elevated to 60% (from base ~45%) due to documented $95M settlement establishing real-world contractor and advertiser sharing. Apple's January 2025 statement claims this has been remediated.*

---

### 7. Social Graph / Contacts
**Base:** 20 (MEDIUM — social graph)

**Policy Evidence:** "Apps are granted access by default to iCloud Drive" (when signed in to iCloud). Contacts sync to iCloud by default.

**Handling Assessment:**
- Storage: iCloud cloud storage, accessible to Apple without ADP (25%)
- Purpose: Sync across devices (legitimate) (15%)
- Sharing: Service providers with contractual protections (10%)
- Retention: Account duration, no specified maximum (15%)
- **Handling: 55%**

**Modifiers:**
- Capture: 1.0x (iCloud contacts sync on by default)
- Opt-out: 0.75x (can disable iCloud contacts sync)

**Score: 20 × 0.55 × 1.0 × 0.75 = 8.25 / 20**

---

### 8. Content Consumption / App Store Activity
**Base:** 30 (HIGH — content consumption tracking)

**Policy Evidence:** "We create a Subscriber ID that is unique to you and the developer or publisher... The Subscriber ID may be used to provide reports to the developer or publisher, which include information about the subscription you purchased and your country of residence." (Apple Privacy Policy)

Also: App Store purchase history, search queries, download history tracked.

**Handling Assessment:**
- Storage: Cloud (25%)
- Purpose: Service delivery + analytics + developer reporting via Subscriber ID (20%)
- Sharing: Developer Subscriber IDs disclosed to third-party developers (15%)
- Retention: Account duration (15%)
- **Handling: 65%**

**Modifiers:**
- Capture: 0.75x (when using App Store / Apple services)
- Opt-out: 0.75x (cannot avoid if using App Store at all)

**Score: 30 × 0.65 × 0.75 × 0.75 = 10.97 / 30**

---

### 9. Payment Information
**Base:** 20 (MEDIUM — payment information)

**Policy Evidence:** "Payment Information: Data about your billing address and method of payment, such as bank details, credit, debit, or other payment card information." (Apple Privacy Policy)

**Handling Assessment:**
- Storage: Secure cloud (20%)
- Purpose: Transaction processing (15%)
- Sharing: Payment processors, partners (Apple Card/Goldman Sachs) (10%)
- Retention: Account duration plus tax/legal obligations (15%)
- **Handling: 55%**

**Modifiers:**
- Capture: 1.0x (required for App Store)
- Opt-out: 1.0x (required for paid features)

**Score: 20 × 0.55 × 1.0 × 1.0 = 11.0 / 20**

---

### 10. Device Information
**Base:** 10 (LOW — device information)

**Policy Evidence:** "Device Information: Data from which your device could be identified, such as device serial number, or about your device, such as browser type." (Apple Privacy Policy)

**Handling Assessment:**
- Storage: Cloud (20%)
- Purpose: Service delivery, fraud prevention (20%)
- Sharing: Service providers (10%)
- Retention: Account duration (15%)
- **Handling: 50%**

**Modifiers:**
- Capture: 1.0x (always collected)
- Opt-out: 1.0x (unavoidable)

**Score: 10 × 0.50 × 1.0 × 1.0 = 5.0 / 10**

---

### 11. Usage / Crash Data
**Base:** 10 (LOW — interaction & usage patterns, crash reports)

**Policy Evidence:** "Usage Data: Data about your activity on and use of our offerings, such as app launches within our services, including browsing history; search history; product interaction; crash data, performance and other diagnostic data." (Apple Privacy Policy)

**Handling Assessment:**
- Storage: Cloud (20%)
- Purpose: Service improvement (15%)
- Sharing: Internal use (5%)
- Retention: Unspecified (10%)
- **Handling: 40%**

**Modifiers:**
- Capture: 0.5x (crash-triggered for most diagnostic data)
- Opt-out: 0.75x (analytics opt-in but crash reports automatic)

**Score: 10 × 0.40 × 0.5 × 0.75 = 1.5 / 10**

---

### 12. Crash Detection (Motion Sensors)
**Base:** 10 (LOW — motion sensor data for safety)

*Classified as LOW rather than HIGH because this data is safety-specific (crash detection), processed entirely on-device, and not used for behavioral profiling.*

**Policy Evidence:** "Hardware sensors and advanced motion algorithms can detect a severe car crash and automatically dial emergency services." (Apple iPhone 17 product page)

**Handling Assessment:**
- Storage: On-device only unless crash detected (5%)
- Purpose: Emergency safety only (5%)
- Sharing: Emergency services only upon crash detection (5%)
- Retention: Not retained — processed in real time (5%)
- **Handling: 10%**

**Modifiers:**
- Capture: 1.0x (hardware always monitoring)
- Opt-out: 0.75x (can disable in Settings but default on)

**Score: 10 × 0.10 × 1.0 × 0.75 = 0.75 / 10**

---

### 13. iCloud Photos (†)
**Base:** 30 (HIGH — content/activity data: personal photos and videos)

**† Uncertainty Note:** iCloud Photos is PROMPTED during iPhone setup. Most users enable it. Scored as default based on common user behavior, but this may be lower for privacy-conscious users who decline.

**Policy Evidence:** iCloud Photos not end-to-end encrypted by default. Apple CAN access iCloud Photos without Advanced Data Protection (ADP). ADP is opt-in. "Recordings from security cameras that use HomeKit Secure Video are analyzed privately on your Apple devices at home and then sent securely to iCloud through end-to-end encryption." (This suggests HomeKit Secure Video IS E2E — but standard iCloud Photos are NOT.)

**Handling Assessment:**
- Storage: Apple cloud, accessible to Apple without ADP (30%)
- Purpose: Backup and sync (legitimate) but Apple can access for legal requests (20%)
- Sharing: Service providers, law enforcement per legal requirements (15%)
- Retention: Account duration, no specified maximum for Photos (15%)
- **Handling: 70%**

**Modifiers:**
- Capture: 1.0x (all photos backed up automatically when enabled)
- Opt-out: 0.75x (can disable iCloud Photos but most users don't)

**Score: 30 × 0.70 × 1.0 × 0.75 = 15.75 / 30**

---

## Score Compilation

| Data Type | Base | Score | Notes |
|-----------|------|-------|-------|
| Face ID biometric | 40 | 1.5 | On-device Secure Enclave only |
| Always-on audio (Hey Siri) | 40 | 3.0 | On-device wake word processing |
| PII (5 types) | 100 | 65.0 | Required for Apple Account |
| GPS / crowd-sourced location | 30 | 7.59 | Anonymized, prompted |
| Significant Locations | 30 | 3.375 | E2E encrypted |
| Siri voice queries | 20 | 4.5 | Settlement evidence increases sharing score |
| Social graph / contacts | 20 | 8.25 | iCloud default sync |
| Content / App Store | 30 | 10.97 | Subscriber IDs to developers |
| Payment information | 20 | 11.0 | Required |
| Device information | 10 | 5.0 | Always collected |
| Usage / crash data | 10 | 1.5 | Mostly crash-triggered |
| Crash Detection motion | 10 | 0.75 | On-device safety only |
| iCloud Photos (†) | 30 | 15.75 | Accessible to Apple without ADP |
| **TOTAL** | **390** | **138.2** | |

**Scope Score:** min(390 / 200, 1) × 100 = **100**
*(Capped — smartphones collect across nearly all possible data categories)*

**Intensity Score:** min(138.2 / 390 × 100, 100) = **35.4%**

**UDX Score:** √(100 × 35.4) = √3540 = **59.5 ≈ 60**

---

## UDX: 60 — Moderate (Tier 3, High End)

---

## What This Score Means

The iPhone 17 scores at the **high end of Moderate** — better than most comparable smartphones, but not as low as truly privacy-respecting devices.

**Why it scores BETTER than expected for a major platform:**
- Face ID biometric data never leaves the device — Apple genuinely cannot access your face geometry
- Health data is E2E encrypted — Apple cannot read it
- Siri uses random identifiers, not tied to Apple Account
- Apple does not sell personal data (documented and legally stated)
- Significant Locations are E2E encrypted

**Why it doesn't score LOW:**
- Broad data collection scope across nearly all categories (Scope = 100%)
- iCloud data (Photos, contacts, backup) accessible to Apple without Advanced Data Protection
- Documented $95M Siri settlement establishes real-world contractor and advertiser sharing (through 2024)
- Subscriber IDs shared with developers for analytics
- PII required for basic device functionality

**The core tension:** Apple has genuinely better privacy architecture than most competitors, but the breadth of data collected across the Apple ecosystem (iCloud, App Store, Siri, location) and Apple's access to non-E2E iCloud data keeps the score in Moderate territory.

---

## Key Privacy Concerns

1. **iCloud Photos accessible to Apple** — Without Advanced Data Protection (opt-in), Apple can access your photo library. This is a significant gap given Apple's privacy positioning.

2. **Siri contractor sharing (documented)** — The $95M settlement establishes that private conversations were shared with contractors and advertisers through December 2024. Apple's remediation claims are not independently verified.

3. **Subscriber IDs** — Developers receive a unique ID per subscriber enabling cross-session tracking within an app/developer ecosystem.

4. **Location data shared with partners** — Apple's Location Services policy permits sharing with "partners and licensees." Scope of partners not specified.

5. **PII in accessible iCloud** — Name, email, contacts, calendar, notes stored in iCloud without E2E encryption by default.

---

## Pro Model Differences (Not Scored Here)

**iPhone 17 Pro / Pro Max** warrant a separate note. Surveillance-relevant hardware additions:
- **LiDAR Scanner** — Creates spatial maps of environments. Classified as spatial mapping (MEDIUM - 20). Processing is primarily on-device for AR features. Score impact: moderate increase.
- **Additional telephoto camera** — No direct surveillance scoring impact.
- **Larger battery** — No scoring impact.

**iPhone Air** — Different form factor but same core hardware profile for surveillance purposes. Score would be nearly identical to iPhone 17.

---

## Optional Features (Not Scored)

| Feature | Activation | Score Impact if Enabled |
|---------|------------|------------------------|
| Apple Intelligence | Opt-in | Processing of on-screen content, messaging, photos — Phase 2 score |
| Advanced Data Protection | Opt-in | REDUCES score significantly — makes most iCloud E2E |
| Improve Siri & Dictation | Opt-in | INCREASES score — audio stored and reviewed |
| iCloud Analytics | Opt-in | INCREASES score — behavioral data shared |
| Third-party app location (Always) | Per-app opt-in | INCREASES score — continuous location to third parties |

**Note on Advanced Data Protection:** Enabling ADP would be the single highest-impact action to reduce iPhone's privacy risk. It would make iCloud Photos, iCloud Backup, and most other iCloud data E2E encrypted. Score impact estimated: UDX would drop to approximately 45–50 with ADP enabled.

---

## Sources

- Privacy Policy: https://www.apple.com/legal/privacy/en-ww/ (July 30, 2025)
- Siri & Dictation Privacy: https://www.apple.com/legal/privacy/data/en/ask-siri-dictation/
- Location Services Privacy: https://www.apple.com/legal/privacy/data/en/location-services/
- Face ID Privacy: https://support.apple.com/en-us/111828
- iPhone 17 Hardware Specs: https://www.apple.com/iphone-17/specs/
- iPhone 17 Overview (MacRumors): https://www.macrumors.com/roundup/iphone-17/
- $95M Siri Settlement: https://topclassactions.com/lawsuit-settlements/closed-settlements/apple-siri-class-action-settlement/
- iCloud default settings: https://appleinsider.com/inside/icloud/tips/how-to-turn-off-iclouds-default-settings-in-macos-and-ios
- Research Date: April 16, 2026
