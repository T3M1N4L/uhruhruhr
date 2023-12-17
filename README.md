# Hello, world!

```
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <style>
    canvas {
      border: 1px solid #000;
      display: block;
      margin: 20px auto;
    }
  </style>
  <title>Gravity Simulation</title>
</head>
<body>
  <canvas id="gravityCanvas" width="800" height="600"></canvas>

  <script>
    const canvas = document.getElementById('gravityCanvas');
    const ctx = canvas.getContext('2d');

    // Initial position and velocity of the object
    let x = 100;
    let y = 100;
    let velocityY = 0; // Initial vertical velocity
    const gravity = 0.1; // Gravity strength

    function draw() {
      // Clear the canvas
      ctx.clearRect(0, 0, canvas.width, canvas.height);

      // Update position and velocity
      velocityY += gravity;
      y += velocityY;

      // Draw the object
      ctx.fillStyle = '#3498db';
      ctx.beginPath();
      ctx.arc(x, y, 20, 0, 2 * Math.PI);
      ctx.fill();

      // Request the next animation frame
      requestAnimationFrame(draw);
    }

    // Start the animation loop
    draw();
  </script>
</body>
</html>

```
