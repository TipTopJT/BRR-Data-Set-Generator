# Breathing Audio Dataset Collector

## Overview

**Breathing Audio Dataset Collector** is a browser-based application for **guided breathing training** and **generation of labeled breathing audio datasets**.

The application visually guides the user through breathing phases (inhale, hold, exhale, rest) while simultaneously **recording microphone audio** and automatically generating **time-aligned labels** for each breathing phase.

This tool is intended for:
- Research and experimentation
- Machine learning / AI dataset creation
- Signal processing and audio analysis
- Educational and non-medical purposes

---

## ⚠️ Disclaimer (Important)

This application is provided **“as is”**, without any warranties or guarantees.

- The authors **do not provide medical advice**
- The authors **do not take any responsibility** for any physical, mental, or health-related effects resulting from the use of this application
- Users are fully responsible for how they use this software
- Do **not** use this application as a substitute for professional medical guidance
- If you experience discomfort, dizziness, or any health issues, **stop using the app immediately**

By using this software, you agree that **the authors are not liable for any damages, injuries, or losses** resulting from its use.

---

## Features

- Customizable breathing cycle:
  - Inhale duration
  - Pause after inhale (optional)
  - Exhale duration
  - Pause after exhale (optional)
- Visual circular breathing guide
- Real-time breathing phase indicator
- Breathing rate calculation (breaths per minute)
- Microphone audio recording
- Automatic generation of:
  - WAV audio file
  - JSON label file with exact timestamps
- Works fully in the browser (no backend required)

---

## Output Files

After recording, the app automatically downloads:

1. **Audio file**
   - Format: `.wav`
   - Sample rate: `44,100 Hz`
   - Mono channel

2. **Label file**
   - Format: `.json`
   - Contains:
     - Recording metadata
     - Breathing configuration
     - Time-aligned labels for each breathing phase

### Example label structure

```json
{
  "phase": "inhale",
  "startTime": 0.0,
  "endTime": 4.0,
  "duration": 4.0
}
