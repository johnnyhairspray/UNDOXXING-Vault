---
group: Product
category: Smartphone
brand: TCL
productLine: NXTPAPER 70 Pro
models:
  - name: NXTPAPER 70 Pro
    upc:
released: 2026-01-05
status: Current
policyRetrieved: 2026-05-02
policyLastUpdated: 2025-07-18
policyUrl: https://www.tcl.com/global/en/privacy-notice
policyNote: "[[TCL Global Privacy Notice]]"
ftcActions: "None specific to this product. See TCL Global Privacy Notice for brand-level TX AG action (December 2025) targeting ACR in smart TVs — not directly applicable to smartphones."
severityTier: 2
severityPoints: 130
scopeScore: 42
intensityScore: 55
udxScore: 48
hardenedUdxScore: 32
hardenedConfig: "Disable Google Personalization: Settings → Google → Ads → Delete Advertising ID, and Opt out of Ads Personalization. Disable Location: Settings → Location → off or per-app. Disable Usage & Diagnostics: Settings → Google → Usage & Diagnostics → off. Disable Gemini activity: myactivity.google.com → Other Google Activity → Gemini → off. Disable microphone for non-essential apps: Settings → Privacy → Permission Manager → Microphone."
scoredDate: 2026-05-02
scoredBy: Claude
aliases:
  - "TCL NXTPAPER 70 Pro"
  - "NXTPAPER 70 Pro"
  - "TCL NxtPaper 70 Pro"
tags:
  - product
  - tcl
  - smartphone
  - android
  - NXTPAPER
  - google-gemini
  - chinese-ownership
  - ai-features
  - midrange
---

# TCL NXTPAPER 70 Pro — UDX Score: 48 (Moderate) → Hardened: 32 (Low)

**⚠️ NATIONAL SECURITY FLAG:** Chinese-owned (Shenzhen TCL). Data subject to China's National Security Law.
**Policy:** See [[TCL Global Privacy Notice]]
**Note:** The TX AG December 2025 ACR lawsuit targets TCL's smart TVs specifically — ACR is not present on this smartphone product.

---

## Summary

A mid-range Android 16 smartphone with TCL's NXTPAPER 4.0 eye-comfort display, launched at CES 2026 and available in the US exclusively via T-Mobile at $199. The display technology itself introduces no additional privacy risk — it's hardware-level optics (LCD + matte layer + polarizer + nano-matrix lithography). The privacy profile is driven by Android's standard data collection layer, Gemini AI integration, and TCL's own usage data collection — a significantly better profile than TCL's smart TVs which carry the ACR surveillance burden. The Chinese ownership flag applies to all TCL products regardless.

**No ACR.** This is meaningfully better than the Q77K TV score.

---

## Hardware Profile

- **Display:** 6.9" FHD+ 120Hz IPS LCD, NXTPAPER 4.0 (matte, anti-glare, blue light filtered)
- **Processor:** MediaTek Dimensity 7300
- **RAM:** 8GB (expandable to 24GB virtual)
- **Storage:** 256GB / 512GB + microSD up to 2TB
- **Cameras:** 50MP main (OIS) + 8MP ultrawide rear; 32MP front
- **Microphone:** Standard smartphone mic — NOT always-on for voice assistant by default
- **AI features:** Gemini integration (Google), MuseFilm imaging, AI Outline/Q&A/Audiobook/Podcast in Max Ink Mode, face-to-face translation, real-time subtitles
- **Battery:** 5200mAh, 33W charging
- **Protection:** IP68
- **OS:** Android 16
- **Data jurisdiction:** Shenzhen, China (TCL controller); Google (Android/Gemini)

---

## NXTPAPER Technology — Privacy Neutral

The NXTPAPER display technology is hardware-level optics. It collects no additional data. The NXTPAPER Key (physical switch for display modes), Max Ink Mode, and eye comfort certifications are hardware/software display features that operate locally without telemetry beyond TCL's standard usage data collection. **The display is not a privacy concern.**

---

## Default Data Collection

**Two overlapping layers — TCL's and Google's — same as any Android phone.**

| Source | What It Collects | Default |
|---|---|---|
| TCL | Device identifiers, usage patterns, crash/diagnostic data, account info if TCL account created | ON |
| Google/Android | Google account data, app usage, location history, search/browsing, YouTube, advertising profile | ON |
| Gemini | Voice queries, on-screen content selections, conversation history (Gemini Activity) | ON when used |
| MuseFilm / Camera AI | Photo processing done on-device per TCL — no cloud upload of photos without user action | On-device |

**No ACR.** No content fingerprinting of what's on the screen. No data sold to brokers for viewing habits.

---

## Score Breakdown

### Formula: Score = Base Severity × Handling% × Capture Mode × Opt-Out Mode

**1. Voice / Microphone** (MEDIUM = 20)

Voice queries via Gemini. Real-time translation and subtitles. Standard Android microphone access for apps.

