from pathlib import Path
import zipfile, shutil

root = Path("/mnt/data/site_jesus_html_css_js_final")
if root.exists():
    shutil.rmtree(root)

(root / "css").mkdir(parents=True)
(root / "js").mkdir(parents=True)
(root / "images").mkdir(parents=True)

html = """<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <meta name="description" content="Site sobre Jesus Cristo, sua vida, seus ensinamentos e pequenos trechos da Bíblia.">
  <title>Jesus Cristo | Amor, Esperança e Vida</title>
  <link rel="icon" href="images/favicon.svg" type="image/svg+xml">
  <link rel="stylesheet" href="css/style.css">
</head>
<body>

<header class="hero" id="inicio">
  <nav class="navbar">
    <a href="#inicio" class="logo">✝ <span>JESUS</span></a>

    <button class="menu-btn" id="menuBtn" aria-label="Abrir menu" aria-expanded="false">
      ☰
    </button>

    <div class="nav-links" id="navLinks">
      <a href="#inicio">Início</a>
      <a href="#historia">História</a>
      <a href="#vida">Vida</a>
      <a href="#ensinamentos">Ensinamentos</a>
      <a href="#biblia">Bíblia</a>
    </div>

    <a href="#mensagem" class="love-btn">♡ Ele te ama</a>
  </nav>

  <div class="hero-content">
    <p class="small-title">✦ FILHO DE DEUS</p>
    <h1>Jesus Cristo</h1>
    <h2>Amor <span>·</span> Esperança <span>·</span> Vida</h2>

    <p class="hero-text">
      Conheça um pouco da vida de Jesus, seus ensinamentos e a mensagem
      de amor, fé, perdão e esperança.
    </p>

    <a href="#historia" class="main-button">Conheça sua história →</a>
  </div>

  <div class="hero-verse">
    “Eu sou o caminho, e a verdade, e a vida.”
    <small>João 14:6</small>
  </div>
</header>

<main>

<section class="section" id="historia">
  <div class="section-heading">
    <span>01</span>
    <div>
      <p class="gold-title">CONHEÇA</p>
      <h2>A história de Jesus</h2>
    </div>
  </div>

  <div class="history-grid">
    <div class="history-text">
      <p>
        Jesus de Nazaré é a figura central do cristianismo. Os Evangelhos
        do Novo Testamento contam sua vida, seus ensinamentos, seus encontros
        com pessoas, sua crucificação e, para a fé cristã, sua ressurreição.
      </p>

      <p>
        Segundo os Evangelhos, Jesus nasceu em Belém, cresceu em Nazaré e
        começou seu ministério público já adulto. Ele ensinava sobre o amor
        a Deus, o amor ao próximo, o perdão, a misericórdia e o Reino de Deus.
      </p>
    </div>

    <div class="quote-box">
      <div class="quote-mark">“</div>
      <p>Ame o seu próximo como a si mesmo.</p>
      <small>Mateus 22:39</small>
    </div>
  </div>
</section>

<section class="section" id="vida">
  <div class="section-heading centered">
    <span>02</span>
    <div>
      <p class="gold-title">SUA VIDA</p>
      <h2>Momentos importantes</h2>
    </div>
  </div>

  <div class="life-grid">
    <article class="life-card">
      <div class="icon">🌟</div>
      <h3>Nascimento</h3>
      <p>Os Evangelhos de Mateus e Lucas narram o nascimento de Jesus em Belém.</p>
    </article>

    <article class="life-card">
      <div class="icon">🏠</div>
      <h3>Infância</h3>
      <p>Jesus cresceu em Nazaré. Lucas relata um episódio dele no templo aos 12 anos.</p>
    </article>

    <article class="life-card">
      <div class="icon">🕊️</div>
      <h3>Ministério</h3>
      <p>Adulto, Jesus ensinou, anunciou o Reino de Deus e reuniu discípulos.</p>
    </article>

    <article class="life-card">
      <div class="icon">✝️</div>
      <h3>Crucificação</h3>
      <p>Jesus foi condenado e crucificado em Jerusalém, segundo os Evangelhos.</p>
    </article>

    <article class="life-card">
      <div class="icon">🌅</div>
      <h3>Ressurreição</h3>
      <p>Os Evangelhos afirmam que Jesus ressuscitou ao terceiro dia.</p>
    </article>
  </div>
</section>

<section class="teachings" id="ensinamentos">
  <div class="teaching-intro">
    <p class="gold-title">03 · ENSINAMENTOS</p>
    <h2>O que Jesus nos ensinou</h2>
    <p>Amor, perdão, compaixão, humildade e fé.</p>
  </div>

  <article class="teaching-card">
    <div>♡</div>
    <h3>Amor</h3>
    <p>Amar a Deus e ao próximo.</p>
    <small>João 13:34</small>
  </article>

  <article class="teaching-card">
    <div>♢</div>
    <h3>Perdão</h3>
    <p>Perdoar e buscar a reconciliação.</p>
    <small>Mateus 6:14</small>
  </article>

  <article class="teaching-card">
    <div>☼</div>
    <h3>Compaixão</h3>
    <p>Cuidar de quem sofre.</p>
    <small>Mateus 9:36</small>
  </article>

  <article class="teaching-card">
    <div>✧</div>
    <h3>Humildade</h3>
    <p>Servir e tratar todos com respeito.</p>
    <small>Mateus 11:29</small>
  </article>
</section>

<section class="section" id="biblia">
  <div class="section-heading">
    <span>04</span>
    <div>
      <p class="gold-title">PALAVRAS DE FÉ</p>
      <h2>Pequenos trechos da Bíblia</h2>
    </div>
  </div>

  <div class="verse-grid">
    <blockquote>
      “Eu sou o caminho, e a verdade, e a vida.”
      <small>João 14:6</small>
    </blockquote>

    <blockquote>
      “Amai-vos uns aos outros, assim como eu vos amei.”
      <small>João 15:12</small>
    </blockquote>

    <blockquote>
      “Bem-aventurados os misericordiosos, porque alcançarão misericórdia.”
      <small>Mateus 5:7</small>
    </blockquote>

    <blockquote>
      “Vinde a mim, todos os que estais cansados e sobrecarregados,
      e eu vos aliviarei.”
      <small>Mateus 11:28</small>
    </blockquote>
  </div>
</section>

<section class="message" id="mensagem">
  <div class="cross">✝</div>
  <p class="gold-title">UMA MENSAGEM DE ESPERANÇA</p>
  <h2>Que a paz esteja com você</h2>
  <p>
    Que a mensagem de Jesus inspire amor, fé, perdão e esperança
    em cada novo dia.
  </p>

  <div class="message-verse">
    “Porque para Deus nada é impossível.”
    <small>Lucas 1:37</small>
  </div>
</section>

</main>

<footer>
  <div class="footer-content">
    <div>
      <a href="#inicio" class="footer-logo">✝ JESUS</a>
      <p>Amor · Esperança · Vida</p>
    </div>

    <div class="footer-links">
      <a href="#inicio">Início</a>
      <a href="#historia">História</a>
      <a href="#vida">Vida</a>
      <a href="#biblia">Bíblia</a>
    </div>

    <div class="copyright">
      © <span id="year"></span> Jesus Cristo
    </div>
  </div>
</footer>

<script src="js/script.js"></script>
</body>
</html>
"""

