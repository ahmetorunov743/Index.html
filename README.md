<!DOCTYPE html>
<html lang="ru">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>AutoPost Bot Platform</title>
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      font-family: 'Segoe UI', sans-serif;
      background-color: #000;
      color: #fff;
      overflow-x: hidden;
    }

    header {
      display: flex;
      align-items: center;
      justify-content: space-between;
      background: #0d0d0d;
      padding: 20px;
      box-shadow: 0 2px 10px rgba(0,0,0,0.5);
      font-size: 1.6em;
      font-weight: bold;
    }

    .burger {
      width: 30px;
      cursor: pointer;
      margin-left: 10px;
    }

    .burger div {
      background-color: #fff;
      height: 3px;
      margin: 6px 0;
      border-radius: 2px;
      transition: all 0.3s ease;
    }

    .sidebar {
      position: fixed;
      top: 0;
      left: -260px;
      width: 260px;
      height: 100%;
      background-color: #121212;
      padding: 60px 20px;
      box-shadow: 5px 0 15px rgba(0,0,0,0.8);
      transition: left 0.3s ease;
      z-index: 999;
    }

    .sidebar.open {
      left: 0;
    }

    .sidebar a {
      display: block;
      color: #fff;
      text-decoration: none;
      margin: 20px 0;
      font-size: 18px;
      padding: 10px;
      background: #1f1f1f;
      border-radius: 10px;
      transition: background 0.2s;
    }

    .sidebar a:hover {
      background: #333;
    }

    .posts {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
      gap: 20px;
      padding: 30px;
    }

    .post {
      background: #1a1a1a;
      padding: 20px;
      border-radius: 16px;
      box-shadow: 0 2px 12px rgba(0,0,0,0.5);
      animation: fadeIn 0.5s ease-in;
    }

    @keyframes fadeIn {
      from {opacity: 0; transform: translateY(20px);}
      to {opacity: 1; transform: translateY(0);}
    }

    .subscribe {
      text-align: center;
      margin: 40px 0;
    }

    .subscribe a {
      background: linear-gradient(135deg, #007aff, #00c6ff);
      color: #fff;
      padding: 15px 30px;
      border-radius: 30px;
      text-decoration: none;
      font-size: 18px;
      box-shadow: 0 4px 15px rgba(0,0,0,0.4);
      transition: transform 0.2s;
    }

    .subscribe a:hover {
      transform: scale(1.05);
    }
  </style>
</head>
<body>

  <div class="sidebar" id="sidebar">
    <a href="https://t.me/Reklomist777" target="_blank">Связаться в Telegram</a>
  </div>

  <header>
    <div class="burger" onclick="toggleSidebar()">
      <div></div>
      <div></div>
      <div></div>
    </div>
    AutoPost Bot
  </header>

  <section class="posts" id="postContainer">
    <!-- Посты загружаются скриптом -->
  </section>

  <div class="subscribe">
    <a href="https://t.me/biznesss7766" target="_blank">Подписаться на канал</a>
  </div>

  <script>
    const posts = [
      '⚡ Добро пожаловать на платформу автопостинга!',
      '✅ Подключайся, автоматизируй посты и зарабатывай!',
      '🔥 Услуги автопостинга от 30₽! Пиши нам!',
    ];

    const container = document.getElementById('postContainer');
    posts.forEach(text => {
      const div = document.createElement('div');
      div.className = 'post';
      div.textContent = text;
      container.appendChild(div);
    });

    function toggleSidebar() {
      document.getElementById('sidebar').classList.toggle('open');
    }
  </script>

</body>
</html>
