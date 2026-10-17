# 💡 LumenGrid – Smart Streetlight Control

A dashboard to control **12 simulated streetlights** across 3 zones and watch power, energy and cost update live. A day/night street scene shows the city changing with a simulated clock.

**Live demo:** https://YOUR-USERNAME.github.io/YOUR-REPO-NAME/

> Built for the Live Development Webathon (Innovation Day, PRPCET IIC Cell) · Problem: *Smart Streetlight Dashboard*

---

## ✨ Features

**Control**
- 12 streetlights in 3 zones: **Main Road, Market Street, Campus Lane**
- Every light has a glowing bulb, an on/off toggle, a 0–100% brightness slider and a status badge (On / Off / Dimmed / Fault)
- Bulk controls: **All On, All Off, Eco Mode** (dims all to 50%) and per-zone **Zone On / Zone Off**

**Live numbers**
- Summary: total lights, lights on, faults, live power (W), energy used today (kWh) and cost (₹)
- Live power dial with a smooth needle
- Line chart of power over time and bar chart of energy per zone (Chart.js)

**Wow features**
- 🌆 **Live street scene** – a skyline whose sky changes colour with the clock (dawn, day, dusk, night with stars and moon). The 12 lamp posts glow to match the real light states, and you can **click a lamp** to switch it.
- ⏱️ **Simulated clock** – 1 real second = 1 simulated minute
- 🤖 **Auto Mode** – lights switch ON at 18:00 and OFF at 06:00 automatically
- 🌿 **Energy saved vs always-on** counter that grows over time
- ⏩ **+3 h** and **To dawn / To dusk** buttons to fast-forward time for demos

---

## 🧮 Energy math

| Item | Value |
|---|---|
| One LED at full brightness | 100 W |
| Power of a light | 100 W × brightness % |
| Energy | added every simulated minute (power ÷ 1000 ÷ 60 kWh) |
| Cost | ₹8 per kWh |
| Saved vs always-on | (12 × 100 W at full brightness, always) − actual use |

---

## 🛠️ Tech

Plain **HTML + CSS + JavaScript** in a single `index.html`. No React, no build step, no server.

- [Chart.js](https://www.chartjs.org/) (CDN) for the charts
- Google Fonts (Poppins) via CDN
- Neumorphic ("soft UI") design, fully responsive for phones

---

## ▶️ How to run

Just open `index.html` in Chrome. An internet connection is needed for the charts and fonts.

---

## 🎬 Quick demo guide

1. Open the page. It starts at **17:55**, and Auto Mode switches the lights on at 18:00.
2. Click **+3 h** to watch the night scene and the energy counters grow.
3. Click a lamp in the street, or use a card's slider, to dim or switch a single light.
4. Try **Eco Mode** and watch the power dial and the "energy saved" card react.
5. Click **To dawn** and watch Auto Mode switch everything off at 06:00.

---

Built by **Vedant**
