<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Professional Banner</title>
  <script src="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/js/all.min.js"></script>
</head>
<body style="margin: 0; font-family: Arial, sans-serif; background-color: #f4f4f9; color: #333;">

  <!-- Banner Section -->
  <div style="
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    text-align: center;
    height: 400px;
    background: linear-gradient(135deg, #6a11cb, #2575fc);
    color: white;
    position: relative;
    overflow: hidden;">
    <h1 style="
      font-size: 3.5rem;
      margin: 0;
      font-weight: bold;
      text-shadow: 2px 2px 10px rgba(0, 0, 0, 0.3);">
      Welcome to My Portfolio
    </h1>
    <p style="
      font-size: 1.3rem;
      margin: 10px 0;
      text-shadow: 1px 1px 5px rgba(0, 0, 0, 0.2);">
      Building Modern Web Solutions with Passion
    </p>
    <!-- Floating Circles -->
    <div style="
      position: absolute;
      border-radius: 50%;
      background: rgba(255, 255, 255, 0.3);
      width: 120px;
      height: 120px;
      top: 10%;
      left: 15%;
      animation: float 6s infinite ease-in-out alternate;"></div>
    <div style="
      position: absolute;
      border-radius: 50%;
      background: rgba(255, 255, 255, 0.3);
      width: 200px;
      height: 200px;
      bottom: 10%;
      right: 20%;
      animation: float 6s infinite ease-in-out alternate;"></div>
    <div style="
      position: absolute;
      border-radius: 50%;
      background: rgba(255, 255, 255, 0.3);
      width: 150px;
      height: 150px;
      bottom: 20%;
      left: 5%;
      animation: float 6s infinite ease-in-out alternate;"></div>
  </div>

  <!-- Skills Section -->
  <div style="margin: 20px auto; max-width: 900px; text-align: center;">
    <h2 style="font-size: 2rem; margin-bottom: 20px; color: #444;">What I Do</h2>
    <div style="display: flex; justify-content: space-around; flex-wrap: wrap;">
      <div style="text-align: center; margin: 15px; width: 150px;">
        <i class="fas fa-code" style="font-size: 3rem; color: #2575fc; margin-bottom: 10px;"></i>
        <h3 style="font-size: 1.2rem; color: #333; margin: 10px 0;">Web Development</h3>
        <p style="font-size: 0.9rem; color: #666;">Responsive and interactive websites.</p>
      </div>
      <div style="text-align: center; margin: 15px; width: 150px;">
        <i class="fas fa-paint-brush" style="font-size: 3rem; color: #2575fc; margin-bottom: 10px;"></i>
        <h3 style="font-size: 1.2rem; color: #333; margin: 10px 0;">UI/UX Design</h3>
        <p style="font-size: 0.9rem; color: #666;">Intuitive and aesthetic user interfaces.</p>
      </div>
      <div style="text-align: center; margin: 15px; width: 150px;">
        <i class="fas fa-database" style="font-size: 3rem; color: #2575fc; margin-bottom: 10px;"></i>
        <h3 style="font-size: 1.2rem; color: #333; margin: 10px 0;">Database</h3>
        <p style="font-size: 0.9rem; color: #666;">Efficient data storage and management.</p>
      </div>
      <div style="text-align: center; margin: 15px; width: 150px;">
        <i class="fas fa-cloud" style="font-size: 3rem; color: #2575fc; margin-bottom: 10px;"></i>
        <h3 style="font-size: 1.2rem; color: #333; margin: 10px 0;">Cloud Solutions</h3>
        <p style="font-size: 0.9rem; color: #666;">Scalable cloud-based applications.</p>
      </div>
    </div>
  </div>

  <!-- Typing Animation -->
  <div style="font-size: 1.4rem; font-weight: bold; color: #2575fc; text-align: center; margin-top: 30px;">
    <span id="typing-text" style="
      border-right: 2px solid #2575fc;
      white-space: nowrap;
      overflow: hidden;
      display: inline-block;">
    </span>
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
</body>
</html>
