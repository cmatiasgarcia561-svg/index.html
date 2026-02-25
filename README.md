<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>Millonarios FC | Ultra Fan Experience</title>
<meta name="description" content="Millonarios FC futuristic fan website with squad, history, trophies and live features.">

<style>

/* ===== ROOT THEMES ===== */
:root {
  --bg: #061a33;
  --card: rgba(0, 31, 77, 0.7);
  --text: white;
  --accent: #4da3ff;
}

.light {
  --bg: #f5f7fa;
  --card: white;
  --text: black;
  --accent: #0033ff;
}

/* ===== GLOBAL ===== */
body {
  margin: 0;
  font-family: "Segoe UI", Arial, sans-serif;
  background: var(--bg);
  color: var(--text);
  transition: 0.3s;
}

header {
  position: fixed;
  width: 100%;
  background: rgba(0,0,0,0.7);
  backdrop-filter: blur(10px);
  padding: 12px 40px;
  display: flex;
  justify-content: space-between;
  z-index: 1000;
}

header h1 { margin: 0; }

nav a {
  color: var(--accent);
  margin-left: 20px;
  text-decoration: none;
  font-weight: bold;
}

/* ===== HERO ===== */
.hero {
  height: 100vh;
  background: url("https://images.unsplash.com/photo-1508098682722-e99c43a406b2") center/cover;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  text-align: center;
  color: white;
}

.hero h2 {
  font-size: 60px;
  animation: glow 2s infinite alternate;
}

@keyframes glow {
  from { text-shadow: 0 0 10px #4da3ff; }
  to { text-shadow: 0 0 30px white; }
}

button {
  padding: 12px 25px;
  border: none;
  border-radius: 6px;
  background: var(--accent);
  color: black;
  font-size: 16px;
  cursor: pointer;
}

/* ===== SECTIONS ===== */
section {
  padding: 80px 50px;
}

/* ===== CARDS ===== */
.cards {
  display: flex;
  gap: 20px;
}

.card {
  flex: 1;
  background: var(--card);
  backdrop-filter: blur(10px);
  padding: 30px;
  border-radius: 15px;
  text-align: center;
  font-size: 20px;
  transition: 0.3s;
}

.card:hover {
  transform: scale(1.05);
}

/* ===== SQUAD ===== */
.squad-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 20px;
}

.player {
  background: var(--card);
  border-radius: 12px;
  padding: 15px;
  text-align: center;
  backdrop-filter: blur(10px);
  transition: 0.3s;
}

.player img {
  width: 100%;
  border-radius: 10px;
}

.player:hover {
  transform: scale(1.05);
}

/* ===== LIVE SCORE ===== */
.scoreboard {
  font-size: 28px;
  text-align: center;
  padding: 20px;
  background: black;
}

/* ===== FOOTER ===== */
footer {
  background: black;
  text-align: center;
  padding: 20px;
  font-size: 14px;
}

</style>
</head>

<body>

<header>
  <h1>Millonarios FC</h1>
  <nav>
    <a href="#home">Home</a>
    <a href="#history">History</a>
    <a href="#squad">Squad</a>
    <a href="#trophies">Trophies</a>
    <button onclick="toggleMode()">🌙</button>
  </nav>
</header>

<!-- HERO -->
<div id="home" class="hero">
  <h2>El Embajador del Fútbol Colombiano</h2>
  <p>Bogotá • Founded 1946 • Estadio El Campín</p>
  <button onclick="playHimno()">Play Anthem</button>
</div>

<!-- LIVE SCORE -->
<div class="scoreboard" id="score">Millonarios 0 - 0 Nacional</div>

<!-- CARDS -->
<section class="cards">
  <div class="card" id="titles">🏆 League Titles: 0</div>
  <div class="card">⭐ Legendary Di Stéfano Era</div>
  <div class="card">👥 10M+ Fans Worldwide</div>
</section>

<!-- HISTORY -->
<section id="history">
  <h2>History</h2>
  <p>Millonarios FC was founded in 1946 and dominated South America in the 1950s with stars like Alfredo Di Stéfano.</p>
  <p>It remains one of Colombia’s biggest football institutions.</p>
</section>

<!-- SQUAD -->
<section id="squad">
  <h2>Current Squad</h2>
  <div class="squad-grid">
    <div class="player"><img src="https://via.placeholder.com/300"><p>Álvaro Montero - GK</p></div>
    <div class="player"><img src="https://via.placeholder.com/300"><p>Andrés Llinás - DF</p></div>
    <div class="player"><img src="https://via.placeholder.com/300"><p>Daniel Ruiz - MF</p></div>
    <div class="player"><img src="https://via.placeholder.com/300"><p>Leonardo Castro - FW</p></div>
    <div class="player"><img src="https://via.placeholder.com/300"><p>David Silva - MF</p></div>
    <div class="player"><img src="https://via.placeholder.com/300"><p>Juan Pereira - MF</p></div>
  </div>
</section>

<!-- TROPHIES -->
<section id="trophies">
  <h2>Trophies</h2>
  <ul>
    <li>🏆 Colombian League</li>
    <li>🏆 Copa Colombia</li>
    <li>🏆 Superliga Colombiana</li>
    <li>🏆 Copa Simón Bolívar</li>
  </ul>
</section>

<footer>
  Fan-made futuristic site • Created by Matias
</footer>

<script>
// Anthem
function playHimno() {
  alert("🎶 Millonarios anthem playing...");
}

// Smooth Scroll
document.querySelectorAll("nav a").forEach(a => {
  a.addEventListener("click", e => {
    e.preventDefault();
    document.querySelector(a.getAttribute("href")).scrollIntoView({behavior:"smooth"});
  });
});

// Dark / Light Mode
function toggleMode() {
  document.body.classList.toggle("light");
}

// Trophy counter animation
let titles = 0;
let interval = setInterval(() => {
  titles++;
  document.getElementById("titles").innerText = "🏆 League Titles: " + titles;
  if (titles >= 16) clearInterval(interval);
}, 200);

// Fake live score
let home = 0, away = 0;
setInterval(() => {
  if (Math.random() > 0.7) home++;
  if (Math.random() > 0.85) away++;
  document.getElementById("score").innerText = `Millonarios ${home} - ${away} Nacional`;
}, 3000);

</script>

</body>
</html>
