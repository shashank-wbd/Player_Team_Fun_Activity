# 🤥 Two Truths & A Lie — Zoom Team Edition 🎮

A highly interactive, visually stunning, and responsive single-page web game designed to be played with team members over Zoom (or any video-conferencing platform). Perfect for icebreakers, team-building sessions, and virtual fun activities!

---

## ✨ Features

- **🎮 Host-Controlled Game Flow:** Built specifically for a host to screen-share on Zoom while driving the game interactively with the team.
- **⏱️ Integrated Phase Timers:** 
  - `30s` Reading Timer 📖 (Pause & Skip available).
  - `30s` Discussion Timer 💬 (To deliberate on who wrote the facts).
  - `30s` Lie Discussion Timer 🤥 (To sniff out the fib).
- **🗳️ Interactive Name Grid:** Instead of typing names, choose from an organized grid of **20 team members** to select the team's top **2 guesses**.
- **🎤 Interactive Story Mode:** A dedicated storytelling screen where the player can speak and reveal their actual lie with immediate feedback (and celebratory confetti if the team guessed right!).
- **✨ Visual & Audio Polish:** Immersive purple-to-pink linear gradient backgrounds, subtle hover effects, card-flipping/reveal layouts, pulsing timers, and custom CSS-based particle confetti!
- **📦 Fully Self-Contained:** Written entirely in a single `index.html` file—no complex installations, Node modules, or backend servers required. Simply open and play!

---

## 🚀 How to Play

### 1. 📢 Host Screen-Shares on Zoom
Open the `index.html` file in any modern web browser, share your window/screen, and click **Start Game ▶**.

### 2. 📖 Step 1: Reading Phase
- 30-second timer starts.
- The team reads the 3 mysterious facts listed on the screen.
- *Host can Pause or Skip early if the team is ready!*

### 3. 💬 Step 2: Guess Who!
- 30-second discussion timer starts.
- The team deliberates and suggests names.
- The host clicks the team's **top 2 candidates** from the name button grid.
- Click **Reveal the Name 🎭** to see if the team got it right (confetti bursts if correct!).

### 4. 🤥 Step 3: Spot the Lie
- 30-second timer starts.
- The team deliberates which of the 3 facts is the lie.
- The host clicks the chosen card (turning it red with a `Team says LIE 🤥` tag) and hits **Lock it in & hear the story 🔒**.

### 5. 🎤 Step 4: Story Time & Reveal
- The spotlight turns to the player! They explain the stories behind their facts.
- The host clicks on the **actual lie** card as revealed by the player.
- Instant feedback is shown:
  - 🎉 **"The team spotted the lie!"** with celebratory confetti if the team's choice matches.
  - 😈 **"[Name] fooled everyone!"** if the player successfully tricked the team.
- Click **Next Person ➜** to proceed.

---

## 🛠️ Tech Stack

- **HTML5** & **CSS3** (Fluid layout, CSS custom variables, beautiful flex/grid systems, and keyframe animations).
- **Vanilla JavaScript** (State-machine style game loop, interactive timers, input validation, and shuffling algorithms).
- **HTML5 Canvas** API (High-performance rendering for the particle confetti system).
- **Google Fonts** (`Poppins` for sleek, modern typography).

---

## ⚙️ How to Customize (Add Your Team)

To edit, add, or remove team members and their facts:

1. Open `index.html` in any text editor.
2. Scroll to the `<script>` section at the bottom.
3. Update the `PEOPLE` array with your team's names and facts:

```javascript
const PEOPLE = [
  { 
    name: "Raushan", 
    facts: [
      "My commute used to take two hours each way.",
      "I once sent a company-wide email that was meant for one person.",
      "I once fell asleep in a meeting, and nobody noticed."
    ]
  },
  // Add more team members here...
];
```

4. Update the `TEAM` array with the names that should appear as buttons in the guess grid:

```javascript
const TEAM = [
  "Bikash", "Manisha", "Poonam", "Prashant", "Sathish", "Shiva", "Digendra",
  "Amulya", "Anusha", "Keerthi", "Pushpavathi", "Sahithi", "Sree", "Subramani",
];
```

---

## 📦 How to Run Locally

Since the game is completely self-contained, running it is incredibly simple:

- **Option A (Easiest):** Simply double-click the `index.html` file on your computer to open it directly in your browser.
- **Option B (Simple Server):** Run a quick local server using Python or Node:
  ```bash
  # Python 3
  python3 -m http.server 8000
  
  # Node.js (via npx)
  npx serve
  ```
  Then open `http://localhost:8000` (or the port specified) in your browser.

---

## 🌐 Deploy to GitHub Pages

Since this repository is already public, you can make this playable on the web instantly using **GitHub Pages**:

1. Go to your repository settings on GitHub: [Player_Team_Fun_Activity Settings](https://github.com/shashank-wbd/Player_Team_Fun_Activity/settings).
2. On the left sidebar, click **Pages**.
3. Under **Build and deployment**, set the source to **Deploy from a branch**.
4. Select the **`main`** branch and the **`/ (root)`** folder, then click **Save**.
5. Within a minute, your game will be live at:  
   `https://shashank-wbd.github.io/Player_Team_Fun_Activity/`

---

*Made with ❤️ for team fun and bonding.*
