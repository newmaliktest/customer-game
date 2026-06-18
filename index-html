<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Will You Be Our Customer?</title>
  <style>
    * {
      box-sizing: border-box;
      font-family: Arial, sans-serif;
    }

    body {
      margin: 0;
      min-height: 100vh;
      display: flex;
      align-items: center;
      justify-content: center;
      background: linear-gradient(135deg, #111, #8b0000);
      overflow: hidden;
      color: white;
    }

    .card {
      width: 90%;
      max-width: 430px;
      background: rgba(255, 255, 255, 0.12);
      backdrop-filter: blur(12px);
      border: 1px solid rgba(255, 255, 255, 0.25);
      border-radius: 25px;
      padding: 35px 25px;
      text-align: center;
      box-shadow: 0 20px 50px rgba(0,0,0,0.35);
      position: relative;
    }

    .emoji {
      font-size: 55px;
      margin-bottom: 10px;
      animation: bounce 1.5s infinite;
    }

    h1 {
      font-size: 30px;
      margin: 10px 0;
    }

    p {
      font-size: 16px;
      opacity: 0.9;
      margin-bottom: 30px;
    }

    .buttons {
      height: 80px;
      position: relative;
    }

    button {
      border: none;
      padding: 14px 28px;
      border-radius: 30px;
      font-size: 17px;
      cursor: pointer;
      transition: 0.25s;
      font-weight: bold;
    }

    #yesBtn {
      background: #00c853;
      color: white;
      margin-right: 15px;
      box-shadow: 0 8px 20px rgba(0, 200, 83, 0.4);
    }

    #yesBtn:hover {
      transform: scale(1.1);
      background: #00e676;
    }

    #noBtn {
      background: white;
      color: #8b0000;
      position: absolute;
    }

    .success {
      display: none;
      margin-top: 25px;
      font-size: 22px;
      font-weight: bold;
      color: #00ff88;
      animation: pop 0.5s ease;
    }

    .small-text {
      margin-top: 20px;
      font-size: 13px;
      opacity: 0.75;
    }

    @keyframes bounce {
      0%, 100% { transform: translateY(0); }
      50% { transform: translateY(-10px); }
    }

    @keyframes pop {
      from { transform: scale(0.5); opacity: 0; }
      to { transform: scale(1); opacity: 1; }
    }

    .heart {
      position: fixed;
      font-size: 24px;
      animation: floatUp 2s linear forwards;
      pointer-events: none;
    }

    @keyframes floatUp {
      from {
        transform: translateY(0) scale(1);
        opacity: 1;
      }
      to {
        transform: translateY(-180px) scale(1.8);
        opacity: 0;
      }
    }
  </style>
</head>
<body>

  <div class="card">
    <div class="emoji">🤝</div>
    <h1>Will You Be Our Customer?</h1>
    <p>We promise good service, fair price, and fast response.</p>

    <div class="buttons">
      <button id="yesBtn">Yes, Sure ✅</button>
      <button id="noBtn">No ❌</button>
    </div>

    <div class="success" id="successMsg">
      Welcome! You made the right choice 😄
    </div>

    <div class="small-text">
      Try clicking “No” if you can 👀
    </div>
  </div>

  <script>
    const noBtn = document.getElementById("noBtn");
    const yesBtn = document.getElementById("yesBtn");
    const successMsg = document.getElementById("successMsg");

    const funnyTexts = [
      "No ❌",
      "Are you sure?",
      "Think again 😅",
      "Best price!",
      "Fast service!",
      "Don't say no 😭",
      "Click Yes 😄"
    ];

    let count = 0;

    function moveNoButton() {
      const maxX = window.innerWidth - noBtn.offsetWidth - 20;
      const maxY = window.innerHeight - noBtn.offsetHeight - 20;

      const randomX = Math.random() * maxX;
      const randomY = Math.random() * maxY;

      noBtn.style.position = "fixed";
      noBtn.style.left = randomX + "px";
      noBtn.style.top = randomY + "px";

      count++;
      noBtn.textContent = funnyTexts[count % funnyTexts.length];

      if (count > 4) {
        noBtn.style.transform = "scale(0.8)";
      }

      if (count > 8) {
        noBtn.style.transform = "scale(0.6)";
      }
    }

    noBtn.addEventListener("mouseover", moveNoButton);
    noBtn.addEventListener("click", moveNoButton);
    noBtn.addEventListener("touchstart", moveNoButton);

    yesBtn.addEventListener("click", () => {
      successMsg.style.display = "block";
      yesBtn.textContent = "Confirmed 🎉";
      noBtn.style.display = "none";

      for (let i = 0; i < 25; i++) {
        setTimeout(createHeart, i * 80);
      }
    });

    function createHeart() {
      const heart = document.createElement("div");
      heart.className = "heart";
      heart.textContent = ["❤️", "🤝", "🎉", "⭐"][Math.floor(Math.random() * 4)];
      heart.style.left = Math.random() * window.innerWidth + "px";
      heart.style.top = window.innerHeight - 40 + "px";
      document.body.appendChild(heart);

      setTimeout(() => {
        heart.remove();
      }, 2000);
    }
  </script>

</body>
</html>
