# 📻 HamThing

**A modern ham radio dashboard for the Spotify Car Thing**

Transform your discontinued Spotify Car Thing into a beautiful, glanceable ham radio command center. Built for [DeskThing](https://deskthing.app).

![Version](https://img.shields.io/badge/version-2.1.0-blue)
![DeskThing](https://img.shields.io/badge/DeskThing-v0.11+-green)
![Author](https://img.shields.io/badge/author-DudeTested-orange)

---

## ✨ Features

### 🌤️ Weather-Style Dashboard
HamThing ditches the "1990s ham radio software" look for a clean, modern interface inspired by Apple Weather. At-a-glance information with beautiful blue gradients and frosted glass cards.

### 📊 5 Swipeable Panels

| Panel | What You See |
|-------|--------------|
| **Overview** | Giant K-index, SFI/SSN/A-index, UTC/Local time, band conditions |
| **Solar** | Detailed solar flux, sunspots, X-ray, proton flux, geomagnetic data |
| **Propagation** | Full HF band conditions table (80m-10m), day/night, MUF/foF2 |
| **POTA** | Live Parks on the Air spots with callsign, frequency, park reference |
| **SOTA** | Live Summits on the Air spots with summit codes and comments |

### 📡 Live Data Sources

| Data | Source | Refresh |
|------|--------|---------|
| Solar & Propagation | [hamqsl.com](https://www.hamqsl.com) (N0NBH) | 5 min |
| POTA Spots | [pota.app](https://pota.app) API | 30 sec |
| SOTA Spots | [sota.org.uk](https://www.sota.org.uk) API | 1 min |

---

## 🖼️ Screenshots

### Overview Panel
```
┌─────────────────────────────────────────────────┐
│                                                 │
│                      K2                         │
│                    Quiet                        │
│           SFI 156 • SSN 87 • A 10              │
│                                                 │
├─────────────────────────────────────────────────┤
│     14:32:45          │         09:32:45       │
│        UTC            │          Local          │
├─────────────────────────────────────────────────┤
│  80m    40m    20m    15m    10m               │
│  Good   Good   Fair   Fair   Poor              │
└─────────────────────────────────────────────────┘
```

---

## 🚀 Installation

### Prerequisites
- Spotify Car Thing (rooted)
- [DeskThing](https://deskthing.app) Server v0.11.0+ running on your PC
- DeskThing Client installed on your Car Thing

### Install the App

1. Download `hamthing-v2.1.0.zip` from releases
2. Open DeskThing Server on your computer
3. Go to **Apps** → **Add App**
4. Select the downloaded `.zip` file
5. Enable HamThing and set it as your active app

---

## 🎮 Controls

| Input | Action |
|-------|--------|
| **Swipe Left/Right** | Change panels |
| **Button 1** | Previous panel |
| **Button 4** | Next panel |
| **Rotate Dial** | Scroll through POTA/SOTA spots |
| **Touch Screen** | Swipe to navigate |

---

## ⚙️ Configuration

In DeskThing Settings for HamThing:

| Setting | Default | Description |
|---------|---------|-------------|
| Callsign | (empty) | Your amateur radio callsign |
| Grid Square | (empty) | Your Maidenhead grid locator |
| Solar Refresh | 300000 | Solar data refresh rate (ms) |
| Spots Refresh | 30000 | POTA/SOTA refresh rate (ms) |

---

## 🛠️ Building from Source

```bash
# Clone/download the source
cd hamthing

# Install dependencies
npm install

# Development mode
npm run dev

# Build for production
npm run build
```

The built app will be at `dist/hamthing-v*.zip`

### Project Structure

```
hamthing/
├── deskthing/
│   └── manifest.json         # App metadata
├── public/
│   └── icons/
│       └── hamthing.svg      # App icon
├── server/
│   ├── index.ts              # Server: API fetching, data processing
│   └── package.json
├── src/
│   ├── App.tsx               # Client: React UI, all 5 panels
│   ├── main.tsx              # React entry point
│   └── index.css             # Tailwind styles
├── index.html
├── package.json
├── vite.config.ts
├── tailwind.config.js
└── tsconfig.json
```

---

## 📋 Version History

### v2.1.0 (Current)
- 🎨 New Weather-style UI with blue gradient
- 📱 Giant hero K-index display
- 🧊 Frosted glass card design
- ✨ Clean, modern typography

### v2.0.0
- 🎨 Glassmorphism redesign
- 📱 Larger fonts for readability
- 🛠️ Updated to DeskThing SDK patterns v2.2
- 👤 Author: DudeTested

### v1.0.0
- 🚀 Initial release
- 📊 5-panel dashboard
- 📡 Solar, propagation, POTA, SOTA data

---

## 🔧 Troubleshooting

### App won't load
- Check DeskThing Server logs for errors
- Ensure you're running DeskThing Server v0.11.0+
- Try restarting the DeskThing server

### No data showing
- Check your internet connection
- Solar data may take up to 5 minutes to load initially
- POTA/SOTA APIs occasionally have downtime

### Buttons not working
- Go to DeskThing Settings → Mappings
- Ensure buttons are mapped to your app's actions
- Try resetting mappings to default

---

## 🤝 Contributing

Pull requests welcome! Please open an issue first to discuss proposed changes.

### Ideas for Future Features
- [ ] DX Cluster integration
- [ ] Satellite pass predictions
- [ ] Contest countdown timers
- [ ] Custom color themes
- [ ] Favorite parks/summits alerts
- [ ] QRZ lookup integration

---

## 📜 Credits

- **UI Design & Development**: Built with ❤️ by Claude, commissioned by DudeTested
- **Solar Data**: [N0NBH](https://www.hamqsl.com) — Paul Herrman
- **POTA API**: [Parks on the Air](https://pota.app)
- **SOTA API**: [Summits on the Air](https://www.sota.org.uk)
- **Platform**: [DeskThing](https://deskthing.app) by ItsRiprod
- **Inspiration**: [HamClock](http://www.clearskyinstitute.com/ham/HamClock/) by Elwood Downey (WB0OEW)

---

## 📄 License

MIT License — See [LICENSE](LICENSE) file for details.

---

## 🔗 Links

- **DeskThing**: https://deskthing.app
- **DeskThing Discord**: https://deskthing.app/discord
- **DudeTested YouTube**: https://youtube.com/@DudeTested
- **POTA**: https://pota.app
- **SOTA**: https://www.sota.org.uk

---

**73 de DudeTested!** 📻✨
