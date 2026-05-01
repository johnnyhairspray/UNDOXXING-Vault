---
group: Product
category: Smart TV
brand: TCL
productLine: Q77K Series
models:
  - name: 65Q77K
    upc:
      - "050054109075"
released: 2024-01-01
status: Current
policyRetrieved: 2026-05-02
policyLastUpdated: 2025-07-18
policyUrl: https://www.tcl.com/global/en/privacy-notice
ftcActions: "Active — Texas AG Ken Paxton filed suit December 15, 2025 (State of Texas v. TCL Technology Group Corporation) for unlawful ACR data collection and sale to data brokers under Texas Deceptive Trade Practices Act. No FTC federal action to date. Vizio precedent: FTC $2.2M settlement 2017 for same ACR practices."
severityTier: 3
severityPoints: 100
scopeScore: 50
intensityScore: 55
udxScore: 52
hardenedUdxScore: 39
hardenedConfig: "Disabled ACR via Settings → Privacy → User Agreements → opt out of User Experience Improvement Program; deleted Advertising ID via Settings → Privacy → Ads → Delete Advertising ID; disabled Google Assistant via Settings → Device Preferences → Google Assistant → off. Eliminates ACR (HIGH/30) and voice data (MEDIUM/20) entirely from scoring."
scoredDate: 2026-05-02
scoredBy: Claude
aliases:
  - "TCL Q77"
  - "TCL 65Q77K"
  - "TCL Q77K"
tags:
  - product
  - tcl
  - smart-tv
  - google-tv
  - ACR
  - content-tracking
  - chinese-ownership
  - data-broker
  - advertising-profile
  - active-lawsuit
---

# TCL 65Q77K — UDX Score: 52 (Moderate) → Hardened: 39 (Low)

**⚠️ ACTIVE LEGAL ACTION:** Texas AG filed suit December 15, 2025 against TCL for ACR surveillance and data brokering. Case active as of scoring date.

**⚠️ NATIONAL SECURITY FLAG:** TCL is Chinese-owned (Shenzhen TCL New Technology Co., Ltd.). Data collected may be subject to China's National Security Law compelling disclosure to Chinese government. Texas AG complaint explicitly raises this concern.

---

## Summary

The TCL Q77K is a Google TV smart television that collects viewing data through Automated Content Recognition (ACR) technology by default, tracking what you watch approximately every 500 milliseconds — including content from cable boxes, gaming consoles, Blu-ray players, and any device connected via HDMI. This data is sold to data brokers and advertising networks. The TV runs two overlapping data collection layers: TCL's own and Google TV's. Both are active by default. The Chinese ownership of TCL adds a foreign adversary data access risk beyond typical smart TV concerns.

**Disabling ACR and the advertising ID drops the score from Moderate (52) to Low (39).** These are the two changes with the most meaningful real-world privacy impact.

---

## Hardware Profile (Q77K)

- **Display:** 65" QLED 4K, Google TV OS
- **Microphone:** Remote-activated only (press-to-talk for Google Assistant) — NOT always-on
- **Camera:** None on Q77K model — confirmed not listed in specs
- **ACR:** Built-in, active by default
- **Voice assistant:** Google Assistant via remote
- **Data jurisdiction:** Shenzhen, China (parent company data controller)

---

## Step 0 — Setup Flow and Default Mapping

**Default on (scored):**
- ACR content recognition / "Watchware" — ON by default per TX AG complaint
- Google TV data collection — required to use smart TV features
- Usage/interaction data collection — ON by default
- Device identifier collection — always active
- IP geolocation — always active
- PII collection (Google/TCL account required for full functionality)

**Opt-in (not scored):**
- Precise GPS location
- TCL account personalization features
- Third-party app data collection (governed by individual app policies)
- Market research participation

**Opt-out available (scored at 0.75x):**
- ACR — can be disabled in Settings > Privacy > User Agreements
- Advertising ID — can be deleted: Settings > Privacy > Ads > Delete Advertising ID
- User Experience Improvement Program — can be opted out

---

## Scoring — Data Type Breakdown

### Formula: Score = Base Severity × Handling% × Capture Mode × Opt-Out Mode

---

**1. ACR / Content Consumption Tracking** (HIGH = 30)

What it collects: Second-by-second fingerprinting of all content displayed on screen including cable, HDMI-connected devices, streaming apps. Captures every ~500ms per TX AG complaint.

