# Padosi: Your Neighbours Are the Network

Offline neighbourhood safety net for floods, cyclones and tower outages.
Track 08 · Community App · iQOO Hackathon Grand Finale

## The problem
When towers fail (about 30% of Chennai's 42,747 towers were still offline on 5 Dec 2023, a day after Cyclone Michaung's peak), people can't call for help, and the few messages that get out are chaotic: mixed languages, duplicates, no urgency.

## The idea
Speak → Triage → Relay → Respond, all offline.

1. **Speak** in Tamil, Hindi, English or a mix. Speech-to-text runs on the phone.
2. **Triage**: a small local model turns it into a card (need, urgency, headcount, GPS).
3. **Relay**: nearby phones pass the alert hop by hop over Bluetooth and Wi-Fi Direct.
4. **Respond**: responders see a sorted queue and tap "On my way".

No internet. No cloud. No data leaves the device.

## What is in this repo
| File | Description |
|---|---|
| `index.html` | Interactive prototype of the core loop (open in a browser, no install) |
| `Padosi_Finale_Deck.pptx` | Finale pitch deck |

## Prototype status (honest scope)
The prototype demonstrates the **user flow**. Triage uses a lightweight keyword model, the relay is simulated, and the location is a fixed demo point.

## Planned build
- Whisper (whisper.cpp) for Tamil/Hindi/English speech
- Gemma / Llama 3.2 (small, quantised) for structured JSON triage
- Android Nearby Connections (Bluetooth + Wi-Fi Direct) for relay
- Kotlin + Jetpack Compose, Room (SQLite), Fused Location
- Responder laptop view via Office Kit

## Run it
Open `index.html` in Chrome. Voice input works in Chrome; other browsers can use the sample chips.

## Live demo
`https://kailashnatarajan.github.io/padosi/`

## Team: Semicolon Survivors
- **Kailash N**, Team Leader & Lead Developer
- **Jayakrishna M**, On-device AI & Backend
- **Pavithrraraj R**, UI/UX & Demo
