
[index.html](https://github.com/user-attachments/files/33420757/index.html)
<!DOCTYPE html>
<html lang="ja">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <meta name="description" content="りおん｜下書きなしの一発描き。モンスターとひよこの世界を描くイラストレーター。">
  <title>りおん｜一発描きアートの世界</title>
  <style>
    @import url('https://fonts.googleapis.com/css2?family=Kosugi+Maru&family=M+PLUS+Rounded+1c:wght@400;500;700;800&display=swap');

    :root {
      --ink: #22213b;
      --pink: #ff6fae;
      --yellow: #ffe66d;
      --blue: #73d7f5;
      --green: #a8edb5;
      --purple: #b8a0ff;
      --paper: #fffdf7;
      --line: 3px solid var(--ink);
      --shadow: 5px 5px 0 var(--ink);
    }

    * { box-sizing: border-box; }
    html { scroll-behavior: smooth; }
    body {
      margin: 0;
      color: var(--ink);
      background: var(--paper);
      font-family: "M PLUS Rounded 1c", "Kosugi Maru", sans-serif;
      line-height: 1.7;
    }
    a { color: inherit; }
    .wrap { width: min(1120px, calc(100% - 36px)); margin: auto; }
    .topbar {
      background: var(--yellow);
      border-bottom: var(--line);
      font-weight: 800;
      text-align: center;
      padding: 8px 12px;
      font-size: .85rem;
      letter-spacing: .06em;
    }
    header {
      display: flex;
      justify-content: space-between;
      align-items: center;
      gap: 18px;
      padding: 20px 0;
    }
    .logo {
      text-decoration: none;
      font-weight: 800;
      font-size: 1.6rem;
      letter-spacing: -.06em;
    }
    .logo span { display: inline-block; transform: rotate(-8deg); color: #ff4c9b; }
    nav { display: flex; gap: 22px; flex-wrap: wrap; }
    nav a { text-decoration: none; font-size: .92rem; font-weight: 800; }
    nav a:hover { color: #ed3f8d; }
    .hero {
      position: relative;
      display: grid;
      grid-template-columns: 1.05fr .95fr;
      align-items: center;
      gap: 32px;
      padding: 48px 0 72px;
    }
    .eyebrow {
      display: inline-block;
      background: var(--green);
      border: 2px solid var(--ink);
      border-radius: 999px;
      padding: 5px 14px;
      font-size: .8rem;
      font-weight: 800;
      transform: rotate(-2deg);
    }
    h1 {
      font-size: clamp(2.7rem, 6vw, 5.6rem);
      line-height: 1.12;
      letter-spacing: -.075em;
      margin: 22px 0;
    }
    h1 .highlight {
      position: relative;
      display: inline;
      z-index: 0;
    }
    h1 .highlight::after {
      content: "";
      position: absolute;
      left: 0; right: -4px; bottom: 4px;
      height: 23%;
      background: var(--pink);
      z-index: -1;
      transform: rotate(-1deg);
    }
    .hero p { max-width: 500px; font-size: 1.04rem; }
    .actions { display: flex; gap: 13px; flex-wrap: wrap; margin-top: 26px; }
    .btn {
      display: inline-flex;
      justify-content: center;
      align-items: center;
      gap: 8px;
      padding: 12px 19px;
      border: var(--line);
      border-radius: 13px;
      text-decoration: none;
      font-weight: 800;
      box-shadow: 4px 4px 0 var(--ink);
      transition: transform .18s, box-shadow .18s;
    }
    .btn:hover { transform: translate(3px, 3px); box-shadow: 1px 1px 0 var(--ink); }
    .btn-primary { background: var(--pink); }
    .btn-secondary { background: white; }
    .art-board {
      min-height: 390px;
      position: relative;
      border: var(--line);
      border-radius: 30px;
      background: var(--blue);
      box-shadow: 8px 8px 0 var(--ink);
      display: grid;
      place-items: center;
      overflow: hidden;
      transform: rotate(2deg);
    }
    .art-board::before, .art-board::after {
      content: "✦";
      position: absolute;
      font-size: 3.5rem;
      color: var(--ink);
    }
    .art-board::before { top: 18px; left: 22px; transform: rotate(-12deg); }
    .art-board::after { right: 22px; bottom: 16px; color: #ff4c9b; }
    .art-placeholder {
      width: 72%;
      min-height: 265px;
      border: 3px dashed var(--ink);
      border-radius: 22px;
      background: rgba(255,255,255,.55);
      display: grid;
      place-items: center;
      text-align: center;
      padding: 20px;
      font-weight: 800;
    }
    .art-placeholder .emoji { display: block; font-size: 5.2rem; line-height: 1.2; }
    .art-placeholder small { display: block; font-size: .82rem; font-weight: 500; margin-top: 8px; }
    .sticker {
      position: absolute;
      right: 5px; top: 30px;
      background: var(--yellow);
      border: var(--line);
      border-radius: 50%;
      width: 95px; height: 95px;
      display: grid; place-items: center;
      text-align: center;
      font-size: .78rem; font-weight: 800;
      line-height: 1.3;
      transform: rotate(12deg);
    }
    .ticker {
      background: var(--ink);
      color: white;
      padding: 12px 0;
      overflow: hidden;
      white-space: nowrap;
      font-weight: 800;
      letter-spacing: .06em;
    }
    .ticker span { display: inline-block; animation: slide 24s linear infinite; }
    @keyframes slide { from { transform: translateX(0); } to { transform: translateX(-35%); } }
    section { padding: 76px 0; }
    .section-head { display: flex; align-items: end; justify-content: space-between; gap: 18px; margin-bottom: 28px; }
    .section-kicker { font-size: .78rem; font-weight: 800; letter-spacing: .12em; color: #7561d8; }
    h2 { font-size: clamp(2rem, 4vw, 3rem); line-height: 1.2; letter-spacing: -.06em; margin: 5px 0 0; }
    .section-head p { margin: 0; max-width: 390px; font-size: .92rem; }
    .gallery {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 22px;
    }
    .work-card {
      border: var(--line);
      border-radius: 18px;
      overflow: hidden;
      background: white;
      box-shadow: 4px 4px 0 var(--ink);
      transition: transform .2s;
    }
    .work-card:hover { transform: translateY(-6px) rotate(-.5deg); }
    .work-image {
      min-height: 220px;
      display: grid;
      place-items: center;
      text-align: center;
      padding: 18px;
      border-bottom: var(--line);
      font-weight: 800;
    }
    .work-image .big { font-size: 3.7rem; display: block; }
    .work-image small { display: block; font-weight: 500; }
    .pink-bg { background: #ffc5df; }
    .yellow-bg { background: #fff0a6; }
    .purple-bg { background: #d4c8ff; }
    .green-bg { background: #c7f4ce; }
    .blue-bg { background: #b7efff; }
    .orange-bg { background: #ffd0a8; }
    .work-info { padding: 16px; }
    .work-info h3 { margin: 0 0 4px; font-size: 1.05rem; }
    .work-info p { margin: 0; color: #5b5971; font-size: .86rem; }
    .about-grid { display: grid; grid-template-columns: .8fr 1.2fr; gap: 32px; align-items: stretch; }
    .about-art {
      border: var(--line);
      border-radius: 24px;
      background: var(--yellow);
      min-height: 300px;
      display: grid;
      place-items: center;
      text-align: center;
      padding: 25px;
      box-shadow: var(--shadow);
    }
    .about-art .emoji { font-size: 5rem; display: block; }
    .about-copy {
      border: var(--line);
      border-radius: 24px;
      padding: clamp(22px, 4vw, 38px);
      background: white;
    }
    .about-copy p { margin-top: 0; }
    .tags { display: flex; flex-wrap: wrap; gap: 9px; margin-top: 20px; }
    .tag { border: 2px solid var(--ink); padding: 5px 11px; border-radius: 999px; font-size: .8rem; font-weight: 800; }
    .tag:nth-child(1) { background: var(--pink); }
    .tag:nth-child(2) { background: var(--blue); }
    .tag:nth-child(3) { background: var(--green); }
    .tag:nth-child(4) { background: var(--purple); }
    .social-section { background: #f1ecff; border-top: var(--line); border-bottom: var(--line); }
    .social-grid { display: grid; grid-template-columns: repeat(4, 1fr); gap: 15px; }
    .social-card {
      background: white;
      border: var(--line);
      border-radius: 16px;
      padding: 20px 15px;
      text-align: center;
      text-decoration: none;
      box-shadow: 4px 4px 0 var(--ink);
      transition: transform .2s;
    }
    .social-card:hover { transform: translateY(-4px); }
    .social-card .social-icon { font-size: 2rem; display: block; }
    .social-card strong { display: block; margin: 6px 0 2px; }
    .social-card small { font-size: .78rem; color: #67647a; }
    .contact-box {
      text-align: center;
      border: var(--line);
      border-radius: 28px;
      padding: 42px 20px;
      background: var(--green);
      box-shadow: 7px 7px 0 var(--ink);
    }
    .contact-box h2 { margin-bottom: 13px; }
    .contact-box p { max-width: 580px; margin: 0 auto 23px; }
    footer { padding: 28px 0; text-align: center; font-size: .8rem; }
    footer .footer-logo { font-weight: 800; font-size: 1.15rem; }
    .note { font-size: .78rem; color: #625f75; margin-top: 12px; }
    @media (max-width: 760px) {
      header { align-items: flex-start; flex-direction: column; }
      nav { gap: 13px; }
      .hero { grid-template-columns: 1fr; padding: 30px 0 52px; }
      .art-board { min-height: 310px; margin: 0 5px 5px 0; }
      .art-placeholder { min-height: 210px; }
      .sticker { right: 0; top: 15px; width: 78px; height: 78px; font-size: .68rem; }
      section { padding: 55px 0; }
      .section-head { align-items: flex-start; flex-direction: column; }
      .gallery { grid-template-columns: repeat(2, 1fr); gap: 14px; }
      .work-image { min-height: 165px; }
      .about-grid { grid-template-columns: 1fr; }
      .about-art { min-height: 220px; }
      .social-grid { grid-template-columns: repeat(2, 1fr); }
    }
    @media (max-width: 430px) {
      .wrap { width: min(100% - 26px, 1120px); }
      .gallery { grid-template-columns: 1fr; }
      .work-image { min-height: 210px; }
      nav a { font-size: .84rem; }
    }
  </style>
</head>
<body>
  <div class="topbar">WELCOME TO MY LITTLE ART WORLD ✦ 下書きなしの一発描き！</div>

  <div class="wrap">
    <header>
      <a class="logo" href="#top" aria-label="りおん ホーム"><span>●</span> りおん / RION</a>
      <nav aria-label="メインナビゲーション">
        <a href="#works">作品を見る</a>
        <a href="#about">りおんについて</a>
        <a href="#sns">SNS</a>
        <a href="#contact">ご依頼・お問い合わせ</a>
      </nav>
    </header>

    <main id="top">
      <section class="hero">
        <div>
          <span class="eyebrow">ONE-STROKE ILLUSTRATION</span>
          <h1>下書きなし、<br><span class="highlight">一発描き。</span></h1>
          <p>
            モンスターとひよこが暮らす、ちょっと不思議な世界。
            ペン一本から生まれる、キモかわいいイラストを描いています。
          </p>
          <div class="actions">
            <a class="btn btn-primary" href="#works">作品を見てみる <span>↘</span></a>
            <a class="btn btn-secondary" href="#sns">SNSをチェック <span>↗</span></a>
          </div>
        </div>
        <div class="art-board" aria-label="メイン作品画像のプレースホルダー">
          <div class="art-placeholder">
            <div>
              <span class="emoji">🐣 👾</span>
              ここにお気に入りの作品画像を追加！
              <small>画像を入れるときは、この部分を img タグに置き換えてね。</small>
            </div>
          </div>
          <div class="sticker">NO DRAFT<br>JUST DRAW! ✍️</div>
        </div>
      </section>
    </main>
  </div>

  <div class="ticker" aria-hidden="true">
    <span> ✦ DRAW WITHOUT A DRAFT ✦ MONSTERS & CHICKS ✦ ONE LINE, ONE WORLD ✦ DRAW WITHOUT A DRAFT ✦ MONSTERS & CHICKS ✦ ONE LINE, ONE WORLD ✦ </span>
  </div>

  <section id="works">
    <div class="wrap">
      <div class="section-head">
        <div>
          <div class="section-kicker">01 / MY WORKS</div>
          <h2>作品ギャラリー 🎨</h2>
        </div>
        <p>一枚ずつ違う表情、違う物語。お気に入りの作品を見つけてね！</p>
      </div>
      <div class="gallery">
        <article class="work-card">
          <div class="work-image pink-bg"><div><span class="big">👾</span>作品画像 01<small>ここに画像を設定</small></div></div>
          <div class="work-info"><h3>MONSTER #01</h3><p>不気味で、ちょっとかわいい。</p></div>
        </article>
        <article class="work-card">
          <div class="work-image yellow-bg"><div><span class="big">🐣</span>作品画像 02<small>ここに画像を設定</small></div></div>
          <div class="work-info"><h3>CHICK #02</h3><p>小さな相棒、ひよこの世界。</p></div>
        </article>
        <article class="work-card">
          <div class="work-image purple-bg"><div><span class="big">⚙️</span>作品画像 03<small>ここに画像を設定</small></div></div>
          <div class="work-info"><h3>MECHANICAL #03</h3><p>機械と生き物のあいだ。</p></div>
        </article>
        <article class="work-card">
          <div class="work-image green-bg"><div><span class="big">✍️</span>作品画像 04<small>ここに画像を設定</small></div></div>
          <div class="work-info"><h3>ONE STROKE #04</h3><p>線がつながって生まれる形。</p></div>
        </article>
        <article class="work-card">
          <div class="work-image blue-bg"><div><span class="big">💙</span>作品画像 05<small>ここに画像を設定</small></div></div>
          <div class="work-info"><h3>BLUE WORLD #05</h3><p>青い色で描く、不思議な景色。</p></div>
        </article>
        <article class="work-card">
          <div class="work-image orange-bg"><div><span class="big">✨</span>作品画像 06<small>ここに画像を設定</small></div></div>
          <div class="work-info"><h3>NEW STORY #06</h3><p>次はどんな世界が生まれる？</p></div>
        </article>
      </div>
      <p class="note">※ 作品名・説明文・画像は自由に変更できます。</p>
    </div>
  </section>

  <section id="about">
    <div class="wrap">
      <div class="section-head">
        <div>
          <div class="section-kicker">02 / ABOUT ME</div>
          <h2>描いている人について</h2>
        </div>
      </div>
      <div class="about-grid">
        <div class="about-art">
          <div><span class="emoji">🐣✏️</span><strong>HELLO, I'M RION!</strong><br>ここに自分の写真や作品を入れてもOK</div>
        </div>
        <div class="about-copy">
          <p>はじめまして、りおんです！</p>
          <p>
            下書きをせず、ペンで一気に描き上げる「一発描き」を中心に活動しています。
            モンスターの不気味さと、ひよこのポップなかわいさを組み合わせた、
            どこかクセになる世界を制作中。
          </p>
          <p>
            絵を通して、見た人の想像力が広がったり、
            「なんだこれ！」と少しでも心が動いたりしたらうれしいです。
          </p>
          <div class="tags">
            <span class="tag">#一発描き</span>
            <span class="tag">#モンスター</span>
            <span class="tag">#ひよこ</span>
            <span class="tag">#キモかわ</span>
          </div>
        </div>
      </div>
    </div>
  </section>

  <section id="sns" class="social-section">
    <div class="wrap">
      <div class="section-head">
        <div>
          <div class="section-kicker">03 / FOLLOW ME</div>
          <h2>SNSでつながろう！</h2>
        </div>
        <p>制作動画や新作のお知らせ、普段の活動はこちらから。</p>
      </div>
      <div class="social-grid">
        <a class="social-card" href="https://www.youtube.com/" target="_blank" rel="noopener noreferrer">
          <span class="social-icon">▶️</span><strong>YouTube</strong><small>一発描き動画を見る ↗</small>
        </a>
        <a class="social-card" href="https://www.instagram.com/" target="_blank" rel="noopener noreferrer">
          <span class="social-icon">📸</span><strong>Instagram</strong><small>作品・制作風景 ↗</small>
        </a>
        <a class="social-card" href="https://www.tiktok.com/" target="_blank" rel="noopener noreferrer">
          <span class="social-icon">🎵</span><strong>TikTok</strong><small>ショート動画を見る ↗</small>
        </a>
        <a class="social-card" href="https://thebase.com/" target="_blank" rel="noopener noreferrer">
          <span class="social-icon">🛍️</span><strong>ONLINE SHOP</strong><small>原画・グッズをチェック ↗</small>
        </a>
      </div>
      <p class="note">※ 上のリンクはサンプルです。自分のSNS・ショップのURLに変更してください。</p>
    </div>
  </section>

  <section id="contact">
    <div class="wrap">
      <div class="contact-box">
        <div class="section-kicker">04 / CONTACT</div>
        <h2>一緒に作品をつくりませんか？</h2>
        <p>イラストのご依頼、コラボレーションなど、お気軽にご連絡ください！</p>
        <a class="btn btn-primary" href="https://www.instagram.com/" target="_blank" rel="noopener noreferrer">お問い合わせはこちら ↗</a>
        <p class="note">※ ボタンのリンク先は、DMやお問い合わせフォームのURLに変更してください。</p>
      </div>
    </div>
  </section>

  <footer>
    <div class="wrap">
      <div class="footer-logo">りおん / RION ✦</div>
      <div>© <span id="year"></span> RION. All rights reserved.</div>
      <div class="note">Made with curiosity, lines, and a little bit of chaos.</div>
    </div>
  </footer>

  <script>
    document.getElementById("year").textContent = new Date().getFullYear();
  </script>
</body>
</html>