css = """@import url('https://fonts.googleapis.com/css2?family=Cormorant+Garamond:wght@500;600;700&family=Inter:wght@400;500;600;700&display=swap');

:root {
  --blue-dark: #08263f;
  --blue: #174d70;
  --gold: #e3b45f;
  --cream: #f8f6f0;
  --white: #ffffff;
  --text: #172d40;
  --muted: #687786;
  --line: #e0e4e5;
}

* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

html {
  scroll-behavior: smooth;
}

body {
  font-family: Inter, Arial, sans-serif;
  background: var(--cream);
  color: var(--text);
  line-height: 1.7;
}

h1, h2, h3 {
  font-family: "Cormorant Garamond", Georgia, serif;
}

.hero {
  min-height: 720px;
  position: relative;
  overflow: hidden;
  color: white;
  background:
    radial-gradient(circle at 75% 30%, rgba(255,255,255,.22), transparent 25%),
    linear-gradient(90deg, #061e35 0%, #092f4d 45%, #1d5879 100%);
}

.hero::before {
  content: "✝";
  position: absolute;
  right: 10%;
  bottom: 4%;
  font: 300 390px Georgia, serif;
  color: rgba(255,255,255,.055);
}

.navbar {
  height: 70px;
  max-width: 1250px;
  margin: auto;
  padding: 0 25px;
  display: flex;
  align-items: center;
  border-bottom: 1px solid rgba(255,255,255,.2);
  position: relative;
  z-index: 5;
}

.logo,
.footer-logo {
  color: white;
  text-decoration: none;
  font: 700 25px "Cormorant Garamond", serif;
  letter-spacing: .06em;
}

.logo:first-letter {
  font-size: 35px;
}

.nav-links {
  display: flex;
  gap: 27px;
  margin: auto;
}

.nav-links a,
.love-btn {
  color: white;
  text-decoration: none;
  font-size: 12px;
  font-weight: 600;
}

.nav-links a:hover {
  color: var(--gold);
}

.love-btn {
  border: 1px solid white;
  border-radius: 25px;
  padding: 8px 17px;
}

.menu-btn {
  display: none;
  background: none;
  border: 0;
  color: white;
  font-size: 28px;
  cursor: pointer;
}

.hero-content {
  position: relative;
  z-index: 2;
  max-width: 1250px;
  margin: auto;
  padding: 120px 25px;
}

.small-title,
.gold-title {
  color: var(--gold);
  letter-spacing: .22em;
  font-size: 11px;
  font
