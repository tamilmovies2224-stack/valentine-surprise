# valentine-surprise
<!DOCTYPE html>
<html lang="ta">
<head>
  <meta charset="UTF-8">
  <title>Sandhiya Priya ❤️ Naveen</title>
  <style>
    body {
      margin: 0;
      font-family: 'Segoe UI', sans-serif;
      background: linear-gradient(to right, #ff6a88, #ff99ac);
      color: white;
      text-align: center;
      overflow-x: hidden;
    }

    h1 {
      margin-top: 40px;
      font-size: 2.6em;
      animation: fadeIn 2s;
    }

    p {
      font-size: 1.4em;
      margin: 20px;
      line-height: 1.8;
      animation: fadeIn 3s;
    }

    .photos {
      display: flex;
      justify-content: center;
      gap: 20px;
      flex-wrap: wrap;
      margin-top: 30px;
    }

    .photos img {
      width: 220px;
      height: 260px;
      object-fit: cover;
      border-radius: 20px;
      box-shadow: 0 10px 25px rgba(0,0,0,0.3);
    }

    button {
      background: white;
      color: #ff4d6d;
      border: none;
      padding: 15px 30px;
      font-size: 1.2em;
      border-radius: 30px;
      cursor: pointer;
      margin: 15px;
    }

    button:hover {
      background: #ffe3ea;
    }

    .question {
      margin-top: 50px;
      font-size: 1.8em;
      animation: fadeIn 2s;
    }

    .result {
      display: none;
      font-size: 1.8em;
      margin-top: 40px;
      animation: fadeIn 2s;
    }

    #noBtn {
      position: relative;
    }

    .heart {
      position: fixed;
      top: -10px;
      font-size: 20px;
      animation: fall linear infinite;
    }

    @keyframes fall {
      to { transform: translateY(100vh); }
    }

    @keyframes fadeIn {
      from { opacity: 0; }
      to { opacity: 1; }
    }
  </style>
</head>
<body>

  <h1>Happy Valentine’s Day 💖</h1>

  <p>
    Sandhiya Priya 💕<br>
    Nee en life-ku vandhadhula irundhu,<br>
    ellame konjam azhaga maariduchu 😌
  </p>

  <div class="photos">
    <img src="her.jpg" alt="Sandhiya Priya">
    <img src="us.jpg" alt="Us">
  </div>

  <div class="question">
    En kooda indha smile-oda journey-la irukka aasaiyaa? 🥹❤️
  </div>

  <div>
    <button onclick="yesClicked()">YES 💖</button>
    <button id="noBtn" onmouseover="moveNo()">NO 😜</button>
  </div>

  <div class="result" id="yesResult">
    Enakku theriyum 😌💞<br>
    Idhu just beginning mattum dhaan ❤️<br><br>
    – Un Naveen 🌹
  </div>

  <script>
    function yesClicked() {
      document.getElementById("yesResult").style.display = "block";
    }

    function moveNo() {
      const btn = document.getElementById("noBtn");
      btn.style.left = Math.random() * 200 - 100 + "px";
      btn.style.top = Math.random() * 200 - 100 + "px";
    }

    setInterval(() => {
      const heart = document.createElement("div");
      heart.className = "heart";
      heart.innerHTML = "❤️";
      heart.style.left = Math.random() * 100 + "vw";
      heart.style.animationDuration = (Math.random() * 3 + 3) + "s";
      document.body.appendChild(heart);
      setTimeout(() => heart.remove(), 6000);
    }, 300);
  </script>

</body>
</html>
