<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>احصل على ألعابك المفضلة الآن!</title>
  <style>
    body {
      background-color: #121212;
      color: #ffffff;
      font-family: 'Tajawal', sans-serif;
      margin: 0;
      padding: 20px;
      text-align: center;
    }
    h1 {
      color: #FFD700;
      margin-bottom: 20px;
    }
    .game {
      background: #1e1e1e;
      margin: 30px auto;
      padding: 20px;
      border-radius: 12px;
      width: 90%;
      max-width: 400px;
      box-shadow: 0 4px 10px rgba(255, 215, 0, 0.2);
      position: relative;
    }
    img {
      width: 100%;
      border-radius: 10px;
      margin-bottom: 15px;
    }
    .btn {
      background: #FFD700;
      color: #121212;
      padding: 12px 25px;
      margin-top: 10px;
      display: inline-block;
      font-size: 18px;
      border-radius: 30px;
      text-decoration: none;
      font-weight: bold;
      transition: background 0.3s;
    }
    .btn:hover {
      background: #ffcc00;
    }
    .timer {
      margin-top: 10px;
      font-size: 16px;
      color: #FFD700;
    }
    .popup {
      display: none;
      position: fixed;
      top: 50%;
      left: 50%;
      transform: translate(-50%, -50%);
      background: #1e1e1e;
      padding: 20px;
      border-radius: 10px;
      box-shadow: 0 4px 10px rgba(255, 215, 0, 0.5);
      z-index: 999;
    }
    .popup p {
      margin: 0;
      margin-bottom: 10px;
    }
  </style>
</head>
<body>

<h1>🎮 احصل على ألعابك المفضلة الآن!</h1>

<div class="game">
  <img src="images/gta.jpg" alt="GTA V">
  <h2>تحميل GTA V مجانا</h2>
  <div class="timer" id="timer1"></div>
  <a href="#" class="btn" onclick="showPopup()">ابدأ التحميل</a>
</div>

<div class="game">
  <img src="images/pubg.jpg" alt="PUBG UC">
  <h2>احصل على UC مجانا - PUBG Mobile</h2>
  <div class="timer" id="timer2"></div>
  <a href="#" class="btn" onclick="showPopup()">ابدأ التحميل</a>
</div>

<div class="game">
  <img src="images/freefire.jpg" alt="Free Fire Diamonds">
  <h2>احصل على Diamonds مجانا - Free Fire</h2>
  <div class="timer" id="timer3"></div>
  <a href="#" class="btn" onclick="showPopup()">ابدأ التحميل</a>
</div>

<div class="game">
  <img src="images/minecraft.jpg" alt="Minecraft">
  <h2>تحميل Minecraft Java Edition مجانا</h2>
  <div class="timer" id="timer4"></div>
  <a href="#" class="btn" onclick="showPopup()">ابدأ التحميل</a>
</div>

<div class="popup" id="popup">
  <p>✅ تم حجز العرض لك!</p>
  <p>أكمل خطوة التحقق لتحميل اللعبة 🎮</p>
  <button class="btn" onclick="hidePopup()">موافق</button>
</div>

<script>
function startTimer(id, minutes) {
  let duration = minutes * 60;
  const timerDisplay = document.getElementById(id);

  setInterval(function () {
    let minutes = parseInt(duration / 60, 10);
    let seconds = parseInt(duration % 60, 10);

    minutes = minutes < 10 ? "0" + minutes : minutes;
    seconds = seconds < 10 ? "0" + seconds : seconds;

    timerDisplay.textContent = "ينتهي العرض خلال: " + minutes + ":" + seconds;

    if (--duration < 0) {
      duration = 0;
    }
  }, 1000);
}

function showPopup() {
  document.getElementById('popup').style.display = 'block';
}

function hidePopup() {
  document.getElementById('popup').style.display = 'none';
}

startTimer('timer1', 5);
startTimer('timer2', 5);
startTimer('timer3', 5);
startTimer('timer4', 5);
</script>

</body>
</html>
