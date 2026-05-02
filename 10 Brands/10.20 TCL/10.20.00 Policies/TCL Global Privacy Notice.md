---
group: Policy
category: Corporate Privacy Policy
company: TCL Technology Group Corporation
url: https://www.tcl.com/global/en/privacy-notice
retrieved: 2026-05-02
last_updated: 2025-07-18
aliases:
  - TCL Privacy Policy
  - TCL Global Privacy Notice
tags:
  - policy
  - tcl
  - privacy
  - data-collection
  - ACR
  - chinese-ownership
  - active-lawsuit
---

# TCL Global Privacy Notice

**Source:** https://www.tcl.com/global/en/privacy-notice
**Effective:** 2025-07-18
**Controller:** Shenzhen TCL New Technology Co., Ltd., China

⚠️ **NATIONAL SECURITY FLAG:** TCL is Chinese-owned. Data collected may be subject to China's National Security Law compelling disclosure to Chinese government authorities without user notification.

⚠️ **ACTIVE LITIGATION:** Texas AG Ken Paxton filed suit December 15, 2025 (State of Texas v. TCL Technology Group Corporation) under Texas Deceptive Trade Practices Act for unlawful ACR collection and sale to data brokers.

---

## Data Controller

Shenzhen TCL New Technology Co., Ltd., 18/F, TCL Technology Building, No. 17, Huifeng Third Road, Zhongkai High-tech Zone, Huizhou, Guangdong, China. Data may be stored on servers in China as well as internationally.

---

## Data Collected

### Device and Usage Data
- IP address, MAC address, Device-ID, Terminal ID, serial number, IMEI, IMSI, and other device identifiers
- App usage, button clicks, page views, time spent, feature usage, navigation paths, videos played, duration
- Activation time, device configuration

**Policy language:** "the IP address, MAC address, Device-ID, Terminal ID, serial number, IMEI number, IMSI number and any other device identifiers or device-specific information about your TCL materials"

"data about your usage of system functions, applications and smart services, and device activation and registration details, such as activation time format, page and button clicks, page viewed and time spent on those pages, time and duration of service usage, name and duration of videos played, and user favorites"

### ACR / Content Consumption
Automated Content Recognition fingerprints all content displayed on screen approximately every 500ms — including cable, streaming apps, and all HDMI-connected devices (gaming consoles, Blu-ray, cable box).

**Policy language:** "details about your usage of the products that we supply to you such as the content viewed through the device and usage habits"

**TX AG complaint language:** "TCL secretly monitors what consumers watch across streaming apps, cable, and even connected devices like gaming consoles or Blu-ray players."

**Default status:** ON. Opt-out available via Settings → Privacy → User Agreements.

### Voice Data
Voice commands when remote microphone is pressed. Includes device description, voice recording, Skill Token, Voice command. Processed by Google or Amazon directly.

**Policy language:** "The Smart TV products capture data of the Amazon Alexa or Google Action voice assistant function on your Smart TV products. This information includes a device description, your voice, Skill Token and Voice command. When you use the voice assistant function, your voice data will be processed by Google or Amazon."

**Capture mode:** Remote-activated (press-to-talk) — NOT always-on.

### Personal Information (Account)
Name, email, shipping/billing address, phone number. Google account required for Google TV functionality. TCL account optional.

### Geolocation
IP-based city-level geolocation. Precise GPS opt-in only.

---

## Data Sharing

- **Advertising networks and data brokers** — confirmed by TX AG complaint. ACR data sold to demand-side platforms.
- **TCL Group companies** — usage and device data
- **Google / Amazon** — voice assistant data processed directly
- **Internet service providers** — per CCPA disclosure table
- **Law enforcement** — including potential compelled disclosure under China's National Security Law

**TCL states it does not sell personal data** under California/Nevada definitions — contradicted by TX AG complaint which alleges exactly this.

---

## Retention

Vague. "As long as needed for the purposes described." No specific retention periods stated for most data categories.

---

## User Rights

CCPA/CPRA rights for California residents. GDPR rights for EU residents. Exercise via privacy form on TCL website.

---

## Opt-Out Mechanisms

| Data Type | Opt-Out Available | How |
|---|---|---|
| ACR / content tracking | Yes | Settings → Privacy → User Agreements → opt out of User Experience Improvement Program |
| Advertising ID | Yes (delete/reset) | Settings → Privacy → Ads → Delete Advertising ID |
| Voice assistant | Yes | Settings → Device Preferences → Google Assistant → off |
| Google TV layer | Yes (nuclear) | Choose "Basic TV" at initial setup — requires factory reset to change |
| Location | Yes | Settings → Privacy → Location → Off |
| Diagnostic data | Yes | Settings → Privacy → User Agreements → opt out of diagnostic data |
| Device identifiers | No | Always active |
| IP geolocation | No | Always active |

---

## Legal Actions

- **Texas AG December 15, 2025:** State of Texas v. TCL Technology Group Corporation — unlawful ACR collection and sale to data brokers under DTPA. Active case.
- **Vizio precedent:** FTC $2.2M settlement 2017 for same ACR practices. TCL not yet subject to FTC action.

---

## UNDOXXING Scoring Notes

**Key tension points for product scoring:**

- ACR is the highest-severity data type (HIGH/30) — confirmed sold to brokers, default on, buried opt-out
- Chinese ownership adds national security dimension beyond standard scoring — flag on all TCL products
- Google TV layer adds a second privacy policy (Google's) that applies simultaneously — both must be considered
- Voice data lower severity due to remote-activated (not always-on) capture mode
- Device identifiers have no opt-out — always scored at 1.0x opt-out multiplier
- "Basic TV mode" at setup eliminates Google TV layer entirely — hardened config option for privacy-focused users
- Retention language is uniformly vague — score at maximum retention tier (7.5%)

**Applies to:** All TCL smart TV products running Google TV OS. Verify hardware-specific differences (microphone presence, camera presence) per model before scoring.
