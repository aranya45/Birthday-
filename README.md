<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Happy Birthday ❤️</title>
  <style>
    body {
      margin: 0;
      font-family: 'Segoe UI', sans-serif;
      background: linear-gradient(135deg, #ff9a9e, #fad0c4);
      color: #fff;
      text-align: center;
      overflow-x: hidden;
    }
    .container {
      padding: 40px 20px;
    }
    h1 {
      font-size: 2.5rem;
      animation: fadeIn 2s ease-in-out;
    }
    p {
      font-size: 1.2rem;
      max-width: 600px;
      margin: 20px auto;
      line-height: 1.6;
      animation: fadeIn 3s ease-in-out;
    }
    button {
      padding: 12px 25px;
      font-size: 1rem;
      border: none;
      border-radius: 25px;
      background: #fff;
      color: #ff4b5c;
      cursor: pointer;
      transition: 0.3s;
    }
    button:hover {
      background: #ff4b5c;
      color: #fff;
    }
    .hidden-message {
      display: none;
      margin-top: 20px;
      font-size: 1.3rem;
      animation: fadeIn 2s ease-in-out;
    }
    @keyframes fadeIn {
      from { opacity: 0; transform: translateY(20px);} 
      to { opacity: 1; transform: translateY(0);} 
    }
    .hearts {
      position: fixed;
      width: 100%;
      height: 100%;
      top: 0;
      left: 0;
      pointer-events: none;
    }
    .heart {
      position: absolute;
      color: red;
      animation: float 5s linear infinite;
    }
    @keyframes float {
      from { transform: translateY(100vh); opacity: 1; }
      to { transform: translateY(-10vh); opacity: 0; }
    }
  </style>
</head>
<body>

<div class="container">
  <h1>Happy Birthday My Mummum ❤️</h1>
  <p>
    I love you Sagarika a lot
    You are the most special person in my life. Your smile makes my world brighter, 
    and your love makes me stronger. I am so lucky to have you.
  </p>

  <button onclick="showMessage()">Click for Surprise 🎁</button>

  <div class="hidden-message" id="message">
    I love you more than words can express. You are my happiness, my peace, and my everything. 💖
  </div>
</div>

<div class="hearts" id="hearts"></div>

<script>
  function showMessage() {
    document.getElementById("message").style.display = "block";
  }

  function createHeart() {
    const heart = document.createElement("div");
    heart.classList.add("heart");
    heart.innerHTML = "❤️";
    heart.style.left = Math.random() * 100 + "vw";
    heart.style.fontSize = Math.random() * 20 + 10 + "px";
    heart.style.animationDuration = Math.random() * 3 + 3 + "s";
    document.getElementById("hearts").appendChild(heart);

    setTimeout(() => {
      heart.remove();
    }, 5000);
  }

  setInterval(createHeart, 300);
</script>

</body>
</html>
