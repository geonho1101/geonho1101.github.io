<!doctype html>
<html lang="ko">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>geonho1101 · K-Magpie · Solo Game Developer</title>
  <meta name="description" content="K-Magpie · 1인 인디 게임 개발자. 캐주얼 · 퍼즐 · 방치형. Seal the Rift! 등 모바일 게임 개발." />
  <meta property="og:title" content="geonho1101 · K-Magpie · Solo Game Developer" />
  <meta property="og:description" content="1인 인디 게임 개발자 K-Magpie의 작품과 소식." />
  <meta property="og:type" content="website" />
  <meta property="og:url" content="https://geonho1101.github.io" />
  <meta name="theme-color" content="#0ea5e9" />
  <style>
    /* 스타일은 동일하게 유지 */
  </style>
</head>
<body>
  <!-- NAV -->
  <div class="nav">
    <div class="container nav-inner">
      <a class="brand" href="https://geonho1101.github.io">
        <span class="logo">KM</span>
        <span>K-Magpie</span>
      </a>
      <nav class="row">
        <a class="btn" href="#games">Games</a>
        <a class="btn" href="#about">About</a>
        <a class="btn" href="#contact">Contact</a>
      </nav>
    </div>
  </div>

  <main class="container">
    <!-- HERO -->
    <section class="hero">
      <div class="row">
        <span class="tag">🕹️ Solo Dev</span>
        <span class="tag">Unity · Mobile</span>
        <span class="tag">Casual · Puzzle</span>
      </div>
      <h1>안녕하세요, <strong>K-Magpie</strong> 입니다.<br/>가볍게 즐기고 오래 남는 게임을 만들어요.</h1>
      <p>광고 기반 캐주얼과 퍼즐, 그리고 방치형을 좋아하는 1인 개발자. 빠른 출시, 꾸준한 업데이트가 목표입니다.</p>
      <div class="cta">
        <a class="btn primary" href="#games">🎮 작품 보러가기</a>
        <a class="btn" href="#contact">📣 제휴/문의</a>
      </div>
      <div id="adsStatus" class="status warn" style="margin-top:10px">app-ads.txt 상태 확인 중…</div>
    </section>

    <!-- GAMES -->
    <section id="games" class="section">
      <h2>Games</h2>
      <div class="grid">
        <article class="card">
          <div class="thumb">SEAL THE RIFT!</div>
          <div class="row" style="justify-content:space-between; align-items:center">
            <span class="pill">New</span>
            <span class="muted">캐주얼 · 하이스코어</span>
          </div>
          <h3 style="margin:6px 0 8px">Seal the Rift!</h3>
          <p class="muted" style="margin:0">화면을 터치해 균열을 봉인하며 점수를 올리는 한 손 플레이 게임.</p>
          <div class="row">
            <a class="btn" href="#" title="Google Play 링크로 교체">Google Play</a>
          </div>
        </article>
        <article class="card">
          <div class="thumb">DRAGON FEED</div>
          <div class="row" style="justify-content:space-between; align-items:center">
            <span class="pill" style="background:var(--accent); color:#0a0620">WIP</span>
            <span class="muted">아케이드 · 회피</span>
          </div>
          <h3 style="margin:6px 0 8px">드래곤 먹이주기</h3>
          <p class="muted" style="margin:0">음식은 먹이고 폭탄은 피해라! 단계별로 속도가 빨라지는 클래식 아케이드.</p>
          <div class="row">
            <span class="btn" aria-disabled="true">Coming soon</span>
          </div>
        </article>
      </div>
    </section>

    <!-- ABOUT -->
    <section id="about" class="section">
      <h2>About</h2>
      <div class="card">
        <p style="margin:0 0 8px">Unity로 빠르게 만들고, 데이터로 개선하는 것을 좋아합니다. 보유 에셋을 적극 재활용하여 개발 효율을 끌어올립니다.</p>
        <ul class="muted" style="margin:0 0 6px 18px">
          <li>플랫폼: Android (iOS 예정)</li>
          <li>엔진: Unity 6</li>
          <li>선호 장르: 캐주얼, 퍼즐, 방치형</li>
        </ul>
      </div>
    </section>

    <!-- CONTACT -->
    <section id="contact" class="section">
      <h2>Contact</h2>
      <div class="card">
        <p class="muted" style="margin:0 0 8px">제휴/문의는 이메일로 연락 주세요.</p>
        <div class="row">
          <a class="btn" href="mailto:lewlew123rnrmf@gmail.com">📧 이메일 보내기</a>
          <a class="btn" href="/app-ads.txt" target="_blank">🔎 app-ads.txt 열기</a>
          <a class="btn" href="https://github.com/geonho1101" target="_blank">🐙 GitHub</a>
        </div>
      </div>
    </section>

    <footer class="container" style="padding:20px 0 0">
      <div class="row" style="justify-content:space-between; align-items:center">
        <span class="muted">© <span id="year"></span> K-Magpie • Made with ❤︎ & Unity</span>
      </div>
    </footer>
  </main>

  <script>
    document.getElementById('year').textContent = new Date().getFullYear();
    (async () => {
      const el = document.getElementById('adsStatus');
      try {
        const res = await fetch('/app-ads.txt', {cache:'no-store'});
        if (res.ok) {
          const txt = (await res.text()).trim();
          const looksValid = txt.includes('google.com') && txt.includes('pub-');
          el.className = 'status ok';
          el.textContent = looksValid ? 'app-ads.txt 감지됨 · OK' : 'app-ads.txt 감지됨 · 내용을 확인하세요';
        } else {
          el.className = 'status warn';
          el.textContent = 'app-ads.txt가 보이지 않습니다 (루트에 업로드 필요)';
        }
      } catch (e) {
        el.className = 'status warn';
        el.textContent = 'app-ads.txt 확인 실패 (네트워크)';
      }
    })();
  </script>
</body>
</html>
