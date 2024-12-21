<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Professional Banner</title>
  <style>
    /* General Reset */
    body {
      margin: 0;
      font-family: 'Arial', sans-serif;
      background-color: #f4f4f9;
      color: #333;
    }
    .banner {
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      text-align: center;
      height: 400px;
      background: linear-gradient(135deg, #6a11cb, #2575fc);
      color: white;
      position: relative;
      overflow: hidden;
    }
    /* Banner Text */
    .banner h1 {
      font-size: 3.5rem;
      margin: 0;
      font-weight: bold;
      text-shadow: 2px 2px 10px rgba(0, 0, 0, 0.3);
    }
    .banner p {
      font-size: 1.3rem;
      margin: 10px 0;
      text-shadow: 1px 1px 5px rgba(0, 0, 0, 0.2);
    }
    /* Floating Decorative Elements */
    .circle {
      position: absolute;
      border-radius: 50%;
      background: rgba(255, 255, 255, 0.3);
      animation: float 6s infinite ease-in-out alternate;
    }
    .circle.one {
      width: 120px;
      height: 120px;
      top: 10%;
      left: 15%;
    }
    .circle.two {
      width: 200px;
      height: 200px;
      bottom: 10%;
      right: 20%;
    }
    .circle.three {
      width: 150px;
      height: 150px;
      bottom: 20%;
      left: 5%;
    }
    @keyframes float {
      from {
        transform: translate(0, 0);
      }
      to {
        transform: translate(15px, -15px);
      }
    }
    /* Skills Section */
    .skills {
      margin: 20px auto;
      max-width: 900px;
      text-align: center;
    }
    .skills h2 {
      font-size: 2rem;
      margin-bottom: 20px;
      color: #444;
    }
    .skills-list {
      display: flex;
      justify-content: space-around;
      flex-wrap: wrap;
    }
    .skill {
      text-align: center;
      margin: 15px;
      width: 150px;
    }
    .skill i {
      font-size: 3rem;
      color: #2575fc;
      margin-bottom: 10px;
    }
    .skill h3 {
      font-size: 1.2rem;
      color: #333;
      margin: 10px 0;
    }
    .skill p {
      font-size: 0.9rem;
      color: #666;
    }
    /* Typing Animation */
    .typing {
      font-size: 1.4rem;
      font-weight: bold;
      color: #2575fc;
      text-align: center;
      margin-top: 30px;
    }
    .typing span {
      border-right: 2px solid #2575fc;
      white-space: nowrap;
      overflow: hidden;
      display: inline-block;
      animation: typing 3s steps(30, end) infinite, blink 0.5s step-end infinite;
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
  <!-- Banner Section -->
  <div class="banner">
    <h1>Welcome to My Portfolio</h1>
    <p>Building Modern Web Solutions with Passion</p>
    <!-- Floating Circles -->
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
        <p>Responsive and interactive websites.</p>
      </div>
      <div class="skill">
        <i class="fas fa-paint-brush"></i>
        <h3>UI/UX Design</h3>
        <p>Intuitive and aesthetic user interfaces.</p>
      </div>
      <div class="skill">
        <i class="fas fa-database"></i>
        <h3>Database</h3>
        <p>Efficient data storage and management.</p>
      </div>
      <div class="skill">
        <i class="fas fa-cloud"></i>
        <h3>Cloud Solutions</h3>
        <p>Scalable cloud-based applications.</p>
      </div>
    </div>
  </div>

  <!-- Typing Animation -->
  <div class="typing">
    <span id="typing-text"></span>
  </div>

  <!-- JavaScript for Typing Animation -->
  <script>
    const text = "Creating solutions for the modern web!";
    const speed = 100; // Typing speed in milliseconds
    let index = 0;

    function typeText() {
      const typingText = document.getElementById("typing-text");
      if (index < text.length) {
        typingText.textContent += text.charAt(index);
        index++;
        setTimeout(typeText, speed);
      } else {
        setTimeout(() => {
          typingText.textContent = ""; // Reset text
          index = 0; // Restart typing
          typeText(); // Loop the animation
        }, 2000);
      }
    }

    typeText();
  </script>

  <!-- Add Font Awesome for Icons -->
  <script src="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/js/all.min.js"></script>
</body>
</html>
