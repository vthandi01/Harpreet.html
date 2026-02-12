<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Harpreet, Will You Be My Valentine? ❤️</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <style>
    body {
      margin: 0;
      height: 100vh;
      font-family: 'Segoe UI', sans-serif;
      background: linear-gradient(135deg, #ff4d6d, #ff8fa3);
      display: flex;
      align-items: center;
      justify-content: center;
      overflow: hidden;
      color: white;
      text-align: center;
    }

    .card {
      background: rgba(0,0,0,0.3);
      padding: 25px;
      border-radius: 22px;
      max-width: 360px;
      box-shadow: 0 15px 35px rgba(0,0,0,0.35);
      animation: fadeIn 1.5s ease;
    }

    img {
      width: 100%;
      border-radius: 16px;
      margin-bottom: 15px;
      box-shadow: 0 8px 20px rgba(0,0,0,0.4);
    }

    h1 {
      margin: 10px 0;
      font-size: 1.8rem;
    }

    p {
      font-size: 1.05rem;
      line-height: 1.5;
    }

    .buttons {
      display: flex;
      justify-content: center;
      gap: 15px;
      margin-top: 20px;
    }

    button {
      padding: 12px 26px;
      font-size: 1rem;
      border: none;
      border-radius: 30px;
      cursor: pointer;
      transition: transform 0.2s ease;
    }

    .yes {
      background: #fff;
      color: #ff4d6d;
    }

    .no {
      background: rgba(255,255,255,0.3);
      color: #fff;
      position: relative;
    }

    button:hover {
      transform: scale(1.05);
    }

    .hidden {
      display: none;
    }

    .heart {
      position: absolute;
      bottom: -20px;
      font-size: 20px;
      animation: floatUp 6s linear infinite;
      opacity: 0.85;
    }

    @keyframes floatUp {
      from { transform: translateY(0); opacity: 1; }
      to { transform: translateY(-110vh); opacity: 0; }
    }

    @keyframes fadeIn {
      from { opacity: 0; transform: scale(0.9); }
      to { opacity: 1; transform: scale(1); }
    }
  </style>
</head>
<body>

  <div class="card">
    <img src="harpreet.jpg" alt="Us ❤️">

    <h1>Harpreet ❤️</h1>
    <p>Will you be my Valentine?</p>

    <div class="buttons" id="questionButtons">
      <button class="yes" onclick="sayYes()">Yes 💕</button>
      <button class="no" onmouseover="moveNo()">No 😅</button>
    </div>

    <p id="loveMessage" class="hidden">
      I knew you’d say yes 😘<br><br>
      Every day with you is my favorite day.  
      Thank you for being my wife, my best friend, and my forever.  
      <br><br>
      I choose you today, tomorrow, and always.  
      <br><br>
      I love you endlessly 💖  
      <br>— Your Husband
    </p>
  </div>

  <script>
    function sayYes() {
      document.getElementById("questionButtons").classList.add("hidden");
      document.getElementById("loveMessage").classList.remove("hidden");
    }

    function moveNo() {
      const noBtn = document.querySelector(".no");
      const x = Math.random() * 200 - 100;
      const y = Math.random() * 200 - 100;
      noBtn.style.transform = `translate(${x}px, ${y}px)`;
    }

    function createHeart() {
      const heart = document.createElement("div");
      heart.classList.add("heart");
      heart.innerHTML = "❤️";
      heart.style.left = Math.random() * 100 + "vw";
      heart.style.animationDuration = (4 + Math.random() * 4) + "s";
      document.body.appendChild(heart);

      setTimeout(() => heart.remove(), 8000);
    }

    setInterval(createHeart, 500);
  </script>

</body>
</html>