Policy evidence: "details about your usage of the products that we supply to you such as the content viewed through the device and usage habits" — TCL Global Privacy Notice. TX AG complaint: "TCL secretly monitors what consumers watch across streaming apps, cable, and even connected devices like gaming consoles or Blu-ray players."

- Storage: 30% (cloud servers including China-based infrastructure)
- Purpose: 30% (behavioral profiling, targeted advertising — confirmed by TX AG)
- Sharing: 15% (demand-side platforms, ad networks, data brokers — confirmed by TX AG complaint)
- Retention: 7.5% (vague: "as long as needed")
- **Handling: 82.5%**
- Capture mode: 1.0x (continuous during use — default on)
- Opt-out: 0.75x (opt-out available but buried in settings)
- **Score: 30 × 0.825 × 1.0 × 0.75 = 18.56 / 30**

---

**2. Voice Commands** (MEDIUM = 20)

What it collects: Voice data when remote microphone button is pressed. Includes device description, voice, Skill Token, Voice command.

Policy evidence: "The Smart TV products capture data of the Amazon Alexa or Google Action voice assistant function on your Smart TV products. This information includes a device description, your voice, Skill Token and Voice command. When you use the voice assistant function, your voice data will be processed by Google or Amazon."

Note: Remote-activated (press to talk) — NOT always-on. Significantly reduces severity vs. always-on microphone.

- Storage: 15% (TCL logs metadata; voice processed by Google/Amazon)
- Purpose: 15% (command processing and service improvement)
- Sharing: 15% (Google or Amazon directly)
- Retention: 7.5% (not specified by TCL)
- **Handling: 52.5%**
- Capture mode: 0.5x (motion/button-activated)
- Opt-out: 1.0x (on by default when you use voice remote)
- **Score: 20 × 0.525 × 0.5 × 1.0 = 5.25 / 20**

---

**3. Usage / Interaction Patterns** (LOW = 10)

What it collects: App usage, button clicks, page views, time spent, feature usage, navigation paths, videos played, duration.

Policy evidence: "data about your usage of system functions, applications and smart services, and device activation and registration details, such as activation time format, page and button clicks, page viewed and time spent on those pages, time and duration of service usage, name and duration of videos played, and user favorites"

- Storage: 30% (cloud)
- Purpose: 15% (product improvement — relatively benign stated purpose)
- Sharing: 7.5% (TCL group companies)
- Retention: 7.5% (vague)
- **Handling: 60%**
- Capture mode: 1.0x (continuous during use)
- Opt-out: 0.75x (User Experience Improvement Program opt-out available)
- **Score: 10 × 0.60 × 1.0 × 0.75 = 4.50 / 10**

---

**4. Device Identifiers** (LOW = 10)

What it collects: IP address, MAC address, Device-ID, Terminal ID, serial number, and other device-specific identifiers.

Policy evidence: "the IP address, MAC address, Device-ID, Terminal ID, serial number, IMEI number, IMSI number and any other device identifiers or device-specific information about your TCL materials"

- Storage: 30% (cloud)
- Purpose: 15% (service delivery — functionally necessary)
- Sharing: 7.5% (TCL group)
- Retention: 7.5% (vague)
- **Handling: 60%**
- Capture mode: 1.0x (always active)
- Opt-out: 1.0x (no opt-out available)
- **Score: 10 × 0.60 × 1.0 × 1.0 = 6.00 / 10**

---

**5. PII — Account Information** (MEDIUM = 20)

What it collects: Name, email address, account credentials for Google account (required for Google TV functionality) and optional TCL account.

Policy evidence: "Personal and/or business contact information: your name, shipping, billing and/or business address, email address, phone number" — TCL Privacy Notice. Google TV requires Google account per Consumer Reports setup analysis.

- Storage: 30% (cloud, Google servers + TCL servers)
- Purpose: 15% (account management — functionally necessary)
- Sharing: 15% (Google, TCL group companies, payment processors)
- Retention: 7.5% (as long as account active)
- **Handling: 67.5%**
- Capture mode: 1.0x (collected during required setup)
- Opt-out: 1.0x (required for full functionality)
- **Score: 20 × 0.675 × 1.0 × 1.0 = 13.50 / 20**

---

**6. IP Geolocation** (LOW = 10)

What it collects: City-level location from IP address.

Policy evidence: "Geolocation data, which may include physical location or movements" listed under CCPA disclosures with sharing to "internet service providers."

- Storage: 30% (cloud)
- Purpose: 15% (service delivery + targeted advertising)
- Sharing: 15% (TCL group, internet service providers per CCPA table)
- Retention: 7.5% (vague)
- **Handling: 67.5%**
- Capture mode: 1.0x (always active)
- Opt-out: 1.0x (no opt-out)
- **Score: 10 × 0.675 × 1.0 × 1.0 = 6.75 / 10**

