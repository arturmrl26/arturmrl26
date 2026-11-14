html
<style>.md-bio {
    --void: #07070a;
    --yellow: #fcee0a;
    --cyan: #00f0ff;
    --pink: #ff2a6d;
    --green: #19ff7a;
    --orange: #ff9f1c;
    box-sizing: border-box;
    position: relative;
    isolation: isolate;
    width: 100%;
    max-width: 860px;
    margin: 0 auto;
    overflow: hidden;
    border: 1px solid var(--yellow);
    background:
      linear-gradient(rgba(252,238,10,.04) 1px, transparent 1px) 0 0 / 26px 26px,
      linear-gradient(90deg, rgba(252,238,10,.04) 1px, transparent 1px) 0 0 / 26px 26px,
      var(--void);
    color: #e2dfcc;
    box-shadow: 0 0 0 3px #000, 0 0 0 4px #fcee0a55, 0 0 30px #fcee0a33, 0 20px 50px #000c;
    font: 16px/1.6 "Segoe UI", Arial, sans-serif;
  }

  .md-bio *, .md-bio *::before, .md-bio *::after { box-sizing: border-box; }
  .md-bio a { color: inherit; text-decoration: none; }

  .md-bio::after {
    content: "";
    position: absolute;
    inset: 0;
    z-index: 30;
    pointer-events: none;
    background: repeating-linear-gradient(0deg, transparent 0 2px, #00000030 2px 3px);
  }

  .md-trim {
    height: 10px;
    background: repeating-linear-gradient(-45deg, var(--yellow) 0 10px, #000 10px 20px);
    background-size: 28.28px 28.28px;
    animation: md-stripes 1.2s linear infinite;
  }

  .md-top {
    display: flex;
    justify-content: space-between;
    align-items: center;
    gap: 12px;
    padding: 9px 20px;
    border-bottom: 1px solid #fcee0a55;
    background: #000;
    color: var(--yellow);
    font: bold 11px/1.4 Consolas, "Courier New", monospace;
    letter-spacing: .14em;
    text-transform: uppercase;
  }

  .md-top span:last-child { color: var(--cyan); white-space: nowrap; }

  .md-dot {
    display: inline-block;
    width: 8px;
    height: 8px;
    margin-right: 8px;
    border-radius: 50%;
    background: var(--green);
    box-shadow: 0 0 8px var(--green);
    animation: md-blink 1.1s steps(2) infinite;
  }

  /* ---------- HERO ---------- */
  .md-hero {
    position: relative;
    overflow: hidden;
    padding: 30px 26px 26px;
    border-bottom: 1px solid #fcee0a77;
  }

  .md-hero::before {
    content: "";
    position: absolute;
    left: 0;
    right: 0;
    top: -70px;
    height: 60px;
    pointer-events: none;
    background: linear-gradient(180deg, transparent, #fcee0a1c 70%, #fcee0a44);
    animation: md-scan 5s linear infinite;
  }

  .md-trace {
    position: absolute;
    left: 0;
    right: 0;
    height: 1px;
    background: #fcee0a2a;
    overflow: hidden;
    pointer-events: none;
  }

  .md-trace::after {
    content: "";
    position: absolute;
    top: -1px;
    left: 0;
    width: 90px;
    height: 3px;
    background: linear-gradient(90deg, transparent, var(--yellow), #fff);
    box-shadow: 0 0 10px var(--yellow);
    animation: md-run 3.4s linear infinite;
  }

  .md-trace.t1 { top: 14%; }
  .md-trace.t2 { top: 88%; }
  .md-trace.t2::after { background: linear-gradient(90deg, transparent, var(--cyan), #fff); box-shadow: 0 0 10px var(--cyan); animation-duration: 4.6s; animation-delay: -1.6s; }

  .md-bolt {
    position: absolute;
    right: 22px;
    top: 24px;
    width: 54px;
    height: auto;
    fill: var(--yellow);
    filter: drop-shadow(0 0 8px var(--yellow));
    animation: md-zap 3.4s infinite;
    pointer-events: none;
  }

  .md-hero-copy { position: relative; z-index: 2; }

  .md-kicker {
    margin: 0 0 12px;
    color: var(--yellow);
    font: bold 11px/1.45 Consolas, "Courier New", monospace;
    letter-spacing: .17em;
    text-transform: uppercase;
  }

  .md-kicker::after { content: "_"; margin-left: 3px; animation: md-blink 1s steps(2) infinite; }

  .md-title {
    margin: 0;
    color: var(--yellow);
    font: 900 clamp(42px, 9vw, 74px)/.92 Impact, "Arial Black", sans-serif;
    text-transform: uppercase;
    text-shadow: 0 0 14px #fcee0a88, 2px 0 var(--cyan), -2px 0 var(--pink);
    animation: md-glitch 5s infinite;
  }

  .md-title span { color: #fff; text-shadow: 0 0 14px #fff6, 2px 0 var(--pink), -2px 0 var(--cyan); }

  .md-role {
    display: inline-block;
    margin: 16px 0 10px;
    padding: 5px 12px;
    background: var(--yellow);
    color: #000;
    font: bold 12px/1.5 Consolas, "Courier New", monospace;
    letter-spacing: .08em;
    text-transform: uppercase;
    clip-path: polygon(0 0, calc(100% - 10px) 0, 100% 10px, 100% 100%, 10px 100%, 0 calc(100% - 10px));
  }

  .md-intro { max-width: 540px; margin: 0; font-size: 15px; }
  .md-intro strong { color: var(--yellow); }

  /* ---------- BOTÕES / HIGHLIGHTS ---------- */
  .md-main { padding: 24px 22px 6px; }

  .md-label {
    display: flex;
    align-items: center;
    gap: 10px;
    margin: 0 0 12px;
    color: var(--yellow);
    font: bold 12px/1.3 Consolas, "Courier New", monospace;
    letter-spacing: .2em;
    text-transform: uppercase;
  }

  .md-label::before { content: "//"; color: var(--pink); }

  .md-label::after {
    content: "";
    flex: 1;
    height: 2px;
    background: linear-gradient(90deg, var(--yellow), transparent) 0 0 / 200% 100%;
    animation: md-line 2.6s linear infinite;
  }

  .md-grid {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    gap: 12px;
    margin-bottom: 26px;
  }

  .md-btn {
    --c: var(--yellow);
    position: relative;
    display: block;
    min-width: 0;
    padding: 16px 18px 16px 22px;
    overflow: hidden;
    cursor: pointer;
    border: 1px solid var(--c);
    background: #0c0c0f;
    color: #e2dfcc;
    clip-path: polygon(0 0, calc(100% - 16px) 0, 100% 16px, 100% 100%, 16px 100%, 0 calc(100% - 16px));
    transition: background .2s, color .2s, box-shadow .2s, border-color .2s;
    outline: none;
  }

  .md-btn.c2 { --c: var(--cyan); }
  .md-btn.c3 { --c: var(--pink); }
  .md-btn.c4 { --c: var(--green); }
  .md-btn.c5 { --c: var(--orange); }

  /* barra lateral que vira preenchimento */
  .md-btn::before {
    content: "";
    position: absolute;
    left: 0;
    top: 0;
    bottom: 0;
    width: 5px;
    background: var(--c);
    box-shadow: 0 0 10px var(--c);
    transition: width .25s ease;
  }

  /* pulso elétrico no topo */
  .md-btn::after {
    content: "";
    position: absolute;
    top: 0;
    left: 0;
    width: 40%;
    height: 2px;
    background: linear-gradient(90deg, transparent, var(--c), transparent);
    transform: translateX(-100%);
    animation: md-sweep 3.2s linear infinite;
  }

  .md-btn small {
    position: relative;
    z-index: 1;
    display: block;
    margin-bottom: 6px;
    color: var(--c);
    font: bold 11px/1.4 Consolas, monospace;
    letter-spacing: .16em;
    text-transform: uppercase;
    transition: color .2s;
  }

  .md-btn b {
    position: relative;
    z-index: 1;
    display: block;
    margin-bottom: 4px;
    color: #fff;
    font-size: 16px;
    line-height: 1.3;
    text-transform: uppercase;
    letter-spacing: .03em;
    transition: color .2s;
  }

  .md-btn p { position: relative; z-index: 1; margin: 0; font-size: 14px; color: #cfccb9; transition: color .2s; }

  .md-btn:hover,
  .md-btn:focus-visible {
    background: var(--c);
    border-color: var(--c);
    color: #000;
    box-shadow: 0 0 26px var(--c);
  }

  .md-btn:hover::before,
  .md-btn:focus-visible::before { width: 100%; opacity: 0; }

  .md-btn:hover small,
  .md-btn:hover b,
  .md-btn:hover p,
  .md-btn:focus-visible small,
  .md-btn:focus-visible b,
  .md-btn:focus-visible p { color: #000; }

  .md-btn.wide { grid-column: 1 / -1; }

  .md-btn.big b { font-size: 20px; }

  /* ---------- RODAPÉ ---------- */
  .md-footer {
    padding: 20px 22px 24px;
    border-top: 1px solid var(--yellow);
    background: #000;
  }

  .md-footer p { margin: 0 0 14px; font-size: 14px; color: #e4e0cc; }

  .md-links { display: flex; flex-wrap: wrap; gap: 10px; }

  .md-links a {
    --c: var(--yellow);
    display: inline-block;
    padding: 10px 16px;
    border: 1px solid var(--c);
    background: transparent;
    color: var(--c);
    font: bold 13px/1.4 Consolas, monospace;
    letter-spacing: .06em;
    text-transform: uppercase;
    clip-path: polygon(0 0, calc(100% - 9px) 0, 100% 9px, 100% 100%, 9px 100%, 0 calc(100% - 9px));
    transition: background .15s, color .15s, box-shadow .15s;
  }

  .md-links a:nth-child(2) { --c: var(--cyan); }
  .md-links a:nth-child(3) { --c: var(--pink); }
  .md-links a:nth-child(4) { --c: var(--green); }

  .md-links a:hover,
  .md-links a:focus-visible {
    background: var(--c);
    color: #000;
    box-shadow: 0 0 18px var(--c);
    outline: none;
  }

  .md-end {
    margin-top: 16px;
    color: #8f8a5c;
    font: 11px/1.4 Consolas, monospace;
    letter-spacing: .12em;
    text-transform: uppercase;
  }

  .md-end::after { content: " █"; color: var(--yellow); animation: md-blink 1s steps(2) infinite; }

  /* ---------- ANIMAÇÕES ---------- */
  @keyframes md-stripes { to { background-position: 28.28px 0; } }
  @keyframes md-scan { from { transform: translateY(0); } to { transform: translateY(600px); } }
  @keyframes md-run { from { transform: translateX(-100px); } to { transform: translateX(900px); } }
  @keyframes md-blink { 50% { opacity: .25; } }
  @keyframes md-line { to { background-position: -200% 0; } }
  @keyframes md-sweep { from { transform: translateX(-100%); } to { transform: translateX(350%); } }
  @keyframes md-zap {
    0%, 86%, 92%, 100% { opacity: .15; }
    88%, 90%, 94% { opacity: 1; }
    96% { opacity: .5; }
  }
  @keyframes md-glitch {
    0%, 90%, 100% { text-shadow: 0 0 14px #fcee0a88, 2px 0 var(--cyan), -2px 0 var(--pink); }
    92% { text-shadow: 0 0 14px #fcee0a88, 6px 0 var(--cyan), -6px 0 var(--pink); }
    94% { text-shadow: 0 0 14px #fcee0a88, -5px 0 var(--cyan), 5px 0 var(--pink); }
  }
  @media (max-width: 650px) {
    .md-top { padding: 9px 12px; font-size: 10px; }
    .md-hero { padding: 26px 16px 22px; }
    .md-bolt { width: 36px; right: 12px; top: 14px; }
    .md-main { padding: 22px 12px 4px; }
    .md-grid { grid-template-columns: repeat(2, minmax(0, 1fr)); gap: 8px; }
    .md-btn { padding: 12px 10px 12px 14px; overflow-wrap: anywhere; }
    .md-btn small { font-size: 9px; letter-spacing: .1em; }
    .md-btn b, .md-btn.big b { font-size: 13px; }
    .md-btn p { font-size: 12px; line-height: 1.45; }
    .md-footer { padding: 20px 14px; }
  }

  @media (prefers-reduced-motion: reduce) {
    .md-bio, .md-bio *, .md-bio *::before, .md-bio *::after {
      animation: none !important;
      transition: none !important;
    }
  }</style><div class="md-bio" lang="pt-BR">
  <div class="md-trim"></div>

  <div class="md-top">
    <span><i class="md-dot"></i>SYS://ARTUR_ARAUJO</span>
    <span>Guarulhos · SP</span>
  </div>

  <header class="md-hero">
    <span class="md-trace t1"></span>
    <span class="md-trace t2"></span>
    <svg class="md-bolt" viewBox="0 0 60 100" aria-hidden="true">
      <polygon points="34,0 6,56 28,56 18,100 54,38 32,38 44,0"/>
    </svg>

    <div class="md-hero-copy">
      <p class="md-kicker">Boot 01 // novo upgrade detectado</p>

      <h1 class="md-title">Artur <span>Araujo</span></h1>

      <p class="md-role">Técnico em Eletrônica · Futuro dev</p>

      <p class="md-intro">
        <strong>8+ anos</strong> consertando o que ninguém conseguia ligar.
        Agora levo essa precisão de bancada para o código,
        com Ciência da Computação, dados e IA.
      </p>
    </div>
  </header>

  <main class="md-main">

    <h2 class="md-label">Highlights</h2>

    <div class="md-grid">

      <div class="md-btn" tabindex="0">
        <small>01 / Experiência</small>
        <b>8+ anos de bancada</b>
        <p>Manutenção, testes de engenharia, calibração e instrumentação analítica.</p>
      </div>

      <div class="md-btn c2" tabindex="0">
        <small>02 / Especialidade</small>
        <b>Solda SMD / BGA</b>
        <p>Diagnóstico de falhas e reparo de placas eletrônicas.</p>
      </div>

      <div class="md-btn c3" tabindex="0">
        <small>03 / Hardware</small>
        <b>Do pesado ao delicado</b>
        <p>Empilhadeiras, equipamentos farmacêuticos, servidores, switches, HDs, acessórios para músicos e mesas de som.</p>
      </div>

      <div class="md-btn c4" tabindex="0">
        <small>04 / Ferramentas</small>
        <b>Bancada de precisão</b>
        <p>Osciloscópios, multímetros e instrumentação analítica.</p>
      </div>

      <div class="md-btn c5" tabindex="0">
        <small>05 / Registro</small>
        <b>Documentação técnica</b>
        <p>Manuais de reparo, relatórios, POPs e controle de qualidade com rastreabilidade.</p>
      </div>

      <div class="md-btn" tabindex="0">
        <small>06 / Formação</small>
        <b>Ciência da Computação</b>
        <p>Em andamento na Universidade Cruzeiro do Sul.</p>
      </div>

    </div>

    <h2 class="md-label">Em treinamento</h2>

    <div class="md-grid">

      <div class="md-btn c2 big" tabindex="0">
        <small>Skill tree</small>
        <b>Python · SQL · C</b>
        <p>Construindo as bases na graduação e em projetos práticos.</p>
      </div>

      <div class="md-btn c3 big" tabindex="0">
        <small>Skill tree</small>
        <b>Dados · IA</b>
        <p>Início de carreira em tecnologia, com a mente de quem já abriu muita placa.</p>
      </div>

      <div class="md-btn c4 wide" tabindex="0">
        <small>Missão principal</small>
        <b>Próximo alvo: primeira vaga em tech</b>
        <p>Estágio ou júnior em Dados, Python, C ou IA, levando a disciplina da eletrônica para soluções em software.</p>
      </div>

    </div>

  </main>

  <footer class="md-footer">

    <p>Canal aberto. Confira meus projetos ou me chame:</p>

    <div class="md-links">
      <a target="_blank" rel="noopener noreferrer" href="https://github.com/arturmrl26">↗ GitHub</a>
      <a target="_blank" rel="noopener noreferrer" href="mailto:arturmrl26@gmail.com">✉ E-mail</a>
      <a target="_blank" rel="noopener noreferrer" href="https://enois.ia.br/perfil/arturaraujo">↗ Énois</a>
      <a target="_blank" rel="noopener noreferrer" href="https://www.linkedin.com/in/arturaraujosantos">↗ LinkedIn</a>
    </div>

    <div class="md-end">Sinal ativo. O upgrade está só começando.</div>

  </footer>
</div>
