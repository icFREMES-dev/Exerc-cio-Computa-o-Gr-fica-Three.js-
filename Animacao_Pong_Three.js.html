<!DOCTYPE html>
<html lang="pt-br">
<head>
  <meta charset="UTF-8">
  <title>Pong com Three.js</title>
  <style>
    body { margin: 0; overflow: hidden; background: black; }

    // Placar 
    #score {
      position: absolute;
      top: 20px;
      width: 100%;
      text-align: center;
      color: white;
      font-size: 32px;
      font-family: Arial, sans-serif;
    }
  </style>
</head>
<body>

<div id="score">0 x 0</div>

<script src="https://cdn.jsdelivr.net/npm/three@0.160.0/build/three.min.js"></script>

<script>
// Cena
const scene = new THREE.Scene();

// Câmera
const camera = new THREE.OrthographicCamera(-10, 10, 5, -5, 0.1, 100);
camera.position.z = 10;

// Renderizador
const renderer = new THREE.WebGLRenderer();
renderer.setSize(window.innerWidth, window.innerHeight);
document.body.appendChild(renderer.domElement);

// Material 
const material = new THREE.MeshBasicMaterial({ color: 0xffffff });

// Bola
const ballMaterial = new THREE.MeshBasicMaterial({ color: 0xff0000 });
const ball = new THREE.Mesh(
  new THREE.SphereGeometry(0.30, 32, 32),
  ballMaterial
);
scene.add(ball);

// Jogador
const player = new THREE.Mesh(
  new THREE.BoxGeometry(0.5, 1.3, 0.5),
  material
);
player.position.x = -8;
scene.add(player);

// CPU
const cpu = new THREE.Mesh(
  new THREE.BoxGeometry(0.5, 1.3, 0.5),
  material
);
cpu.position.x = 8;
scene.add(cpu);

// Velocidade bola
let ballSpeedX = 0.10;
let ballSpeedY = 0.10;

// Placar
let playerScore = 0;
let cpuScore = 0;
const scoreElement = document.getElementById("score");

function updateScore() {
  scoreElement.innerText = `${playerScore} x ${cpuScore}`;
}

// Controles
document.addEventListener("keydown", (e) => {
  if (e.key === "ArrowUp") player.position.y += 0.5;
  if (e.key === "ArrowDown") player.position.y -= 0.5;
});

// Reset bola
function resetBall() {
  ball.position.set(0, 0, 0);
  ballSpeedX = (Math.random() > 0.5 ? 0.1 : -0.1);
  ballSpeedY = (Math.random() * 0.2 - 0.1);
}

// Loop
function animate() {
  requestAnimationFrame(animate);

  // Movimento bola
  ball.position.x += ballSpeedX;
  ball.position.y += ballSpeedY;

  // Colisão topo/baixo
  if (ball.position.y > 4.5 || ball.position.y < -4.5) {
    ballSpeedY *= -1;
  }

  // Colisão jogador
  if (
    ball.position.x < player.position.x + 0.5 &&
    ball.position.y < player.position.y + 1 &&
    ball.position.y > player.position.y - 1
  ) {
    ballSpeedX *= -1;
  }

  // Colisão CPU
  if (
    ball.position.x > cpu.position.x - 0.5 &&
    ball.position.y < cpu.position.y + 1 &&
    ball.position.y > cpu.position.y - 1
  ) {
    ballSpeedX *= -1;
  }

  // CPU segue a bola
  cpu.position.y += (ball.position.y - cpu.position.y) * 0.09;

  // Pontuação
  if (ball.position.x > 10) {
    playerScore++;
    updateScore();
    resetBall();
  }

  if (ball.position.x < -10) {
    cpuScore++;
    updateScore();
    resetBall();
  }

  renderer.render(scene, camera);
}

animate();
</script>

</body>
</html>
