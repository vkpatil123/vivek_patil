<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Vivek's Crazy Portfolio</title>
  <style>
    body {
      margin: 0;
      font-family: 'Poppins', sans-serif;
      background: linear-gradient(135deg, #ff512f, #dd2476);
      color: white;
      text-align: center;
      overflow-x: hidden;
    }
    h1 {
      font-size: 3rem;
      animation: glow 2s infinite alternate;
    }
    @keyframes glow {
      from { text-shadow: 0 0 10px #ff0; }
      to   { text-shadow: 0 0 20px #0ff; }
    }
    .card {
      margin: 20px auto;
      padding: 20px;
      width: 300px;
      background: rgba(255,255,255,0.1);
      border-radius: 20px;
      backdrop-filter: blur(10px);
      transition: transform 0.3s;
    }
    .card:hover {
      transform: scale(1.1) rotate(3deg);
    }
  </style>
</head>
<body>
  <h1>🔥 Vivek Patil 🔥</h1>
  <p>Full-Stack Developer | DSA Enthusiast</p>

  <div class="card">
    <h2>💻 LeetCode</h2>
    <p>150+ Problems Solved</p>
  </div>

  <div class="card">
    <h2>📚 GeeksforGeeks</h2>
    <p>500+ Practice Problems</p>
  </div>

  <div class="card">
    <h2>⚡ GitHub</h2>
    <p>Open-source Projects & Stats</p>
  </div>
</body>
</html>
