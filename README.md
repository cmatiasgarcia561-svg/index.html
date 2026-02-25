<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>Millonarios FC | Ultimate Fan Website</title>
<meta name="description" content="Millonarios FC history, squad, trophies, and legacy website.">

<style>

/* ===== GLOBAL STYLE ===== */
body {
  margin: 0;
  font-family: Arial, sans-serif;
  background: #061a33;
  color: white;
}

header {
  background: #001f4d;
  padding: 15px 30px;
  display: flex;
  justify-content: space-between;
  align-items: center;
  position: fixed;
  width: 100%;
  top: 0;
  z-index: 1000;
}

header h1 {
  margin: 0;
  font-size: 24px;
}

nav a {
  color: #4da3ff;
  margin-left: 20px;
  text-decoration: none;
  font-weight: bold;
}

nav a:hover {
  text-decoration: underline;
}

/* ===== HERO ===== */
.hero {
  height: 100vh;
  background: linear-gradient(135deg, #003366, #000814);
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  text-align: center;
  padding-top: 60px;
}

.hero h2 {
  font-size: 50px;
}

.hero p {
  font-size: 20px;
}

button {
  padding: 12px 30px;
  border: none;
  background: #4da3ff;
  color: black;
  font-size: 18px;
  border-radius: 5px;
  cursor: pointer;
  margin-top: 20px;
}

button:hover {
  background: white;
}

/* ===== SECTIONS ===== */
section {
  padding: 80px 50px;
}

.cards {
  display: flex;
  gap: 20px;
}

.card {
  flex: 1;
  background: #001f4d;
  padding: 30px;
  border-radius: 15px;
  text-align: center;
  font-size: 20px;
  transition: 0.3s;
}

.card:hover {
  transform: scale(1.05);
  background: #003366;
}

/* ===== HISTORY ===== */
.history p {
  font-size: 18px;
  max-width: 800px;
}

/* ===== SQUAD ===== */
.squad-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 20px;
}

.player {
  background: #001f4d;
  padding: 20px;
  border-radius: 10px;
  text-align: center;
  transition: 0.3s;
}

.player:hover {
  background: #003366;
  transform: scale(1.03);
}

/* ===== TROPHIES ===== */
.trophies ul {
  font-size: 20px;
  line-height: 2;
}

/* ===== FOOTER ===== */
footer {
  background: #001f4d;
  text-align: center;
  padding: 20px;
  font-size: 14px;
}

</style>
</head>

<body>

<!-- ===== HEADER ===== -->
<header>
  <h1>Millonarios FC</h1>
  <nav>
    <a href="#home">Home</a>
    <a href="#history">History</a>
    <a href="#squad">Squad</a>
    <a href="#trophies">Trophies</a>
  </nav>
</header>

<!-- ===== HOME ===== -->
<div id="home" class="hero">
  <h2>El Embajador del Fútbol Colombiano</h2>
  <p>Bogotá • Founded 1946 • Estadio El Campín</p>
  <button onclick="playHimno()">Play Club Anthem</button>
</div>

<!-- ===== CARDS ===== -->
<section class="cards">
  <div class="card">🏆 16+ League Titles</div>
  <div class="card">⭐ Alfredo Di Stéfano Era</div>
  <div class="card">👥 Millions of Fans Worldwide</div>
</section>

<!-- ===== HISTORY ===== -->
<section id="history" class="history">
  <h2>History</h2>
  <p>
    Millonarios FC was founded in 1946 in Bogotá, Colombia. The club became famous in the 1950s during the El Dorado era, signing world stars like Alfredo Di Stéfano.
  </p>
  <p>
    Millonarios is one of Colombia’s biggest clubs, with intense rivalries and a massive fanbase.
  </p>
</section>

<!-- ===== SQUAD ===== -->
<section id="squad">
  <h2>Current Squad</h2>
  <div class="squad-grid">
    <div class="player">🧤 Álvaro Montero - Goalkeeper</div>
    <div class="player">🛡 Andrés Llinás - Defender</div>
    <div class="player">⚡ Daniel Ruiz - Midfielder</div>
    <div class="player">🔥 Leonardo Castro - Forward</div>
    <div class="player">🧠 David Silva - Midfielder</div>
    <div class="player">🚀 Juan Pereira - Midfielder</div>
  </div>
</section>

<!-- ===== TROPHIES ===== -->
<section id="trophies" class="trophies">
  <h2>Trophies</h2>
  <ul>
    <li>🏆 Colombian League Titles: 16+</li>
    <li>🏆 Copa Colombia Titles</li>
    <li>🏆 Superliga Colombiana</li>
    <li>🏆 Copa Simón Bolívar</li>
  </ul>
</section>

<!-- ===== FOOTER ===== -->
<footer>
  Fan-made website • Not official • Created by Matias
</footer>

<script>
function playHimno() {
  alert("🎶 Millonarios FC anthem would play here!");
}

// Smooth scroll
document.querySelectorAll('nav a').forEach(link => {
  link.addEventListener('click', function(e) {
    e.preventDefault();
    document.querySelector(this.getAttribute('href')).scrollIntoView({
      behavior: 'smooth'
    });
  });
});
</script>

</body>
</html>
