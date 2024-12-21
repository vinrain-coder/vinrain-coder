<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Comprehensive Banner</title>
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
  <style>
    /* General Reset */
    body {
      margin: 0;
      font-family: 'Arial', sans-serif;
      background-color: #f3f4f6;
      color: #333;
    }
    .banner {
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      text-align: center;
      height: 350px;
      background: linear-gradient(135deg, #ff7eb3, #ff758c, #ffd452);
      color: white;
      overflow: hidden;
      position: relative;
    }
    .circle {
      position: absolute;
      border-radius: 50%;
      opacity: 0.3;
      animation: move 8s infinite alternate;
    }
    .circle.one {
      background: rgba(255, 255, 255, 0.3);
      width: 120px;
      height: 120px;
      top: 10%;
      left: 10%;
    }
    .circle.two {
      background: rgba(255, 255, 255, 0.2);
      width: 180px;
      height: 180px;
      top: 50%;
      left: 80%;
    }
    .circle.three {
      background: rgba(255, 255, 255, 0.1);
      width: 200px;
      height: 200px;
      top: 80%;
      left: 30%;
    }
    @keyframes move {
      0% {
        transform: translate(0, 0);
      }
      100% {
        transform: translate(20px, -20px);
      }
    }
    /* Banner Content */
    .banner h1 {
      font-size: 3.5rem;
      font-weight: bold;
      margin: 0;
      text-shadow: 2px 2px 8px rgba(0, 0, 0, 0.3);
    }
    .banner p {
      font-size: 1.3rem;
      margin: 10px 0 20px;
      text-shadow: 1px 1px 4px rgba(0, 0, 0, 0.2);
    }
    .skills {
      text-align: center;
      margin: 30px auto;
      padding: 20px;
      max-width: 900px;
      background: white;
      border-radius: 10px;
      box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
    }
    .skills h2 {
      font-size: 2rem;
      margin-bottom: 15px;
      color: #333;
    }
    .skills-list {
      display: flex;
      justify-content: space-around;
      flex-wrap: wrap;
    }
    .skill {
      text-align: center;
      width: 150px;
      margin: 15px;
    }
    .skill i {
      font-size: 2.5rem;
      color: #ff758c;
      margin-bottom: 10px;
    }
    .skill h3 {
      font-size: 1.2rem;
      margin: 0;
      color: #444;
    }
    .skill p {
      font-size: 0.9rem;
      color: #666;
    }
    .typing-animation {
      font-size: 1.5rem;
      font-weight: bold;
      color: #444;
      margin-top: 20px;
      text-align: center;
    }
    .typing-animation span {
      display: inline-block;
      border-right: 2px solid #444;
      white-space: nowrap;
      overflow: hidden;
      animation: typing 4s steps(30, end) infinite, blink 0.6s step-end infinite;
    }
    @keyframes typing {
      from {
        width: 0;
      }
      to {
        width: 100%;
      }
    }
    @keyframes blink {
      50% {
        border-color: transparent;
      }
    }
  </style>
</head>
<body>
  <div class="banner">
    <div>
      <h1>Welcome to My Github</h1>
      <p>Creating Modern Web Solutions with Passion and Precision</p>
    </div>
    <div class="circle one"></div>
    <div class="circle two"></div>
    <div class="circle three"></div>
  </div>

  <!-- Skills Section -->
  <div class="skills">
    <h2>What I Do</h2>
    <div class="skills-list">
      <div class="skill">
        <i class="fas fa-code"></i>
        <h3>Web Development</h3>
        <p>Responsive and dynamic websites using modern frameworks.</p>
      </div>
      <div class="skill">
        <i class="fas fa-paint-brush"></i>
        <h3>UI/UX Design</h3>
        <p>Creating user-friendly and visually appealing designs.</p>
      </div>
      <div class="skill">
        <i class="fas fa-database"></i>
        <h3>Database Management</h3>
        <p>Efficient data storage and retrieval solutions.</p>
      </div>
      <div class="skill">
        <i class="fas fa-chart-line"></i>
        <h3>SEO Optimization</h3>
        <p>Improving website visibility on search engines.</p>
      </div>
      <div class="skill">
        <i class="fas fa-mobile-alt"></i>
        <h3>Mobile Apps</h3>
        <p>Building apps that work seamlessly on all devices.</p>
      </div>
      <div class="skill">
        <i class="fas fa-cloud"></i>
        <h3>Cloud Integration</h3>
        <p>Deploying scalable and reliable cloud solutions.</p>
      </div>
    </div>
  </div>

  <!-- Typing Animation -->
  <div class="typing-animation">
    <span id="typed-text"></span>
  </div>

  <!-- JavaScript for Typing Animation -->
  <script>
    const text = "Exploring the Art of Development and Design!";
    const speed = 100; // Typing speed in milliseconds
    let index = 0;

    function typeText() {
      const typedText = document.getElementById("typed-text");
      if (index < text.length) {
        typedText.textContent += text.charAt(index);
        index++;
        setTimeout(typeText, speed);
      } else {
        setTimeout(() => {
          typedText.textContent = ""; // Clear text
          index = 0; // Reset index
          typeText(); // Restart animation
        }, 2000);
      }
    }

    typeText();
  </script>
</body>
</html>