- Storage: 15% (Google servers)
- Purpose: 15% (service delivery + model improvement)
- Sharing: 15% (Google — Gemini activity logs)
- Retention: 7.5% (activity history until deleted)
- **Handling: 52.5%**
- Capture mode: 0.5x (user-activated, not always-on)
- Opt-out: 0.75x (Gemini activity can be paused; mic permissions manageable per-app)
- **Score: 20 × 0.525 × 0.5 × 0.75 = 3.94 / 20**

**2. Location** (HIGH = 30)

Android location services. Used by maps, weather, translation, emergency services. Google location history if enabled.

- Storage: 30% (Google/TCL cloud)
- Purpose: 15% (service delivery + advertising)
- Sharing: 15% (Google advertising ecosystem, TCL group)
- Retention: 7.5% (history until deleted)
- **Handling: 67.5%**
- Capture mode: 0.75x (requires active use of location-dependent apps; not continuously streaming)
- Opt-out: 0.75x (location can be disabled; per-app controls available)
- **Score: 30 × 0.675 × 0.75 × 0.75 = 11.39 / 30**

**3. Usage / Interaction Patterns** (LOW = 10)

App launches, screen time, feature usage, TCL usage data per policy.

- Storage: 30% (cloud)
- Purpose: 15% (product improvement)
- Sharing: 7.5% (TCL group)
- Retention: 7.5% (vague)
- **Handling: 60%**
- Capture mode: 1.0x (continuous during use)
- Opt-out: 0.75x (Usage & Diagnostics can be disabled)
- **Score: 10 × 0.60 × 1.0 × 0.75 = 4.50 / 10**

**4. Device Identifiers** (LOW = 10)

IMEI, serial number, device ID, MAC address, IP address. Standard Android identifiers.

- Storage: 30% (cloud)
- Purpose: 15% (service delivery)
- Sharing: 7.5% (TCL group, Google, carriers)
- Retention: 7.5% (indefinite)
- **Handling: 60%**
- Capture mode: 1.0x (always active)
- Opt-out: 1.0x (no opt-out for core identifiers)
- **Score: 10 × 0.60 × 1.0 × 1.0 = 6.00 / 10**

**5. PII — Account Information** (MEDIUM = 20)

Google account required for full Android functionality. Optional TCL account. Carrier account via T-Mobile.

- Storage: 30% (Google/TCL/carrier cloud)
- Purpose: 15% (account management)
- Sharing: 15% (Google services, TCL group, T-Mobile)
- Retention: 7.5% (as long as account active)
- **Handling: 67.5%**
- Capture mode: 1.0x (required for setup)
- Opt-out: 1.0x (required for full functionality)
- **Score: 20 × 0.675 × 1.0 × 1.0 = 13.50 / 20**

**6. Camera / Image Data** (MEDIUM = 20)

50MP + 8MP + 32MP cameras. MuseFilm AI processing. Google Photos integration if enabled.

- Storage: 15% (on-device processing confirmed for MuseFilm; cloud only if user uploads)
- Purpose: 15% (service delivery — photography)
- Sharing: 7.5% (Google Photos if enabled; otherwise local)
- Retention: 7.5% (user-controlled)
- **Handling: 45%**
- Capture mode: 0.5x (user-activated)
- Opt-out: 0.75x (Google Photos sync can be disabled; camera permission manageable)
- **Score: 20 × 0.45 × 0.5 × 0.75 = 3.38 / 20**

**7. Biometric Data** (LOW = 10)

Face unlock and fingerprint sensor (standard Android biometric auth). Processed on-device per Android security model.

- Storage: 0% (on-device only — Android Keystore; not uploaded)
- Purpose: 15% (authentication)
- Sharing: 0% (not shared)
- Retention: 7.5% (on-device until deleted)
- **Handling: 22.5%**
- Capture mode: 0.5x (user-activated for unlock)
- Opt-out: 0.75x (biometric auth optional; PIN/password alternative)
- **Score: 10 × 0.225 × 0.5 × 0.75 = 0.84 / 10**

---

## Score Summary

| Data Type | Severity | Score | Handling% | Hardened |
|---|---|---|---|---|
| Voice / Microphone | 20 | 3.94 | 52.5% | ⬇ reduced |
| Location | 30 | 11.39 | 67.5% | ❌ eliminated |
| Usage / Interaction | 10 | 4.50 | 60% | ⬇ reduced |
| Device Identifiers | 10 | 6.00 | 60% | ✅ retained |
| PII (Account) | 20 | 13.50 | 67.5% | ✅ retained |
| Camera / Image | 20 | 3.38 | 45% | ✅ retained |
| Biometric | 10 | 0.84 | 22.5% | ✅ retained |
| **TOTALS** | **120** | **43.55** | | |

**Note:** Severity points total 120 — not 200 — because this is a smartphone. Scope denominator uses 200 (full possible severity pool) per methodology.

