<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Danillo & Ana</title>
  <style>
    body {
      margin: 0;
      font-family: 'Arial', sans-serif;
      background: linear-gradient(to right, #fceabb, #f8b500);
      color: #fff;
      text-align: center;
      padding: 20px;
    }

    h1 {
      font-size: 3em;
      margin-top: 30px;
    }

    .timer {
      font-size: 2em;
      margin: 20px 0;
    }

    .message {
      font-size: 1.5em;
      margin: 30px 0;
    }

    .photos {
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
      gap: 15px;
      margin-top: 30px;
    }

    .photos img {
      width: 250px;
      height: auto;
      border-radius: 15px;
      box-shadow: 0 0 10px rgba(0,0,0,0.3);
    }

    audio {
      margin-top: 40px;
    }
  </style>
</head>
<body>
  <h1>Danillo & Ana</h1>
  <div class="timer" id="timer"></div>
  <div class="message">
    Desde a primeira vez que eu te vi, te amei profundamente.
  </div>

  <div class="photos">
    <!-- Adicione suas fotos aqui -->
    <img src="foto1.jpg" alt="Foto juntos">
    <img src="foto2.jpg" alt="Foto juntos">
    <img src="foto3.jpg" alt="Foto juntos">
    <!-- Substitua os arquivos pelas suas fotos reais -->
  </div>

  <audio controls autoplay loop>
    <source src="sunshine-delacruz.mp3" type="audio/mpeg">
    Seu navegador não suporta áudio.
  </audio>

  <script>
    const startDate = new Date('2022-10-21T00:00:00');
    const timerEl = document.getElementById('timer');

    function updateTimer() {
      const now = new Date();
      const diff = now - startDate;

      const days = Math.floor(diff / (1000 * 60 * 60 * 24));
      const hours = Math.floor((diff / (1000 * 60 * 60)) % 24);
      const minutes = Math.floor((diff / (1000 * 60)) % 60);
      const seconds = Math.floor((diff / 1000) % 60);

      timerEl.textContent = `Estamos juntos há ${days} dias, ${hours} horas, ${minutes} minutos e ${seconds} segundos.`;
    }

    setInterval(updateTimer, 1000);
    updateTimer();
  </script>
</body>
</html>
