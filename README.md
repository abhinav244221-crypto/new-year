<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>Happy New Year ❤️</title>
<style>
  body {
    margin: 0;
    height: 100vh;
    background: linear-gradient(135deg, #ffdde1, #ee9ca7);
    font-family: 'Arial', sans-serif;
    display: flex;
    align-items: center;
    justify-content: center;
    overflow: hidden;
  }

  .screen {
    text-align: center;
    background: white;
    padding: 35px;
    border-radius: 25px;
    box-shadow: 0 15px 30px rgba(0,0,0,0.2);
    max-width: 320px;
    animation: fadeIn 1s ease;
  }

  h1 {
    color: #ff4d6d;
  }

  button {
    background: #ff4d6d;
    color: white;
    border: none;
    padding: 12px 20px;
    border-radius: 20px;
    font-size: 16px;
    cursor: pointer;
  }

  button:hover {
    background: #ff2f55;
  }

  .hidden {
    display: none;
  }

  .heart {
    position: absolute;
    color: #ff4d6d;
    font-size: 20px;
    animation: floatUp 5s linear infinite;
  }

  @keyframes floatUp {
    from {
      transform: translateY(100vh);
      opacity: 1;
    }
    to {
      transform: translateY(-10vh);
      opacity: 0;
    }
  }

  @keyframes fadeIn {
    from { opacity: 0; transform: scale(0.9); }
    to { opacity: 1; transform: scale(1); }
  }
</style>
</head>

<body>

<div id="start" class="screen">
  <h1>🎁 Hey You</h1>
  <p>Tap below to open your New Year surprise ❤️</p>
  <button onclick="openSurprise()">Tap to Open</button>
</div>

<div id="message" class="screen hidden">
  <h1>🎆 Happy New Year My Love 🎆</h1>
  <p>
    This year was special because of you ❤️<br><br>
    Your smile, your care, your presence —
    they made everything brighter.<br><br>
    As the new year begins, I wish for more laughs,
    more memories, and more *us*.<br><br>
    Thank you for being my favorite person 💕
  </p>
  <p><strong>— Yours, always ❤️</strong></p>
</div>

<script>
function openSurprise() {
  document.getElementById('start').classList.add('hidden');
  document.getElementById('message').classList.remove('hidden');
  createHearts();
}

function createHearts() {
  setInterval(() => {
    const heart = document.createElement('div');
    heart.className = 'heart';
    heart.innerHTML = '❤️';
    heart.style.left = Math.random() * 100 + 'vw';
    heart.style.fontSize = (15 + Math.random() * 20) + 'px';
    document.body.appendChild(heart);
    setTimeout(() => heart.remove(), 5000);
  }, 300);
}
</script>

</body>
</html>
