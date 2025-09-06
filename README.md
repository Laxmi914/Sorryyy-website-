<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>I'm Sorry 💔</title>
  <style>
    body {
      margin: 0;
      font-family: 'Poppins', sans-serif;
      background: linear-gradient(135deg, #ff9a9e, #fad0c4);
      text-align: center;
      color: #fff;
      overflow: hidden;
    }
    h1 {
      margin-top: 100px;
      font-size: 3em;
      animation: fadeIn 2s ease-in-out;
    }
    p {
      font-size: 1.5em;
      margin: 20px;
      animation: fadeIn 3s ease-in-out;
    }
    button {
      background: #e63946;
      color: white;
      border: none;
      padding: 15px 40px;
      font-size: 1.2em;
      border-radius: 30px;
      cursor: pointer;
      margin-top: 20px;
      transition: 0.3s;
    }
    button:hover {
      background: #d62828;
      transform: scale(1.1);
    }
    @keyframes fadeIn {
      from {opacity: 0;}
      to {opacity: 1;}
    }
    /* Floating hearts */
    .heart {
      position: fixed;
      bottom: -10px;
      color: #fff;
      font-size: 20px;
      animation: floatUp 6s linear infinite;
    }
    @keyframes floatUp {
      0% {transform: translateY(0) scale(1);}
      100% {transform: translateY(-100vh) scale(1.5); opacity: 0;}
    }
  </style>
</head>
<body>
  <h1>I'm Really Sorry 💔</h1>
  <p>I never meant to hurt you... Please forgive me 💙</p>
  <button onclick="alert('Yay! Thank you for forgiving me ❤️')">Forgive Me?</button>

  <!-- Background Music -->
  <audio id="bg-music" autoplay loop>
    <source src="music.mp3" type="audio/mpeg">
    Your browser does not support the audio element.
  </audio>

  <script>
    // Floating hearts
    function createHeart() {
      const heart = document.createElement("div");
      heart.classList.add("heart");
      heart.innerHTML = "❤️";
      heart.style.left = Math.random() * 100 + "vw";
      heart.style.fontSize = Math.random() * 20 + 20 + "px";
      heart.style.animationDuration = Math.random() * 3 + 3 + "s";
      document.body.appendChild(heart);

      setTimeout(() => {
        heart.remove();
      }, 6000);
    }
    setInterval(createHeart, 500);

    // Popup message after 5 seconds
    setTimeout(() => {
      alert("I really mean it 💙 Please forgive me");
    }, 5000);
  </script>
</body>
</html>
