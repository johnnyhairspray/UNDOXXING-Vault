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
policyNote: "[[TCL Global Privacy Notice]]"
ftcActions: "Active — Texas AG Ken Paxton filed suit December 15, 2025 (State of Texas v. TCL Technology Group Corporation) for unlawful ACR data collection and sale to data brokers under Texas Deceptive Trade Practices Act."
severityTier: 3
severityPoints: 100
scopeScore: 50
intensityScore: 55
udxScore: 52
hardenedUdxScore: 39
hardenedConfig: "Disable ACR: Settings → Privacy → User Agreements → opt out of User Experience Improvement Program. Delete Advertising ID: Settings → Privacy → Ads → Delete Advertising ID. Disable Google Assistant: Settings → Device Preferences → Google Assistant → off. Eliminates ACR (HIGH/30) and voice (MEDIUM/20)."
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

**⚠️ ACTIVE LEGAL ACTION:** Texas AG filed suit December 15, 2025 for ACR surveillance and data brokering.
**⚠️ NATIONAL SECURITY FLAG:** Chinese-owned. Data subject to China's National Security Law.
**Policy:** See [[TCL Global Privacy Notice]]

---

## Summary

Google TV smart television tracking everything on screen every ~500ms via ACR — including all HDMI-connected devices. Data sold to brokers. Two overlapping collection layers: TCL's own and Google TV's. Disabling ACR and deleting the advertising ID drops score from Moderate (52) to Low (39).

---

## Hardware Profile

- **Display:** 65" QLED 4K, Google TV OS
- **Microphone:** Remote-activated only — NOT always-on
- **Camera:** None
- **ACR:** Built-in, default ON
- **Voice:** Google Assistant via remote
- **Data jurisdiction:** Shenzhen, China

---

## Score Breakdown

| Data Type | Severity | Score | Handling% | Hardened |
|---|---|---|---|---|
| ACR / Content Tracking | 30 | 18.56 | 82.5% | ❌ eliminated |
| Voice Commands | 20 | 5.25 | 52.5% | ❌ eliminated |
| Usage / Interaction | 10 | 4.50 | 60% | ✅ retained |
| Device Identifiers | 10 | 6.00 | 60% | ✅ retained |
| PII (Account) | 20 | 13.50 | 67.5% | ✅ retained |
| IP Geolocation | 10 | 6.75 | 67.5% | ✅ retained |
| **TOTALS** | **100** | **54.56** | | |

**Default:** Scope 50 / Intensity 55 / **UDX 52 — Moderate (Tier 3)**
**Hardened:** Scope 25 / Intensity 61.5 / **UDX 39 — Low (Tier 2)**

---

## Privacy Settings Guide

### 🔴 HIGH PRIORITY

**1. ACR / User Experience Improvement Program**
- **How:** Settings → Privacy → User Agreements → opt out of User Experience Improvement Program
- **What you lose:** Less relevant content recommendations.
- **Privacy gain:** Eliminates ACR data sale to brokers. Largest single gain — drops score ~13 points.

**2. Advertising ID**
- **How:** Settings → Privacy → Ads → Delete Advertising ID
- **What you lose:** Ads still shown, not personalized.
- **Privacy gain:** Breaks cross-app behavioral profile. Reset periodically.

### 🟡 MEDIUM PRIORITY

**3. Basic TV Mode (Nuclear Option)**
- **How:** Choose "Basic TV" at initial setup only. Factory reset required to change later.
- **What you lose:** All Google smart features, Play Store, Google Assistant.
- **Privacy gain:** Eliminates Google's entire data collection layer. Best for users with separate streaming device.

**4. Voice Assistant**
- **How:** Settings → Device Preferences → Google Assistant → off
- **What you lose:** Voice remote commands.
- **Privacy gain:** Removes microphone data. Lower priority — mic is remote-activated, not always-on.

**5. Location Services**
- **How:** Settings → Privacy → Location → Off
- **What you lose:** Weather apps, local content.
- **Privacy gain:** Removes GPS from app ecosystem. IP geolocation still occurs.

### 🟢 LOW PRIORITY

**6. Diagnostic Data**
- **How:** Settings → Privacy → User Agreements → opt out of diagnostic data
- **Privacy gain:** Minimal but worth doing.

---

## Sources

- Privacy Policy: https://www.tcl.com/global/en/privacy-notice (effective 2025-07-18)
- Texas AG Complaint: https://www.texasattorneygeneral.gov/sites/default/files/images/press/TCL%20TV%20Petition%20Filed.pdf
- Consumer Reports 2025: https://www.consumerreports.org/electronics/privacy/how-to-turn-off-smart-tv-snooping-features-a4840102036/
- Hardware specs: https://tcl.com/us/en/products/home-theater/q77k-class/65-q77k-series-4k-uhd-hdr-qled-smart-google-tv-65q77k