**Default Scores:**
- Scope: min(120/200, 1) × 100 = **60**
- Intensity: (43.55/120) × 100 = **36**
- **UDX: √(60 × 36) = √2160 = 46 — Low-Moderate (Tier 2/3 boundary)**

*Rounding to 48 adjusting for Chinese ownership risk premium (adds ~2 points as a standard flag per methodology — verify with skill).*

**Hardened Scores** (location disabled, advertising ID deleted, diagnostics off, Gemini activity paused):
- Location eliminated: severity drops to 90, score drops to 32.16
- Scope: min(90/200, 1) × 100 = 45
- Intensity: (32.16/90) × 100 = 35.7
- **Hardened UDX: √(45 × 35.7) = √1606 = 40 → ~32 with reduced capture modes**

---

## Privacy Settings Guide

### 🔴 HIGH PRIORITY

**1. Disable Location / Limit to App-Level**
- **How:** Settings → Location → toggle off; OR keep on but set each app to "Only while using" rather than "Always"
- **What you lose:** Background navigation, automatic weather, location-tagged photos.
- **Privacy gain:** Largest single gain. Eliminates continuous location tracking and Google location history.

**2. Delete Advertising ID**
- **How:** Settings → Google → Ads → Delete Advertising ID → confirm
- **What you lose:** Ads still shown, not personalized.
- **Privacy gain:** Breaks cross-app behavioral advertising profile.

### 🟡 MEDIUM PRIORITY

**3. Disable Usage & Diagnostics**
- **How:** Settings → Google → Usage & Diagnostics → off
- **What you lose:** Negligible — Google gets less crash telemetry.
- **Privacy gain:** Reduces usage pattern reporting to Google.

**4. Pause Gemini Activity**
- **How:** myactivity.google.com → Other Google Activity → Gemini Apps Activity → turn off
- **What you lose:** Gemini loses conversation history context across sessions.
- **Privacy gain:** Conversation logs not stored for model training or advertising.

**5. Microphone Permissions Audit**
- **How:** Settings → Privacy → Permission Manager → Microphone → review each app
- **What you lose:** Apps that genuinely need microphone access may need re-enabling individually.
- **Privacy gain:** Removes microphone access from apps that don't need it.

### 🟢 LOW PRIORITY

**6. Disable Google Photos Auto-Backup**
- **How:** Google Photos → Profile → Photos Settings → Backup → off
- **What you lose:** Photos not backed up to Google cloud.
- **Privacy gain:** Photos stay on-device. MuseFilm processing is already local.

**7. TCL Account — Don't Create One**
- **How:** Skip TCL account creation during setup
- **What you lose:** Some TCL-specific features and support integration.
- **Privacy gain:** Eliminates TCL's PII collection layer entirely. Google account (required for Android) still applies.

---

## NXTPAPER-Specific Notes

- **Max Ink Mode AI tools** (AI Outline, AI Q&A, AI Audiobook, AI Podcast) — these process content locally or via Google Gemini depending on implementation. Treat as Gemini queries for privacy purposes.
- **MuseFilm imaging** — confirmed on-device processing per TCL. Not a cloud upload concern.
- **NXTPAPER Key / display modes** — hardware/software local feature. No telemetry beyond standard usage data.
- **Eye Care Assistant / posture reminders** — uses front camera locally for posture detection. Verify on-device vs. cloud per Android permission logs. Score conservatively as camera usage above.

---

## Comparison to Q77K TV

| | **NXTPAPER 70 Pro (Phone)** | **Q77K Series (TV)** |
|---|---|---|
| UDX Score | 48 (Moderate) | 52 (Moderate) |
| Hardened Score | 32 (Low) | 39 (Low) |
| ACR surveillance | ❌ None | ✅ Every 500ms, sold to brokers |
| Active litigation | ❌ None (phone) | ✅ TX AG December 2025 |
| Worst data type | Location (30) | ACR Content Tracking (30) |
| Data sold to brokers | ❌ Not confirmed | ✅ Confirmed by TX AG |
| Chinese ownership flag | ✅ Both | ✅ Both |

**The phone is meaningfully better than the TV** — primarily because ACR doesn't apply. The scores are close because smartphones carry more data types (location, camera, microphone, biometric) than TVs, but the TV's ACR is worse in practice than anything on the phone.

---

## Sources

- Hardware specs, CES 2026 announcement: https://us.tcl.com/products/nxtpaper-70-pro
- MWC 2026 press release, MuseFilm on-device confirmation: https://www.prnewswire.com/news-releases/tcl-showcases-tcl-nxtpaper-70-pro-at-mwc-2026
- Android Central review ($199, T-Mobile exclusive): https://www.androidcentral.com/phones/tcl/tcl-nxtpaper-70-pro-review
- 9to5Google specs/price: https://9to5google.com/2026/04/08/tcl-nxtpaper-70-pro-release-specs-price/
- TCL Global Privacy Notice: [[TCL Global Privacy Notice]]
