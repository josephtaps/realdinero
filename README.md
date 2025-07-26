<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Señales para Aviator - Mateo Molina</title>
  <style>
    body {
      margin: 0;
      font-family: 'Segoe UI', sans-serif;
      background: linear-gradient(to bottom, #2c003e, #1e002a);
      color: #222;
      display: flex;
      flex-direction: column;
      align-items: center;
      padding: 20px;
    }

    header {
      text-align: center;
      margin-bottom: 10px;
      position: relative;
    }

    h1 {
      font-size: 26px;
      font-weight: bold;
      margin: 0 0 5px 0;
      color: white;
      text-shadow: 0 0 8px #ffffff;
    }

    header img {
      display: block;
      margin: 0 auto 5px;
      width: 40px;
    }

    .online-counter {
      font-size: 16px;
      margin-bottom: 10px;
      font-weight: 500;
      color: #00FFFF;
      display: flex;
      align-items: center;
      justify-content: center;
      gap: 8px;
    }

    .online-indicator {
      width: 10px;
      height: 10px;
      background-color: #00FF00;
      border-radius: 50%;
    }

    .screen {
      width: 100%;
      max-width: 400px;
      height: 100px;
      border: 2px solid #222;
      border-radius: 8px;
      background: #fff;
      margin-bottom: 10px;
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 22px;
      font-weight: 500;
      text-align: center;
    }

    .safe-text {
      font-size: 14px;
      color: goldenrod;
      font-weight: 500;
      margin-bottom: 15px;
    }

    .safe-text::before {
      content: "\1F512 ";
    }

    button {
      display: block;
      width: 100%;
      max-width: 360px;
      padding: 12px;
      margin: 10px 0;
      font-size: 16px;
      font-weight: bold;
      border: none;
      border-radius: 6px;
      cursor: pointer;
    }

    .signal-btn {
      background-color: #FFD100;
      color: black;
      font-size: 20px;
      padding: 16px;
      animation: blink 1.5s infinite;
      box-shadow: 0 0 15px #FFD100;
    }

    @keyframes blink {
      0% { opacity: 1; }
      50% { opacity: 0.75; }
      100% { opacity: 1; }
    }

    .link-btn {
      background-color: #0072CE;
      color: white;
      font-size: 15px;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
    }

    .link-btn span:last-child {
      color: #FFD100;
      font-size: 13px;
    }

    .contact-btn {
      background-color: #EF3340;
      color: white;
      font-size: 15px;
    }
  </style>
</head>
<body>
  <header>
    <img src="https://flagcdn.com/w40/ec.png" alt="Bandera de Ecuador">
    <h1>SEÑALES PARA AVIATOR por Mateo</h1>
    <div class="online-counter" id="onlineCounter">
      <span class="online-indicator"></span>
      <span>78 usuarios en línea</span>
    </div>
  </header>

  <div class="screen" id="signalScreen">Presiona el botón para obtener señal</div>

  <div class="safe-text">100% seguridad. Programa oficial para jugar AVIATOR</div>

  <button class="signal-btn" onclick="generateSignal()">OBTENER SEÑAL</button>
  <button class="link-btn" onclick="window.location.href='https://mqzegh.top/2peu?p=%2Fregistration%2F&s1=muh'">
    <span>IR AL SITIO</span>
    <span>Usa el código ECU10</span>
  </button>
  <button class="contact-btn" onclick="window.location.href='https://t.me/MateoMolinaBot'">
    ¿Tienes preguntas? Escríbeme <img src="https://upload.wikimedia.org/wikipedia/commons/8/82/Telegram_logo.svg" alt="Telegram" style="width:18px; height:18px; vertical-align:middle; margin-left:5px;">
  </button>

  <script>
    const signalScreen = document.getElementById('signalScreen');
    const onlineCounter = document.getElementById('onlineCounter').querySelector('span:last-child');
    let currentUsers = 78;

    function generateSignal() {
      signalScreen.textContent = 'Generando señal...';
      setTimeout(() => {
        const rand = Math.random() * 100;
        let coef = 1.0;

        if (rand < 60) {
          coef = (Math.random() * (2.0 - 1.0) + 1.0).toFixed(2);
        } else if (rand < 80) {
          coef = (Math.random() * (3.0 - 2.0) + 2.0).toFixed(2);
        } else if (rand < 90) {
          coef = (Math.random() * (4.0 - 3.0) + 3.0).toFixed(2);
        } else if (rand < 98) {
          coef = (Math.random() * (8.0 - 4.0) + 4.0).toFixed(2);
        } else {
          coef = (Math.random() * (38.0 - 8.0) + 8.0).toFixed(2);
        }

        const delay = Math.floor(Math.random() * 30) + 10;
        signalScreen.textContent = `🎯 Señal: ${coef}x\n⏱️ Apuesta en ${delay} segundos`;
      }, 2000);
    }

    function updateOnlineUsers() {
      const change = Math.floor(Math.random() * 5) - 2;
      currentUsers += change;
      if (currentUsers < 65) currentUsers = 65;
      if (currentUsers > 89) currentUsers = 89;
      onlineCounter.textContent = `${currentUsers} usuarios en línea`;
    }

    setInterval(updateOnlineUsers, 4000);
  </script>
</body>
</html>
