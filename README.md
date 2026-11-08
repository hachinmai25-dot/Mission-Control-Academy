# 🚀 Mission Control Academy

> A game that trains junior astronauts using **real NASA data**. Complete missions, earn XP, and rise from Cadet to Commander.

Built for the **NASA Space Apps Challenge 2026**
Challenge: **Build a Junior Astronaut Mission Trainer**

🔗 **Live demo:** _add Vercel link here_
🎥 **Demo video:** _add link here_

---

## 🌍 The Problem

Space learning for kids is often boring: textbooks, slides, and facts to memorize. Young learners need to *do* things, not just read about them.

## 💡 Our Solution

Mission Control Academy turns real NASA data into playable missions. Instead of reading about the ISS, asteroids, or exoplanets, players **track, decide, and discover** using live data, and learn by playing.

## ✨ Features

- 🎮 **5 playable missions**, each built on real NASA data
- ⭐ **XP and ranks**: Cadet → Pilot → Commander
- 🏅 **Badges** for achievements
- 🏆 **Global leaderboard**
- 👤 **Player accounts** with saved progress
- 📶 **Offline-safe**: cached NASA data keeps the game running without internet
- 📱 Responsive design for laptop, tablet, and phone

## 🛰️ Missions

| # | Mission | What the player does | NASA data used |
|---|---------|----------------------|----------------|
| 1 | Track the ISS | Predict where the space station will be | ISS live location |
| 2 | Asteroid Watch | Decide which near-Earth asteroids are dangerous | NASA NeoWs |
| 3 | Planet Hunter | Choose which planet could support life | NASA Exoplanet Archive |
| 4 | Space Photo Quiz | Identify what's in real space photos | NASA APOD |
| 5 | Final Exam | Mixed challenge to earn the Commander rank | All of the above |

## 🧱 Tech Stack

| Layer | Technology |
|-------|-----------|
| Frontend | React, Vite, Tailwind CSS |
| Animation | Framer Motion |
| Routing | React Router |
| Backend / Auth / Database | Supabase |
| Hosting | Vercel |
| Data | NASA Open APIs |

## 📁 Project Structure

```
mission-control-academy/
├── public/                 # Static assets (images, sounds, icons)
├── src/
│   ├── pages/              # Home, MissionSelect, Profile, Leaderboard
│   ├── missions/           # One folder per mission
│   │   ├── iss/
│   │   ├── asteroids/
│   │   ├── planets/
│   │   ├── photo-quiz/
│   │   └── final-exam/
│   ├── components/         # Reusable UI (buttons, cards, XP bar)
│   ├── lib/                # supabase.js, nasaApi.js
│   ├── data/               # Cached NASA data (offline fallback)
│   ├── App.jsx
│   └── main.jsx
├── .env.example            # Template for environment variables
├── .gitignore
└── README.md
```

## ⚙️ Getting Started

### Prerequisites
- Node.js 18 or higher
- A GitHub account
- A free [NASA API key](https://api.nasa.gov/)
- A [Supabase](https://supabase.com/) project

### Installation

```bash
# 1. Clone the repository
git clone https://github.com/<your-username>/mission-control-academy.git
cd mission-control-academy

# 2. Install dependencies
npm install

# 3. Create your environment file
cp .env.example .env
# Then open .env and add your keys

# 4. Start the development server
npm run dev
```

The game runs at `http://localhost:5173`.

### Environment Variables

Create a `.env` file in the project root:

```
VITE_NASA_API_KEY=your_nasa_api_key
VITE_SUPABASE_URL=your_supabase_project_url
VITE_SUPABASE_ANON_KEY=your_supabase_anon_key
```

> ⚠️ Never commit your `.env` file. It is already listed in `.gitignore`.

## 🗄️ Database (Supabase)

Main tables:

| Table | Purpose |
|-------|---------|
| `profiles` | Player name, XP, rank |
| `mission_progress` | Which missions each player completed and their scores |
| `badges` | Badges earned by each player |

Row Level Security (RLS) is enabled so players can only edit their own data.

## 🤝 Contributing (Team Workflow)

1. **Never commit directly to `main`.**
2. Create a branch for your work:
   ```bash
   git checkout -b mission-iss
   ```
3. Commit small and often with clear messages:
   ```bash
   git commit -m "add ISS map component"
   ```
4. Push and open a **Pull Request**.
5. The team lead reviews and merges.

**Branch naming:** `mission-<name>`, `feature-<name>`, `fix-<name>`, `ui-<name>`


## 🗺️ Roadmap

- [x] Game design
- [ ] Core game loop, XP, and ranks
- [ ] Mission 1: Track the ISS
- [ ] Connect real NASA data
- [ ] Supabase login, progress, and leaderboard
- [ ] Remaining missions
- [ ] Sound, animation, and polish
- [ ] Testing and demo

## 🙏 Acknowledgments

- [NASA Open APIs](https://api.nasa.gov/) and the NASA Exoplanet Archive for the data
- NASA Space Apps Challenge organizers and our college host

## 📄 License

MIT License. See `LICENSE` for details.