---

## Score Summary

| Data Type | Severity | Score | Handling% | Hardened |
|---|---|---|---|---|
| ACR / Content Tracking | 30 | 18.56 | 82.5% | ❌ eliminated |
| Voice Commands | 20 | 5.25 | 52.5% | ❌ eliminated |
| Usage / Interaction | 10 | 4.50 | 60% | ✅ retained |
| Device Identifiers | 10 | 6.00 | 60% | ✅ retained |
| PII (Account) | 20 | 13.50 | 67.5% | ✅ retained |
| IP Geolocation | 10 | 6.75 | 67.5% | ✅ retained |
| **TOTALS** | **100** | **54.56** | | |

**Default Scores:**
- Scope: 50 | Intensity: 55 | **UDX: 52 — Moderate (Tier 3)**

**Hardened Scores** (ACR + voice disabled):
- Remaining severity: 50 | Remaining score: 30.75
- Scope: 25 | Intensity: 61.5 | **Hardened UDX: 39 — Low (Tier 2)**

---

## Key Privacy Concerns

- **ACR data sold to data brokers** — confirmed by Texas AG lawsuit
- **Chinese ownership** — China's National Security Law can compel data disclosure
- **Dual collection layers** — TCL + Google TV both active by default
- **Active litigation** — Texas AG filed suit December 2025
- **HDMI surveillance** — ACR captures content from ALL connected sources

---

## Privacy Settings Guide

### 🔴 HIGH PRIORITY

**1. ACR / User Experience Improvement Program**
- **How:** Settings → Privacy → User Agreements → opt out of User Experience Improvement Program
- **What you lose:** Less relevant content recommendations. Ads still appear but untargeted.
- **Privacy gain:** Eliminates ACR data collection and sale to brokers. Largest single gain. **Drops score by ~13 points.**

**2. Advertising ID**
- **How:** Settings → Privacy → Ads → Delete Advertising ID
- **What you lose:** Ads still shown, just not personalized.
- **Privacy gain:** Breaks cross-app behavioral profile. Delete periodically for ongoing protection.

### 🟡 MEDIUM PRIORITY

**3. Basic TV Mode (Nuclear Option)**
- **How:** During initial setup only — choose "Basic TV" instead of "Google TV." Requires factory reset to change later.
- **What you lose:** Google Assistant, Play Store, streaming app integration, all Google smart features.
- **Privacy gain:** Eliminates Google's entire data collection layer. Best for users with a separate streaming device (Apple TV, Roku, Shield).

**4. Voice Assistant**
- **How:** Settings → Device Preferences → Google Assistant → off
- **What you lose:** Voice commands via remote. Navigation by button only.
- **Privacy gain:** Removes microphone data collection. Lower priority since mic is remote-activated, not always-on.

**5. Location Services**
- **How:** Settings → Privacy → Location → Off
- **What you lose:** Weather apps, local content recommendations.
- **Privacy gain:** Removes GPS/location from app ecosystem. IP geolocation still occurs.

### 🟢 LOW PRIORITY

**6. Diagnostic Data**
- **How:** Settings → Privacy → User Agreements → opt out of diagnostic data
- **What you lose:** Negligible.
- **Privacy gain:** Small. Worth doing but lowest priority.

---

## Optional Features (Not Scored — Opt-In)

- Precise GPS location
- TCL Health features
- Smart Home / TCL Home App device graph
- Social login (Facebook/Google to TCL Channel)

---

## Sources

- Privacy Policy: https://www.tcl.com/global/en/privacy-notice (effective 2025-07-18)
- Texas AG Complaint: https://www.texasattorneygeneral.gov/sites/default/files/images/press/TCL%20TV%20Petition%20Filed.pdf
- Texas AG lawsuit coverage: https://www.techradar.com/televisions/your-tv-is-a-mass-surveillance-system-says-texas
- IAPP ACR enforcement analysis: https://iapp.org/news/a/automated-content-recognition-technology-takes-privacy-enforcement-spotlight
- Consumer Reports 2025 TCL setup guide: https://www.consumerreports.org/electronics/privacy/how-to-turn-off-smart-tv-snooping-features-a4840102036/
- Hardware specs: https://tcl.com/us/en/products/home-theater/q77k-class/65-q77k-series-4k-uhd-hdr-qled-smart-google-tv-65q77k
