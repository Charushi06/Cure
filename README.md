# MediQueue

**Hospital Patient Flow & Overcrowding Management Platform**

MediQueue is a **single-file web app** that helps hospitals manage patient flow, reduce overcrowding, and provide real-time wait-time visibility.

---

## Overview

Hospitals often struggle with:

* Invisible queues
* Manual triage
* Unstructured intake

**MediQueue** combines intake, triage, appointments, and live hospital status into one simple interface for patients and staff.

---

## Features

### 🧾 Patient Intake

* Personal details, medical history, symptoms
* Insurance (optional)
* Returning patient fast-track

### 🧮 PriorityScore Triage

Generates a **0–100 score** mapped to **ESI levels (1–5)**.

```
PriorityScore =
  (Symptom × 0.30) +
  (Chronic × 0.10) +
  (Treatment × 0.05) +
  (Medication × 0.05) +
  (Age × 0.05) +
  (Emergency × 0.20) +
  (Wait × 0.15) +
  (Crowd × 0.10)
```

| Score  | ESI | Action    |
| ------ | --- | --------- |
| 80–100 | 1   | Immediate |
| 60–79  | 2   | <8 min    |
| 40–59  | 3   | ~18 min   |
| 20–39  | 4   | ~35 min   |
| 0–19   | 5   | Routine   |

---

### 📊 Hospital Status

* 7-day crowd view (🟢🟡🔴)
* Department-wise wait times & load

### 📅 Appointments

* Browse doctors
* Real-time slots
* One-tap booking + notifications (simulated)

### 🚨 Emergency

* One-click emergency call
* Live connection + ETA (simulated)

### 👨‍⚕️ Staff Directory

* Doctors & staff with availability

### 🌐 Accessibility

* 8 languages
* Large font mode
* SMS & push toggles

---

## Tech Stack

* HTML5 + CSS3
* Vanilla JavaScript
* Google Fonts
* Google Maps (deep link)

No frameworks, no dependencies (for initial prototype)

---

##  Getting Started
Deployed Link (Prototype): https://charushi06.github.io/Cure/

##  Customization

Edit values in the `<script>`:

* Hospital name & location
* Departments (`depts`)
* Doctors (`doctors`)
* Google Maps destination
* Triage weights

---

## 🔐 Compliance (Prototype)

Requires for production:

* Encryption (TLS + AES-256)
* Auth & access control
* Audit logs
* Patient consent & data policies

---

## 📄 License

Prototype only. Not for clinical deployment.

---

## 💡 Vision

A **smarter, faster, patient-first hospital flow system** that reduces wait times and improves care delivery.
