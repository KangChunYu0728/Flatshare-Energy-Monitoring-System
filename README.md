# Flatshare-Energy-Monitoring-System

## Goal
Build a **personal room energy monitoring system** that measures real electricity usage of devices (starting with a 3D printer), visualizes it on an **embedded display**, and analyzes usage patterns and cost.  
The project is designed to be **scalable**, allowing future integration with laundry machines and a Telegram flatshare bot for notifications and expense tracking.

---

## Scope (v1)
- Measure power and energy consumption using smart plugs
- Display live and daily energy data on an embedded LCD
- Log data for basic analytics (patterns, peaks, cost)

No cameras, no privacy-sensitive data.

---

## Hardware

### Required (v1)
- Smart plugs with energy metering (EU Schuko)
- Arduino UNO (Elegoo Starter Kit)
- LCD1602 display
- Buttons / LEDs (optional, for UI)
- PC or laptop (data collection & analysis)

### Future (v2+)
- Additional smart plugs (e.g. laundry machine)
- ESP32 or similar (Wi-Fi embedded controller)

---

## Software

- Arduino (C/C++) – embedded display & UI
- Python – data collection, logging, analytics
- CSV files – local storage (v1)
- Telegram Bot API – notifications (future)
- Google Sheets API – expense logging (future)

---

## System Overview

```
[ Smart Plug ]
     ↓
 Power / Energy Data
     ↓
 Python Collector & Analytics
     ↓
 Arduino UNO + LCD Display
     ↓
 (Future) Events → Telegram Bot / Expense System
```

---

## Development Plan

### Week 1 – Measurement & Display (v1)
- Install and configure smart plugs
- Measure energy usage of 3D printer (idle, heating, printing)
- Build Arduino + LCD setup
- Display live power and daily energy consumption

### Week 2 – Data Logging & Analytics
- Log time-series power data (CSV)
- Compute daily energy usage and cost (€/kWh)
- Identify basic patterns (peaks, standby, print phases)

### Week 3 – Cost & Pattern Evaluation
- Analyze cost per print
- Compare different usage patterns
- Define simple states (idle / active / finished)

### Week 4 – Scalability Preparation
- Clean project structure
- Define event format (e.g. device_finished)
- Prepare interfaces for Telegram bot and expense integration

---

## Future Extensions
- Laundry machine monitoring
- Automatic Telegram notifications ("Laundry done", "Print finished")
- Energy-based cost sharing in flatshare

---

## Status
- [x] Project scope defined
- [x] Hardware acquired
- [ ] Smart plug data ingestion
- [ ] Embedded display implementation
- [ ] Analytics & cost modeling

