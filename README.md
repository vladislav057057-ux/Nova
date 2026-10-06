<html lang="ru">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <meta name="description" content="NOVA — современные цифровые решения для бизнеса">
  <title>NOVA — Цифровые решения для бизнеса</title>

  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    html {
      scroll-behavior: smooth;
    }

    body {
      font-family: Arial, Helvetica, sans-serif;
      background: #07111f;
      color: #f5f7fb;
      line-height: 1.6;
    }

    a {
      color: inherit;
      text-decoration: none;
    }

    .container {
      width: min(1120px, 92%);
      margin: 0 auto;
    }

    /* HEADER */

    header {
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      z-index: 1000;
      background: rgba(7, 17, 31, 0.75);
      backdrop-filter: blur(15px);
      border-bottom: 1px solid rgba(255,255,255,0.08);
    }

    .nav {
      height: 76px;
      display: flex;
      align-items: center;
      justify-content: space-between;
    }

    .logo {
      font-size: 25px;
      font-weight: 800;
      letter-spacing: 1px;
    }

    .logo span {
      color: #5ee7ff;
    }

    .menu {
      display: flex;
      gap: 32px;
      align-items: center;
      list-style: none;
    }

    .menu a {
      color: #b7c2d3;
      font-size: 15px;
      transition: .25s;
    }

    .menu a:hover {
      color: #fff;
    }

    .nav-button {
      background: #5ee7ff;
      color: #06111c !important;
      padding: 11px 18px;
      border-radius: 10px;
      font-weight: 700;
    }

    /* HERO */

    .hero {
      min-height: 100vh;
      display: flex;
      align-items: center;
      position: relative;
      overflow: hidden;
      padding-top: 80px;
    }

    .hero::before {
      content: "";
      position: absolute;
      width: 600px;
      height: 600px;
      background: #006eff;
      filter: blur(180px);
      opacity: .22;
      top: -200px;
      right: -150px;
    }

    .hero::after {
      content: "";
      position: absolute;
      width: 400px;
      height: 400px;
      background: #00e5ff;
      filter: blur(180px);
      opacity: .12;
      bottom: -200px;
      left: -100px;
    }

    .hero-content {
      position: relative;
      z-index: 2;
      max-width: 780px;
    }

    .badge {
      display: inline-flex;
      padding: 8px 14px;
      border: 1px solid rgba(94,231,255,.25);
      background: rgba(94,231,255,.07);
      color: #5ee7ff;
      border-radius: 50px;
      font-size: 13px;
      margin-bottom: 25px;
    }

    h1 {
      font-size: clamp(45px, 7vw, 82px);
      line-height: 1.03;
      letter-spacing: -3px;
      margin-bottom: 25px;
    }

    h1 span {
      background: linear-gradient(90deg, #5ee7ff, #8d7aff);
      -webkit-background-clip: text;
      color: transparent;
    }

    .hero-text {
      max-width: 650px;
      color: #aab6c8;
      font-size: 19px;
      margin-bottom: 35px;
    }

    .buttons {
      display: flex;
      gap: 14px;
      flex-wrap: wrap;
    }

    .button {
      padding: 14px 22px;
      border-radius: 11px;
      font-weight: 700;
      transition: .25s;
      display: inline-block;
    }

    .button-primary {
      background: linear-gradient(135deg, #5ee7ff, #6c7cff);
      color: #06111c;
      box-shadow: 0 10px 30px rgba(94,231,255,.15);
    }

    .button-primary:hover {
      transform: translateY(-3px);
    }

    .button-secondary {
      border: 1px solid #26364b;
      color: #d8e0ec;
    }

    .button-secondary:hover {
      background: #101d2d;
    }

    /* STATS */

    .stats {
      padding: 35px 0;
      border-top: 1px solid rgba(255,255,255,.07);
      border-bottom: 1px solid rgba(255,255,255,.07);
      background: rgba(255,255,255,.015);
    }

    .stats-grid {
      display: grid;
      grid-template-columns: repeat(4, 1fr);
      gap: 20px;
    }

    .stat {
      text-align: center;
    }

    .stat strong {
      display: block;
      font-size: 30px;
      margin-bottom: 3px;
    }

    .stat span {
      color: #8290a4;
      font-size: 14px;
    }

    /* SECTIONS */

    section {
      padding: 100px 0;
    }

    .section-heading {
      max-width: 650px;
      margin-bottom: 50px;
    }

    .section-heading small {
      color: #5ee7ff;
      text-transform: uppercase;
      letter-spacing: 2px;
      font-size: 12px;
      font-weight: bold;
    }

    .section-heading h2 {
      font-size: clamp(34px, 5vw, 50px);
      line-height: 1.1;
      margin: 12px 0 15px;
    }

    .section-heading p {
      color: #8f9caf;
      font-size: 17px;
    }

    /* SERVICES */

    .services {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 20px;
    }

    .card {
      padding: 30px;
      border-radius: 18px;
      border: 1px solid #1c2a3d;
      background: linear-gradient(145deg, #0c1929, #091422);
      transition: .3s;
    }

    .card:hover {
      transform: translateY(-7px);
      border-color: #31516d;
      box-shadow: 0 20px 50px rgba(0,0,0,.2);
    }

    .icon {
      width: 52px;
      height: 52px;
      border-radius: 14px;
      display: grid;
      place-items: center;
      background: rgba(94,231,255,.08);
      color: #5ee7ff;
      font-size: 24px;
      margin-bottom: 22px;
    }

    .card h3 {
      margin-bottom: 10px;
      font-size: 21px;
    }

    .card p {
      color: #8794a7;
      font-size: 15px;
    }

    /* ABOUT */

    .about {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 60px;
      align-items: center;
    }

    .about-box {
      padding: 40px;
      border-radius: 24px;
      background:
        radial-gradient(circle at top right, rgba(94,231,255,.12), transparent 40%),
        #0b1828;
      border: 1px solid #1d2b3d;
    }

    .about-box h3 {
      font-size: 28px;
      margin-bottom: 18px;
    }

    .about-box p {
      color: #8f9caf;
    }

    .check-list {
      list-style: none;
      margin-top: 25px;
    }

    .check-list li {
      margin: 13px 0;
      color: #cbd5e2;
    }

    .check-list li::before {
      content: "✓";
      color: #5ee7ff;
      font-weight: bold;
      margin-right: 10px;
    }

    /* PROCESS */

    .process {
      display: grid;
      grid-template-columns: repeat(4, 1fr);
      gap: 18px;
    }

    .step {
      position: relative;
      padding: 25px;
      border-top: 2px solid #27384c;
    }

    .number {
      color: #5ee7ff;
      font-size: 13px;
      font-weight: bold;
      margin-bottom: 18px;
    }

    .step h3 {
      margin-bottom: 9px;
    }

    .step p {
      color: #8290a4;
      font-size: 14px;
    }

    /* CTA */

    .cta {
      text-align: center;
      padding: 75px 30px;
      border: 1px solid #20344a;
      border-radius: 25px;
      background:
        radial-gradient(circle at center, rgba(74,126,255,.18), transparent 60%),
        #0a1727;
    }

    .cta h2 {
      font-size: clamp(35px, 5vw, 55px);
      margin-bottom: 15px;
    }

    .cta p {
      color: #8997aa;
      max-width: 600px;
      margin: 0 auto 30px;
    }

    /* FOOTER */

    footer {
      padding: 35px 0;
      border-top: 1px solid rgba(255,255,255,.07);
      color: #718095;
      font-size: 14px;
    }

    .footer-content {
      display: flex;
      justify-content: space-between;
      gap: 20px;
    }

    /* MOBILE */

    @media (max-width: 800px) {
      .menu {
        display: none;
      }

      .stats-grid {
        grid-template-columns: repeat(2, 1fr);
      }

      .services {
        grid-template-columns: 1fr;
      }

      .about {
        grid-template-columns: 1fr;
      }

      .process {
        grid-template-columns: 1fr 1fr;
      }

      section {
        padding: 75px 0;
      }
    }

    @media (max-width: 500px) {
      h1 {
        letter-spacing: -2px;
      }

      .process {
        grid-template-columns: 1fr;
      }

      .footer-content {
        flex-direction: column;
      }

      .hero-text {
        font-size: 17px;
      }
    }
  </style>
</head>

<body>

  <header>
    <div class="container nav">
      <a href="#" class="logo">NO<span>VA</span></a>

      <ul class="menu">
        <li><a href="#services">Услуги</a></li>
        <li><a href="#about">О компании</a></li>
        <li><a href="#process">Процесс</a></li>
        <li><a href="#contacts" class="nav-button">Связаться</a></li>
      </ul>
    </div>
  </header>

  <main>

    <!-- HERO -->

    <section class="hero">
      <div class="container">
        <div class="hero-content">

          <div class="badge">
            ● Цифровое агентство нового поколения
          </div>

          <h1>
            Создаём решения,<br>
            которые <span>двигают бизнес</span>
          </h1>

          <p class="hero-text">
            NOVA помогает компаниям развиваться в цифровой среде:
            создаём сайты, автоматизируем процессы и превращаем идеи
            в работающие продукты.
          </p>

          <div class="buttons">
            <a href="#contacts" class="button button-primary">
              Обсудить проект →
            </a>

            <a href="#services" class="button button-secondary">
              Наши услуги
            </a>
          </div>

        </div>
      </div>
    </section>

    <!-- STATS -->

    <div class="stats">
      <div class="container stats-grid">

        <div class="stat">
          <strong>120+</strong>
          <span>реализованных проектов</span>
        </div>

        <div class="stat">
          <strong>8 лет</strong>
          <span>опыта в digital</span>
        </div>

        <div class="stat">
          <strong>24/7</strong>
          <span>поддержка клиентов</span>
        </div>

        <div class="stat">
          <strong>98%</strong>
          <span>довольных клиентов</span>
        </div>

      </div>
    </div>

    <!-- SERVICES -->

    <section id="services">
      <div class="container">

        <div class="section-heading">
          <small>Что мы делаем</small>
          <h2>Всё необходимое для роста вашего бизнеса</h2>
          <p>
            От идеи до полноценного цифрового продукта —
            берём на себя весь процесс.
          </p>
        </div>

        <div class="services">

          <div class="card">
            <div class="icon">✦</div>
            <h3>Веб-разработка</h3>
            <p>
              Быстрые, современные и адаптивные сайты,
              которые отлично выглядят на любом устройстве.
            </p>
          </div>

          <div class="card">
            <div class="icon">◈</div>
            <h3>Дизайн</h3>
            <p>
              Создаём понятный и привлекательный интерфейс,
              который помогает пользователю сделать нужное действие.
            </p>
          </div>

          <div class="card">
            <div class="icon">↗</div>
            <h3>Digital-маркетинг</h3>
            <p>
              Помогаем привлекать клиентов и увеличивать
              эффективность вашего бизнеса в интернете.
            </p>
          </div>

          <div class="card">
            <div class="icon">⚡</div>
            <h3>Автоматизация</h3>
            <p>
              Убираем рутинные процессы и внедряем инструменты,
              которые экономят время вашей команды.
            </p>
          </div>

          <div class="card">
            <div class="icon">◎</div>
            <h3>Аналитика</h3>
            <p>
              Превращаем данные в понятные решения,
              которые помогают бизнесу расти быстрее.
            </p>
          </div>

          <div class="card">
            <div class="icon">∞</div>
            <h3>Поддержка</h3>
            <p>
              Остаёмся рядом после запуска и помогаем
              развивать цифровой продукт дальше.
            </p>
          </div>

        </div>
      </div>
    </section>

    <!-- ABOUT -->

    <section id="about">
      <div class="container about">

        <div class="section-heading">
          <small>Почему NOVA</small>

          <h2>
            Мы не просто создаём сайты
          </h2>

          <p>
            Мы погружаемся в задачи бизнеса, изучаем аудиторию
            и создаём решения, которые приносят реальную пользу.
          </p>

          <ul class="check-list">
            <li>Прозрачный процесс работы</li>
            <li>Фокус на результате</li>
            <li>Современные технологии</li>
            <li>Поддержка после запуска</li>
          </ul>
        </div>

        <div class="about-box">
          <h3>Ваш бизнес должен выглядеть современно.</h3>

          <p>
            Первое впечатление клиента формируется за считанные секунды.
            Поэтому мы создаём цифровые продукты, которые вызывают доверие,
            подчёркивают экспертность компании и помогают превращать
            посетителей в клиентов.
          </p>
        </div>

      </div>
    </section>

    <!-- PROCESS -->

    <section id="process">
      <div class="container">

        <div class="section-heading">
          <small>Как мы работаем</small>
          <h2>От идеи до результата</h2>
        </div>

        <div class="process">

          <div class="step">
            <div class="number">01 / АНАЛИЗ</div>
            <h3>Изучаем задачу</h3>
            <p>
              Определяем цели, аудиторию и ключевые задачи проекта.
            </p>
          </div>

          <div class="step">
            <div class="number">02 / КОНЦЕПЦИЯ</div>
            <h3>Создаём решение</h3>
            <p>
              Продумываем структуру, дизайн и пользовательский сценарий.
            </p>
          </div>

          <div class="step">
            <div class="number">03 / РАЗРАБОТКА</div>
            <h3>Запускаем</h3>
            <p>
              Превращаем концепцию в быстрый и функциональный продукт.
            </p>
          </div>

          <div class="step">
            <div class="number">04 / РОСТ</div>
            <h3>Развиваем</h3>
            <p>
              Анализируем результаты и улучшаем продукт после запуска.
            </p>
          </div>

        </div>
      </div>
    </section>

    <!-- CTA -->

    <section id="contacts">
      <div class="container">

        <div class="cta">
          <h2>Есть идея?</h2>

          <p>
            Расскажите о своём проекте. Мы поможем превратить
            идею в современный цифровой продукт.
          </p>

          <a
            href="mailto:hello@nova.example"
            class="button button-primary"
          >
            Написать нам →
          </a>
        </div>

      </div>
    </section>

  </main>

  <footer>
    <div class="container footer-content">
      <div>
        © 2026 NOVA. Все права защищены.
      </div>

      <div>
        Digital solutions for modern business.
      </div>
    </div>
  </footer>

</body>
</html>
