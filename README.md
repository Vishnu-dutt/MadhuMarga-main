<div align="center">

<!-- Honey comb banner using emoji art -->
<img src="https://readme-typing-svg.demolab.com?font=Georgia&size=13&duration=3000&pause=1000&color=F5A623&center=true&vCenter=true&width=435&lines=🍯+The+Digital+Beekeeper's+Diary+🍯" alt="Typing SVG" />

# 🐝 Madhu-Marga
### *ಜೇನು ಮಾರ್ಗ— The Path of Honey*

**An AI-Powered Hive Management Android Application**

[![Android](https://img.shields.io/badge/Platform-Android-3DDC84?style=for-the-badge&logo=android&logoColor=white)](https://developer.android.com)
[![Kotlin](https://img.shields.io/badge/Language-Kotlin-7F52FF?style=for-the-badge&logo=kotlin&logoColor=white)](https://kotlinlang.org)
[![Gemini AI](https://img.shields.io/badge/AI-Gemini_API-4285F4?style=for-the-badge&logo=google&logoColor=white)](https://ai.google.dev)
[![Jetpack Compose](https://img.shields.io/badge/UI-Jetpack_Compose-FF6F00?style=for-the-badge&logo=jetpackcompose&logoColor=white)](https://developer.android.com/jetpack/compose)
[![Room DB](https://img.shields.io/badge/DB-Room-F5A623?style=for-the-badge&logo=sqlite&logoColor=white)](https://developer.android.com/training/data-storage/room)
[![License](https://img.shields.io/badge/Purpose-Academic-8B4513?style=for-the-badge)](.)

<br/>

> *"Every thriving hive begins with a single observation."*

<br/>

</div>

---

## 🌼 The Problem We're Solving

Honeybees are the **unsung heroes of agriculture** — responsible for pollination that sustains crop yields across India. Yet, thousands of beginner beekeepers lose entire colonies every year — not due to lack of care, but lack of **knowledge at the right moment**.

```
😟 Without Madhu-Marga           🐝 With Madhu-Marga
────────────────────────         ──────────────────────────
❌ Missed hive inspections       ✅ Guided weekly checklists
❌ Undetected pest infestations  ✅ Auto Intervention Alerts
❌ Lost honey harvest windows    ✅ Visual Honey Flow Tracker
❌ No expert advice available    ✅ AI Health Reports in 5s
❌ Colony collapse & income loss ✅ 40% reduction in colony loss
```

---

## ✨ Features

<table>
<tr>
<td width="50%">

### 🏠 Hive Registry
Register and tag each hive with a unique **Hive ID** (format: `MM-2026-HIVE-001`). Maintain a complete digital profile for your entire apiary in one place.

</td>
<td width="50%">

### 📋 Digital Inspection Log
A clean, tap-friendly **weekly checklist** covering:
- 👑 Queen spotted?
- 📊 Activity level
- 🪲 Pest presence

</td>
</tr>
<tr>
<td width="50%">

### 🚨 Intervention Alerts
Automatic, logic-based alerts triggered by negative observations:
- `⚠️ HIGH RISK: Swarming Detected`
- `🔴 LOW ACTIVITY: Inspect Immediately`

</td>
<td width="50%">

### 🍯 Harvest Tracker
A **visual progress bar** representing the Honey Flow season, logging yield per hive to help you time your harvest perfectly.

</td>
</tr>
<tr>
<td width="50%">

### 📡 Full Offline Support
Powered by **Room DB**, all your hive data is stored locally — because your farm doesn't always have WiFi, but your bees never take a day off.

</td>
<td width="50%">

### 🤖 GenAI Flora Insights
**Gemini API** generates:
- Hive Health Summaries in plain language
- Seasonal blooming pattern tips
- Suggested actions tailored to your logs

</td>
</tr>
</table>

---

## 🏗️ Tech Stack

```
╔══════════════════════════════════════════════════════════╗
║                    MADHU-MARGA STACK                     ║
╠══════════════╦═══════════════════════════════════════════╣
║  Language    ║  Kotlin                                   ║
║  UI Toolkit  ║  Jetpack Compose (Material 3)             ║
║  Architecture║  MVVM (Clean Architecture)                ║
║  Local DB    ║  Room DB                                  ║
║  GenAI       ║  Gemini API                               ║
║  Async       ║  Kotlin Coroutines                        ║
║  Theme       ║  Honey-Yellow Material 3 Design System    ║
╚══════════════╩═══════════════════════════════════════════╝
```

### Architecture Overview

```
┌─────────────────────────────────────────────────┐
│                   UI LAYER                      │
│         Jetpack Compose Screens                 │
│   HiveList · InspectionLog · HarvestTracker     │
└────────────────────┬────────────────────────────┘
                     │ observes
┌────────────────────▼────────────────────────────┐
│               VIEWMODEL LAYER                   │
│      HiveViewModel · InspectionViewModel        │
│         Holds UI State · Triggers Alerts        │
└──────────┬──────────────────────┬───────────────┘
           │ reads/writes         │ calls
┌──────────▼──────────┐  ┌───────▼───────────────┐
│    ROOM DATABASE    │  │     GEMINI API        │
│  HiveDao · LogDao   │  │  Flora Insights       │
│  Offline-first 💾   │  │  Health Summaries 🤖  │
└─────────────────────┘  └───────────────────────┘
```

---

## 🗂️ Log Format

Every inspection log follows a standardized ID format:

```
MM  -  2026  -  HIVE  -  001
│       │         │        │
│       │         │        └── Unique Hive Number
│       │         └─────────── Hive Identifier
│       └───────────────────── Year
└───────────────────────────── Madhu-Marga Prefix
```

---

## 🎯 Success Criteria

| # | Milestone | Status |
|---|-----------|--------|
| ✅ | Hive registered and saved to Room DB | Target |
| ✅ | Intervention Alert triggers on "Low Activity" log | Target |
| ✅ | Honey Flow Progress Bar reflects harvested volume | Target |
| ✅ | GenAI Health Report generated in **< 5 seconds** | Target |
| ✅ | UI adheres to Honey/Yellow color palette | Target |

---

## 🌍 Impact Goals

```
🍯 SWEET REVOLUTION
   Standardize hive data → Higher quality honey production

🌸 BIODIVERSITY
   Healthy bee populations → Better local crop pollination

💰 SUSTAINABLE INCOME
   Early alerts → 40% reduction in colony loss
```

---

## 📁 Project Structure

```
madhu-marga/
├── 📂 app/
│   ├── 📂 data/
│   │   ├── local/          # Room DB — Entities, DAOs
│   │   └── repository/     # HiveRepository, LogRepository
│   ├── 📂 domain/
│   │   └── model/          # Hive, InspectionLog, HarvestEntry
│   ├── 📂 presentation/
│   │   ├── screens/        # Compose UI Screens
│   │   └── viewmodel/      # HiveViewModel, AlertViewModel
│   └── 📂 ai/
│       └── GeminiService.kt # Gemini API integration
├── 📄 README.md
└── 📄 build.gradle.kts
```

---

## 🚀 Getting Started

### Prerequisites
- Android Studio Hedgehog or newer
- Android SDK 26+
- A valid **Gemini API Key** from [Google AI Studio](https://aistudio.google.com)

### Setup

```bash
# 1. Clone the repository
git clone https://github.com/[<your-username>](https://github.com/Vishnu-dutt/MadhuMarga-main)/madhu-marga.git

# 2. Open in Android Studio
# File → Open → Select the cloned folder

# 3. Add your Gemini API key in local.properties
echo "GEMINI_API_KEY=your_api_key_here" >> local.properties

# 4. Build & Run on an emulator or physical device
```

---

## 📋 Functional Requirements

| ID | Requirement | Priority |
|----|-------------|----------|
| FR-01 | Register and tag individual hives with unique IDs | 🔴 Critical |
| FR-02 | Digital checklist for weekly hive inspections | 🔴 Critical |
| FR-03 | Trigger Intervention Alerts on negative log entries | 🔴 Critical |
| FR-04 | Visual Progress Bar for honey flow season | 🟠 High |
| FR-05 | Store all hive logs locally via Room DB | 🟠 High |
| FR-06 | GenAI generates Hive Health Summary & actions | 🟡 Medium |

---

## 👨‍💻 Developer

<table>
<tr>
<td align="center">
<b>Vishnu Dutt</b><br/>
<sub>1SJ22CS182</sub><br/>
<sub>Computer Science and Engineering</sub><br/>
<sub>SJC Institute of Technology, Chickaballapur</sub>
</td>
</tr>
</table>

---

## 🏫 Academic Context

> This project is developed as part of the **MindMatrix Industry Readiness Programme**
> under the track: *Android App Development using GenAI — Agriculture / Smart Farming*
>
> **Project #64 · Project Title #48: Madhu-Marga (Digital Beekeeper's Diary)**

---

<div align="center">

**🐝 Built with love for India's beekeepers 🐝**

*"Protect the bees. Protect the harvest. Protect the future."*

</div>
