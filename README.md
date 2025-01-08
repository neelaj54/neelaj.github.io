<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Exclusive Premium Access</title>
  <style>
    body {
      margin: 0;
      padding: 0;
      font-family: "Arial", sans-serif;
      height: 100vh;
      display: flex;
      justify-content: center;
      align-items: center;
      background: linear-gradient(135deg, #0b0b0d, #1e1e1f);
      color: #fff;
      overflow: hidden;
    }

    .container {
      text-align: center;
      padding: 40px;
      background: rgba(20, 0, 0, 0.9);
      border: 1px solid #800000;
      border-radius: 20px;
      box-shadow: 0 0 20px rgba(255, 0, 0, 0.5), 0 0 40px rgba(255, 0, 0, 0.2);
      animation: zoomIn 0.8s ease-in-out;
    }

    h1 {
      font-size: 3rem;
      margin-bottom: 15px;
      color: #ff0000;
      text-shadow: 0 0 10px #ff0000, 0 0 20px #ff0000, 0 0 40px #ff3333;
      animation: glowText 2s infinite alternate;
    }

    p {
      font-size: 1.2rem;
      color: #ddd;
      margin-bottom: 20px;
    }

    .btn {
      padding: 15px 30px;
      font-size: 1.2rem;
      color: #fff;
      background: linear-gradient(135deg, #660000, #ff0000);
      border: none;
      border-radius: 10px;
      cursor: pointer;
      box-shadow: 0 5px 15px rgba(255, 0, 0, 0.4);
      transition: transform 0.3s, box-shadow 0.3s;
    }

    .btn:hover {
      transform: scale(1.1);
      box-shadow: 0 10px 30px rgba(255, 0, 0, 0.6);
    }

    .btn:active {
      transform: scale(0.95);
      box-shadow: 0 4px 10px rgba(255, 0, 0, 0.5);
    }

    .loading-text {
      display: none;
      font-size: 1.1rem;
      color: #ff3333;
      margin-top: 20px;
      animation: blink 1.5s infinite;
    }

    /* Animations */
    @keyframes zoomIn {
      from {
        opacity: 0;
        transform: scale(0.8);
      }
      to {
        opacity: 1;
        transform: scale(1);
      }
    }

    @keyframes glowText {
      0% {
        text-shadow: 0 0 10px #ff3333, 0 0 20px #ff3333, 0 0 40px #ff6666;
      }
      100% {
        text-shadow: 0 0 20px #ff3333, 0 0 40px #ff6666, 0 0 60px #ff9999;
      }
    }

    @keyframes blink {
      0%, 100% {
        opacity: 1;
      }
      50% {
        opacity: 0.5;
      }
    }

    /* Background Dots */
    .background-dots {
      position: absolute;
      width: 100%;
      height: 100%;
      overflow: hidden;
      z-index: -1;
    }

    .dot {
      position: absolute;
      width: 6px;
      height: 6px;
      background: rgba(255, 0, 0, 0.2);
      border-radius: 50%;
      animation: moveDots 10s linear infinite;
    }

    @keyframes moveDots {
      from {
        transform: translateY(0) translateX(0);
      }
      to {
        transform: translateY(100vh) translateX(100vw);
      }
    }
  </style>
</head>
<body>
  <!-- Background Dots -->
  <div class="background-dots">
    <script>
      const dotsContainer = document.querySelector("body");
      for (let i = 0; i < 80; i++) {
        const dot = document.createElement("div");
        dot.classList.add("dot");
        dot.style.top = `${Math.random() * 100}vh`;
        dot.style.left = `${Math.random() * 100}vw`;
        dot.style.animationDuration = `${5 + Math.random() * 10}s`;
        dot.style.animationDelay = `${Math.random() * 5}s`;
        dotsContainer.appendChild(dot);
      }
    </script>
  </div>

  <!-- Content -->
  <div class="container">
    <h1>Premium Access</h1>
    <p>Welcome to your exclusive content experience. Click the button below to reveal your premium content.</p>
    <button class="btn" onclick="revealContent()">Unlock Now</button>
    <p class="loading-text" id="loading">Loading your premium content...</p>
  </div>

  <script>
    function revealContent() {
      const loadingText = document.getElementById("loading");
      loadingText.style.display = "block"; // Show loading text

      setTimeout(() => {
        // Redirect to Rick Astley's Never Gonna Give You Up video
        window.location.href = "https://www.youtube.com/watch?v=dQw4w9WgXcQ";
      }, 4000); // Delay for dramatic effect
    }
  </script>
</body>
</html>
